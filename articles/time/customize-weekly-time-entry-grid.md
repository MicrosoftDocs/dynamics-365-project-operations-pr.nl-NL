---
title: Tijdinvoer uitbreiden
description: Dit onderwerp biedt informatie over de manier waarop ontwikkelaars het besturingselement voor tijdinvoer kunnen uitbreiden.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930874"
---
# <a name="extending-time-entries"></a>Tijdinvoer uitbreiden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations bevat een uitbreidbaar aangepast besturingselement voor tijdinvoer. Dit besturingselement bevat de volgende functies:

- Tijd horizontaal voor een week invoeren
- Totalen per dag, rij of week
- Rijen of weken kopiëren
- Tijdinvoer via UU:mm of UU.uu (wordt automatisch UU.uu)
- Importeren vanuit toewijzingen, boekingen of afspraken

Het uitbreiden van tijdinvoer is mogelijk in twee gebieden:
- [Aangepaste tijdinvoer voor eigen gebruik toevoegen](#add)
- [Het besturingselement voor wekelijkse tijdinvoer aanpassen](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Voeg aangepaste tijdinvoer voor eigen gebruik toe.

Tijdinvoer is een kernentiteit die is ontworpen om voor meerdere scenario's te worden gebruikt. In wave 1 in april 2020 werd de TESA-kernoplossing geïntroduceerd die een entiteit **Instellingen** en een nieuwe beveiligingsrol **Tijdinvoergebruiker** bood. De nieuwe velden **msdyn_start** en **msdyn_end**, die een directe relatie hebben met **msdyn_duration**, waren ook inbegrepen. De nieuwe entiteit, beveiligingsrol en velden zorgen voor een meer uniforme benadering van tijd voor meerdere producten.


### <a name="time-source-entity"></a>Entiteit Tijdbron
| Veld | Beschrijving | 
|-------|------------|
| Meetcriterium  | De naam van het tijdbronitem dat wordt gebruikt als selectiewaarde tijdens het maken van tijdinvoer. |
| Standaardtijdbron [Tijdbron: isdefault] | Standaard kan er slechts één tijdbron worden gemarkeerd als standaardtijdbron. Deze mogelijkheid zorgt ervoor dat voor items een standaardtijdbron wordt ingesteld als er geen is opgegeven. |
|Type tijdbron [Tijdbron: sourcetype] | Het brontype is een optie (type tijdinvoerbron) waarmee de tijdbron aan een app kan worden gekoppeld. Extra waarden worden aan deze optieset toegevoegd als er extra toepassingen worden toegevoegd. Houd er rekening mee dat Microsoft waarden hoger dan 190.000.000 terugboekt.|


### <a name="time-entries-and-the-time-source-entity"></a>Tijdinvoer en de entiteit Tijdbron
Elke tijdinvoer is gekoppeld aan een tijdbronrecord. Dit record bepaalt hoe en welke passingen de tijdinvoer moeten verwerken.

Tijdinvoer is altijd een aaneengesloten tijdsblok waaraan het begin, het einde en de duur zijn gekoppeld.

Door de logica wordt het tijdinvoerrecord automatisch bijgewerkt in de volgende situaties:

- Als twee van de volgende drie velden zijn opgegeven, wordt de derde automatisch berekend 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- De velden **msdyn_start** en **msdyn_end** zijn tijdzonebewust.
- Tijdinvoer gemaakt met alleen **msdyn_date** en **msdyn_duration** begint om middernacht en **msdyn_start** en **msdyn_end** worden dienovereenkomstig bijgewerkt.

#### <a name="time-entry-types"></a>Typen tijdinvoer

Records voor tijdinvoer hebben een bijbehorend type dat het gedrag in de indieningsstroom voor de bijbehorende toepassing definieert.

|Etiket | Weergegeven als|
|-----|-----|
|Met pauze   |192,355,000|
|Op reis | 192,355,001|
|Overwerk   | 192,354,320|
|Werk   | 192,350,000|
|Afwezigheid    | 192,350,001|
|Vakantie   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Het besturingselement voor wekelijkse tijdinvoer aanpassen
Ontwikkelaars kunnen extra velden en zoekacties toevoegen aan andere entiteiten en aangepaste bedrijfsregels implementeren om hun bedrijfsscenario's te ondersteunen.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Aangepaste velden met zoekacties voor andere entiteiten toevoegen
Er zijn drie belangrijke stappen voor het toevoegen van een aangepast veld aan het wekelijkse tijdinvoerraster.

- Voeg het aangepaste veld toe aan het dialoogvenster Snelle invoer.
- Configureer het raster om het aangepaste veld weer te geven.
- Voeg het aangepaste veld toe aan de taakstromen voor het bewerken van rijen of cellen.

Zorg ook dat het nieuwe veld de vereiste validaties bevat in de taakstroom voor het bewerken van rijen of cellen. Als onderdeel van deze stap moet u het veld vergrendelen op basis van de status van de tijdinvoer.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Het aangepaste veld toevoegen aan het dialoogvenster Snelle invoer
Voeg het aangepaste veld toe aan het dialoogvenster **Snelle invoer voor tijdsvermelding maken**. Gebruikers kunnen vervolgens een waarde invoeren wanneer ze tijdinvoer toevoegen door **Nieuw** te selecteren.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Het raster configureren om het aangepaste veld weer te geven
Er zijn twee manieren voor het toevoegen van een aangepast veld aan het wekelijkse tijdinvoerraster:

  - Een weergave aanpassen en een aangepast veld toevoegen
  - Een nieuwe standaardtijdinvoer maken 


**Een weergave aanpassen en een aangepast veld toevoegen**

U kunt de weergave **Mijn wekelijkse tijdsvermeldingen** aanpassen en het aangepaste veld hieraan toe te voegen. U kunt de positie en grootte van het aangepaste veld in het raster kiezen door deze eigenschappen in de weergave te bewerken.

**Een nieuwe standaardtijdinvoer maken** 

Deze weergave moet naast de kolommen die u in het raster wilt opnemen, de velden **Beschrijving** en **Externe opmerkingen** bevatten. 

1. Kies de positie, grootte en standaardsorteervolgorde van het raster door deze eigenschappen in de weergave te bewerken. 
2. Configureer het aangepaste besturingselement voor deze weergave, zodat het een besturingselement **Tijdsvermeldingsraster** is. 
3. Voeg dit besturingselement toe aan de weergave en selecteer het voor web, telefoon en tablet. 
4. Configureer de parameters voor het wekelijkse tijdinvoerraster. Stel het veld **Begindatum** in op **msdyn_date**, stel het veld **Duur** in op **msdyn_duration** en stel het veld **Status** in op **msdyn_entrystatus**. 
5. Voor de standaardweergave is het veld **Lijst voor status Alleen-lezen** ingesteld op **192350002, 192350003, 192350004**, het veld **Taakstroom voor rij bewerken** op**msdyn_timeentryrowedit** en het veld **Taakstroom voor cel bewerken** op **msdyn_timeentryedit**. 
6. U kunt deze velden aanpassen om de status alleen-lezen toe te voegen of te verwijderen, of om een andere op taken gebaseerde ervaring (TBX) te gebruiken voor het bewerken van rijen of cellen. Deze velden moeten afhankelijk zijn van een statische waarde.


> [!NOTE] 
> Met beide opties worden sommige standaardfilters voor **project**- en **projecttaak**entiteiten verwijderd, zodat alle opzoekweergaven voor de entiteiten zichtbaar zijn. Standaard zijn alleen de relevante opzoekweergaven zichtbaar.
U moet de juiste taakstroom voor het aangepaste veld bepalen. Als u het veld aan het raster hebt toegevoegd, gaat het waarschijnlijk naar de taakstroom voor rij bewerken die wordt gebruikt voor velden die van toepassing zijn op de hele rij met tijdsvermeldingen. Als het aangepaste veld elke dag een unieke waarde heeft, zoals een aangepast veld voor **Eindtijd**, moet het naar de taakstroom voor cel bewerken gaan.

Als u het aangepaste veld aan een taakstroom wilt toevoegen, sleept u een element **Veld** naar de juiste positie op de pagina en stelt u de veldeigenschappen in. Stel de eigenschap **Bron** in op **Tijdsvermelding** en stel de eigenschap **Gegevensveld** in op het aangepaste veld. De eigenschap **Veld** geeft de weergavenaam aan op de TBX-pagina. Selecteer **Toepassen** om uw wijzigingen in het veld op te slaan en selecteer vervolgens **Bijwerken** om uw wijzigingen op de pagina op te slaan.

Als u in plaats daarvan een nieuwe aangepaste TBX-pagina wilt gebruiken, maakt u een nieuw proces. Stel de categorie in op **Bedrijfsprocesstroom**, stel de entiteit in op **Tijdsvermelding** en stel het bedrijfsprocestype in op **Proces uitvoeren als takenstroom**. Onder **Eigenschappen** moet de eigenschap **Paginanaam** worden ingesteld op de weergavenaam voor de pagina. Voeg alle relevante velden toe aan de TBX-pagina. Sla het proces op en activeer het. Werk vervolgens de aangepaste besturingselementeigenschap voor de desbetreffende taakstroom bij met de waarde van de **Naam** in het proces.

### <a name="add-new-option-set-values"></a>Nieuwe optiesetwaarden toevoegen
Als u optiesetwaarden wilt toevoegen aan een standaardveld, opent u de bewerkingspagina voor het veld en selecteert u vervolgens onder **Type** de optie **Bewerken** naast de optieset. Voeg vervolgens een nieuwe optie toe met een aangepast label en een aangepaste kleur. Als u een nieuwe status voor de tijdsvermelding wilt toevoegen, krijgt het standaardveld de naam **Vermeldingsstatus**, niet **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Een nieuwe status voor een tijdsvermelding aanwijzen als alleen-lezen
Als u een nieuwe tiijdsvermeldingsstatus wilt aanwijzen als alleen-lezen, voegt u de nieuwe waarde voor de tijdsvermelding toe aan de eigenschap **Lijst voor status Alleen-lezen**. Het bewerkbare deel van het tijdinvoerraster wordt vergrendeld voor rijen met de nieuwe status.
Voeg vervolgens bedrijfsregels toe om alle velden op de pagina's **Rij met tijdsvermelding bewerken** en **Tijdsvermelding bewerken** te vergrendelen. U hebt toegang tot de bedrijfsregels voor deze pagina's door de bedrijfsprocesstroom-editor voor de pagina te openen en vervolgens **Bedrijfsregels** te selecteren. U kunt de nieuwe status toevoegen aan de voorwaarde in de bestaande bedrijfsregels of u kunt een nieuwe bedrijfsregel toevoegen voor de nieuwe status.

### <a name="add-custom-validation-rules"></a>Aangepaste validatieregels toevoegen
Er zijn twee soorten validatieregels die u kunt toevoegen voor de functie voor het wekelijkse tijdsvermeldingsraster:

- Bedrijfsregels op de client die werken in dialoogvensters voor snelle invoer en op TBX-pagina's.
- Validatie van invoegtoepassingen op de server die van toepassing zijn op alle updates van tijdsvermeldingen.

#### <a name="business-rules"></a>Bedrijfsregels
Gebruik bedrijfsregels om velden te vergrendelen en te ontgrendelen, standaardwaarden in te voeren in velden en validaties te definiëren die alleen informatie uit de huidige tijdsvermeldingsrecord vereisen. U hebt toegang tot de bedrijfsregels voor een TBX-pagina door de bedrijfsprocesstroom-editor voor de pagina te openen en vervolgens **Bedrijfsregels** te selecteren. U kunt vervolgens de bestaande bedrijfsregels bewerken of een nieuwe bedrijfsregel toevoegen. Voor nog meer aangepaste validaties kunt u een bedrijfsregel gebruiken om JavaScript uit te voeren.

#### <a name="plug-in-validations"></a>Validaties van invoegtoepassingen
U moet validaties van invoegtoepassingen gebruiken voor validaties die meer context vereisen dan beschikbaar is in één tijdsvermeldingsrecord of voor eventuele validaties die u wilt uitvoeren op inline-updates in het raster. Als u de validatie wilt voltooien, maakt u een aangepaste invoegtoepassing in de entiteit **Tijdsvermelding**.

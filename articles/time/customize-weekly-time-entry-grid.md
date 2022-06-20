---
title: Tijdinvoer uitbreiden
description: Dit artikel biedt informatie over hoe ontwikkelaars het besturingselement voor tijdinvoer kunnen uitbreiden.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914764"
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

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Aangepaste tijdinvoer voor eigen gebruik toevoegen

Tijdinvoer is een kernentiteit die in meerdere scenario's wordt gebruikt. In april Wave 1 2020 werd de TESA-kernoplossing geïntroduceerd. TESA biedt een **Instellingen**-entiteit en de nieuwe beveiligingsrol **Gebruiker tijdinvoer**. De nieuwe velden **msdyn_start** en **msdyn_end**, die een directe relatie hebben met **msdyn_duration**, waren ook inbegrepen. De nieuwe entiteit, beveiligingsrol en velden zorgen voor een meer uniforme benadering van tijd voor meerdere producten.


### <a name="time-source-entity"></a>Entiteit Tijdbron
| Veld | Beschrijving | 
|-------|------------|
| Meetcriterium  | De naam van de tijdbroninvoer die wordt gebruikt als selectiewaarde bij het maken van tijdinvoer. |
| Standaardtijdbron [Tijdbron: isdefault] | Standaard kan er slechts één tijdbron worden gemarkeerd als standaardtijdbron. Hierdoor kunnen items standaard worden ingesteld op een tijdbron als er geen is opgegeven. |
|Type tijdbron [Tijdbron: sourcetype] | Het brontype is een optie (type tijdinvoerbron) waarmee de tijdbron aan een app kan worden gekoppeld. Microsoft boekt waarden hoger dan 190.000.000 terug.|


### <a name="time-entries-and-the-time-source-entity"></a>Tijdinvoer en de entiteit Tijdbron
Elke tijdinvoer is gekoppeld aan een tijdbronrecord. Deze record bepaalt welke toepassingen de tijdsvermelding moeten verwerken en hoe dit moet gebeuren.

Tijdinvoer is altijd een aaneengesloten tijdsblok waaraan het begin, het einde en de duur zijn gekoppeld.

Door de logica wordt het tijdinvoerrecord automatisch bijgewerkt in de volgende situaties:

- Als twee van de volgende drie velden zijn opgegeven, wordt het derde veld automatisch berekend: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- De velden **msdyn_start** en **msdyn_end** zijn tijdzonebewust.
- Tijdinvoer die is gemaakt terwijl alleen **msdyn_date** en **msdyn_duration** zijn opgegeven, begint om middernacht. De velden **msdyn_start** en **msdyn_end** worden dienovereenkomstig bijgewerkt.

#### <a name="time-entry-types"></a>Typen tijdinvoer

Records voor tijdinvoer hebben een bijbehorend type waarmee het gedrag in de indieningsstroom voor de bijbehorende toepassing wordt gedefinieerd.

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

1. Voeg het aangepaste veld toe aan het dialoogvenster **Snelle invoer**.
2. Configureer het raster om het aangepaste veld weer te geven.
3. Voeg het aangepaste veld toe aan de pagina **Rij bewerken** of **Tijdsvermelding bewerken**, indien van toepassing.

Zorg ervoor dat het nieuwe veld de vereiste validaties bevat op de pagina **Rij bewerken** of **Tijdsvermelding bewerken**. Als onderdeel van deze taak vergrendelt u het veld op basis van de status van de tijdsvermelding.

Wanneer u een aangepast veld toevoegt aan het raster **Tijdsvermelding** raster en vervolgens tijdsvermeldingen rechtstreeks in het raster maakt, wordt het aangepaste veld voor die vermeldingen automatisch zo ingesteld dat deze overeenkomt met de rij. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Voeg het aangepaste veld toe aan het dialoogvenster Snelle invoer
Voeg het aangepaste veld toe aan het dialoogvenster **Snelle invoer: Tijdsvermelding maken**. Gebruikers kunnen vervolgens een waarde invoeren wanneer ze tijdinvoer toevoegen door **Nieuw** te selecteren.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Het raster configureren om het aangepaste veld weer te geven
Er zijn twee manieren voor het toevoegen van een aangepast veld aan het raster **Wekelijkse tijdsvermeldingen**:

- Pas de weergave **Mijn wekelijkse tijdsvermeldingen** aan en voeg het aangepaste veld hieraan toe. U kunt de positie en grootte van het aangepaste veld in het raster opgeeven door de eigenschappen in de weergave te bewerken.
- Maak een nieuwe aangepaste weergave voor tijdsvermeldingen en stel deze in als de standaardweergave. Deze weergave moet de velden **Beschrijving** en **Externe opmerkingen** bevatten, naast de kolommen die u in het raster wilt opnemen. U kunt de positie, grootte en standaardsorteervolgorde van het raster opgeven door de eigenschappen in de weergave te bewerken. Vervolgens configureert u het aangepaste besturingselement voor deze weergave, zodat het een besturingselement voor een **Tijdinvoerraster** is. Voeg de besturingselement toe aan de weergave en selecteer het voor **Web**, **Telefoon** en **Tablet**. Configureer vervolgens de parameters voor het raster **Wekelijke tijdsvermeldingen**. Stel het veld **Begindatum** in op **msdyn\_date**, stel het veld **Duur** in op **msdyn\_duration** en stel het veld **Status** in op **msdyn\_entrystatus**. Het veld **Lijst voor status Alleen-lezen** is ingesteld op **192350002 (Goedgekeurd)**, **192350003 (Ingediend)** of **192350004 (Intrekking aangevraagd)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Het aangepaste veld toevoegen aan de juiste bewerkingspagina
De pagina's die worden gebruikt om een tijdsvermelding of een rij met tijdvermeldingen te bewerken, vindt u onder **Formulieren**. De knop **Vermelding bewerken** in het raster opent de pagina **Vermelding bewerken** en de knop **Rij bewerken** opent de pagina **Rij bewerken**. U kunt deze pagina's bewerken zodat ze aangepaste velden bevatten.

Met beide opties worden sommige standaardfilters voor entiteiten **Project** en **Projecttaak** verwijderd, zodat alle opzoekweergaven voor de entiteiten zichtbaar zijn. Standaard zijn alleen de relevante opzoekweergaven zichtbaar.

U moet de juiste pagina voor het aangepaste veld bepalen. Als u het veld aan het raster hebt toegevoegd, gaat het waarschijnlijk naar de pagina **Rij bewerken** die wordt gebruikt voor velden die van toepassing zijn op de hele rij met tijdsvermeldingen. Als het aangepaste veld elke dag een unieke waarde in de rij heeft (bijvoorbeeld als het een aangepast veld voor de eindtijd is), moet het naar de pagina **Tijdsvermelding bewerken** gaan.

Als u het aangepaste veld aan een pagina wilt toevoegen, sleept u een element **Veld** naar de juiste positie op de pagina en stelt u de eigenschappen ervan in.

### <a name="add-new-option-set-values"></a>Nieuwe optiesetwaarden toevoegen
Volg deze stappen als u optiesetwaarden wilt toevoegen aan een standaardveld.

1. Open de bewerkingspagina voor het veld en selecteer vervolgens onder **Type** de optie **Bewerken** naast de optieset.
2. Voeg een nieuwe optie toe met een aangepast label en een aangepaste kleur. Als u een nieuwe status voor de tijdsvermelding wilt toevoegen, krijgt het standaardveld de naam **Vermeldingsstatus**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Een nieuwe status voor een tijdsvermelding aanwijzen als alleen-lezen
Als u een nieuwe tiijdsvermeldingsstatus wilt aanwijzen als alleen-lezen, voegt u de nieuwe waarde voor de tijdsvermelding toe aan de eigenschap **Lijst voor status Alleen-lezen**. Zorg ervoor dat u het nummer toevoegt, niet het label. Het bewerkbare deel van het tijdinvoerraster wordt nu vergrendeld voor rijen met de nieuwe status. Als u de eigenschap **Lijst voor status Alleen-lezen** wilt instellen op een andere waarde voor verschillende weergaven van **Tijdsvermelding**, voegt u het raster **Tijdsvermelding** toe in de sectie **Aangepaste besturingselementen** van een weergave en configureert u de parameters zoals van toepassing.

Voeg vervolgens bedrijfsregels toe om alle velden op de pagina's **Rij bewerken** en **Tijdsvermelding bewerken** te vergrendelen. U kunt toegang krijgen tot de bedrijfsregels voor deze pagina's door de fomuliereneditor voor elke pagina te openen en vervolgens **Bedrijfsregels** te selecteren. U kunt de nieuwe status toevoegen aan de voorwaarde in de bestaande bedrijfsregels of u kunt een nieuwe bedrijfsregel toevoegen voor de nieuwe status.

### <a name="add-custom-validation-rules"></a>Aangepaste validatieregels toevoegen
U kunt twee typen validatieregels toevoegen voor de rasterervaring **Wekelijkse tijdsvermeldingen**:

- Bedrijfsregels op de client die werken op pagina's
- Validatie van invoegtoepassingen op de server die van toepassing zijn op alle updates van tijdsvermeldingen

#### <a name="client-side-business-rules"></a>Bedrijfsregels op de client
Gebruik bedrijfsregels om velden te vergrendelen en te ontgrendelen, standaardwaarden in te voeren in velden en validaties te definiëren die alleen informatie uit de huidige tijdsvermeldingsrecord vereisen. U kunt toegang krijgen tot de bedrijfsregels voor een pagina door de fomuliereneditor te openen en vervolgens **Bedrijfsregels** te selecteren. U kunt vervolgens de bestaande bedrijfsregels bewerken of een nieuwe bedrijfsregel toevoegen.

#### <a name="server-side-plug-in-validations"></a>Validaties van invoertoepassingen op de server
U moet validaties van invoegtoepassingen gebruiken voor validaties die meer context vereisen dan beschikbaar is in één tijdsvermeldingsrecord. U moet ze ook gebruiken voor eventuele validaties die u wilt uitvoeren op inline-updates in het raster. Als u de validaties wilt voltooien, maakt u een aangepaste invoegtoepassing in de entiteit **Tijdsvermelding**.

### <a name="limits"></a>Limieten
Momenteel heeft het raster **Tijdsvermelding** een maximale grootte van 500 rijen. Als er meer dan 500 rijen zijn, worden de extra rijen niet weergegeven. Er is geen manier om deze limiet te verhogen.

### <a name="copying-time-entries"></a>Tijdsvermeldingen kopiëren
Gebruik de weergave **Kolommen met tijdsvermelding kopiëren** om de lijst met velden te definiëren die moeten worden gekopieerd tijdens het invoeren van tijd. **Datum** en **Duur** zijn verplichte velden en mogen niet uit de weergave worden verwijderd.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

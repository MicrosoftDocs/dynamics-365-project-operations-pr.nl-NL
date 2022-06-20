---
title: Wekelijkse tijdinvoer aanpassen
description: Dit artikel bevat informatie over het implementeren van aangepaste bedrijfsregels die de werkwijzen van een organisatie ondersteunen.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: bdc8df4050d895504fa126e2ee55fcd3b4de123f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918950"
---
# <a name="customize-weekly-time-entry"></a>Wekelijkse tijdinvoer aanpassen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Microsoft Dynamics 365 Project Service Automation versie 3.3 heeft Microsoft een modern raster geïntroduceerd waarin projectresources snel uren kunnen invoeren voor maximaal één week tegelijk. Het nieuwe wekelijkse tijdinvoerraster kan totalen weergeven voor vermeldingen per datum, per rij of per week. Resources kunnen kopieën maken van tijdsvermeldingen binnen de week en ook bulksgewijs kopiëren van eerdere weken. Systeemaanpassers kunnen de weergave aanpassen door velden toe te voegen, zoekopdrachten toe te voegen aan andere entiteiten en aangepaste bedrijfsregels te implementeren om de werkwijze van hun organisatie te ondersteunen.

Tijdsvermeldingen en het nieuwe wekelijkse tijdraster zijn toegankelijk via het siteoverzicht. De niet-uitbreidbare functionaliteit voor tijdsvermeldingen die deel uitmaakte van eerdere PSA-versies, is vervangen door het uitbreidbare wekelijkse raster voor tijdsvermeldingen en een alternatieve voorzieningen voor het alleen-lezen raster en de agenda. Vanwege deze wijziging kunnen gebruikers tijd invoeren in wekelijkse hoeveelheden.

## <a name="page-layout"></a>Pagina-indeling
Het nieuwe wekelijkse tijdinvoerraster is een aangepast besturingselement met een werkbalk en de twee hoofdsecties **Dimensies** en **Duur**. De werkbalk bevat een knop die alleen van toepassing is op dit aangepaste besturingselement voor het tijdinvoerraster. De knoppen in het actievenster boven aan de pagina zijn daarentegen van toepassing op de drie typen besturingselementen die worden ondersteund voor tijdinvoer: de wekelijkse tijdinvoer, het besturingselement alleen-lezen en het agendabesturingselement.

### <a name="dimensions"></a>Afmetingen
De sectie **Dimensies** bevat, als kolomkoppen, alle dimensies waarvoor tijd kan worden ingevoerd. De volgende dimensies worden standaard ondersteund:

- Project
- Projecttaak
- Rol
- Type
- Vermeldingsstatus

De sectie **Dimensies** staat geen inline bewerking toe. Deze sectie wordt ondersteund door een weergave waarmee aangepaste velden kunnen worden toegevoegd aan het wekelijkse tijdinvoerraster. Zie de sectie "Uitbreidbaarheid" verderop in dit artikel voor meer informatie over het toevoegen van aangepaste velden.

### <a name="duration"></a>Duration
In de sectie Duur worden de dagen van de week weergegeven als kolomkoppen. In deze sectie is ook inline bewerken mogelijk. Nadat een rij voor tijdinvoer is gemaakt met de juiste dimensies, kunnen gebruikers snel inline de hoeveelheid tijd invoeren die ze aan deze dimensies hebben besteed.

## <a name="create-a-new-time-entry"></a>Een nieuwe tijdsvermelding maken
Als u een nieuwe tijdsvermelding wilt maken in het tijdinvoerraster, selecteert u **Nieuw**. Het dialoogvenster **Snelle invoer van tijdsvermelding** wordt weergegeven. In dit dialoogvenster kunnen gebruikers de tijdvermeldingsdatum selecteren en vervolgens gegevens invoeren voor de dimensies **Project**, **Projecttaak**, **Rol** en **Duur** in minuten, uren of dagen door **u**, **m** of **d** in te voeren, samen met het aantal. Gebruikers kunnen ook een beschrijving en opmerkingen invoeren die extern kunnen worden gedeeld voor de tijdinvoer. Wanneer gebruikers hun wijzigingen opslaan, worden de waarden die ze hebben ingevoerd voor de dimensies weergegeven in de sectie **Dimensies**. De gegevens over duur die in het veld **Duur** zijn ingevoerd, worden weergegeven op de datum waarop de tijdsvermelding is gemaakt.

Opzoekvelden worden ondersteund door systeemweergaven. Nadat een gebruiker bijvoorbeeld een project heeft ingevoerd, wordt het veld **Projecttaak** standaard ingesteld op de weergave **Kopiëren**. Als u tijdsvermeldingen wilt maken voor taken die niet aan een gebruiker zijn toegewezen, klikt u op **Weergave wijzigen** in het zoekvenster en selecteert u de weergave **Alle actieve projecttaken**.

## <a name="edit-a-time-entry"></a>Een tijdsvermelding bewerken
Details van bepaalde velden op de pagina voor tijdinvoer, zoals **Beschrijving** en **Externe opmerkingen**, worden niet weergegeven in het wekelijkse tijdinvoerraster. In plaats daarvan wordt een kleine driehoekige indicator weergegeven in duurcellen waarvoor aanvullende gegevens bestaan. Selecteer de cel en selecteer vervolgens **Details bewerken** om de gegevens in het deelvenster **Snel bewerken** weer te geven. Als u de details voor een specifieke tijdsvermelding wilt bewerken of bijwerken die niet deel uitmaakt van het wekelijkse tijdinvoerraster, moeten gebruikers het deelvenster **Snel bewerken** openen.

## <a name="copy-a-time-entry-row"></a>Een rij met tijdinvoer kopiëren
Nadat de eerste rij voor de tijdinvoer is gemaakt, kunnen gebruikers **Rij kopiëren** selecteren om de hele rij naar een nieuwe rij te kopiëren. Wanneer een rij op deze manier wordt gekopieerd, worden ook dimensies en duur gekopieerd. Gebruikers kunnen ook **Rij bewerken** selecteren om dimensiewaarden en duur inline bij te werken in de sectie **Duur**.

## <a name="open-a-time-entry"></a>Een tijdsvermelding openen
Om een optimale en snelle invoer in de belangrijkste velden te ondersteunen, wordt in het wekelijkse tijdinvoerraster een subset van de geselecteerde dimensies en tijdsduur weergegeven. Als u alle details van een enkele tijdsvermelding wilt weergeven , selecteert u onder **Vermelding bewerken** de optie **Openen**.

## <a name="submit-a-time-entry"></a>Een tijdsvermelding indienen
Gebruikers kunnen één tijdsvermelding of een groep tijdsvermeldingen indienen door een blok cellen of een hele rij met tijdsvermeldingen te selecteren en vervolgens **Indienen** te kiezen. Ingediende tijdsvermeldingen worden weergegeven als posten die wachten op goedkeuring op de pagina **Goedkeuring** van de fiatteurs. Nadat de tijdsvermeldingen zijn verzonden, kunnen ze niet meer worden bewerkt.

## <a name="recall-a-time-entry"></a>Een tijdsvermelding intrekken
U kunt tijdvermeldingen die u hebt ingediend, intrekken. U kunt één tijdsvermelding, een blok met tijdsvermeldingen of een hele rij met tijdsvermeldingen intrekken. Teruggeroepen tijdsvermeldingen kunnen worden bewerkt door resources.

## <a name="time-entry-status"></a>Status van tijdsvermelding
Nieuwe tijdsvermeldingen krijgen automatisch de status **Concept** toegewezen. Wanneer een tijdsvermelding wordt ingediend, wordt de status bijgewerkt naar **Ingediend**. Wanneer een ingediende tijdsvermelding wordt goedgekeurd, wordt de status bijgewerkt naar **Goedgekeurd**. Als een tijdsvermelding wordt afgewezen, wordt de status bijgewerkt naar **Geretourneerd** en wordt de vermelding beschikbaar voor correctie en opnieuw indienen. Alleen tijdsvermeldingen met de status **Concept** kunnen worden verwijderd.

## <a name="view-rejection-comments"></a>Opmerkingen bij afwijzing weergeven
Wanneer een tijdsvermelding wordt afgewezen door een fiatteur, kan de fiatteur opmerkingen voor afwijzing toevoegen om de resource te helpen de reden voor de afwijzing te begrijpen. Als u de afwijzingsopmerkingen voor een tijdsvermelding wilt weergeven, selecteert u **Vermelding openen**. De opmerkingen voor afwijzing worden weergegeven in de tijdlijn. In de tijdlijn kan de resource reageren op de afwijzingsopmerkingen voordat hij of zij de vermelding opnieuw indient.

## <a name="copy-week"></a>Week kopiëren
Nadat er enkele tijdsvermeldingen zijn gemaakt, kunnen gebruikers **Week kopiëren** selecteren om bulksgewijs extra tijdsvermeldingen te maken. Het dialoogvenster **Kopiëren** wordt weergegeven. Gebruik in de sectie **Van-periode** de velden **Begindatum** en **Einddatum** om het datumbereik te definiëren waaruit u tijdsvermeldingen wilt kopiëren. Geef in de sectie **Tot-periode** in het veld **Begindatum** de datum op waarop u tijdsvermeldingen wilt maken. Selecteer vervolgens **Kopiëren**. Vervolgens wordt voor de opgegeven datum in de "tot"-periode een kopie gemaakt van de tijdsvermeldingen van de overeenkomstige dag van de week in de "van"-periode. De tijdsvermelding van maandag van vorige week wordt bijvoorbeeld gekopieerd naar maandag voor de week die is aangegeven in de "tot"-periode.

## <a name="import"></a>Importeren
Hetzelfde basisproces wordt gebruikt om te importeren uit boekingen, toewijzingen en uitwisselingen. Gebruikers kunnen het datumbereik opgeven waaruit boekingen worden geïmporteerd. Vervolgens moeten ze expliciet de boekingen selecteren die moeten worden gekopieerd naar de concept-tijdsvermeldingen. In de vorige release werden voorgestelde tijdsvermeldingen in het raster en in de agenda weergegeven die verloren gingen bij het vernieuwen van de sessie.

## <a name="extensibility"></a>-uitbreidbaarheid
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Aangepaste velden toevoegen met zoekacties voor andere entiteiten
Er zijn drie belangrijke stappen voor het toevoegen van een aangepast veld aan het wekelijkse tijdinvoerraster.

1.  Voeg het aangepaste veld toe aan het dialoogvenster Snelle invoer.
2.  Configureer het raster om het aangepaste veld weer te geven.
3.  Voeg het aangepaste veld toe aan de taakstromen voor het bewerken van rijen of cellen, indien van toepassing.

Zorg ook dat het nieuwe veld de vereiste validaties bevat in de taakstroom voor het bewerken van rijen of cellen. Als onderdeel van deze stap moet u het veld vergrendelen op basis van de status van de tijdsvermelding.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Het aangepaste veld toevoegen aan het dialoogvenster Snelle invoer
Voeg het aangepaste veld toe aan het dialoogvenster Snelle invoer voor tijdsvermelding maken. Gebruikers kunnen dan een waarde invoeren wanneer ze tijdsvermeldingen toevoegen met de knop **Nieuw**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Het raster configureren om het aangepaste veld weer te geven
Er zijn twee manieren voor het toevoegen van een aangepast veld aan het wekelijkse tijdinvoerraster. De eerste optie is het aanpassen van de weergave **Mijn wekelijkse tijdsvermeldingen** en het aangepaste veld hieraan toe te voegen. U kunt de positie en grootte van het aangepaste veld in het raster kiezen door deze eigenschappen in de weergave te bewerken.

De tweede optie is om een nieuwe aangepaste weergave voor tijdsvermeldingen te maken en deze in te stellen als de standaardweergave. Deze weergave moet naast de kolommen die u in het raster wilt opnemen, de velden **Beschrijving** en **Externe opmerkingen** bevatten. U kunt de positie, grootte en standaardsorteervolgorde van het raster kiezen door deze eigenschappen in de weergave te bewerken. Vervolgens configureert u het aangepaste besturingselement voor deze weergave, zodat het een besturingselement voor een **Tijdinvoerraster** is. Voeg dit besturingselement toe aan de weergave en selecteer het voor web, telefoon en tablet. Configureer vervolgens de parameters voor het wekelijkse tijdinvoerraster. Stel het veld **Begindatum** in op **msdyn_date**, stel het veld **Duur** in op **msdyn_duration** en stel het veld **Status** in op **msdyn_entrystatus**. Voor de standaardweergave is het veld **Lijst voor status Alleen-lezen** ingesteld op **192350002, 192350003, 192350004**, het veld **Taakstroom voor rij bewerken** op **msdyn_timeentryrowedit** en het veld **Taakstroom voor cel bewerken** op **msdyn_timeentryedit**. U kunt deze velden aanpassen om de status alleen-lezen toe te voegen of te verwijderen, of om een andere op taken gebaseerde ervaring (TBX) te gebruiken voor het bewerken van rijen of cellen. Deze velden moeten afhankelijk zijn van een statische waarde.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Het aangepaste veld toevoegen aan de juiste bewerkingsstroom voor taken
De TBX-pagina's die worden gebruikt voor bewerken bevinden zich onder **Processen**. De standaardpagina's zijn **Project Service - Rij met tijdsvermelding bewerken** en **Project Service - Tijdsvermelding bewerken**. U kunt deze standaardpagina's bewerken of nieuwe aangepaste TBX-pagina's maken.

> [!NOTE] 
> Met beide opties worden sommige standaardfilters voor **project**- en **projecttaak** entiteiten verwijderd, zodat alle opzoekweergaven voor de entiteiten zichtbaar zijn. Standaard zijn alleen de relevante opzoekweergaven zichtbaar.

U moet de juiste taakstroom voor het aangepaste veld bepalen. Als u het veld aan het raster hebt toegevoegd, gaat het waarschijnlijk naar de taakstroom voor rij bewerken die wordt gebruikt voor velden die van toepassing zijn op de hele rij met tijdsvermeldingen. Als het aangepaste veld elke dag een unieke waarde heeft, zoals een aangepast veld voor **Eindtijd**, moet het naar de taakstroom voor cel bewerken gaan.

Als u het aangepaste veld aan een taakstroom wilt toevoegen, sleept u een **veld** element naar de juiste positie op de pagina en stelt u de eigenschappen ervan in. Stel de eigenschap **Bron** in op **Tijdsvermelding** en stel de eigenschap **Gegevensveld** in op het aangepaste veld. De eigenschap **Veld** geeft de weergavenaam aan op de TBX-pagina. Selecteer **Toepassen** om uw wijzigingen in het veld op te slaan. Selecteer **Bijwerken** om uw wijzigingen in de pagina op te slaan.

Als u in plaats daarvan een nieuwe aangepaste TBX-pagina wilt gebruiken, maakt u een nieuw proces. Stel de categorie in op **Bedrijfsprocesstroom**, stel de entiteit in op **Tijdsvermelding** en stel het bedrijfsprocestype in op **Proces uitvoeren als takenstroom**. Onder **Eigenschappen** moet de eigenschap **Paginanaam** worden ingesteld op de weergavenaam voor de pagina. Voeg alle relevante velden toe aan de TBX-pagina. Sla het proces op en activeer het. Werk vervolgens de aangepaste besturingselementeigenschap voor de desbetreffende taakstroom bij met de waarde van de **Naam** in het proces.

### <a name="add-new-option-set-values"></a>Nieuwe optiesetwaarden toevoegen
Als u optiesetwaarden wilt toevoegen aan een standaardveld, opent u de bewerkingspagina voor het veld en selecteert u vervolgens onder **Type** de optie **Bewerken** naast de optieset. Voeg vervolgens een nieuwe optie toe met een aangepast label en een aangepaste kleur. Als u een nieuwe status voor de tijdsvermelding wilt toevoegen, krijgt het standaardveld de naam **Vermeldingsstatus**, niet **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Een nieuwe status voor een tijdsvermelding aanwijzen als alleen-lezen
Als u een nieuwe tiijdsvermeldingsstatus wilt aanwijzen als alleen-lezen, voegt u de nieuwe waarde voor de tijdsvermelding (het nummer, niet het label) toe aan de eigenschap **Lijst voor status Alleen-lezen**. Het bewerkbare deel van het tijdinvoerraster wordt vergrendeld voor rijen met de nieuwe status.
Voeg vervolgens bedrijfsregels toe om alle velden op de pagina's **Rij met tijdsvermelding bewerken** en **Tijdsvermelding bewerken** te vergrendelen. U hebt toegang tot de bedrijfsregels voor deze pagina's door de bedrijfsprocesstroom-editor voor de pagina te openen en vervolgens **Bedrijfsregels** te selecteren. U kunt de nieuwe status toevoegen aan de voorwaarde in de bestaande bedrijfsregels of u kunt een nieuwe bedrijfsregel toevoegen voor de nieuwe status.

### <a name="add-custom-validation-rules"></a>Aangepaste validatieregels toevoegen
Er zijn twee typen validatieregels die u toevoegen voor het wekelijkse tijdinvoerraster: • bedrijfsregels op de client die werken in dialoogvensters voor snelle invoer en op TBX-pagina's • validatie van invoegtoepassingen op de server die van toepassing op alle updates van tijdsvermeldingen

#### <a name="business-rules"></a>Bedrijfsregels
Gebruik bedrijfsregels om velden te vergrendelen en te ontgrendelen, standaardwaarden in te voeren in velden en validaties te definiëren die alleen informatie uit de huidige tijdsvermeldingsrecord vereisen. U hebt toegang tot de bedrijfsregels voor een TBX-pagina door de bedrijfsprocesstroom-editor voor de pagina te openen en vervolgens **Bedrijfsregels** te selecteren. U kunt vervolgens de bestaande bedrijfsregels bewerken of een nieuwe bedrijfsregel toevoegen. Voor nog meer aangepaste validaties kunt u een bedrijfsregel gebruiken om JavaScript uit te voeren.

#### <a name="plug-in-validations"></a>Validaties van invoegtoepassingen
U moet validaties van invoegtoepassingen gebruiken voor validaties die meer context vereisen dan beschikbaar is in één tijdsvermeldingsrecord of voor eventuele validaties die u wilt uitvoeren op inline-updates in het raster. Als u de validatie wilt voltooien, maakt u een aangepaste invoegtoepassing in de entiteit **Tijdsvermelding**.

> [!IMPORTANT] 
> Op dit moment voorkomt een bekend probleem op de TBX-pagina's dat gebruikers informatie kunnen corrigeren en Gereed selecteren wanneer een update niet kan worden gevalideerd voor een invoegtoepassing. Als tijdelijke oplossing kunt u zakelijke regelvalidaties instellen om deze situatie zoveel mogelijk te voorkomen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

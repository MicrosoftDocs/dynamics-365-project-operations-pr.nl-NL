---
title: Koptekstdetails voor subcontracten
description: In dit artikel wordt de functionaliteit uitgelegd die wordt geboden in de subcontractheader in Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 85649d08228b16178eb8d6be9af5a6731def74bf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914166"
---
# <a name="header-details-for-subcontracts"></a>Koptekstdetails voor subcontracten

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In dit artikel wordt de functionaliteit uitgelegd die wordt geboden in de subcontractheader in Dynamics 365 Project Operations.

Omdat een projectmanager projecten plant en uitvoert, kunnen ze onderaannemers in dienst hebben en producten en diensten van leveranciers kopen. Wanneer een projectmanager producten of diensten moet kopen, kunnen ze een subcontract maken in Project Operations.

Voer de volgende stappen uit om een subcontract te maken.

1. Selecteer in het navigatievenster de optie **Subcontracten** en selecteer op de pagina **Subcontract** de optie **Nieuw**.
2. Geef de vereiste informatie op en selecteer vervolgens **Opslaan**.

    De volgende tabel bevat informatie over de velden op de pagina **Koptekst subcontract**.

    | Veld | Beschrijving |Functionele impact |
    |---|------|---| 
    | Meetcriterium | De naam van het subcontract. | In alle vervolgkeuzelijsten voor subcontracten wordt de naam van het subcontract vermeld in de eerste kolom om u te helpen bij het identificeren van het subcontract. | 
    | Beschrijving | Een korte beschrijving van services en producten die worden gekocht in het subcontract. | Geen |
    | Verkoper | De naam van het bedrijf waarvan de producten en diensten worden gekocht. Deze accountrecord heeft het relatietype **Verkoper** of **Leverancier**. | Op basis van de geselecteerde leverancier worden automatisch standaardwaarden ingevoerd voor de volgende velden:<br/> **• Valuta** </br> **• Prijslijsten** </br> **• Betalingsvoorwaarden**</br> **• Betalingsadres**</br> **• Factuuradres**</br> **• Naam voor factuur** </br>**• Leveranciersaccountmanager**|
    | Datum subcontract | De datum waarop het subcontract is gemaakt. | De datum van het subcontract wordt gebruikt om de juiste inkoopprijslijst te selecteren uit de prijslijsten die aan de gerelateerde leverancier zijn gekoppeld of uit de projectparameters. |
    | Reden van status | De status van het subcontract. | De status bepaalt waar het subcontract zich in het bedrijfsproces bevindt en of het kan worden bewerkt. <br/>Tot de waarden behoren:<br>• **Concept**: het subcontract kan worden bewerkt. U kunt alleen subcontracten bewerken met de status **Concept**.<br/>• **Bevestigd**: de onderhandeling met de verkoper is afgerond en het subcontract is goedgekeurd voor levering. <br/>• **Gesloten**: de levering volgens het subcontract is voltooid.<br/>• **Geannuleerd**: het subcontract is geannuleerd en er is geen levering gepland.  | 
    | Valuta | De valuta waarin producten en services worden gekocht. De standaardwaarde wordt automatisch ingevoerd vanuit het leveranciersaccount, maar kan worden gewijzigd. | De valuta van het subcontract wordt gebruikt om de inkoopprijslijst te selecteren uit de prijslijsten die aan de gerelateerde leverancier zijn gekoppeld of uit de projectparameters. Prijslijsten in een andere valuta kunnen niet aan het subcontract worden gekoppeld. De kosten van tijd, uitgaven en materialen die leveranciersresources uit dit subcontract leveren, worden in deze valuta vastgelegd voor het project. Nadat de subcontractrecord is opgeslagen, kan de valuta op het subcontract niet meer worden gewijzigd.|
    | Contracterende eenheid | De afdeling van het bedrijf die een koop- of een subcontractovereenkomst aangaat met de leverancier. | Geen |
    | Betalingsvoorwaarden | De betalingsvoorwaarden op leveranciersfacturen die zijn uitgegeven voor dit subcontract. De standaardwaarde wordt automatisch ingevoerd vanuit de leveranciersaccountrecord. | Betalingscondities uit het subcontract worden gekopieerd naar alle leveranciersfacturen die betrekking hebben op dit subcontract. Betalingsvoorwaarden kunnen worden bijgewerkt als het subcontract de status **Concept** heeft. | 
    | Betalingsadres | Het adres van de leverancier waarnaar de betalingen moeten worden verzonden. De standaardwaarde wordt automatisch ingevoerd vanuit de leveranciersaccountrecord. | Het betalingsadres van het subcontract wordt als betalingsadres gekopieerd naar alle leveranciersfacturen die voor dit subcontract worden gemaakt. Het betalingsadres kan worden bijgewerkt als het subcontract de status **Concept** heeft.|
    | Naam voor factuur | De naam van de persoon of afdeling in het bedrijf van de leverancier die de factuur verzendt. De standaardwaarde wordt automatisch ingevoerd vanuit de leveranciersaccountrecord. | De waarde bij **Naam voor factuur** uit het subcontract wordt gekopieerd naar alle leveranciersfacturen die betrekking hebben op dit subcontract. Dit veld kan worden bijgewerkt als het subcontract de status **Concept** heeft.|
    | Factuuradres | Het adres dat wordt gebruikt op facturen van de leverancier. De standaardwaarde wordt automatisch ingevoerd vanuit de leveranciersaccountrecord. | Dit adres is het "factuur van"-adres op leveranciersfacturen die voor dit subcontract zijn gemaakt. |
    | Subtotaal | Als een subcontract geen regels heeft, voert u het subtotaal van de order vóór belastingen in. Als het subcontract regels heeft, is dit veld alleen-lezen. Het weergegeven bedrag is het subtotaalbedrag van alle regels op het subcontract. | Geen |
    | Totale belasting | Als een subcontract geen regels heeft, voert u de totale belastingen voor dit subcontract in. Als het subcontract regels heeft, is dit veld alleen-lezen. Het weergegeven bedrag is de som van het belastingbedrag van alle regels op het subcontract. | Geen |
    | Totale bedrag | Dit berekende veld toont het totale bedrag van de subcontract, inclusief belastingen. | Geen |
    | Bevestigde datum | De datum waarop het subcontract is bevestigd. | Geen |
    | Aangevraagd door | Dit veld is standaard ingesteld op de naam van de gebruiker die het subcontract maakt. De maker van het subcontract kan de waarde echter wijzigen om de persoon aan te geven voor wie hij het subcontract maakt. | Geen |
    | Leveranciersaccountmanager | De naam van de primaire contactpersoon van de leveranciersrekening. De standaardwaarde wordt automatisch ingevoerd vanuit de leveranciersaccountrecord. U kunt een andere contactpersoon selecteren als de leveranciersaccountmanager van het subcontract. | U kunt e-mailwaarschuwingen instellen om de contactpersoon op de hoogte te stellen wanneer er wijzigingen worden aangebracht in het subcontract als gevolg van prijsonderhandelingen. |

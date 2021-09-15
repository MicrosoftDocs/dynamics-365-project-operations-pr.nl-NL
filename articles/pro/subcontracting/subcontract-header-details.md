---
title: Koptekstdetails voor subcontracten
description: In dit wordt de functionaliteit uitgelegd die wordt geboden in de koptekst voor subcontracten in Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323635"
---
# <a name="header-details-for-subcontracts"></a>Koptekstdetails voor subcontracten

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In dit wordt de functionaliteit uitgelegd die wordt geboden in de koptekst voor subcontracten in Dynamics 365 Project Operations.

Omdat een projectmanager projecten plant en uitvoert, kunnen ze onderaannemers in dienst hebben en producten en diensten van leveranciers kopen. Wanneer een projectmanager producten of diensten moet kopen, kunnen ze een subcontract maken in Project Operations.

Voer de volgende stappen uit om een subcontract te maken.

1. Selecteer in het navigatievenster de optie **Subcontracten** en selecteer op de pagina **Subcontract** de optie **Nieuw**.
2. Geef de vereiste informatie op en selecteer vervolgens **Opslaan**.

    De volgende tabel bevat informatie over de velden op de koptekstpagina Subcontract.

    | **Veld** | **Beschrijving** |
    | --- | --- | 
    | Meetcriterium | De naam van het subcontract. |
    | Beschrijving | Een korte beschrijving van services en producten die worden gekocht in het subcontract. |
    | Verkoper | De naam van het bedrijf waarvan de producten en diensten worden gekocht. Deze accountrecord heeft het relatietype **Verkoper** of **Leverancier**. |
    | Datum subcontract | De datum waarop het subcontract is gemaakt. |
    | Reden van status  | De status van het subcontract. |
    | Valuta | De valuta waarin producten en diensten worden gekocht. De waarde in dit veld is standaard afkomstig van de leveranciersrekening, maar kan worden gewijzigd. Projectprijslijsten die worden gebruikt voor de prijsstelling van producten en diensten in het subcontract moeten in deze valuta zijn. Prijslijsten in een andere valuta kunnen niet aan het subcontract worden gekoppeld. De kosten van producten en diensten die in dit subcontract zijn gemaakt, worden in deze valuta voor het project geboekt. |
    | Contracterende eenheid | De afdeling van het bedrijf die een koop- of een subcontractovereenkomst aangaat met de leverancier. |
    | Betalingsvoorwaarden | De betalingsvoorwaarden op de leveranciersfacturen die zijn uitgegeven voor dit subcontract. De waarde in dit veld is standaard afkomstig van de leveranciersrekeningrecord. |
    | Betalingsadres | Het adres waarnaar de betaling op leveranciersfacturen naartoe wordt gestuurd. De waarde in dit veld is standaard afkomstig van de leveranciersrekeningrecord. |
    | Naam voor factuur | De naam van de persoon of afdeling in het bedrijf van de leverancier die de factuur verzendt. De waarde in dit veld komt standaard uit de leveranciersaccountrecord en wordt gebruikt als de naam van de primaire contactpersoon op leveranciersfacturen die voor dit subcontract zijn gemaakt. |
    | Factuuradres | Het adres dat wordt gebruikt op facturen van deze leverancier. De waarde in dit veld is standaard afkomstig van de leveranciersrekeningrecord. Dit adres wordt ook gebruikt als het factuurafzenderadres op leveranciersfacturen die voor dit subcontract zijn gemaakt. |
    | Subtotaal | Als een subcontract geen regels bevat, voert u in dit veld een waarde in die het ordersubtotaal vóór belastingen aangeeft. Als het subcontract regels heeft, is dit veld alleen-lezen. Het weergegeven bedrag is het subtotaalbedrag van alle regels in het subcontract. |
    | Totale belasting | Als een subcontract geen regels bevat, voert u in dit veld een waarde in voor de belastingen in dit subcontract. Als het subcontract regels heeft, is dit veld alleen-lezen. Het weergegeven bedrag is het totaal van het belastingbedrag van alle regels in het subcontract. |
    | Totale bedrag |  Dit berekende veld toont het totale bedrag van de subcontract, inclusief belastingen.  |
    | Bevestigde datum | De datum waarop het subcontract is bevestigd.  |
    | Aangevraagd door | De waarde in dit veld is standaard de naam van de gebruiker die het subcontract maakt. Deze waarde kan worden gewijzigd door de maker van het subcontract om de persoon aan te duiden namens wie het subcontract wordt gemaakt.  |
    | Leveranciersaccountmanager | De naam van de primaire contactpersoon van de leveranciersrekening. De waarde in dit veld is standaard afkomstig van de leveranciersrekeningrecord. Deze veldwaarde kan door de gebruiker worden gewijzigd om een andere contactpersoon te selecteren als de accountmanager van de leverancier van het subcontract. E-mailwaarschuwingen en prijsonderhandelingen kunnen door deze contactpersoon worden geconfigureerd en verzonden. |



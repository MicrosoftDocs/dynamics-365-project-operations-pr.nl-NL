---
title: Opnieuw ontworpen onkostendeclaraties
description: Dit onderwerp bevat informatie over de opnieuw ontworpen ervaring voor het invoeren van onkostendeclaraties in Microsoft Dynamics 365 Finance. De nieuwe ervaring vereenvoudigt het proces van het invullen van onkostendeclaraties en verkort de tijd die nodig is.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: d076c0a596940cb08433f7ee57dea54903f6078f
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960241"
---
# <a name="redesigned-expense-reports"></a>Opnieuw ontworpen onkostendeclaraties

De invoer voor onkostendeclaraties is opnieuw ontworpen om het proces voor het invullen van de onkostendeclaraties te vereenvoudigen en de tijd te verkorten die ervoor nodig is. Dit zijn de belangrijkste componenten van de nieuwe onkostenfunctie:

- Een nieuwe werkruimte voor onkostenbeheer waarmee u toegang hebt tot de onkosten van uw gemachtigde.
- Een nieuwe functie voor het afstemmen van betalingsbewijzen om betalingsbewijzen beter weer te geven op koptekstniveau en het proces voor het koppelen van betalingsbewijzen aan onkostenregels te vereenvoudigen.
- Een nieuw alleen-lezen raster waarmee u veel meer onkostenregels en extra kolommen met gegevens kunt bekijken. U kunt nu alle gespecificeerde en gesplitste regels zien, samen met hun bovenliggende onkosten.
- Een vereenvoudigd deelvenster voor het bewerken van onkosten.
- Vernieuwde fout-, waarschuwings- en beleidsberichten om ervoor te zorgen dat u de juiste context hebt om te begrijpen wat het probleem is en hoe het probleem kan worden opgelost. Microsoft heeft veel berichten verwijderd die verschenen voordat gebruikers de gelegenheid hadden om hun taken uit te voeren en de problemen op te lossen, zoals het onvolledige specificatiebericht.
- Een nieuwe pagina om op te geven welke velden vereist zijn door uw organisatie, welke velden optioneel zijn en welke velden niet moeten worden vastgelegd. Met deze pagina kan het aantal velden worden beperkt dat gebruikers moeten instellen.
- Een nieuwe vormgeving voor onkostennota's, zodat deze er niet langer uitzien alsof ze zijn ontworpen voor boekhoudkundige persona's.

Om de nieuwe ervaring in te schakelen, gebruikt u de werkruimte **Functiebeheer** om de functie **Opnieuw ontworpen onkostendeclaraties** in te schakelen. Wanneer u deze functie inschakelt, vinden de volgende acties plaats:

- De bestaande werkruimte voor onkosten wordt vervangen door de nieuwe werkruimte.
- Er wordt een nieuw menu-item voor de zichtbaarheid van onkostenvelden toegevoegd.
- Er worden geen bestaande menu-items voor onkostennota's (de bestaande pagina) of onkostennotavelden verwijderd.
- Via werkstromen en goedkeuringen komt u nog steeds uit bij de bestaande pagina met onkostennota's.

## <a name="getting-started-video-for-new-users"></a>Aan de slag-video's voor nieuwe gebruikers

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

De video [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (hierboven weergegeven) is opgenomen in de [Finance and Operations-afspeellijst](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) op YouTube.

## <a name="new-features"></a>Nieuwe functies

| Nieuwe functie | Beschrijving |
|---|----|
| Zichtbaarheid van onkostenveld | Op een nieuwe instellingenpagina kunt u aangeven welke velden moeten worden uitgeschakeld voor een organisatie, welke velden verplicht moeten zijn en welke velden worden aanbevolen. |
| Vereiste velden | Dankzij de nieuwe eenvoudige configuratie kunt u enkele velden verplicht maken zonder het beleidsframework te hoeven gebruiken. |
| Optionele velden | Er is een tweede pagina voor optionele velden toegevoegd. Op deze manier hebben medewerkers niet het gevoel dat ze de velden moeten instellen, maar zijn de velden nog steeds goed toegankelijk. |
| Niet-bijgevoegde betalingsbewijzen toevoegen | De mogelijkheid om niet-bijgevoegde betalingsbewijzen toe te voegen aan de onkostennota is beter zichtbaar vanuit de werkruimte en in de onkostennota. |
| Verbeterde berichten | De zichtbaarheid van onkostenregels met waarschuwingen of fouten is verbeterd. |
| Minder berichten in de berichtbalk| Het aantal Infolog-berichten is verminderd en er is geprobeerd om in veel gevallen te voorkomen dat dubbele berichten verschijnen. |
| Gemeenschappelijke acties zijn gegroepeerd | De interface is opgeruimd door de toevoeging van een nieuwe actieknop voor de meeste gangbare acties op regelniveau en de toevoeging van een knop met beletselteken (...) voor koptekst- en andere minder gebruikte acties. |
| Nieuwe werkruimte om de zichtbaarheid te vergroten | Een nieuwe werkruimte met functies en koppelingen waarmee gebruikers naar verschillende gebieden kunnen gaan. |
| Bestaande onkosten en betalingsbewijzen toevoegen tijdens het maken van onkosten | Wanneer u onkostennota's maakt, kunt u alle of geselecteerde onkosten en betalingsbewijzen toevoegen. |
| Wisselkoerscalculator | Er is een wisselkoerscalculator toegevoegd waarmee u de wisselkoers kunt berekenen voor contante transacties in meerdere valuta's. |
| Onkostenregels opslaan en toevoegen | De knoppen **Opslaan** en **Nieuw** zijn beschikbaar wanneer er nieuwe onkosten worden ingevoerd, zodat u snel onkostenregels kunt invoeren. |
| Beter inzicht in opgesplitste en gespecificeerde regels | Gespecificeerde en gesplitste regels worden rechtstreeks aan de lijst met onkosten toegevoegd om de zichtbaarheid te vergroten en u te helpen gemakkelijk te bepalen of er beleidsfouten of andere fouten zijn. |
| Betalingsbewijzen weergeven tijdens specificatie | Betalingsbewijzen kunnen worden weergeven tijdens specificatie. |

De eerste release is gericht op scenario's voor het invoeren van onkosten. Elk beoordelings- of goedkeuringsscenario voor onkostennota's blijft de bestaande pagina voor de invoer van onkostennota's gebruiken.

De volgende functies zijn aanwezig op de bestaande pagina, maar nog niet op de nieuwe pagina. Deze functies worden in de volgende releases opnieuw geïntroduceerd:

- Goedkeuringen
- Goedkeuringen van leveranciers en de mogelijkheid om de boekhouding te bewerken
- Meerdere toegangspunten
- Integratie van reiskosten
- Gegevensentiteit voor zichtbaarheid van onkostenveld
- Invoer voor dagonkosten
- Werkstroom op regelniveau
- Ondersteuning voor tijdelijke fiatteur
- Geavanceerde specificatie

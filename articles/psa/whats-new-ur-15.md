---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 15, v3
description: Dit onderwerp bevat informatie over wat er nieuw en gewijzigd is in Project Service Automation updaterelease 15, v3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6112e4874025e528a2bb583cf215fd9eff681534
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074521"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, updaterelease 15, v3

Met genoegen kondigen we de nieuwste update voor de toepassing Dynamics 365 Project Service Automation (PSA) aan. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365. Hierin gaat u naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor PSA v3, updaterelease 15. Deze versie heeft het buildnummer V3.10.5.28 en is algemeen beschikbaar via een zelf-update vanaf januari 2020.

## <a name="update-release-15"></a>Updaterelease 15 

### <a name="enhancements"></a>Verbeteringen

- Projectbeheer

### <a name="bug-fixes"></a>Bugfixes

- Tijd en onkosten

  - Opgelost: foutafhandeling tijdens laden toegevoegd in de afstemmingsweergave.
  - Opgelost: Hub voor Projectresources: **Aantal** heeft een andere naam gekregen om dubbelzinnigheid te verminderen.
  - Opgelost: de weergave **Kolommen met tijdsvermelding kopiëren** aangepast, bevat nu ook het type.
  - Opgelost: het bewerken van de tijdsinvoerduur in de rasterweergave met behulp van decimale getallen resulteert in een onbekende fout voor sommige getallen.

- Projectbeheer

  - Opgelost: het vervolgkeuzemenu voor **Gebruiken in traceringsweergave** wordt nu groter, afhankelijk van de breedte van de opties.
  - Opgelost: bij het beheren van projecten in de tijdzone +13 kunnen taakberekeningen onnauwkeurige resultaten weergeven.
  - Opgelost: **Eindtijd teamlid** is gecorrigeerd bij gebruik van een 24-uurs agenda.
  - Opgelost: de **BPF** in hoofdformulier **msdyn_project** is opnieuw geactiveerd.
  - Opgelost: de toewijzingsberekening negeert niet langer één dag.
  - Opgelost: er is een nieuwe meldingbanner toegevoegd aan het projectformulier, wanneer gebruiker en project in verschillende tijdzones zitten.

- Sales

  - Opgelost: opzoekveld van categorieën voor onkostenschattingen kan worden gebruikt om duplicaten te filteren.
  - Opgelost: code in **PluginDomain.ExecuteInTryCatchBlock (..)** verbergt niet langer de oorsprong van de uitzondering.
  - Opgelost: geen foutmelding meer in **opzoekweergave van projecten** in het formulier **Prijsopgaveregel** wanneer er meer dan 1000 projecten zijn.
  - Opgelost: het raster **Schattingen** voor schattingen voor arbeid en onkosten geeft nu het juiste valutasymbool weer.
  - Opgelost: nadat een organisatie PSA heeft bijgewerkt van updaterelease 14 naar updaterelease 15, wordt het tabblad **Planning** niet langer leeg weergegeven op het formulier **Project**.
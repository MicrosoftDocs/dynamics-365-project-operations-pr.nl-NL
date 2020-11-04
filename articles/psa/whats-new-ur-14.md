---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 14, v3
description: Dit onderwerp bevat informatie over wat er nieuw en gewijzigd is in Project Service Automation updaterelease 14, v3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074522"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, updaterelease 14, v3
Met genoegen kondigen we de nieuwste update voor de toepassing Dynamics 365 Project Service Automation (PSA) aan. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365. Hierin gaat u naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor PSA v3, updaterelease 14. Deze versie heeft het buildnummer V3.10.4.21 en komt beschikbaar volgens de volgende planning:

- **Algemene beschikbaarheid (zelf-update):** januari 2020
- **Automatische update:** februari 2020

## <a name="update-release-14"></a>Updaterelease 14

### <a name="enhancements"></a>Verbeteringen

- Sales

     - Aangepaste veldwaarden van **Details van prijsopgaveregel** worden gekopieerd naar **Details van projectcontractregels** wanneer een prijsopgave wordt bijgewerkt naar **Afsluiten als binnengehaald**.
     - Bevestigde projecten kunnen worden **afgesloten als gemist**.

- Resourcebeheer

     - Bij het uitbreiden van boekingen wordt gebruikers met een bevestigingsdialoogvenster gevraagd om boekingsresultaten samen te vatten en een link naar Boekingen bijhouden op te geven.


### <a name="bug-fixes"></a>Bugfixes

- Tijd en onkosten

     - Opgelost: verbeterde gebruikerservaring wanneer de gebruiker geen items heeft geselecteerd om te corrigeren.

- Resourcebeheer

     - Opgelost: als een resource meerdere keren wordt geboekt, treedt een overflow van de naam van de te boeken resource op.

- Sales

     - Opgelost: de totale verkoopprijs wordt niet berekend totdat de gebruiker ook een kostprijs invoert voor geschatte onkosten voor een project.
     - Opgelost: een offerte afsluiten als **binnengehaald** mislukt als het bijbehorende projectcontract niet de status **Concept** heeft.

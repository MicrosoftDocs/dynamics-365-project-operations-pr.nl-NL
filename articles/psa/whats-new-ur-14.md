---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 14, v3
description: Dit artikel bevat informatie over nieuwe functies in Project Service Automation-updateversie 14 V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e8e5132f970e3ec5742842175c118faf98a7b079
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926540"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, updateversie 14, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update voor de toepassing Dynamics 365 Project Service Automation (PSA) aan. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365. Hierin gaat u naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor PSA V3, updateversie 14. Deze versie heeft het buildnummer V3.10.4.21 en komt beschikbaar volgens de volgende planning:

- **Algemene beschikbaarheid (zelf-update):** januari 2020
- **Automatische update:** februari 2020

## <a name="update-release-14"></a>Updateversie 14

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]

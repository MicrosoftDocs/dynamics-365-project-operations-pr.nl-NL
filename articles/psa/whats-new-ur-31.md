---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 31, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 31, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945529"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 31, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 31. Deze versie heeft een buildnummer van V3.10.52.77 en is algemeen beschikbaar via een zelfupdate in mei 2021.

## <a name="update-release-31"></a>Updaterelease 31

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost:

- De opdrachtknoppen voor tijdinvoer op de pagina **Boekbare resource** waren verwarrend.
- Er werd een null-referentie-uitzondering gegenereerd in **Project.SetTrackingFields** bij het goedkeuren van een tijdinvoer.

**Resourcebeheer**

De volgende problemen zijn opgelost:

- **Teamlid maken** geeft de metadata-instelling van de boekingsinstellingen niet correct weer voor **Standaardstatus van vastgelegde boeking**.
- Bij het upgraden van PSA 1.X naar 3.X mislukt het upgradeproces bij **UpgradeResourceRequirements**.


**Verkoop**

De volgende problemen zijn opgelost:

- Werkelijke opbrengst converteert de bedragen naar de projectvaluta in het traceringsraster.
- De standaardvaluta is onduidelijk bij het maken van dagboekregels, prijsopgaveregels en contractregels in scenario's waarin de basisvaluta van een organisatie verschilt van de projectvaluta.
- De query **In afwachting van correctiejournaalvalidatie** filtert niet op project.
- De resterende omzet wordt onjuist berekend voor een project.
- Prijsopgaven op basis van een contactpersoon mislukken als ze worden gemaakt zonder prijslijst.
- Er wordt geen verwerkingsdraaischijf weergegeven wanneer u **Factuur bevestigen** selecteert.
- Er wordt geen verwerkingsdraaischijf weergegeven wanneer u **Factuur maken** selecteert.
- Als u een prijsopgave sluit als verloren, worden de boekingen niet geannuleerd.








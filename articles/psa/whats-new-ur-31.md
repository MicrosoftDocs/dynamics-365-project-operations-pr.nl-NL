---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 31, v3
description: In dit artikel worden de functies en oplossingen vermeld die beschikbaar zijn in Project Service Automation-updateversie 31, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d62b12a5363637e46b29c2e9edf4e1f17da729f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925022"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 31, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 31, V3. Deze versie heeft een buildnummer van V3.10.52.77 en is algemeen beschikbaar via een zelfupdate in mei 2021.

## <a name="update-release-31"></a>Updateversie 31

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








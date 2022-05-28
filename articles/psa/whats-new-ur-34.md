---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 34, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 34, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588684"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 34, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 34. Deze versie heeft een buildnummer van V3.10.55.38 en is algemeen beschikbaar via een zelfupdate in juli 2021.

## <a name="update-release-34"></a>Updaterelease 34

### <a name="bug-fixes"></a>Opgeloste fouten
De volgende problemen zijn opgelost.

**Algemeen**

- Door uitgevers aangestuurde updates activeren de nieuwe, moderne goedkeuringswerkstroom niet.
- De kenmerken **Doelstatus** en **Actietype** ontbreken op de hoofdpagina van **Goedkeuringsset**.

**Tijd en onkosten**

- Een intrekkingsaanvraag kan niet worden goedgekeurd via de moderne goedkeuringswerkstroom.
- Het kopiëren van een week met tijdsvermeldingen werkt niet bij het kopiëren van vermeldingen die niet zijn gerelateerd aan de aangemelde gebruiker.

**Projectplanning**

- De contouren van resourcetoewijzingen zijn beschadigd bij het importeren vanuit de Microsoft Project-bureaubladinvoegtoepassing.

**Resourcebeheer**

- Wanneer u een project publiceert vanuit de Microsoft Project-bureaubladclient-invoegtoepassing, wordt de einddatum van bestaande vereisten gewijzigd.
- De decimale precisie overschrijdt twee decimalen in het bevestigingsvenster voor het verlengen van boekingen.

**Verkoop**

- Wanneer u een productgebaseerde lijn met een bestaand product toevoegt aan een projectcontract, wordt een uitzondering **Sleutel niet gevonden in woordenboek** weergegeven.
- Leads kunnen niet worden gekwalificeerd wanneer een ordertype is toegewezen van een lead aan een verkoopkans.

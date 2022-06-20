---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 40, v3
description: Dit artikel biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Microsoft Dynamics 365 Project Service Automation-updateversie 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912786"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 40, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 40, V3. Deze versie heeft buildnummer V3.10.61.61 en is algemeen beschikbaar via een zelfupdate in februari 2022.

## <a name="update-release-40"></a>Updateversie 40

### <a name="features"></a>Functies
Fase 1 van de upgrade van Project Service Automation naar Project Operations - Lite wordt in februari 2022 vrijgegeven voor alle klanten. Zie [Upgrade van Project Service Automation naar Project Operations](upgrade-project-operations-non-stocked.md) om te controleren of u in aanmerking komt. Als de toepassing niet in uw exemplaar verschijnt in het Power Platform-beheercentrum, neemt u contact op met de ondersteuning en vraagt u om inschakeling van de flight voor uw omgevingen. Uw aanvraag moet een lijst met omgevings-id's bevatten waar de flight moet worden ingeschakeld.

### <a name="bug-fixes"></a>Opgeloste fouten

De volgende problemen zijn opgelost.

**Tijd en onkosten**
- Een notitievermelding ontbreekt wanneer een tijdsvermelding wordt afgewezen of geannuleerd. 

**Verkoop**

- Wanneer u kosten- of verkoopramingen bijwerkt met kant-en-klare invoegtoepassingen, mag u ten onrechte JSON-payloads verzenden die niet geldig zijn buiten de gebruikersinterface.
- Wanneer u offerteregels bijwerkt met behulp van de snelle weergave, kunt u offertes activeren.

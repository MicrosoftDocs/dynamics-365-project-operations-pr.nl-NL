---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 45, v3
description: Dit artikel biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Microsoft Dynamics 365 Project Service Automation-updateversie 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169152"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 45, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 45, V3. Deze versie heeft een buildnummer van V3.10.76.168 en is algemeen beschikbaar via een zelfupdate in juli 2022.

## <a name="update-release-45"></a>Updateversie 45

### <a name="bug-fixes"></a>Opgeloste fouten

De volgende problemen zijn opgelost.

**Verkoop**

- Gebruikers kunnen geen facturen maken nadat ze hebben geprobeerd een factuur te maken zonder niet-gefactureerde verkopen, als ze ook hetzelfde exemplaar van de pagina bekijken en deze niet vernieuwen.

**Tijd en onkosten**

- Wanneer Moderne goedkeuringen is ingeschakeld en een ingetrokken projectgoedkeuring is goedgekeurd, wordt de recordfase op onjuiste wijze bijgewerkt naar **De intrekkingsaanvraag is goedgekeurd**.
- Wanneer Moderne goedkeuringen is ingeschakeld en Cloudstromen inactief is, mislukt het goedkeuringsproces en worden de indienende of goedkeurende gebruikers niet op de hoogte gesteld.

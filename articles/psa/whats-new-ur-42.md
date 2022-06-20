---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 42, v3
description: Dit artikel biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Microsoft Dynamics 365 Project Service Automation-updateversie 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912709"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 42, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 42, V3. Deze versie heeft een buildnummer van V3.10.73.61 en is algemeen beschikbaar via een zelfupdate in april 2022.

## <a name="update-release-42"></a>Updateversie 42

### <a name="bug-fixes"></a>Opgeloste fouten

De volgende problemen zijn opgelost.

**Tijd en onkosten**

- Wanneer een urenstaat wordt afgewezen, wordt de gebruiker die deze heeft afgewezen ten onrechte geïdentificeerd als **Systeem**.
- Wanneer tijdsvermeldingen worden geïmporteerd, ontbreekt de waarde voor **Resourcecategorie**.
- Projectfiatteurs kunnen ingediende projecten goedkeuren wanneer hun machtigingen niet specifiek zijn ingesteld op **Kan goedkeuren**.

**Verkoop**

- Wanneer werkelijke waarden worden vastgelegd voor taken die zich niet op het hoofdniveau bevonden, worden de werkelijke kosten onjuist geaggregeerd.

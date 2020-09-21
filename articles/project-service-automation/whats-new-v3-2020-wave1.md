---
title: Wat is er nieuw of gewijzigd in Project Service Automation versie 3.x, wave 1 van 2020
description: In dit onderwerp vindt u informatie over wat er nieuw en gewijzigd is in Project Service Automation versie 3, wave 1 van 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750750"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Wat is er nieuw of gewijzigd in Project Service Automation versie 3, wave 1 van 2020
In dit onderwerp worden belangrijke overwegingen belicht voor upgraden, wanneer u wilt overstappen naar de nieuwste release van Project Service Automation (PSA) versie 3.x, wave 1 van 2020.

## <a name="time-entry"></a>Tijdsvermelding
De tijdinvoerervaring is uitgebreid en biedt nu mogelijkheden voor het uitbreiden van tijdinvoer naar meer klantenscenario's. Dit omvat de mogelijkheid om invoertypen toe te voegen, die nu specifiek gedrag aansturen op basis van de veldschemanaam **Instellingen voor tijdinvoer**, weergegeven als **Tijdsbron**.

### <a name="upgrade-consideration"></a>Overwegingen voor het upgraden
Ter ondersteuning van deze functionaliteit zijn de rollen in PSA bijgewerkt met nieuwe rechten. Deze rechten verlenen leestoegang tot de nieuwe entiteit **Instellingen voor tijdinvoer**.

Gebruikers die tijd moeten kunnen invoeren, moeten de gebruikersrol **Tijdinvoergebruiker** hebben naast bestaande rollen. Deze rol omvat de nieuwe functionaliteit en zorgt ervoor dat tijdinvoer blijft werken.

### <a name="currently-extended-time-entry-changes"></a>Momenteel uitgebreide wijzigingen in tijdinvoer
Om de impact voor huidige gebruikers van tijdinvoer zo klein mogelijk te houden, is deze rolverandering de enige kernvereiste die nodig is om tijdinvoer te blijven gebruiken. Als u aangepaste weergaven of afzonderlijke tijdinvoerervaringen hebt gemaakt, moet u de velden **Instellingen voor tijdinvoer** instellen op de juiste PSA-waarde.

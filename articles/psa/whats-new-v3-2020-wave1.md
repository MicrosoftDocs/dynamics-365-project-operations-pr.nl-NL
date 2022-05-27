---
title: Wat is er nieuw of gewijzigd in Project Service Automation versie 3.x, wave 1 van 2020
description: In dit onderwerp vindt u informatie over wat er nieuw en gewijzigd is in Project Service Automation versie 3, wave 1 van 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
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
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577874"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Wat is er nieuw of gewijzigd in Project Service Automation versie 3, wave 1 van 2020

[!include [banner](../includes/psa-now-project-operations.md)]

In dit onderwerp worden belangrijke overwegingen belicht voor upgraden, wanneer u wilt overstappen naar de nieuwste release van Project Service Automation (PSA) versie 3.x, wave 1 van 2020.

## <a name="time-entry"></a>Tijdsvermelding
De tijdinvoerervaring is uitgebreid en biedt nu mogelijkheden voor het uitbreiden van tijdinvoer naar meer klantenscenario's. Dit omvat de mogelijkheid om invoertypen toe te voegen, die nu specifiek gedrag aansturen op basis van de veldschemanaam **Instellingen voor tijdinvoer**, weergegeven als **Tijdsbron**. De nieuwe oplossing TESA (Time, Expense, Statusing and Approvals) is toegevoegd om deze functionaliteit te ondersteunen.

### <a name="upgrade-consideration"></a>Overwegingen voor het upgraden
Ter ondersteuning van deze functionaliteit zijn de rollen in PSA bijgewerkt met nieuwe rechten. Deze rechten verlenen leestoegang tot de nieuwe entiteit **Instellingen voor tijdinvoer**.

Gebruikers die tijd moeten kunnen invoeren, moeten de gebruikersrol **Tijdinvoergebruiker** hebben naast bestaande rollen. Deze rol omvat de nieuwe functionaliteit en zorgt ervoor dat tijdinvoer blijft werken.

Als u bovendien aangepaste app-modules hebt die alle formulieren voor de entiteit tijdsvermeldingen bevatten, moet u het **Formulier voor snelle invoer van TESA-tijdsvermeldingen** uit de module verwijderen.

### <a name="currently-extended-time-entry-changes"></a>Momenteel uitgebreide wijzigingen in tijdinvoer
Om de impact voor huidige gebruikers van tijdinvoer zo klein mogelijk te houden, is deze rolverandering de enige kernvereiste die nodig is om tijdinvoer te blijven gebruiken. Als u aangepaste weergaven of afzonderlijke tijdinvoerervaringen hebt gemaakt, moet u de velden **Instellingen voor tijdinvoer** instellen op de juiste PSA-waarde.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

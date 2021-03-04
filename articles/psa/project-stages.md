---
title: Typen projectfasen
description: In dit onderwerp krijgt u informatie over projectfasen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148097"
---
# <a name="project-stage-types"></a>Typen projectfasen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projectfasen zijn ontworpen om tijdens de voortgang van het project de status aan te geven. Aanpassingen kunnen worden gebruikt om de fasen automatisch bij te werken met bedrijfsprocesstromen, Power Automate, of plug-in extensies.

De volgende fasen worden gedefinieerd in de standaardbedrijfsprocesstroom:

- Nieuw:
- Prijsopgave
- Plannen
- Leveren
- Voltooid
- Sluiten 

## <a name="new"></a>Nieuw

Wanneer u een project maakt, wordt de projectfase ingesteld op **Nieuw**. Als het project is gemaakt op basis van een sjabloon, kan het project plannings-, schattings- en teamgegevens bevatten. Als dit niet het geval is, is het slechts een schets van het project en moeten de resterende onderdelen worden ingevoerd.

## <a name="quote"></a>Prijsopgave

Wanneer u een project aan een prijsopgave koppelt of wanneer u een project maakt op basis van een prijsopgave, wordt de projectfase ingesteld op **Prijsopgave** en worden de geschatte begin- en einddatum bijgewerkt. Als het project zich in de fase **Prijsopgave** bevindt, worden op het tabblad **Verkoop** van de pagina **Projectentiteit** details van de prijsopgave weergegeven.

## <a name="plan"></a>Plannen

Wanneer u een order binnenhaalt op basis van een prijsopgave die aan een project is gekoppeld en het project overgaat naar de fase **Contract**, wordt de projectfase bijgewerkt naar **Plannen**. Als het project zich in de fase **Plannen** bevindt, worden op de pagina **Projectentiteit** de details van het contract weergegeven.

## <a name="deliver"></a>Leveren

Wanneer het projectplan is voltooid en u aan het project kunt beginnen, moet de projectmanager de projectfase bijwerken naar **Leveren** om aan te geven dat het project is gestart.

## <a name="complete"></a>Voltooid 

Wanneer het werk voor het project is voltooid, kan de projectmanager de fase bijwerken naar **Voltooid**. Als u de projectfase bijwerkt naar **Voltooid**, geeft de projectmanager aan dat het werk voor 100 procent is voltooid, maar dat het project nog open wordt gehouden om eventuele openstaande tijdsvermeldingen of onkostenposten te kunnen vastleggen.

## <a name="close"></a>Sluiten

Wanneer alle transacties voor het project zijn vastgelegd, kan de projectmanager de fase bijwerken naar **Sluiten**. Op dat moment kunnen er geen transacties meer worden vastgelegd en wordt het project ingesteld op alleen-lezen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
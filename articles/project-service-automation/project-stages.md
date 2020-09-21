---
title: Projectfasen
description: In dit onderwerp krijgt u informatie over projectfasen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750729"
---
# <a name="project-stages"></a>Projectfasen 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projectfasen worden bijgewerkt om tijdens de voortgang van het project de status aan te geven. Met de standaardbedrijfsprocesstroom worden bepaalde fasen van het project automatisch bijgewerkt, terwijl andere fasen handmatig door de projectmanager worden bijgewerkt. 

De volgende fasen worden gedefinieerd in de standaardbedrijfsprocesstroom:

- Nieuw
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

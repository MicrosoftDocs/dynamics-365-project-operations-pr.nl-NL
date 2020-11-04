---
title: Projectfasen
description: Dit onderwerp bevat informatie over de projectfasen die beschikbaar zijn in Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 554ad63bc44cbe5a1fe91eb47fedbb74bbedd4b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074691"
---
# <a name="project-stages"></a>Projectfasen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Projectfasen zijn ontworpen om tijdens de voortgang van het project de status aan te geven. Aanpassingen kunnen worden gebruikt om de fasen automatisch bij te werken met bedrijfsprocesstromen, Power Automate, of plug-in extensies.

De volgende fasen worden gedefinieerd in de standaardbedrijfsprocesstroom:

- Nieuw:
- Prijsopgave
- Plan
- Bezorgen
- Voltooien
- Afsluiten 

## <a name="new"></a>Nieuw:

Wanneer u een project maakt, wordt de projectfase ingesteld op **Nieuw**. Als het project is gemaakt op basis van een sjabloon, kan het project plannings-, schattings- en teamgegevens bevatten. Als dit niet het geval is, is het een schets van het project en moeten de resterende onderdelen worden ingevoerd.

## <a name="quote"></a>Prijsopgave

Wanneer u een project aan een prijsopgave koppelt of wanneer u een project maakt op basis van een prijsopgave, wordt de projectfase ingesteld op **Prijsopgave** en worden de geschatte begin- en einddatum bijgewerkt. Als het project zich in de fase **Prijsopgave** bevindt, worden op het tabblad **Verkoop** van de pagina **Projectentiteit** details van de prijsopgave weergegeven.

## <a name="plan"></a>Plannen

Wanneer u een order binnenhaalt op basis van een prijsopgave die aan een project is gekoppeld en het project overgaat naar de fase **Contract** , wordt de projectfase bijgewerkt naar **Plannen**. Als het project zich in de fase **Plannen** bevindt, worden op de pagina **Projectentiteit** de details van het contract weergegeven.

## <a name="deliver"></a>Leveren

Wanneer het projectplan is voltooid en u aan het project kunt beginnen, moet de projectmanager de projectfase bijwerken naar **Leveren** om aan te geven dat het project is gestart.

## <a name="complete"></a>Voltooid 

Wanneer het werk voor het project is voltooid, kan de projectmanager de fase bijwerken naar **Voltooid**. Als u de projectfase bijwerkt naar **Voltooid** , geeft de projectmanager aan dat het werk voor 100 procent is voltooid, maar dat het project nog open wordt gehouden om eventuele openstaande tijdsvermeldingen of onkostenposten te kunnen vastleggen.

## <a name="close"></a>Sluiten

Wanneer alle transacties voor het project zijn vastgelegd, kan de projectmanager de fase bijwerken naar **Sluiten**. Op dat moment kunnen er geen transacties meer worden vastgelegd en wordt het project ingesteld op alleen-lezen.


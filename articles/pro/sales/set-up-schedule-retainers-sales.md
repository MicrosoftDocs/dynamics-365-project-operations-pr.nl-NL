---
title: Een voorschotschema instellen
description: Dit onderwerp bevat informatie over hoe u een voorschotschema in Project Operations instelt.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596366"
---
# <a name="set-up-a-retainer-schedule"></a>Een voorschotschema instellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Voorschotschema's worden opgesteld op de pagina **Projectcontract** in Dynamics 365 Project Operations.

1. Selecteer op de pagina **Projectcontract** op het tabblad **Vooruitbetalingen en voorschotten** de optie **Een voorschotschema instellen**.
2. Op de dialoogpagina die wordt geopend, worden de velden in de volgende tabel weergegeven. De tabel geeft een idee van hoe de ingevoerde waarden van invloed zijn op het voorschotschema dat wordt gemaakt.

| Veld | Beschrijving | Downstreamimpact |
| --- | --- | --- |
| Projectcontractklant | De klant op het contract aan wie dit voorschot of de vooruitbetaling in rekening zal worden gebracht. | Als er meerdere klanten in het contract staan en u aan elk van hen een specifiek vooruitbetalings- of voorschotbedrag wilt factureren, maakt u voor elke klant handmatig één factuur. |
| Start voorschotschema | Voer de begindatum van het voorschotschema in. | Deze datum is mogelijk niet de datum waarop de eerste vooruitbetaling of het eerste voorschot is gemaakt. De datum waarop de eerste vooruitbetaling of het eerste voorschot wordt gemaakt, wordt mede beïnvloed door de factuurfrequentie. |
| Einde voorschotschema | Voer de einddatum van het voorschotschema in. | Deze datum is mogelijk niet de datum waarop de laatste vooruitbetaling of het laatste voorschot is gemaakt. De datum waarop de laatste vooruitbetaling of het laatste voorschot wordt gemaakt, wordt mede beïnvloed door de factuurfrequentie. |
| Aantal te maken voorschotten | Wanneer u het aantal aan te maken voorschotten invoert, gebruikt het systeem de begindatum en de frequentie om het aantal in dit veld aan te maken. | Wanneer dit veld handmatig wordt bijgewerkt, negeert het systeem de waarde in het veld **Einde van het voorschotschema** en creëert in plaats daarvan het specifieke aantal vooruitbetalingen of voorschotten. |
| Factuurfrequentie | Hoe vaak de applicatie vooruitbetalingen en voorschotten maakt. | Deze waarde heeft direct invloed op het aantal vooruitbetalingen en voorschotten en de aanmaakdatums. |
| Totaalbedrag | Het totale bedrag is het bedrag dat wordt opgesplitst in de individuele voorschotten of vooruitbetalingen die worden gemaakt. | Er is geen impact op dit veld. |

---
title: Projectverkooporders voor projecten voor tijd en materiaal
description: In dit onderwerp wordt uitgelegd hoe u projectgebaseerde verkooporders kunt maken voor projecten voor tijd en materiaal.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750709"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projectverkooporders voor projecten voor tijd en materiaal

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u een verkooporder voor een project maakt. Verkooporders kunnen alleen worden gemaakt voor projecten van het type **tijd en materiaal**.

Als een project voor tijd en materiaal meerdere financieringsbronnen in het projectcontract heeft, moet u de parameter **Verkooporders toestaan voor projecten met meerdere financieringsbronnen** op de pagina **Parameters voor Projectmanagement en financiële administratie** inschakelen. 

> [!NOTE]
> - Ondersteuning voor verkooporders voor projecten met meerdere financieringsbronnen is beschikbaar vanaf toepassingsversie 10.0.2 en hoger.
> - De parameter om de ondersteuning voor projectverkooporders met meerdere financieringsbronnen in te schakelen, wordt verwijderd in de releasewave van april 2020, waarna de functionaliteit altijd wordt ingeschakeld.

U kunt op twee manieren projectgebaseerde verkooporders maken:

- Ga naar het project zelf. Selecteer in het actievenster **Beheren > Artikeltaken > Verkooporder**. De projectinformatie wordt standaard gebruikt in de verkooporder van het project. Als het projectcontract meer dan één financieringsbron heeft, moet u de financieringsbron selecteren om de klant voor de verkooporder in te stellen. Als er maar één financieringsbron voor het project is, wordt de klant automatisch ingesteld.
- Ga naar de lijstpagina **Alle verkooporders** en maak een nieuwe verkooporder. U moet het project voor de verkooporder selecteren. Nadat het project is geselecteerd, wordt de klant gekozen uit de financieringsbron of moet u de financieringsbron selecteren als het projectcontract meerdere financieringsbronnen heeft.


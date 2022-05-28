---
title: Projectverkooporders voor projecten voor tijd en materiaal
description: In dit onderwerp wordt uitgelegd hoe u projectgebaseerde verkooporders kunt maken voor projecten voor tijd en materiaal.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3e88235b08ca2b8a5ccaab3dfdd7bcff4ab64f5f
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684498"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projectverkooporders voor projecten voor tijd en materiaal

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een verkooporder voor een project maakt. Verkooporders kunnen alleen worden gemaakt voor projecten van het type **tijd en materiaal**.

Als een project voor tijd en materiaal meerdere financieringsbronnen in het projectcontract heeft, moet u de parameter **Verkooporders toestaan voor projecten met meerdere financieringsbronnen** op de pagina **Parameters voor Projectmanagement en financiële administratie** inschakelen. 

> [!NOTE]
> - Ondersteuning voor verkooporders voor projecten met meerdere financieringsbronnen is beschikbaar vanaf toepassingsversie 10.0.2 en hoger.
> - De parameter om de ondersteuning voor projectverkooporders met meerdere financieringsbronnen in te schakelen, wordt verwijderd in de releasewave van april 2020, waarna de functionaliteit altijd wordt ingeschakeld.

U kunt op twee manieren projectgebaseerde verkooporders maken:

- Ga naar het project zelf. Selecteer in het actievenster **Beheren > Artikeltaken > Verkooporder**. De projectinformatie wordt standaard gebruikt in de verkooporder van het project. Als het projectcontract meer dan één financieringsbron heeft, moet u de financieringsbron selecteren om de klant voor de verkooporder in te stellen. Als er maar één financieringsbron voor het project is, wordt de klant automatisch ingesteld.
- Ga naar de lijstpagina **Alle verkooporders** en maak een nieuwe verkooporder. U moet het project voor de verkooporder selecteren. Nadat het project is geselecteerd, wordt de klant gekozen uit de financieringsbron of moet u de financieringsbron selecteren als het projectcontract meerdere financieringsbronnen heeft.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
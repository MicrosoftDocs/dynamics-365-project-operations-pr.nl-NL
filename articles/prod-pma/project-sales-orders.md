---
title: Projectverkooporders voor projecten voor tijd en materiaal
description: In dit artikel wordt uitgelegd hoe u op projecten gebaseerde verkooporders voor tijd- en materiaalprojecten maakt.
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
ms.openlocfilehash: 3a040de6d22b626b9e3d462272f43c5763b5b90f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933808"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projectverkooporders voor projecten voor tijd en materiaal

[!include[banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een verkooporder voor een project maakt. Verkooporders kunnen alleen worden gemaakt voor projecten van het type **tijd en materiaal**.

Als een project voor tijd en materiaal meerdere financieringsbronnen in het projectcontract heeft, moet u de parameter **Verkooporders toestaan voor projecten met meerdere financieringsbronnen** op de pagina **Parameters voor Projectmanagement en financiële administratie** inschakelen. 

> [!NOTE]
> - Ondersteuning voor verkooporders voor projecten met meerdere financieringsbronnen is beschikbaar vanaf toepassingsversie 10.0.2 en hoger.
> - De parameter om de ondersteuning voor projectverkooporders met meerdere financieringsbronnen in te schakelen, wordt verwijderd in de releasewave van april 2020, waarna de functionaliteit altijd wordt ingeschakeld.

U kunt op twee manieren projectgebaseerde verkooporders maken:

- Ga naar het project zelf. Selecteer in het actievenster **Beheren > Artikeltaken > Verkooporder**. De projectinformatie wordt standaard gebruikt in de verkooporder van het project. Als het projectcontract meer dan één financieringsbron heeft, moet u de financieringsbron selecteren om de klant voor de verkooporder in te stellen. Als er maar één financieringsbron voor het project is, wordt de klant automatisch ingesteld.
- Ga naar de lijstpagina **Alle verkooporders** en maak een nieuwe verkooporder. U moet het project voor de verkooporder selecteren. Nadat het project is geselecteerd, wordt de klant gekozen uit de financieringsbron of moet u de financieringsbron selecteren als het projectcontract meerdere financieringsbronnen heeft.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Inkooporders voor een project
description: In dit artikel worden de verschillende methoden beschreven die u kunt gebruiken om inkooporders voor een project te maken. De methode die u gebruikt is afhankelijk van het doel van de inkooporder en wanneer de inkooporder wordt verbruikt en in rekening worden gebracht aan een project.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289183"
---
# <a name="purchase-orders-for-a-project"></a>Inkooporders voor een project

[!include [banner](../includes/banner.md)]

In dit artikel worden de verschillende methoden beschreven die u kunt gebruiken om inkooporders voor een project te maken. De methode die u gebruikt is afhankelijk van het doel van de inkooporder en wanneer de inkooporder wordt verbruikt en in rekening worden gebracht aan een project.

### <a name="methods-for-creating-a-purchase-order"></a>Methoden voor het maken van een inkooporder

U kunt een van de volgende methoden gebruiken om een inkooporder te maken in Projectmanagement en financiële administratie. Het doel van de inkooporder bepaalt wanneer de inkooporder wordt verbruikt en dus wanneer artikelen aan een project in rekening worden gebracht.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Methode</th>
<th>Doel</th>
<th>Verbruik van artikelen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Maak rechtstreeks een inkooporder vanuit een project.</td>
<td>Gebruik deze methode voor het aanschaffen van artikelen bij een externe leverancier voor verbruik in een project. U kunt de inkooporder op twee manieren maken:
<ul>
<li>Vanuit het project zelf. In dit geval is het project al gedefinieerd voor de inkooporder.</li>
<li>Door naar de inkooporder van het project te navigeren. U moet zowel de leverancier als het project selecteren waarvoor u de inkooporder wilt maken.</li>
</ul></td>
<td>Artikelen worden verbruikt wanneer de leveranciersfactuur wordt bijgewerkt.</td>
</tr>
<tr class="even">
<td>Maak een inkooporder vanuit een verkooporder.</td>
<td>Gebruik deze methode om artikelen aan te schaffen wanneer u een verkooporder maakt vanuit een project.</td>
<td>Artikelen worden verbruikt wanneer de verkooporder aan de klant wordt gefactureerd.</td>
</tr>
<tr class="odd">
<td>Maak een inkooporder op basis van een artikelvereiste.</td>
<td>Gebruik deze methode om artikelen aan te schaffen wanneer u een artikelvereiste maakt vanuit een project.</td>
<td>Artikelen worden verbruikt wanneer de artikelvereiste wordt bijgewerkt.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Wanneer u de leveranciersfactuur of pakbon bijwerkt, wordt u gevraagd om de pakbon voor de artikelvereiste bij te werken.

Zie [Artikelen op inkooporder ontvangen vanuit artikelvereiste](tasks/receive-items-purchase-order-item-requirement.md) voor meer informatie.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
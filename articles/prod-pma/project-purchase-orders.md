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
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074552"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="36f38-104">Inkooporders voor een project</span><span class="sxs-lookup"><span data-stu-id="36f38-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36f38-105">In dit artikel worden de verschillende methoden beschreven die u kunt gebruiken om inkooporders voor een project te maken.</span><span class="sxs-lookup"><span data-stu-id="36f38-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="36f38-106">De methode die u gebruikt is afhankelijk van het doel van de inkooporder en wanneer de inkooporder wordt verbruikt en in rekening worden gebracht aan een project.</span><span class="sxs-lookup"><span data-stu-id="36f38-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="36f38-107">Methoden voor het maken van een inkooporder</span><span class="sxs-lookup"><span data-stu-id="36f38-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="36f38-108">U kunt een van de volgende methoden gebruiken om een inkooporder te maken in Projectmanagement en financiële administratie.</span><span class="sxs-lookup"><span data-stu-id="36f38-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="36f38-109">Het doel van de inkooporder bepaalt wanneer de inkooporder wordt verbruikt en dus wanneer artikelen aan een project in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="36f38-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36f38-110">Methode</span><span class="sxs-lookup"><span data-stu-id="36f38-110">Method</span></span></th>
<th><span data-ttu-id="36f38-111">Doel</span><span class="sxs-lookup"><span data-stu-id="36f38-111">Purpose</span></span></th>
<th><span data-ttu-id="36f38-112">Verbruik van artikelen</span><span class="sxs-lookup"><span data-stu-id="36f38-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36f38-113">Maak rechtstreeks een inkooporder vanuit een project.</span><span class="sxs-lookup"><span data-stu-id="36f38-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="36f38-114">Gebruik deze methode voor het aanschaffen van artikelen bij een externe leverancier voor verbruik in een project.</span><span class="sxs-lookup"><span data-stu-id="36f38-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="36f38-115">U kunt de inkooporder op twee manieren maken:</span><span class="sxs-lookup"><span data-stu-id="36f38-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="36f38-116">Vanuit het project zelf.</span><span class="sxs-lookup"><span data-stu-id="36f38-116">From the project itself.</span></span> <span data-ttu-id="36f38-117">In dit geval is het project al gedefinieerd voor de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="36f38-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="36f38-118">Door naar de inkooporder van het project te navigeren.</span><span class="sxs-lookup"><span data-stu-id="36f38-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="36f38-119">U moet zowel de leverancier als het project selecteren waarvoor u de inkooporder wilt maken.</span><span class="sxs-lookup"><span data-stu-id="36f38-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="36f38-120">Artikelen worden verbruikt wanneer de leveranciersfactuur wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="36f38-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36f38-121">Maak een inkooporder vanuit een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="36f38-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="36f38-122">Gebruik deze methode om artikelen aan te schaffen wanneer u een verkooporder maakt vanuit een project.</span><span class="sxs-lookup"><span data-stu-id="36f38-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="36f38-123">Artikelen worden verbruikt wanneer de verkooporder aan de klant wordt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="36f38-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36f38-124">Maak een inkooporder op basis van een artikelvereiste.</span><span class="sxs-lookup"><span data-stu-id="36f38-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="36f38-125">Gebruik deze methode om artikelen aan te schaffen wanneer u een artikelvereiste maakt vanuit een project.</span><span class="sxs-lookup"><span data-stu-id="36f38-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="36f38-126">Artikelen worden verbruikt wanneer de artikelvereiste wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="36f38-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="36f38-127">Wanneer u de leveranciersfactuur of pakbon bijwerkt, wordt u gevraagd om de pakbon voor de artikelvereiste bij te werken.</span><span class="sxs-lookup"><span data-stu-id="36f38-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="36f38-128">Zie [Artikelen op inkooporder ontvangen vanuit artikelvereiste](tasks/receive-items-purchase-order-item-requirement.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="36f38-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


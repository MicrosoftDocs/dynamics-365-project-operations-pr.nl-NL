---
title: Artikelen op inkooporder ontvangen vanuit artikelvereiste
description: In dit onderwerp wordt uitgelegd hoe u artikelen op een inkooporder kunt ontvangen vanuit een artikelvereiste.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011680"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="d737b-103">Artikelen op inkooporder ontvangen vanuit artikelvereiste</span><span class="sxs-lookup"><span data-stu-id="d737b-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d737b-104">In dit onderwerp wordt uitgelegd hoe u artikelen op een inkooporder kunt ontvangen vanuit een artikelvereiste.</span><span class="sxs-lookup"><span data-stu-id="d737b-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="d737b-105">Door een artikelvereiste te gebruiken in plaats van een artikeltransactie, kunt u de levering plannen net voordat het artikel daadwerkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het kader van de handelsovereenkomst en de artikelvereiste opnemen in de productieplanning.</span><span class="sxs-lookup"><span data-stu-id="d737b-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="d737b-106">Deze taak maakt gebruik van de USSI-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="d737b-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d737b-107">Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Projecten > Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="d737b-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="d737b-108">Selecteer in de lijst de koppeling in de gewenste rij.</span><span class="sxs-lookup"><span data-stu-id="d737b-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="d737b-109">Selecteer **Plannen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d737b-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="d737b-110">Selecteer **Artikelvereisten**.</span><span class="sxs-lookup"><span data-stu-id="d737b-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="d737b-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="d737b-111">Select **New**.</span></span>
6. <span data-ttu-id="d737b-112">Typ of selecteer in de nieuwe rij een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="d737b-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="d737b-113">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="d737b-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="d737b-114">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d737b-114">Select **Save**.</span></span>
9. <span data-ttu-id="d737b-115">Selecteer **Beheren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d737b-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="d737b-116">Selecteer **Functies**.</span><span class="sxs-lookup"><span data-stu-id="d737b-116">Select **Functions**.</span></span>
11. <span data-ttu-id="d737b-117">Selecteer **Inkooporder maken**.</span><span class="sxs-lookup"><span data-stu-id="d737b-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="d737b-118">Schakel het selectievakje **Alles opnemen** in.</span><span class="sxs-lookup"><span data-stu-id="d737b-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="d737b-119">Typ of selecteer een waarde in het veld **Leveranciersaccount**.</span><span class="sxs-lookup"><span data-stu-id="d737b-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="d737b-120">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d737b-120">Select **OK**.</span></span>
15. <span data-ttu-id="d737b-121">Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="d737b-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="d737b-122">Selecteer in de lijst de koppeling in de gewenste rij.</span><span class="sxs-lookup"><span data-stu-id="d737b-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="d737b-123">Selecteer **Aankoop** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d737b-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="d737b-124">Selecteer **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="d737b-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="d737b-125">Selecteer **Ontvangen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d737b-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="d737b-126">Selecteer **Productontvangst**.</span><span class="sxs-lookup"><span data-stu-id="d737b-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="d737b-127">Typ een waarde in het veld **Productontvangst**.</span><span class="sxs-lookup"><span data-stu-id="d737b-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="d737b-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d737b-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
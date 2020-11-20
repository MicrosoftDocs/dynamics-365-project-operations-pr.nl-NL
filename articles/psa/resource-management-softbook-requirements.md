---
title: Vereisten zacht boeken
description: Dit onderwerp legt uit hoe u resourcevereisten zacht kunt boeken.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124092"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="04781-103">Vereisten zacht boeken</span><span class="sxs-lookup"><span data-stu-id="04781-103">Soft-book requirements</span></span>

<span data-ttu-id="04781-104">Een resourcevereiste kan hard worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="04781-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="04781-105">Een harde boeking maakt een voorstel aan, waardoor de capaciteit van een resource wordt verbruikt.</span><span class="sxs-lookup"><span data-stu-id="04781-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="04781-106">Het voorstel wordt vervolgens ter goedkeuring teruggestuurd naar de aanvrager.</span><span class="sxs-lookup"><span data-stu-id="04781-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="04781-107">Een zachte boeking voegt een resource voorlopig toe aan een projectteam en heeft een andere status op het planbord, maar verbruikt niet de capaciteit van de resource.</span><span class="sxs-lookup"><span data-stu-id="04781-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="04781-108">Als u een resource vanuit het planbord zacht wilt boeken, stelt u het veld **Boekingsstatus** in op **Zacht**.</span><span class="sxs-lookup"><span data-stu-id="04781-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Boekingsstatus is ingesteld op Zacht](media/Resource-Management-image77.png)

<span data-ttu-id="04781-110">Wanneer het tabblad **Team** in de weergave **Benoemde teamleden** staat, wordt de resource daar weergegeven.</span><span class="sxs-lookup"><span data-stu-id="04781-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="04781-111">De zacht geboekte uren worden gerapporteerd in de kolom **Zacht geboekte uren**.</span><span class="sxs-lookup"><span data-stu-id="04781-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Zacht geboekte uren in de weergave met benoemde teamleden](media/Resource-Management-image78.png)

<span data-ttu-id="04781-113">Zacht geboekte teamleden kunnen niet aan taken worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="04781-113">Soft-booked team members can be assigned to tasks.</span></span>

![Zacht geboekt teamlid toegewezen aan een taak](media/Resource-Management-image79.png)

<span data-ttu-id="04781-115">Op het tabblad **Vereffening** worden geen boekingen weergegeven voor een zacht geboekte resource, omdat het tabblad **Vereffening** alleen rekening houdt met harde boekingen.</span><span class="sxs-lookup"><span data-stu-id="04781-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Zacht geboekte resource zonder boekingen op het tabblad Vereffening](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="04781-117">U kunt een resource niet zacht boeken vanuit een vereiste die is gegenereerd op basis van een algemeen teamlid.</span><span class="sxs-lookup"><span data-stu-id="04781-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="04781-118">Op het planbord wordt een andere kleur gebruikt voor zachte boekingen voor een resource.</span><span class="sxs-lookup"><span data-stu-id="04781-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Zachte boekingen op het planbord](media/Resource-Management-image81.png)

<span data-ttu-id="04781-120">Als u een zachte boeking wilt converteren naar een harde boeking, klikt u in het planbord met de rechtermuisknop op de zachte boeking en kiest u **Status wijzigen** \> **Hard boeken** \> **Hard**.</span><span class="sxs-lookup"><span data-stu-id="04781-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![De boekingsstatus wijzigen in hard](media/Resource-Management-image82.png)

<span data-ttu-id="04781-122">De boeking wordt gewijzigd en de status wordt gewijzigd op het planbord.</span><span class="sxs-lookup"><span data-stu-id="04781-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="04781-123">Omdat de boekingsstatus nu **hard** is, wordt de resource weergegeven als geboekt en worden de capaciteit en beschikbaarheid aangepast.</span><span class="sxs-lookup"><span data-stu-id="04781-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="04781-124">U kunt met dezelfde methode een harde boeking of een zachte boeking annuleren op het planbord.</span><span class="sxs-lookup"><span data-stu-id="04781-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="04781-125">Als u een zacht geboekte resource wilt converteren naar hard geboekt op het tabblad **Team** van het project, selecteert u de resource en vervolgens **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="04781-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Opdracht 'Bevestigen'](media/Resource-Management-image83.png)

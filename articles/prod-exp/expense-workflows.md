---
title: Werkstromen voor onkostenbeheer instellen
description: U kunt een werkstroomproces instellen om reis- en onkostendocumenten te beoordelen en goed te keuren.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271617"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="d1bf0-103">Werkstromen voor onkostenbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="d1bf0-103">Set up Expense management workflows</span></span>

<span data-ttu-id="d1bf0-104">U kunt een werkstroomproces instellen dat wordt gebruikt om reis- en onkostendocumenten te beoordelen en goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="d1bf0-105">De documenten waarvoor werkstromen kunnen worden gedefinieerd omvatten onkostendeclaraties, reisaanvragen en aanvragen voor kasvoorschotten.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="d1bf0-106">Een werkstroom vertegenwoordigt een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-106">A workflow represents a business process.</span></span> <span data-ttu-id="d1bf0-107">Met een werkstroom wordt gedefinieerd hoe een document door het systeem wordt verwerkt en wordt aangegeven wie een taak moet voltooien of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="d1bf0-108">Het gebruik van het werkstroomsysteem in uw organisatie heeft verschillende voordelen:</span><span class="sxs-lookup"><span data-stu-id="d1bf0-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="d1bf0-109">**Consistente processen**: u kunt het goedkeuringsproces definiëren voor specifieke documenten, zoals inkoopaanvragen en onkostendeclaraties.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="d1bf0-110">Het gebruik van het werkstroomsysteem zorgt ervoor dat documenten op een consistente en efficiënte manier worden verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="d1bf0-111">Zichtbaarheid van het proces: u kunt de status, geschiedenis en prestatiestatistieken van een specifieke werkstroominstantie volgen.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="d1bf0-112">Dit helpt u om te bepalen of er wijzigingen in de werkstroom moeten worden aangebracht om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="d1bf0-113">Gecentraliseerde werklijst: gebruikers kunnen een gecentraliseerde werklijst weergeven om de werkstroomtaken en goedkeuringen te bekijken die aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="d1bf0-114">**U kunt de volgende typen werkstromen maken**</span><span class="sxs-lookup"><span data-stu-id="d1bf0-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="d1bf0-115">De onderstaande tabel bevat de werkstroomtypen die u kunt maken in **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="d1bf0-116"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="d1bf0-117"><strong>Gebruik dit type voor het volgende</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="d1bf0-118"><strong>Onkostenrapport</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="d1bf0-119">Maken van goedkeuringswerkstromen voor onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="d1bf0-120"><strong>Automatisch boeken van onkostennota's</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="d1bf0-121">Maken van werkstromen voor het automatisch boeken van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="d1bf0-122"><strong>Onkostenregelitem</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="d1bf0-123">Maken van goedkeuringswerkstromen voor regelitems in onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="d1bf0-124"><strong>Automatisch boeken van onkostenregelitems</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="d1bf0-125">Maken van werkstromen voor het automatisch boeken van van regelitems in onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="d1bf0-126"><strong>Reiskosten</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="d1bf0-127">Maken van goedkeuringswerkstromen voor aanvragen voor reis- en verblijfskostenvergoeding.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="d1bf0-128"><strong>Aanvraag voor kasvoorschot</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="d1bf0-129">Maken van goedkeuringswerkstromen voor aanvragen voor kasvoorschotten.</span><span class="sxs-lookup"><span data-stu-id="d1bf0-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="d1bf0-130"><strong>Btw-afschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="d1bf0-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="d1bf0-131">maken van goedkeuringswerkstromen voor het innen van btw (belasting toegevoegde waarde).</span><span class="sxs-lookup"><span data-stu-id="d1bf0-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
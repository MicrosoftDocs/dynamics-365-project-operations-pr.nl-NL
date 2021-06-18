---
title: Werkstromen instellen voor onkostenbeheer
description: U kunt een werkstroomproces instellen dat wordt gebruikt om reis- en onkostendocumenten te beoordelen en goed te keuren.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001015"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="dba46-103">Werkstromen instellen voor onkostenbeheer</span><span class="sxs-lookup"><span data-stu-id="dba46-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="dba46-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="dba46-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dba46-105">U kunt een werkstroomproces instellen om reis- en onkostendocumenten te beoordelen en goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="dba46-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="dba46-106">U kunt werkstromen definiëren voor onkostennota's, aanvragen voor reis- en verblijfskostenvergoeding en aanvragen voor kasvoorschotten.</span><span class="sxs-lookup"><span data-stu-id="dba46-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="dba46-107">Een werkstroom vertegenwoordigt een bedrijfsproces. In een werkstroom wordt gedefinieerd hoe een document door het systeem wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="dba46-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="dba46-108">De werkstroom geeft ook aan wie een taak moet voltooien of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="dba46-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="dba46-109">Het gebruik van het werkstroomsysteem in uw organisatie heeft verschillende voordelen:</span><span class="sxs-lookup"><span data-stu-id="dba46-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="dba46-110">**Consistente processen**: u kunt het goedkeuringsproces definiëren voor specifieke documenten, zoals inkoopaanvragen en onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="dba46-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="dba46-111">Het gebruik van het werkstroomsysteem zorgt ervoor dat documenten op een consistente en efficiënte manier worden verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="dba46-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="dba46-112">**Zichtbaarheid van het proces**: u kunt de status, geschiedenis en prestatiestatistieken van een specifieke werkstroominstantie volgen.</span><span class="sxs-lookup"><span data-stu-id="dba46-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="dba46-113">Dit helpt u om te bepalen of er wijzigingen in de werkstroom moeten worden aangebracht om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="dba46-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="dba46-114">**Gecentraliseerde werklijst**: gebruikers kunnen een gecentraliseerde werklijst weergeven om de werkstroomtaken en goedkeuringen te bekijken die aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="dba46-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="dba46-115">Werkstroomtypen</span><span class="sxs-lookup"><span data-stu-id="dba46-115">Workflow types</span></span>

<span data-ttu-id="dba46-116">De onderstaande tabel bevat de werkstroomtypen die u kunt maken in **Onkostenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="dba46-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="dba46-117"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="dba46-118"><strong>Gebruik dit type voor het volgende</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="dba46-119"><strong>Automatisch goedkeuren van onkostenrapporten</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="dba46-120">Maken van goedkeuringswerkstromen voor onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="dba46-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="dba46-121"><strong>Automatisch boeken van onkostennota's</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="dba46-122">Maken van werkstromen voor het automatisch boeken van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="dba46-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="dba46-123"><strong>Onkostenregelitem</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="dba46-124">Maken van goedkeuringswerkstromen voor regelitems in onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="dba46-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="dba46-125"><strong>Automatisch boeken van onkostenregelitems</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="dba46-126">Maken van werkstromen voor het automatisch boeken van van regelitems in onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="dba46-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="dba46-127"><strong>Reiskosten</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="dba46-128">Maken van goedkeuringswerkstromen voor aanvragen voor reis- en verblijfskostenvergoeding.</span><span class="sxs-lookup"><span data-stu-id="dba46-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="dba46-129"><strong>Aanvraag voor kasvoorschot</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="dba46-130">Maken van goedkeuringswerkstromen voor aanvragen voor kasvoorschotten.</span><span class="sxs-lookup"><span data-stu-id="dba46-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="dba46-131"><strong>Btw-afschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="dba46-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="dba46-132">maken van goedkeuringswerkstromen voor het innen van btw (belasting toegevoegde waarde).</span><span class="sxs-lookup"><span data-stu-id="dba46-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
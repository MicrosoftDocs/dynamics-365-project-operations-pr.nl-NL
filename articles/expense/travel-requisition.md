---
title: Reisaanvragen
description: Dit onderwerp biedt informatie over reisaanvragen.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074433"
---
# <a name="travel-requisitions"></a><span data-ttu-id="e2e07-103">Reisaanvragen</span><span class="sxs-lookup"><span data-stu-id="e2e07-103">Travel requisitions</span></span>

<span data-ttu-id="e2e07-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="e2e07-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e2e07-105">Op een reisaanvraag staan de onkosten vermeld die worden gemaakt om te reizen.</span><span class="sxs-lookup"><span data-stu-id="e2e07-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="e2e07-106">Een reisaanvraag wordt ter beoordeling ingediend en kan worden gebruikt om onkosten te autoriseren.</span><span class="sxs-lookup"><span data-stu-id="e2e07-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="e2e07-107">Mogelijk moet u een reisaanvraag indienen voordat u kosten maakt die aan de organisatie in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="e2e07-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="e2e07-108">Deze vereiste is van toepassing, ongeacht of u kosten in rekening brengt op een bedrijfscreditcard, contant geld uitgeeft dat u van een contant voorschot hebt ontvangen of contante uitgaven doet die door de organisatie worden vergoed.</span><span class="sxs-lookup"><span data-stu-id="e2e07-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="e2e07-109">Reisaanvragen en beleid kunnen worden gebruikt om de uitgaven van de organisatie te beheren.</span><span class="sxs-lookup"><span data-stu-id="e2e07-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="e2e07-110">Als uw organisatie bijvoorbeeld werkt aan een project met vaste prijs waarvoor reizen nodig is, moeten de reiskosten van de teamleden van het project passen binnen het projectbudget.</span><span class="sxs-lookup"><span data-stu-id="e2e07-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="e2e07-111">Door te eisen dat reiskosten worden goedgekeurd voordat ze worden gemaakt, kan de organisatie ervoor zorgen dat het project binnen het budget blijft.</span><span class="sxs-lookup"><span data-stu-id="e2e07-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="e2e07-112">Configuratie</span><span class="sxs-lookup"><span data-stu-id="e2e07-112">Configuration</span></span> 

<span data-ttu-id="e2e07-113">Reisaanvragen kunnen worden geconfigureerd als "verplicht" door het inschakelen van de parameter "Pre-autorisatie van reizen is verplicht" in Parameters voor onkostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="e2e07-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="e2e07-114">Een reisaanvraag maken en indienen</span><span class="sxs-lookup"><span data-stu-id="e2e07-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="e2e07-115">Ga naar **Mijn onkosten: reisaanvraag** en selecteer **Nieuwe reisaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="e2e07-115">Go to **My expenses: Travel Requisition** , and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="e2e07-116">Voer een doel en bestemming in voor de aanvraag.</span><span class="sxs-lookup"><span data-stu-id="e2e07-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="e2e07-117">Voer in het veld **Reisbeschrijving** eventuele aanvullende informatie in.</span><span class="sxs-lookup"><span data-stu-id="e2e07-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="e2e07-118">Maak voor elk van de verwachte uitgaven, zoals vlucht, maaltijden of autoverhuur, een onkostenpost.</span><span class="sxs-lookup"><span data-stu-id="e2e07-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="e2e07-119">Vermeld de geschatte datum, het geschatte bedrag en de valuta voor elke uitgave.</span><span class="sxs-lookup"><span data-stu-id="e2e07-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="e2e07-120">Als u klaar bent met het toevoegen van de verwachte uitgaven, selecteert u **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e2e07-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="e2e07-121">Als u klaar bent om de reisaanvraag in te dienen, selecteert u **Workflow** > **Verzenden**.</span><span class="sxs-lookup"><span data-stu-id="e2e07-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="e2e07-122">U kunt uw goedgekeurde reisaanvragen bekijken onder **Mijn onkosten: reisaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="e2e07-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="e2e07-123">Beschikbare reisaanvragen weergeven</span><span class="sxs-lookup"><span data-stu-id="e2e07-123">View available travel requisitions</span></span>

<span data-ttu-id="e2e07-124">U kunt al uw reisaanvragen bekijken onder **Mijn onkosten: reisaanvragen**.</span><span class="sxs-lookup"><span data-stu-id="e2e07-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="e2e07-125">Reisaanvragen goedkeuren</span><span class="sxs-lookup"><span data-stu-id="e2e07-125">Approve travel requisitions</span></span>

<span data-ttu-id="e2e07-126">Selecteer de reisaanvraag die u wilt goedkeuren en selecteer vervolgens **Workflow** > **Goedkeuren**.</span><span class="sxs-lookup"><span data-stu-id="e2e07-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="e2e07-127">Een onkostendeclaratie indienen met uw goedgekeurde reisaanvraag</span><span class="sxs-lookup"><span data-stu-id="e2e07-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="e2e07-128">Maak een nieuwe onkostendeclaratie en selecteer in de kop van de onkostendeclaratie en in de lijst met goedgekeurde reisaanvragen **Toewijzen aan reisaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="e2e07-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="e2e07-129">Het veld **Bedrag reisaanvraag** wordt automatisch bijgewerkt in de kop van de onkostendeclaratie.</span><span class="sxs-lookup"><span data-stu-id="e2e07-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="e2e07-130">Voeg alle kosten toe die voor de reis zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e2e07-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="e2e07-131">Als het veld **Pre-geautoriseerd** is ingeschakeld, worden het afgestemde bedrag en het geautoriseerde bedrag voor de specifieke onkostencategorie bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="e2e07-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="e2e07-132">Wanneer u een onkostendeclaratie toewijst aan een goedgekeurde reisaanvraag, kan het transactiebedrag niet hoger zijn dan het geautoriseerde bedrag.</span><span class="sxs-lookup"><span data-stu-id="e2e07-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 

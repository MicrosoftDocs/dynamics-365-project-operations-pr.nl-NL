---
title: Onkostenbeleid definiëren
description: U kunt het onkostenbeleid definiëren dat uw werknemers moeten volgen bij het invoeren en indienen van onkostennota's en aanvragen voor reis- en verblijfskostenvergoeding.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001870"
---
# <a name="define-expense-policies"></a><span data-ttu-id="a9d66-103">Onkostenbeleid definiëren</span><span class="sxs-lookup"><span data-stu-id="a9d66-103">Define expense policies</span></span>

<span data-ttu-id="a9d66-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="a9d66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a9d66-105">U kunt beleid definiëren dat uw werknemers moeten volgen bij het invoeren en indienen van onkostennota's en aanvragen voor reis- en verblijfskostenvergoeding.</span><span class="sxs-lookup"><span data-stu-id="a9d66-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="a9d66-106">Als u onkostenbeleid implementeert, kunt u uw uitgaven effectief beheren.</span><span class="sxs-lookup"><span data-stu-id="a9d66-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="a9d66-107">U kunt bijvoorbeeld een beleid instellen voor hotelkosten in New York City, waarin staat dat de kosten per nacht niet hoger mogen zijn dan USD 250.</span><span class="sxs-lookup"><span data-stu-id="a9d66-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="a9d66-108">Als een werknemer een onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient waarbij de kamerprijs hoger is dan dit bedrag, stelt het systeem de</span><span class="sxs-lookup"><span data-stu-id="a9d66-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="a9d66-109">de werknemer op de hoogte dat het bedrag dat in het beleid voor de onkosten is opgenomen, is overschreden.</span><span class="sxs-lookup"><span data-stu-id="a9d66-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="a9d66-110">U kunt het bericht dat de werknemer ontvangt, configureren bij het</span><span class="sxs-lookup"><span data-stu-id="a9d66-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="a9d66-111">definiëren van het beleid.</span><span class="sxs-lookup"><span data-stu-id="a9d66-111">define the policy.</span></span>      
        
<span data-ttu-id="a9d66-112">U kunt drie typen beleid definiëren:</span><span class="sxs-lookup"><span data-stu-id="a9d66-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="a9d66-113">**Waarschuwing**: hiermee kan de werknemer een onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indienen, maar de onkosten worden gemarkeerd voor alle fiatteurs en</span><span class="sxs-lookup"><span data-stu-id="a9d66-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="a9d66-114">voor latere rapportage.</span><span class="sxs-lookup"><span data-stu-id="a9d66-114">for later reporting.</span></span>        

- <span data-ttu-id="a9d66-115">**Fout** : vereist dat de werknemer de onkosten wijzigt om te voldoen aan het beleid voordat hij of zij de onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient.</span><span class="sxs-lookup"><span data-stu-id="a9d66-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="a9d66-116">**Reden**: vereist dat de werknemer of een manager een reden invoert voor het overschrijden van het bedrag in het beleid voordat hij of zij de onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient.</span><span class="sxs-lookup"><span data-stu-id="a9d66-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="a9d66-117">Beleidstips</span><span class="sxs-lookup"><span data-stu-id="a9d66-117">Policy tips</span></span>
<span data-ttu-id="a9d66-118">Hier volgen een paar suggesties die u kunnen helpen bij het maken van nieuw beleid voor onkostenbeheer:</span><span class="sxs-lookup"><span data-stu-id="a9d66-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="a9d66-119">Beleid is van kracht vanaf de datum van ingang, wat inhoudt dat beleid niet van kracht is als het is gemaakt met een datum na de datum waarop de onkosten zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a9d66-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="a9d66-120">U maakt bijvoorbeeld vandaag een nieuw beleid om voor maaltijden een maximumbedrag $ 50 in te stellen.</span><span class="sxs-lookup"><span data-stu-id="a9d66-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="a9d66-121">Alle bestaande uitgaven die vanaf gisteren zijn ingevoerd, worden niet gecontroleerd op basis van dit beleid.</span><span class="sxs-lookup"><span data-stu-id="a9d66-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="a9d66-122">Als u beleid maakt voor een onkostencategorie die kan worden gespecificeerd, moet u overwegen om een voorwaarde toe te voegen voor het type onkostenregel.</span><span class="sxs-lookup"><span data-stu-id="a9d66-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="a9d66-123">Sommige beleidsregels, zoals het eisen van een betalingsbewijs, zijn mogelijk niet zinvol voor gespecificeerde regels.</span><span class="sxs-lookup"><span data-stu-id="a9d66-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="a9d66-124">In deze situatie wordt het beleid alleen toegepast op de koptekstregel of een niet-gespecificeerde regel.</span><span class="sxs-lookup"><span data-stu-id="a9d66-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="a9d66-125">Beleid voor onkostenbeheer wordt standaard geëvalueerd op basis van de bronentiteit.</span><span class="sxs-lookup"><span data-stu-id="a9d66-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="a9d66-126">Voor intercompany-scenario's kunt u het beleid instellen dat in plaats daarvan moet worden geëvalueerd op basis van de doelentiteit (lenende entiteit).</span><span class="sxs-lookup"><span data-stu-id="a9d66-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="a9d66-127">Schakel de optie **Onkostenbeleid evalueren op basis van lenende rechtspersoon** in de werkruimte **Functiebeheer** in om het beleid uit te voeren op basis van de doelentiteit.</span><span class="sxs-lookup"><span data-stu-id="a9d66-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="a9d66-128">Wanneer moet beleid worden geëvalueerd</span><span class="sxs-lookup"><span data-stu-id="a9d66-128">When to evaluate policies</span></span>

<span data-ttu-id="a9d66-129">In de parameters voor onkostenbeheer kunt u ervoor kiezen om beleid voor onkostenbeheer te evalueren wanneer een regel wordt opgeslagen of wanneer een onkostennota wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="a9d66-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="a9d66-130">Als u ervoor kiest om de evaluatie uit te voeren wanneer een regel wordt opgeslagen, hebben gebruikers eerder inzicht in wat ze moeten doen om hun onkostennota in één keer te voltooien.</span><span class="sxs-lookup"><span data-stu-id="a9d66-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="a9d66-131">U kunt de beleidsevaluatie ook uitstellen en tijd besparen door de evaluatie aan het einde uit te voeren tijdens het indienen bij de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="a9d66-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
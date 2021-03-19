---
title: Onkostenbeleid instellen
description: U kunt het onkostenbeleid instellen dat uw werknemers moeten volgen bij het invoeren en indienen van onkostendeclaraties en aanvragen voor reiskostenvergoeding in Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271257"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="9e2c7-103">Onkostenbeleid instellen</span><span class="sxs-lookup"><span data-stu-id="9e2c7-103">Set up expense policies</span></span>

<span data-ttu-id="9e2c7-104">U kunt beleid definiëren dat uw werknemers moeten volgen bij het invoeren en indienen van onkostennota's en aanvragen voor reis- en verblijfskostenvergoeding.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="9e2c7-105">Als u onkostenbeleid implementeert, kunt u uw uitgaven effectief beheren.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="9e2c7-106">U kunt bijvoorbeeld een beleid instellen voor hotelkosten in New York City, waarin staat dat de kosten per nacht niet hoger mogen zijn dan USD 250.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="9e2c7-107">Als een werknemer een onkostendeclaratie of aanvraag voor reiskostenvergoeding indient waarbij de kamerprijs hoger is dan dit bedrag, stelt het systeem de</span><span class="sxs-lookup"><span data-stu-id="9e2c7-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="9e2c7-108">de werknemer op de hoogte dat het bedrag dat in het beleid voor de onkosten is opgenomen, is overschreden.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="9e2c7-109">U kunt het bericht dat de werknemer ontvangt, configureren bij het</span><span class="sxs-lookup"><span data-stu-id="9e2c7-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="9e2c7-110">definiëren van het beleid.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-110">define the policy.</span></span>      
        
<span data-ttu-id="9e2c7-111">U kunt drie typen beleid definiëren:</span><span class="sxs-lookup"><span data-stu-id="9e2c7-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="9e2c7-112">Waarschuwing: hiermee kan de werknemer een onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indienen, maar de onkosten worden gemarkeerd voor alle fiatteurs en</span><span class="sxs-lookup"><span data-stu-id="9e2c7-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="9e2c7-113">voor latere rapportage.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-113">for later reporting.</span></span>        

- <span data-ttu-id="9e2c7-114">Fout: vereist dat de werknemer de onkosten wijzigt om te voldoen aan het beleid voordat hij of zij de onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="9e2c7-115">Reden: vereist dat de werknemer of een manager een reden invoert voor het overschrijden van het bedrag in het beleid voordat hij of zij de onkostennota of aanvraag voor reis- en verblijfskostenvergoeding indient.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="9e2c7-116">Beleidstips</span><span class="sxs-lookup"><span data-stu-id="9e2c7-116">Policy tips</span></span>
<span data-ttu-id="9e2c7-117">Hier volgen een paar suggesties die u kunnen helpen bij het maken van nieuw beleid voor onkostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="9e2c7-118">Beleid werkt met ingangsdatums en wordt pas van kracht als het beleid is gemaakt met een datum na de datum waarop de onkosten zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="9e2c7-119">Als u bijvoorbeeld vandaag een nieuw beleid maakt om een maximale maaltijduitgave van $50 op te leggen, worden bestaande uitgaven die vanaf gisteren zijn ingevoerd, niet vergeleken met dit beleid.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="9e2c7-120">Als u beleid maakt voor een onkostencategorie die kan worden gespecificeerd, moet u overwegen om een voorwaarde toe te voegen voor het type onkostenregel.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="9e2c7-121">Sommige beleidsregels, zoals het vereisen van een ontvangstbewijs, zijn mogelijk niet logisch voor gespecificeerde regels en moeten alleen worden toegepast op de kopregel of een niet-gespecificeerde regel.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="9e2c7-122">Beleid voor onkostenbeheer wordt standaard geëvalueerd op basis van de bronentiteit.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="9e2c7-123">Voor intercompany-scenario's kunt u het beleid instellen dat in plaats daarvan moet worden geëvalueerd op basis van de doelentiteit (lenende entiteit).</span><span class="sxs-lookup"><span data-stu-id="9e2c7-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="9e2c7-124">Schakel de optie Onkostenbeleid evalueren op basis van lenende rechtspersoon in de werkruimte **Functiebeheer** in om het beleid uit te voeren op basis van de doelentiteit.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="9e2c7-125">Wanneer moet beleid worden geëvalueerd</span><span class="sxs-lookup"><span data-stu-id="9e2c7-125">When to evaluate policies</span></span>

<span data-ttu-id="9e2c7-126">In de parameters voor onkostenbeheer kunt u een optie kiezen om beleid voor onkostenbeheer te evalueren wanneer een regel wordt opgeslagen of wanneer een onkostennota wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="9e2c7-127">Als u ervoor kiest om de evaluatie uit te voeren wanneer een regel wordt opgeslagen, zorgt u dat gebruikers eerder inzicht hebben in wat ze moeten doen om hun onkostennota in één keer te voltooien.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="9e2c7-128">U kunt de beleidsevaluatie ook uitstellen en tijd besparen door de evaluatie aan het einde uit te voeren tijdens het indienen bij de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
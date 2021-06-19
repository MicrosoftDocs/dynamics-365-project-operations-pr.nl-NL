---
title: Goedkeuringssets
description: Dit onderwerp biedt informatie over goedkeuringsset, verzoeken en de subsets van die bewerkingen.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116865"
---
# <a name="approval-sets"></a><span data-ttu-id="90f34-103">Goedkeuringssets</span><span class="sxs-lookup"><span data-stu-id="90f34-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="90f34-104">Met goedkeuringssets worden goedkeuringsverzoeken in kleinere subsets van bewerkingen gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="90f34-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="90f34-105">Met deze groepering kunnen goedkeuringen op volgorde worden verwerkt per project en kan opnieuw een poging worden gedaan om ze te verwerken en op volgorde te zetten.</span><span class="sxs-lookup"><span data-stu-id="90f34-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="90f34-106">Groepering verbetert de betrouwbaarheid en traceerbaarheid van goedkeuringsverwerking voor grote hoeveelheden goedkeuringen.</span><span class="sxs-lookup"><span data-stu-id="90f34-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="90f34-107">Goedkeuringssets geven de algehele verwerkingsstatus van gerelateerde records aan.</span><span class="sxs-lookup"><span data-stu-id="90f34-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="90f34-108">Wanneer een goedkeuringsrecord wordt verwerkt met behulp van een goedkeuringsset, wordt de record verplaatst van **Ingediend** naar **Goedgekeurd** en wordt deze losgekoppeld van de goedkeuringsset.</span><span class="sxs-lookup"><span data-stu-id="90f34-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="90f34-109">Als een record mislukt wanneer deze ter goedkeuring wordt ingediend, behoudt het record de status van **Ingediend** en wordt de goedkeuringsset gemarkeerd als mislukt.</span><span class="sxs-lookup"><span data-stu-id="90f34-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="90f34-110">De goedkeuringsset registreert de foutmelding van de storing.</span><span class="sxs-lookup"><span data-stu-id="90f34-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="90f34-111">Goedkeuringen en goedkeuringssets verwerken</span><span class="sxs-lookup"><span data-stu-id="90f34-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="90f34-112">Goedkeuringen die in de wachtrij staan voor verwerking, zijn zichtbaar in de weergave **Goedkeuringen verwerken**.</span><span class="sxs-lookup"><span data-stu-id="90f34-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="90f34-113">Het systeem probeert alle invoer meerdere keren asynchroon te verwerken, inclusief een nieuwe poging om een goedkeuring te verwerken als eerdere pogingen zijn mislukt.</span><span class="sxs-lookup"><span data-stu-id="90f34-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="90f34-114">Met het veld **Levensduur goedkeuringsset** wordt het aantal pogingen dat nog moeten worden verwerkt, geregistreerd voordat deze als mislukt wordt gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="90f34-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="90f34-115">Mislukte goedkeuringen en goedkeuringssets</span><span class="sxs-lookup"><span data-stu-id="90f34-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="90f34-116">In de weergave **Mislukte goedkeuringen** worden alle goedkeuringen weergegeven die tussenkomst van de gebruiker vereisen.</span><span class="sxs-lookup"><span data-stu-id="90f34-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="90f34-117">Open de bijbehorende goedkeuringssetlogboeken om de oorzaak van de storing te achterhalen.</span><span class="sxs-lookup"><span data-stu-id="90f34-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="90f34-118">Als u **Opnieuw proberen** selecteert, wordt dit toegevoegd aan de levensduur van de goedkeuringsset, wordt de goedkeuringsset terug naar de status **Verwerken** verplaatst en wordt getracht de resterende records te verwerken.</span><span class="sxs-lookup"><span data-stu-id="90f34-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="90f34-119">Goedkeuringssets configureren</span><span class="sxs-lookup"><span data-stu-id="90f34-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="90f34-120">De functie Goedkeuringssets inschakelen</span><span class="sxs-lookup"><span data-stu-id="90f34-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="90f34-121">Voordat u de functie Goedkeuringssets inschakelt, moet u controleren of er momenteel geen goedkeuringen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="90f34-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="90f34-122">Ga naar de pagina **Projectparameters** en selecteer **Besturingselement voor functie** > **Moderne goedkeuringen inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="90f34-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="90f34-123">De functie Goedkeuringssets uitschakelen</span><span class="sxs-lookup"><span data-stu-id="90f34-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="90f34-124">Voordat u de functie Goedkeuringssets uitschakelt, moet u controleren of er momenteel geen goedkeuringen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="90f34-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="90f34-125">Ga naar de pagina **Projectparameters** en selecteer **Besturingselement voor functie** > **Moderne goedkeuringen uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="90f34-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="90f34-126">De asynchrone drempel configureren</span><span class="sxs-lookup"><span data-stu-id="90f34-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="90f34-127">Wanneer goedkeuringssets worden gemaakt, wordt de verwerking naar de achtergrond verplaatst wanneer het geselecteerde aantal records voor goedkeuring de aangegeven drempel overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="90f34-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="90f34-128">Gebruik het veld **Asynchrone drempel** om te configureren wanneer goedkeuringsverwerking synchroon of asynchroon moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="90f34-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="90f34-129">Geldige waarden zijn:</span><span class="sxs-lookup"><span data-stu-id="90f34-129">Valid values are:</span></span>

  - <span data-ttu-id="90f34-130">Nul: alle verzoeken moeten asynchroon worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="90f34-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="90f34-131">Aantallen groter dan nul: goedkeuringen worden alleen asynchroon verwerkt wanneer het ingediende aantal goedkeuringen deze waarde overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="90f34-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Inhoudingstermijnen voor leveranciersbetalingen maken en toepassen
description: Dit onderwerp bevat informatie over het instellen en onderhouden van inhoudingstermijnen voor leveranciersbetalingen.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270942"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="a1bdc-103">Inhoudingstermijnen voor leveranciersbetalingen maken en toepassen</span><span class="sxs-lookup"><span data-stu-id="a1bdc-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="a1bdc-104">Het instellen van inhoudingstermijnen voor leveranciersbetalingen voor een project is handig wanneer uw organisatie een deel van de betalingen die voor een leverancier zijn verricht wil inhouden.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="a1bdc-105">Bijvoorbeeld wanneer u de betaling aan een leverancier wilt uitstellen totdat de geleverde producten aan uw verwachtingen voldoen.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="a1bdc-106">Inhoudingstermijnen voor leveranciersbetalingen kunnen worden opgegeven wanneer u onderhandelt over een leverancierscontract.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="a1bdc-107">Inhoudingstermijnen voor leveranciersbetalingen maken</span><span class="sxs-lookup"><span data-stu-id="a1bdc-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="a1bdc-108">U kunt het percentage van de leveranciersbetaling voor inhouding invoeren en het percentage van de eerder ingehouden bedragen die moeten worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="a1bdc-109">Bedragen worden automatisch ingehouden op leveranciersfacturen totdat het contract de opgegeven status van voltooiing bereikt.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="a1bdc-110">Nadat u de inhoudingstermijnen hebt ingesteld, kunt u deze toepassen op elk project voor die leverancier.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="a1bdc-111">Gebruik de volgende stappen om inhoudingstermijnen voor leveranciersbetalingen in te stellen en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="a1bdc-112">Ga naar **Projectmanagement en financiële administratie** > **Inhouding** > **Inhoudingstermijnen voor leveranciersbetalingen**.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="a1bdc-113">Selecteer **Nieuw** om een nieuwe inhoudingstermijn voor leveranciers toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="a1bdc-114">De waarde **Regel-ID** voor de nieuwe termijn wordt automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="a1bdc-115">Voer een korte beschrijving in het veld **Omschrijving** in en selecteer op het sneltabblad **Termijnen** **Regel toevoegen** om termijnwaarden in te voeren voor het volgende:</span><span class="sxs-lookup"><span data-stu-id="a1bdc-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="a1bdc-116">**Percentage geleverde eenheden**: voer een voltooiingspercentage voor de termijn in.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="a1bdc-117">Bedragen worden automatisch ingehouden op leveranciersfacturen totdat de projectfase van voltooiing gelijk is aan het opgegeven percentage.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="a1bdc-118">Als u bijvoorbeeld 50,00 invoert, worden bedragen ingehouden totdat het project voor 50 procent is voltooid.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="a1bdc-119">**Percentage om in te houden**: voer een percentage van het leveranciersfactuurbedrag in dat moet worden ingehouden.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="a1bdc-120">Als u bijvoorbeeld 10,00 invoert, wordt 10 procent van het bedrag op een leveranciersfactuur ingehouden totdat het project het voltooiingspercentage bereikt dat is ingesteld in het veld **Percentage geleverde eenheden**.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="a1bdc-121">**Percentage om vrij te geven**: selecteer **Regel toevoegen** om een percentage in te voeren van eerder ingehouden bedragen die moeten worden vrijgegeven voor het geselecteerde voltooiingsniveau van het project.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="a1bdc-122">Als u meer dan één mijlpaal hebt voor verschillende voltooiingsniveaus van een project, voert u voor elke inhoudingsregel een afzonderlijke inhoudingstermijnregel voor leveranciers in.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="a1bdc-123">Met elke regel kan een ander inhoudingspercentage en een ander vrijgavepercentage worden opgegeven voor elk toegewezen voltooiingsniveau van het project.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="a1bdc-124">Nadat u de inhoudingstermijnen voor een leverancier hebt ingesteld, kunt u de termijnen toepassen op een project.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="a1bdc-125">Inhoudingstermijnen voor leveranciers toepassen op een project</span><span class="sxs-lookup"><span data-stu-id="a1bdc-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="a1bdc-126">Ga naar **Projectmanagement en financiële administratie** > **Projecten** > **Alle projecten** en open een project via de projectlijstpagina.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="a1bdc-127">Selecteer **Regel toevoegen** op het sneltabblad **Leveranciersovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="a1bdc-128">Selecteer in het veld **Rekeningcode** een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="a1bdc-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="a1bdc-129">**Tabel**: de inhoudingstermijnen voor leveranciers zijn van toepassing op één leverancier.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="a1bdc-130">**Groep**: de inhoudingstermijnen voor leveranciers zijn van toepassing op alle leveranciers in een leveranciersgroep.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="a1bdc-131">**Alle**: de inhoudingstermijnen voor leveranciers zijn van toepassing op alle leveranciers.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="a1bdc-132">Selecteer in het veld **Leverancier/Leveranciersgroep** de leverancier of leveranciersgroep waarop de inhoudingstermijnen voor leveranciers van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="a1bdc-133">Als u **Alle** hebt gekozen in de vorige stap, is dit veld niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="a1bdc-134">Selecteer in het veld **Inhoudingstermijnen voor leveranciers** de inhoudingstermijnen die u in de vorige procedure hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="a1bdc-135">Als voor het project ook PWP-voorwaarden (Pay-When-Paid) zijn ingesteld voor de leverancier, voert u het drempelpercentage voor het project in het veld **PWP-drempelpercentage** in.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="a1bdc-136">De inhoudingstermijnen voor leveranciers worden ook weergegeven op inkooporders die u voor de leverancier maakt.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
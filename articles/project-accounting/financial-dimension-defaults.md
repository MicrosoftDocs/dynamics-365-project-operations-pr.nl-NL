---
title: Standaardwaarden voor financiële dimensies
description: Dit onderwerp biedt informatie over het instellen van standaardinstellingen voor financiële dimensies.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950123"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="982e3-103">Standaardwaarden voor financiële dimensies</span><span class="sxs-lookup"><span data-stu-id="982e3-103">Financial dimension defaults</span></span>

<span data-ttu-id="982e3-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="982e3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="982e3-105">Dynamics 365 Project Operations gebruikt het raamwerk [Financiële dimensies](/dynamics365/finance/general-ledger/financial-dimensions) in Dynamics 365 Finance om aanvullende inzichten te bieden in projecttransacties in subadministratie en grootboek.</span><span class="sxs-lookup"><span data-stu-id="982e3-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="982e3-106">Standaard financiële dimensies kunnen worden ingesteld voor een klant, projectfinancieringsbron, mijlpaal, projectcontractregel of project.</span><span class="sxs-lookup"><span data-stu-id="982e3-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="982e3-107">Financiële standaarddimensies voor een klant definiëren</span><span class="sxs-lookup"><span data-stu-id="982e3-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="982e3-108">Standaardinstellingen voor klantdimensies worden opgegeven in Finance.</span><span class="sxs-lookup"><span data-stu-id="982e3-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="982e3-109">Voer de volgende stappen uit om standaardwaarden voor dimensies in te stellen.</span><span class="sxs-lookup"><span data-stu-id="982e3-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="982e3-110">Ga naar **Klanten** > **Klanten** > **Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="982e3-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="982e3-111">Stel op de pagina **Klanten**, op het tabblad **Financiële dimensies** de financiële dimensiewaarden in voor een specifieke klant.</span><span class="sxs-lookup"><span data-stu-id="982e3-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="982e3-112">Financiële standaarddimensies voor projectcontracten definiëren</span><span class="sxs-lookup"><span data-stu-id="982e3-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="982e3-113">Projectcontracten worden aangemaakt en onderhouden in Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="982e3-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="982e3-114">Boekhoudkundige kenmerken voor projectcontracten worden ingesteld in de module **Projectbeheer en boekhouding** in Finance.</span><span class="sxs-lookup"><span data-stu-id="982e3-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="982e3-115">Financiële dimensies instellen voor een financieringsbron voor een project</span><span class="sxs-lookup"><span data-stu-id="982e3-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="982e3-116">Ga naar **Projectmanagement en financiële administratie** > **Projecten** > **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="982e3-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="982e3-117">Selecteer de record die u wilt bijwerken en selecteer op het tabblad **Projectcontract** de optie **Standaardboekhouding weergeven**.</span><span class="sxs-lookup"><span data-stu-id="982e3-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="982e3-118">Vouw **Gerelateerde informatie** uit en selecteer het tabblad **Financieringsbronnen**.</span><span class="sxs-lookup"><span data-stu-id="982e3-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="982e3-119">Stel de standaardwaarden voor financiële dimensies in.</span><span class="sxs-lookup"><span data-stu-id="982e3-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="982e3-120">Merk op dat de financiële dimensies standaard afkomstig zijn van de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="982e3-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="982e3-121">Financiële dimensies instellen voor een contractregel voor een project</span><span class="sxs-lookup"><span data-stu-id="982e3-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="982e3-122">Ga naar **Projectmanagement en financiële administratie** > **Projecten** > **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="982e3-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="982e3-123">Selecteer de record die u wilt bijwerken en selecteer op het tabblad **Projectcontract** de optie **Standaardboekhouding weergeven**.</span><span class="sxs-lookup"><span data-stu-id="982e3-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="982e3-124">Vouw **Gerelateerde informatie** uit en selecteer het tabblad **Contractregels**.</span><span class="sxs-lookup"><span data-stu-id="982e3-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="982e3-125">Stel de standaardwaarden voor financiële dimensies in.</span><span class="sxs-lookup"><span data-stu-id="982e3-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="982e3-126">De standaardinstellingen van de financiële dimensie zijn van toepassing en kunnen alleen worden gebruikt met contractregels met een vaste prijs (mijlpaal).</span><span class="sxs-lookup"><span data-stu-id="982e3-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="982e3-127">Deze standaardwaarden worden gebruikt voor gerelateerde projecttransacties op rekening en factuurregels.</span><span class="sxs-lookup"><span data-stu-id="982e3-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="982e3-128">Financiële standaarddimensies voor projecten definiëren</span><span class="sxs-lookup"><span data-stu-id="982e3-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="982e3-129">Projecten worden aangemaakt en onderhouden in CDS.</span><span class="sxs-lookup"><span data-stu-id="982e3-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="982e3-130">Boekhoudkundige kenmerken voor projecten worden ingesteld in de module **Projectbeheer en boekhouding** in Finance.</span><span class="sxs-lookup"><span data-stu-id="982e3-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="982e3-131">Ga naar **Projectbeheer en boekhouding** > **Projecten** > **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="982e3-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="982e3-132">Selecteer de record die u wilt bijwerken en selecteer op het tabblad **Project** de optie **Standaardboekhouding weergeven**.</span><span class="sxs-lookup"><span data-stu-id="982e3-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="982e3-133">Vouw **Gerelateerde informatie** uit en selecteer het tabblad **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="982e3-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="982e3-134">Stel de standaardwaarden voor financiële dimensies in.</span><span class="sxs-lookup"><span data-stu-id="982e3-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="982e3-135">Merk op dat de financiële dimensies standaard afkomstig zijn van de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="982e3-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="982e3-136">Als het project is gekoppeld aan een contractregel met meerdere projectcontractklanten, wordt de primaire klant gebruikt om de financiële standaarddimensies te bepalen.</span><span class="sxs-lookup"><span data-stu-id="982e3-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="982e3-137">Financiële standaarddimensies van projecten worden gebruikt om de standaardwaarden van journaalregels in te stellen voor transacties voor tijd, onkosten en vergoedingen in het **Project Operations-integratiejournaal** en op gerelateerde projectfactuurregels.</span><span class="sxs-lookup"><span data-stu-id="982e3-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Het automatisch maken van facturen configureren
description: Dit onderwerp geeft informatie over hoe u het systeem kunt configureren om automatisch facturen te genereren.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898120"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="e1788-103">Het automatisch maken van facturen configureren</span><span class="sxs-lookup"><span data-stu-id="e1788-103">Configure automated invoice creation</span></span>

<span data-ttu-id="e1788-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="e1788-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1788-105">Voer de volgende stappen uit om een geautomatiseerde factuur-uitvoeringsbewerking te configureren in Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e1788-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="e1788-106">Ga naar **Instellingen** \> **Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="e1788-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="e1788-107">Maak een batchtaak en noem deze taak **Facturen maken met Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="e1788-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="e1788-108">De naam van de batchtaak moet de woorden 'facturen maken' bevatten.</span><span class="sxs-lookup"><span data-stu-id="e1788-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="e1788-109">Selecteer in het veld **Taaktype** de optie **Geen**.</span><span class="sxs-lookup"><span data-stu-id="e1788-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="e1788-110">Standaard zijn voor de frequentie de opties **Dagelijks** en **Is actief** ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e1788-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="e1788-111">Selecteer **Werkstroom uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="e1788-111">Select **Run Workflow**.</span></span> <span data-ttu-id="e1788-112">In het dialoogvenster **Record opzoeken** ziet u drie werkstromen:</span><span class="sxs-lookup"><span data-stu-id="e1788-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="e1788-113">Aanroeper procesuitvoering</span><span class="sxs-lookup"><span data-stu-id="e1788-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="e1788-114">Proces uitvoeren</span><span class="sxs-lookup"><span data-stu-id="e1788-114">ProcessRunner</span></span>
    - <span data-ttu-id="e1788-115">Rolgebruik bijwerken</span><span class="sxs-lookup"><span data-stu-id="e1788-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="e1788-116">Selecteer **Aanroeper procesuitvoering** en selecteer vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e1788-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="e1788-117">Selecteer in het volgende dialoogvenster de optie **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1788-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="e1788-118">Een **slaapstandwerkstroom** wordt gevolgd door een **proceswerkstroom**.</span><span class="sxs-lookup"><span data-stu-id="e1788-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="e1788-119">U kunt ook **Proces uitvoeren** selecteren in stap 5.</span><span class="sxs-lookup"><span data-stu-id="e1788-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="e1788-120">Wanneer u vervolgens **OK** selecteert, wordt een **proceswerkstroom** gevolgd door een **slaapstandwerkstroom**.</span><span class="sxs-lookup"><span data-stu-id="e1788-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="e1788-121">Met de werkstromen **Aanroeper procesuitvoering** en **Proces uitvoeren** worden facturen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1788-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="e1788-122">**Aanroeper procesuitvoering** roept **Proces uitvoeren** aan.</span><span class="sxs-lookup"><span data-stu-id="e1788-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="e1788-123">**Proces uitvoeren** is de werkstroom waarmee de facturen daadwerkelijk worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1788-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="e1788-124">Met de werkstroom worden alle contractregels doorlopen waarvoor facturen moeten worden gemaakt en worden facturen voor die regels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1788-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="e1788-125">Voor deze taak wordt gekeken naar de uitvoeringsdatums van facturen voor de contractregels om te bepalen voor welke contractregels facturen moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1788-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="e1788-126">Als contractregels die tot één contract behoren, dezelfde factuur-uitvoeringsdatum hebben, worden de transacties samengevoegd tot één factuur met twee factuurregels.</span><span class="sxs-lookup"><span data-stu-id="e1788-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="e1788-127">Als er geen transacties zijn waarvoor facturen kunnen worden gemaakt, wordt bij de taak het maken van de factuur overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="e1788-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="e1788-128">Nadat de werkstroom **Proces uitvoeren** is voltooid, roept deze de werkstroom **Aanroeper procesuitvoering** aan, verstrekt deze de eindtijd en wordt deze afgesloten.</span><span class="sxs-lookup"><span data-stu-id="e1788-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="e1788-129">**Aanroeper procesuitvoering** start vervolgens een timer die 24 uur wordt uitgevoerd vanaf de opgegeven eindtijd.</span><span class="sxs-lookup"><span data-stu-id="e1788-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="e1788-130">Als de timer heeft afgeteld tot nul, wordt **Aanroeper procesuitvoering** gesloten.</span><span class="sxs-lookup"><span data-stu-id="e1788-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="e1788-131">De batchprocestaak voor het maken van facturen is een terugkerende taak.</span><span class="sxs-lookup"><span data-stu-id="e1788-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="e1788-132">Als dit batchproces vaak wordt uitgevoerd, worden er meerdere exemplaren van de taak gemaakt en veroorzaakt dit fouten.</span><span class="sxs-lookup"><span data-stu-id="e1788-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="e1788-133">U moet daarom het batchproces slechts één keer starten en moet u het proces alleen opnieuw opstarten als het proces niet meer wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e1788-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="e1788-134">Batchfacturering wordt alleen uitgevoerd voor projectcontractregels die zijn geconfigureerd door factuurschema's.</span><span class="sxs-lookup"><span data-stu-id="e1788-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="e1788-135">Voor een contractregel met een factureringsmethode met een vaste prijs moeten mijlpalen zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="e1788-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="e1788-136">Voor een projectcontractregel met een factureringsmethode voor tijd en materiaal is een op datum gebaseerd factuurschema nodig.</span><span class="sxs-lookup"><span data-stu-id="e1788-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="e1788-137">Hetzelfde geldt voor een contractregel die op een project is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="e1788-137">The same applies to a project-based contract line.</span></span>     

---
title: Toerekenbare componenten van een projectgebaseerde contractregel configureren
description: Dit onderwerp bevat informatie over het toevoegen van niet-toerekenbare onderdelen aan contractregels in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858467"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="ea65d-103">Toerekenbare componenten van een projectgebaseerde contractregel configureren</span><span class="sxs-lookup"><span data-stu-id="ea65d-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="ea65d-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="ea65d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ea65d-105">Een projectgebaseerde contractregel heeft *opgenomen* onderdelen en *toerekenbare* onderdelen.</span><span class="sxs-lookup"><span data-stu-id="ea65d-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="ea65d-106">Opgenomen onderdelen zijn onderdelen waarop het volgende van toepassing is:</span><span class="sxs-lookup"><span data-stu-id="ea65d-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="ea65d-107">Factureringsmethode en klantsplitsingen</span><span class="sxs-lookup"><span data-stu-id="ea65d-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="ea65d-108">Niet-overschrijdingslimieten</span><span class="sxs-lookup"><span data-stu-id="ea65d-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="ea65d-109">Factuurfrequentie-instellingen die zijn gedefinieerd op de projectgebaseerde contractregel</span><span class="sxs-lookup"><span data-stu-id="ea65d-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="ea65d-110">Een subset van de opgenomen onderdelen kan worden gemarkeerd als toerekenbaar met het veld **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="ea65d-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="ea65d-111">Het veld **Factureringstype** is een optieset die de volgende waarden toestaat in de context van een contractregel:</span><span class="sxs-lookup"><span data-stu-id="ea65d-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="ea65d-112">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-112">Chargeable</span></span>
  - <span data-ttu-id="ea65d-113">Niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-113">Non-chargeable</span></span>

<span data-ttu-id="ea65d-114">Toerekenbare onderdelen kunnen worden gedefinieerd voor taken, rollen en transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="ea65d-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="ea65d-115">Toerekenbaarheid wordt gedefinieerd voor taken van een projectcontractregel en is van toepassing op alle transactieklassen die op de regel zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="ea65d-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="ea65d-116">Als het veld **Taken opnemen** op een contractregel leeg is of is ingesteld op **Geheel project**, is het tabblad **Toerekenbare taken** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="ea65d-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="ea65d-117">Toerekenbaarheid die is gedefinieerd voor rollen voor een projectcontractregel is alleen van toepassing op de transactieklasse **Tijd**.</span><span class="sxs-lookup"><span data-stu-id="ea65d-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="ea65d-118">Als het veld **Tijd opnemen** op een contractregel is ingesteld op **Nee**, is het tabblad **Toerekenbare rollen** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="ea65d-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="ea65d-119">Toerekenbaarheid die is gedefinieerd voor transactiecategorieën voor een projectcontractregel is alleen van toepassing op de transactieklasse **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="ea65d-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="ea65d-120">Als het veld **Onkosten opnemen** is ingesteld op **Nee**, is het tabblad **Toerekenbare categorieën** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="ea65d-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ea65d-121">Een projecttaak bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="ea65d-122">Een projecttaak kan op een specifieke contractregel toerekenbaar of niet-toerekenbaar zijn, waardoor de volgende instellingen mogelijk zijn:</span><span class="sxs-lookup"><span data-stu-id="ea65d-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="ea65d-123">Als een projectgebaseerde contractregel **Tijd** bevat en een bepaalde taak, **T1**, ermee is verbonden als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="ea65d-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="ea65d-124">Als er een tweede contractregel is die **Onkosten** bevat, kunt u de T1-taak op de contractregel als niet-toerekenbaar koppelen.</span><span class="sxs-lookup"><span data-stu-id="ea65d-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="ea65d-125">Het resultaat is dat alle tijd die voor de taak is geregistreerd, toerekenbaar is en dat alle onkosten niet-toerekenbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="ea65d-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="ea65d-126">Het factureringstype van een taak kan worden geconfigureerd op het tabblad **Toerekenbare taken** van de contractregel door het veld **Factureringstype** op het takensubraster van de contractregel bij te werken.</span><span class="sxs-lookup"><span data-stu-id="ea65d-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="ea65d-127">U kunt ook het veld **Factureringstype** op het subraster Factureringsinstellingen van de projecttaak bijwerken dat de contractregels toont die aan een taak zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ea65d-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ea65d-128">Een rol bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="ea65d-129">Een rol kan toerekenbaar of niet-toerekenbaar op een specifieke contractregel zijn.</span><span class="sxs-lookup"><span data-stu-id="ea65d-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="ea65d-130">Het factureringstype van een rol kan worden geconfigureerd op het tabblad **Toerekenbare rollen** van een contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="ea65d-131">Werk hiervoor het veld **Factureringstype** bij in het subraster **Toerekenbare rollen**.</span><span class="sxs-lookup"><span data-stu-id="ea65d-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ea65d-132">Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="ea65d-133">Een transactiecategorie kan toerekenbaar of niet-toerekenbaar zijn op een specifieke contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="ea65d-134">Het factureringstype van een transactiecategorie kan worden geconfigureerd op het tabblad **Toerekenbare categorieën** van een projectgebaseerde contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="ea65d-135">Werk hiervoor het veld **Factureringstype** bij in het subraster **Toerekenbare categorieën**.</span><span class="sxs-lookup"><span data-stu-id="ea65d-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="ea65d-136">Toerekenbaarheid oplossen</span><span class="sxs-lookup"><span data-stu-id="ea65d-136">Resolve chargeability</span></span>

<span data-ttu-id="ea65d-137">Een schatting of werkelijke waarde gemaakt voor tijd wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="ea65d-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="ea65d-138">**Tijd** is opgenomen op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="ea65d-139">**Rol** is geconfigureerd als toerekenbaar op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="ea65d-140">**Opgenomen taken** is ingesteld op **Geselecteerde taken** op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="ea65d-141">Als deze drie dingen van toepassing zijn, is de taak geconfigureerd als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="ea65d-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="ea65d-142">Een schatting of werkelijke waarde gemaakt voor onkosten wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="ea65d-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="ea65d-143">**Onkosten** is opgenomen op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="ea65d-144">**Transactiecategorie** is geconfigureerd als toerekenbaar op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="ea65d-145">**Opgenomen taken** is ingesteld op **Geselecteerde taak** op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="ea65d-146">Als deze drie dingen van toepassing zijn, is de **taak** geconfigureerd als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="ea65d-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="ea65d-147">Een schatting of werkelijke waarde gemaakt voor materiaal wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="ea65d-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="ea65d-148">**Materialen** is opgenomen op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="ea65d-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="ea65d-149">**Opgenomen taken** is ingesteld op **Geselecteerde taken** op de contractregel</span><span class="sxs-lookup"><span data-stu-id="ea65d-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="ea65d-150">Als deze twee dingen van toepassing zijn, is de **taak** geconfigureerd als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="ea65d-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea65d-151">
                    <strong>Bevat Tijd</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ea65d-152">
                    <strong>Bevat Onkosten</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ea65d-153">
                    <strong>Bevat materialen</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="ea65d-154">
                    <strong>Opgenomen taken</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-155">
                    <strong>- Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea65d-156">
                    <strong>Categorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-157">
                    <strong>Opdracht</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="ea65d-158">
                    <strong>Impact op toerekenbaarheid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-159">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-160">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-161">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-162">Geheel project</span><span class="sxs-lookup"><span data-stu-id="ea65d-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-163">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-164">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-165">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-166">Facturering voor een werkelijke waarde van tijd: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-167">Factureringstype voor een werkelijke waarde van onkosten: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-168">Factureringstype voor werkelijke materiaalwaarde: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-169">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-170">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-171">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-172">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="ea65d-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-173">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-174">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-175">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-176">Facturering voor een werkelijke waarde van tijd: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-177">Factureringstype voor een werkelijke waarde van onkosten: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-178">Factureringstype voor werkelijke materiaalwaarde: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-179">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-180">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-181">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-182">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="ea65d-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-183">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-184">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-185">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-186">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-187">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea65d-188">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-189">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-190">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-191">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-192">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="ea65d-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-193">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-194">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-195">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-196">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-197">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-198">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-199">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-200">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-201">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-202">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="ea65d-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-203">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-204">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-205">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-206">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-207">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-208">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-209">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-210">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-211">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-212">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="ea65d-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-213">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea65d-214">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-215">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-216">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-217">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-218">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea65d-219">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-220">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-221">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-222">Geheel project</span><span class="sxs-lookup"><span data-stu-id="ea65d-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-223">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea65d-224">
                    <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-225">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-226">Facturering voor een werkelijke waarde van tijd: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-227">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea65d-228">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea65d-229">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-230">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-231">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-232">Geheel project</span><span class="sxs-lookup"><span data-stu-id="ea65d-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-233">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea65d-234">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-235">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-236">Facturering voor een werkelijke waarde van tijd: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-237">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-238">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-239">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ea65d-240">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-241">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-242">Geheel project</span><span class="sxs-lookup"><span data-stu-id="ea65d-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-243">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-244">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-245">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-246">Facturering voor een werkelijke waarde van tijd: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea65d-247">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-248">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-249">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ea65d-250">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea65d-251">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-252">Geheel project</span><span class="sxs-lookup"><span data-stu-id="ea65d-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-253">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-254">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-255">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-256">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-257">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-258">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-259">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-260">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ea65d-261">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-262">Geheel project</span><span class="sxs-lookup"><span data-stu-id="ea65d-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-263">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-264">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-265">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-266">Facturering voor een werkelijke waarde van tijd: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea65d-267">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="ea65d-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea65d-268">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea65d-269">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea65d-270">Ja</span><span class="sxs-lookup"><span data-stu-id="ea65d-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ea65d-271">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea65d-272">Geheel project</span><span class="sxs-lookup"><span data-stu-id="ea65d-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea65d-273">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea65d-274">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea65d-275">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="ea65d-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea65d-276">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-277">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea65d-278">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea65d-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

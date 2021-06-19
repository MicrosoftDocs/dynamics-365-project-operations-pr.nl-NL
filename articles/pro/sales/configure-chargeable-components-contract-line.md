---
title: Toerekenbare componenten van een projectgebaseerde contractregel configureren
description: Dit onderwerp bevat informatie over het toevoegen van niet-toerekenbare onderdelen aan contractregels in Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003715"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="e9d7c-103">Toerekenbare componenten van een projectgebaseerde contractregel configureren</span><span class="sxs-lookup"><span data-stu-id="e9d7c-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="e9d7c-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="e9d7c-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e9d7c-105">Een projectgebaseerde contractregel heeft *opgenomen* onderdelen en *toerekenbare* onderdelen.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="e9d7c-106">Opgenomen onderdelen zijn onderdelen waarop het volgende van toepassing is:</span><span class="sxs-lookup"><span data-stu-id="e9d7c-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="e9d7c-107">Factureringsmethode en klantsplitsingen</span><span class="sxs-lookup"><span data-stu-id="e9d7c-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="e9d7c-108">Niet-overschrijdingslimieten</span><span class="sxs-lookup"><span data-stu-id="e9d7c-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="e9d7c-109">Factuurfrequentie-instellingen die zijn gedefinieerd op de projectgebaseerde contractregel</span><span class="sxs-lookup"><span data-stu-id="e9d7c-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="e9d7c-110">Een subset van de opgenomen onderdelen kan worden gemarkeerd als toerekenbaar met het veld **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="e9d7c-111">Het veld **Factureringstype** is een optieset die de volgende waarden toestaat in de context van een contractregel:</span><span class="sxs-lookup"><span data-stu-id="e9d7c-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="e9d7c-112">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-112">Chargeable</span></span>
  - <span data-ttu-id="e9d7c-113">Niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-113">Non-chargeable</span></span>

<span data-ttu-id="e9d7c-114">Toerekenbare onderdelen kunnen worden gedefinieerd voor taken, rollen en transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="e9d7c-115">Toerekenbaarheid wordt gedefinieerd voor taken van een projectcontractregel en is van toepassing op alle transactieklassen die op de regel zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="e9d7c-116">Als het veld **Taken opnemen** op een contractregel leeg is of is ingesteld op **Geheel project**, is het tabblad **Toerekenbare taken** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="e9d7c-117">Toerekenbaarheid die is gedefinieerd voor rollen voor een projectcontractregel is alleen van toepassing op de transactieklasse **Tijd**.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="e9d7c-118">Als het veld **Tijd opnemen** op een contractregel is ingesteld op **Nee**, is het tabblad **Toerekenbare rollen** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="e9d7c-119">Toerekenbaarheid die is gedefinieerd voor transactiecategorieën voor een projectcontractregel is alleen van toepassing op de transactieklasse **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="e9d7c-120">Als het veld **Onkosten opnemen** is ingesteld op **Nee**, is het tabblad **Toerekenbare categorieën** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="e9d7c-121">Een projecttaak bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="e9d7c-122">Een projecttaak kan op een specifieke contractregel toerekenbaar of niet-toerekenbaar zijn, waardoor de volgende instellingen mogelijk zijn:</span><span class="sxs-lookup"><span data-stu-id="e9d7c-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="e9d7c-123">Als een projectgebaseerde contractregel **Tijd** bevat en een bepaalde taak, **T1**, ermee is verbonden als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="e9d7c-124">Als er een tweede contractregel is die **Onkosten** bevat, kunt u de T1-taak op de contractregel als niet-toerekenbaar koppelen.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="e9d7c-125">Het resultaat is dat alle tijd die voor de taak is geregistreerd, toerekenbaar is en dat alle onkosten niet-toerekenbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="e9d7c-126">Het factureringstype van een taak kan worden geconfigureerd op het tabblad **Toerekenbare taken** van de contractregel door het veld **Factureringstype** op het takensubraster van de contractregel bij te werken.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="e9d7c-127">U kunt ook het veld **Factureringstype** op het subraster Factureringsinstellingen van de projecttaak bijwerken dat de contractregels toont die aan een taak zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="e9d7c-128">Een rol bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="e9d7c-129">Een rol kan toerekenbaar of niet-toerekenbaar op een specifieke contractregel zijn.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="e9d7c-130">Het factureringstype van een rol kan worden geconfigureerd op het tabblad **Toerekenbare rollen** van een contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="e9d7c-131">Werk hiervoor het veld **Factureringstype** bij in het subraster **Toerekenbare rollen**.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="e9d7c-132">Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="e9d7c-133">Een transactiecategorie kan toerekenbaar of niet-toerekenbaar zijn op een specifieke contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="e9d7c-134">Het factureringstype van een transactiecategorie kan worden geconfigureerd op het tabblad **Toerekenbare categorieën** van een projectgebaseerde contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="e9d7c-135">Werk hiervoor het veld **Factureringstype** bij in het subraster **Toerekenbare categorieën**.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="e9d7c-136">Toerekenbaarheid oplossen</span><span class="sxs-lookup"><span data-stu-id="e9d7c-136">Resolve chargeability</span></span>

<span data-ttu-id="e9d7c-137">Een schatting of werkelijke waarde gemaakt voor tijd wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="e9d7c-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="e9d7c-138">**Tijd** is opgenomen op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="e9d7c-139">**Rol** is geconfigureerd als toerekenbaar op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="e9d7c-140">**Opgenomen taken** is ingesteld op **Geselecteerde taken** op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="e9d7c-141">Als deze drie dingen van toepassing zijn, is de taak geconfigureerd als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="e9d7c-142">Een schatting of werkelijke waarde gemaakt voor onkosten wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="e9d7c-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="e9d7c-143">**Onkosten** is opgenomen op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="e9d7c-144">**Transactiecategorie** is geconfigureerd als toerekenbaar op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="e9d7c-145">**Opgenomen taken** is ingesteld op **Geselecteerde taak** op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="e9d7c-146">Als deze drie dingen van toepassing zijn, is de **taak** geconfigureerd als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="e9d7c-147">Een schatting of werkelijke waarde gemaakt voor materiaal wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="e9d7c-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="e9d7c-148">**Materialen** is opgenomen op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="e9d7c-149">**Opgenomen taken** is ingesteld op **Geselecteerde taken** op de contractregel</span><span class="sxs-lookup"><span data-stu-id="e9d7c-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="e9d7c-150">Als deze twee dingen van toepassing zijn, is de **taak** geconfigureerd als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e9d7c-151">
                    <strong>Bevat Tijd</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e9d7c-152">
                    <strong>Bevat Onkosten</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e9d7c-153">
                    <strong>Bevat materialen</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="e9d7c-154">
                    <strong>Opgenomen taken</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-155">
                    <strong>- Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e9d7c-156">
                    <strong>Categorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-157">
                    <strong>Opdracht</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="e9d7c-158">
                    <strong>Impact op toerekenbaarheid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-159">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-160">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-161">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-162">Geheel project</span><span class="sxs-lookup"><span data-stu-id="e9d7c-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-163">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-164">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-165">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-166">Facturering voor een werkelijke waarde van tijd: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-167">Factureringstype voor een werkelijke waarde van onkosten: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-168">Factureringstype voor werkelijke materiaalwaarde: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-169">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-170">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-171">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-172">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="e9d7c-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-173">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-174">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-175">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-176">Facturering voor een werkelijke waarde van tijd: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-177">Factureringstype voor een werkelijke waarde van onkosten: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-178">Factureringstype voor werkelijke materiaalwaarde: <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-179">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-180">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-181">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-182">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="e9d7c-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-183">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-184">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-185">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-186">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-187">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e9d7c-188">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-189">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-190">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-191">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-192">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="e9d7c-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-193">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-194">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-195">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-196">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-197">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-198">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-199">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-200">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-201">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-202">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="e9d7c-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-203">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-204">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-205">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-206">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-207">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-208">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-209">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-210">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-211">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-212">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="e9d7c-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-213">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e9d7c-214">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-215">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-216">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-217">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-218">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e9d7c-219">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-220">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-221">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-222">Geheel project</span><span class="sxs-lookup"><span data-stu-id="e9d7c-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-223">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e9d7c-224">
                    <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-225">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-226">Facturering voor een werkelijke waarde van tijd: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-227">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e9d7c-228">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e9d7c-229">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-230">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-231">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-232">Geheel project</span><span class="sxs-lookup"><span data-stu-id="e9d7c-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-233">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e9d7c-234">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-235">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-236">Facturering voor een werkelijke waarde van tijd: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-237">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-238">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-239">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e9d7c-240">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-241">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-242">Geheel project</span><span class="sxs-lookup"><span data-stu-id="e9d7c-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-243">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-244">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-245">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-246">Facturering voor een werkelijke waarde van tijd: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e9d7c-247">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-248">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-249">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e9d7c-250">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e9d7c-251">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-252">Geheel project</span><span class="sxs-lookup"><span data-stu-id="e9d7c-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-253">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-254">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-255">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-256">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-257">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-258">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-259">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-260">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e9d7c-261">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-262">Geheel project</span><span class="sxs-lookup"><span data-stu-id="e9d7c-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-263">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-264">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-265">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-266">Facturering voor een werkelijke waarde van tijd: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e9d7c-267">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="e9d7c-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e9d7c-268">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e9d7c-269">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e9d7c-270">Ja</span><span class="sxs-lookup"><span data-stu-id="e9d7c-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e9d7c-271">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e9d7c-272">Geheel project</span><span class="sxs-lookup"><span data-stu-id="e9d7c-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e9d7c-273">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e9d7c-274">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e9d7c-275">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="e9d7c-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e9d7c-276">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-277">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e9d7c-278">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e9d7c-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

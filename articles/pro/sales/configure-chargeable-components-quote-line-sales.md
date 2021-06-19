---
title: De toerekenbare onderdelen van een prijsopgaveregel configureren
description: Dit onderwerp bevat informatie over het instellen van toerekenbare en niet-toerekenbare onderdelen op een projectgebaseerde prijsopgaveregel.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003760"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="9f4a3-103">De toerekenbare componenten van een prijsopgaveregel configureren</span><span class="sxs-lookup"><span data-stu-id="9f4a3-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="9f4a3-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="9f4a3-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9f4a3-105">Een projectgebaseerde prijsopgaveregel heeft het concept van *opgenomen* onderdelen en *toerekenbare* onderdelen.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="9f4a3-106">Op opgenomen onderdelen is het volgende van toepassing:</span><span class="sxs-lookup"><span data-stu-id="9f4a3-106">Included components are subject to:</span></span>

  - <span data-ttu-id="9f4a3-107">Factureringsmethode en klantsplitsingen</span><span class="sxs-lookup"><span data-stu-id="9f4a3-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="9f4a3-108">Niet-overschrijdingslimieten</span><span class="sxs-lookup"><span data-stu-id="9f4a3-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="9f4a3-109">Factuurfrequentie-instellingen die zijn gedefinieerd op de projectgebaseerde prijsopgaveregel</span><span class="sxs-lookup"><span data-stu-id="9f4a3-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="9f4a3-110">Een subset van de opgenomen onderdelen kan worden gemarkeerd als toerekenbaar met het veld **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="9f4a3-111">Het veld **Factureringstype** is een optieset die de volgende waarden toestaat in de context van een prijsopgaveregel:</span><span class="sxs-lookup"><span data-stu-id="9f4a3-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="9f4a3-112">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-112">Chargeable</span></span>
  - <span data-ttu-id="9f4a3-113">Niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-113">Non-chargeable</span></span>

<span data-ttu-id="9f4a3-114">Toerekenbare onderdelen kunnen worden gedefinieerd voor taken, rollen en transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="9f4a3-115">Toerekenbaarheid wordt gedefinieerd voor de taken van een prijsopgaveregel en is van toepassing op alle transactieklassen die op die regel zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="9f4a3-116">Als het veld **Taken opnemen** is ingesteld op **Geheel project** of is leeg gelaten, is het tabblad **Toerekenbare taken** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="9f4a3-117">Toerekenbaarheid die is gedefinieerd voor rollen voor een prijsopgaveregel is alleen van toepassing op de transactieklasse **Tijd**.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="9f4a3-118">Als het veld **Tijd opnemen** is ingesteld op **Nee** op een prijsopgaveregel van een project, is het tabblad **Toerekenbare rollen** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="9f4a3-119">Toerekenbaarheid die is gedefinieerd voor transactiecategorieën voor een prijsopgaveregel is alleen van toepassing op de transactieklasse **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="9f4a3-120">Als het veld **Onkosten opnemen** is ingesteld op **Nee** op een prijsopgaveregel van een project, is het tabblad **Toerekenbare categorieën** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="9f4a3-121">Een projecttaak bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="9f4a3-122">Een projecttaak kan in de context van een projectgebaseerde prijsopgaveregel toerekenbaar of niet-toerekenbaar zijn, waardoor de volgende instellingen mogelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="9f4a3-123">Als een projectgebaseerde prijsopgaveregel **Tijd** en de taak **T1** bevat, wordt de taak als toerekenbaar aan de prijsopgaveregel gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="9f4a3-124">Als er een tweede prijsopgaveregel is die **Onkosten** bevat, kunt u de **T1**-taak op de prijsopgaveregel als niet-toerekenbaar koppelen.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="9f4a3-125">Het resultaat is dat alle tijd die voor de taak is geregistreerd, toerekenbaar is en dat alle onkosten die voor de taak zijn geregistreerd niet-toerekenbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="9f4a3-126">Het factureringstype van een taak kan worden geconfigureerd op het tabblad **Toerekenbare taken** van de projectgebaseerde prijsopgaveregel door het veld **Factureringstype** op het subraster **Taken van contractregel** bij te werken.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="9f4a3-127">U kunt ook het factureringstype voor een projecttaak bijwerken in het veld **Factureringstype** op het subraster Factureringsinstellingen van een project bijwerken dat de prijsopgaveregels toont die aan een taak zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="9f4a3-128">Een rol bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="9f4a3-129">Een rol kan toerekenbaar en niet-toerekenbaar zijn in de context van een specifieke projectgebaseerde prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="9f4a3-130">Het factureringstype van een rol kan worden geconfigureerd op het tabblad **Toerekenbare rollen** door het veld **Factureringstype** op het subraster **Toerekenbare rollen** bij te werken.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="9f4a3-131">Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="9f4a3-132">Een transactiecategorie kan toerekenbaar of niet-toerekenbaar zijn op een specifieke prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="9f4a3-133">Het factureringstype van een transactie kan worden geconfigureerd op het tabblad **Toerekenbare categorieën** door het veld **Factureringstype** op het subraster **Toerekenbare categorieën** bij te werken.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="9f4a3-134">Toerekenbaarheid oplossen</span><span class="sxs-lookup"><span data-stu-id="9f4a3-134">Resolve chargeability</span></span>
<span data-ttu-id="9f4a3-135">Een schatting of werkelijke waarde gemaakt voor de tijd wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="9f4a3-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="9f4a3-136">**Tijd** is opgenomen op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="9f4a3-137">**Rol** is geconfigureerd als toerekenbaar op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="9f4a3-138">**Opgenomen taken** is ingesteld op **Geselecteerde taken** op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="9f4a3-139">Als deze drie dingen van toepassing zijn, is de **taak** is ook geconfigureerd als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="9f4a3-140">Een schatting of werkelijke waarde gemaakt voor onkosten wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="9f4a3-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="9f4a3-141">**Onkosten** is opgenomen op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="9f4a3-142">**Transactiecategorie** is geconfigureerd als toerekenbaar op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="9f4a3-143">**Opgenomen taken** is ingesteld op **Geselecteerde taken** op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="9f4a3-144">Als deze drie dingen van toepassing zijn, is de **taak** is ook geconfigureerd als toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="9f4a3-145">Een schatting of werkelijke waarde gemaakt voor materiaal wordt alleen als toerekenbaar beschouwd als:</span><span class="sxs-lookup"><span data-stu-id="9f4a3-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="9f4a3-146">**Materialen** is opgenomen op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="9f4a3-147">**Opgenomen taken** is ingesteld op **Geselecteerde taken** op de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="9f4a3-148">Als deze twee dingen van toepassing zijn, moet de **taak** ook als toerekenbaar zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="9f4a3-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="9f4a3-149">
                    <strong>Bevat Tijd</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="9f4a3-150">
                    <strong>Bevat Onkosten</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="9f4a3-151">
                    <strong>Bevat materialen</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="9f4a3-152">
                    <strong>Opgenomen taken</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-153">
                    <strong>- Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="9f4a3-154">
                    <strong>Categorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-155">
                    <strong>Opdracht</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="9f4a3-156">
                    <strong>Impact op toerekenbaarheid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-157">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-158">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-159">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-160">Geheel project</span><span class="sxs-lookup"><span data-stu-id="9f4a3-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-161">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-162">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-163">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-164">Facturering voor een werkelijke waarde van tijd: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-165">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-166">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-167">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-168">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-169">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-170">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="9f4a3-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-171">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-172">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-173">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-174">Facturering voor een werkelijke waarde van tijd: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-175">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-176">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-177">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-178">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-179">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-180">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="9f4a3-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-181">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-182">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-183">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-184">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-185">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-186">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-187">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-188">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-189">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-190">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="9f4a3-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-191">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-192">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-193">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-194">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-195">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-196">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-197">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-198">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-199">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-200">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="9f4a3-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-201">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-202">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-203">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-204">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-205">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-206">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-207">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-208">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-209">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-210">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="9f4a3-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-211">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="9f4a3-212">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-213">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-214">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-215">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-216">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="9f4a3-217">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-218">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-219">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-220">Geheel project</span><span class="sxs-lookup"><span data-stu-id="9f4a3-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-221">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="9f4a3-222">
                    <strong>Toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-223">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-224">Facturering voor een werkelijke waarde van tijd: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-225">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-226">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="9f4a3-227">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-228">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-229">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-230">Geheel project</span><span class="sxs-lookup"><span data-stu-id="9f4a3-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-231">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="9f4a3-232">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-233">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-234">Facturering voor een werkelijke waarde van tijd: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-235">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-236">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-237">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="9f4a3-238">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-239">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-240">Geheel project</span><span class="sxs-lookup"><span data-stu-id="9f4a3-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-241">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-242">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-243">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-244">Facturering voor een werkelijke waarde van tijd: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-245">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-246">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-247">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="9f4a3-248">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="9f4a3-249">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-250">Geheel project</span><span class="sxs-lookup"><span data-stu-id="9f4a3-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-251">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-252">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-253">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-254">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-255">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-256">Factureringstype op werkelijke materiaalwaarde: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-257">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-258">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="9f4a3-259">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-260">Geheel project</span><span class="sxs-lookup"><span data-stu-id="9f4a3-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-261">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-262">Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-263">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-264">Facturering voor een werkelijke waarde van tijd: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-265">Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="9f4a3-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="9f4a3-266">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="9f4a3-267">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="9f4a3-268">Ja</span><span class="sxs-lookup"><span data-stu-id="9f4a3-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="9f4a3-269">
                    <strong>Geen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="9f4a3-270">Geheel project</span><span class="sxs-lookup"><span data-stu-id="9f4a3-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9f4a3-271">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="9f4a3-272">
                    <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9f4a3-273">Kan niet worden ingesteld</span><span class="sxs-lookup"><span data-stu-id="9f4a3-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="9f4a3-274">Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-275">Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="9f4a3-276">Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet beschikbaar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9f4a3-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

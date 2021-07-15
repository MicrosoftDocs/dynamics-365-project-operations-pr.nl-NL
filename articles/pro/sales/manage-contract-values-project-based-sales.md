---
title: Overzicht van projectgebaseerde contractregels
description: Dit onderwerp bevat informatie over het werken met projectgebaseerde contractregels.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369910"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="9e8fa-103">Overzicht van projectgebaseerde contractregels</span><span class="sxs-lookup"><span data-stu-id="9e8fa-103">Project-based contract lines overview</span></span>

<span data-ttu-id="9e8fa-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="9e8fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e8fa-105">Projectgebaseerde contractregels in Dynamics 365 Project Operations zijn ontworpen om de schattings- en factureringsovereenkomsten te bevatten voor specifieke onderdelen van projectwerk bij een opdracht.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="9e8fa-106">De structuur van een projectgebaseerde contractregel wordt voor projectschattingen en factureringsscenario's uitgebreid met de volgende concepten:</span><span class="sxs-lookup"><span data-stu-id="9e8fa-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="9e8fa-107">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="9e8fa-107">Billing method</span></span>
- <span data-ttu-id="9e8fa-108">Project- en taaktoewijzing</span><span class="sxs-lookup"><span data-stu-id="9e8fa-108">Project and task mapping</span></span>
- <span data-ttu-id="9e8fa-109">Inbegrepen transactieklassen</span><span class="sxs-lookup"><span data-stu-id="9e8fa-109">Included transaction classes</span></span>
- <span data-ttu-id="9e8fa-110">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="9e8fa-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="9e8fa-111">Instellingen voor toerekenbaarheid</span><span class="sxs-lookup"><span data-stu-id="9e8fa-111">Chargeability setup</span></span>
- <span data-ttu-id="9e8fa-112">Schattingen met behulp van contractregeldetails</span><span class="sxs-lookup"><span data-stu-id="9e8fa-112">Estimates using contract line details</span></span>
- <span data-ttu-id="9e8fa-113">Contractregelklanten</span><span class="sxs-lookup"><span data-stu-id="9e8fa-113">Contract line customers</span></span>

<span data-ttu-id="9e8fa-114">De volgende tabel bevat de velden op het tabblad **Algemeen** met projectgebaseerde contractregels die helpen bij het opzetten van de basis voor een gedetailleerde schatting en factureringsregelingen voor projectgebaseerd werk.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="9e8fa-115">Veld</span><span class="sxs-lookup"><span data-stu-id="9e8fa-115">Field</span></span> | <span data-ttu-id="9e8fa-116">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9e8fa-116">Description</span></span> | <span data-ttu-id="9e8fa-117">Downstreamimpact</span><span class="sxs-lookup"><span data-stu-id="9e8fa-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9e8fa-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-118">**Name**</span></span> | <span data-ttu-id="9e8fa-119">Naam van de contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-119">Name of the contract line.</span></span> <span data-ttu-id="9e8fa-120">Hiermee wordt de afzonderlijke component aangegeven van het contract waarvoor de schatting van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="9e8fa-121">Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van een overeenkomstige waarde van de projectgebaseerde offerteregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="9e8fa-122">De naam die is gekopieerd naar de projectfactuurregel die is gemaakt op basis van deze contractregel wanneer de factuur wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="9e8fa-123">**Factureringsmethode**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-123">**Billing Method**</span></span> | <span data-ttu-id="9e8fa-124">Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van het overeenkomstige waarde op de offerteregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="9e8fa-125">Dit is een optieset die de twee belangrijkste contractmodellen vertegenwoordigt die worden ondersteund door Project Operations:</span><span class="sxs-lookup"><span data-stu-id="9e8fa-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="9e8fa-126">- **Vaste prijs**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-126">- **Fixed Price**</span></span></br><span data-ttu-id="9e8fa-127">- **Tijd- en materiaalverbruik**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-127">- **Time and Material**</span></span> | <span data-ttu-id="9e8fa-128">Op basis van de factureringsmethode van de contractregel waarnaar wordt verwezen, wordt de daadwerkelijke transactie verwerkt.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="9e8fa-129">Als de contractregel waarnaar wordt verwezen door de werkelijke waarde een factureringsmethode voor tijd en materiaal heeft, worden records met de werkelijke waarden voor kosten en niet-gefactureerde verkoop gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="9e8fa-130">Als de contractregel waarnaar wordt verwezen door de werkelijke waarde een factureringsmethode tegen een vaste prijs heeft, wordt alleen een werkelijke waarde voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="9e8fa-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-131">**Project**</span></span> | <span data-ttu-id="9e8fa-132">Gebruik dit veld om het project aan te geven dat wordt gebruikt om het werk voor deze opdracht af te leveren.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="9e8fa-133">Deze waarde wordt gebruikt in combinatie met **Opgenomen taken** en **Opgenomen transactieklassen** om de contractregelverwijzing voor een werkelijke of schattingsregelrecord om te zetten.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="9e8fa-134">**Opgenomen taken**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-134">**Included Tasks**</span></span> | <span data-ttu-id="9e8fa-135">Geeft aan of deze contractregel alle projecttaken voor het geselecteerde project bevat of alleen een subset van de taken.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="9e8fa-136">Dit is een optieset met de volgende mogelijke waarden:</span><span class="sxs-lookup"><span data-stu-id="9e8fa-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="9e8fa-137">- **Alle projecttaken**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-137">- **All Project Tasks**</span></span></br><span data-ttu-id="9e8fa-138">- **Alleen geselecteerde projecttaken**.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="9e8fa-139">Een lege waarde in dit veld is gelijk aan het selecteren van **Alle projecttaken**.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="9e8fa-140">Als **Alleen geselecteerde taken** is geselecteerd, kunt u specifieke taken selecteren en deze koppelen aan deze contractregel op het tabblad **Factureringsinstellingen van taak** op de pagina **Project**.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="9e8fa-141">De waarde wordt gebruikt in combinatie met **Project** en **Opgenomen transactieklassen** om de contractregelreferentie op te lossen voor records met werkelijke waarden of schattingsregels.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9e8fa-142">**Tijd opnemen**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-142">**Include Time**</span></span> | <span data-ttu-id="9e8fa-143">Een waarde van **Ja**/**Nee** geeft aan of tijdtransacties of arbeidskosten voor het geselecteerde project worden opgenomen op deze contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="9e8fa-144">De waarde **Nee** geeft aan dat de tijdtransacties of arbeidskosten niet worden opgenomen in deze contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="9e8fa-145">De waarde **Ja** geeft aan dat dit wel het geval is.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="9e8fa-146">Deze waarde wordt gebruikt in combinatie met het project om de contractregelverwijzing om te zetten op een werkelijke of een geschatte regelrecord.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9e8fa-147">**Onkosten opnemen**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-147">**Include Expense**</span></span> | <span data-ttu-id="9e8fa-148">Een waarde van **Ja**/**Nee** geeft aan of onkosten voor het geselecteerde project worden opgenomen op deze contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="9e8fa-149">De waarde **Nee** geeft aan dat onkosten niet worden opgenomen in deze contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="9e8fa-150">De waarde **Ja** geeft aan dat dit wel het geval is.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="9e8fa-151">Deze waarde wordt gebruikt in combinatie met het project om de contractregelverwijzing om te zetten op een werkelijke of een geschatte regelrecord.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9e8fa-152">**Materialen opnemen**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-152">**Include Materials**</span></span> | <span data-ttu-id="9e8fa-153">Een waarde van **Ja**/**Nee** geeft aan of materiaalkosten voor het geselecteerde project worden opgenomen op deze contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="9e8fa-154">Een waarde van **Nee** geeft aan dat de materiaalkosten niet worden opgenomen op deze contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="9e8fa-155">De waarde **Ja** geeft aan dat dit wel het geval is.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="9e8fa-156">Deze waarde wordt gebruikt in combinatie met het project om de contractregelverwijzing om te zetten op een werkelijke of een geschatte regelrecord.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9e8fa-157">**Tarief opnemen**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-157">**Include Fee**</span></span> | <span data-ttu-id="9e8fa-158">Een waarde van **Ja**/**Nee** geeft aan of vergoedingen voor het geselecteerde project worden opgenomen op deze contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="9e8fa-159">De waarde **Nee** geeft aan dat vergoedingen niet worden opgenomen in deze contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="9e8fa-160">De waarde **Ja** geeft aan dat dit wel het geval is.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="9e8fa-161">Deze waarde wordt gebruikt in combinatie met het project om de contractregelverwijzing om te zetten op een werkelijke of een geschatte regelrecord.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9e8fa-162">**Bedrag van contract**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-162">**Contracted Amount**</span></span> | <span data-ttu-id="9e8fa-163">Op een contractregel met een vaste prijs is dit bedrag de overeengekomen waarde die aan de klant wordt gefactureerd voor alle werkcomponenten die aan deze contractregel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="9e8fa-164">Op een contractregel voor tijd en materiaal is dit bedrag een geschatte waarde waarde van wat aan de klant wordt gefactureerd voor alle werkcomponenten die aan deze contractregel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="9e8fa-165">Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van het overeenkomstige waarde op de offerteregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="9e8fa-166">Als een projectgebaseerde contractregel regeldetails heeft, is dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het bedrag in de contractregeldetails.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="9e8fa-167">Als de contractregel regeldetails heeft, kan deze waarde worden gewijzigd door de bedragen op de regeldetails te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="9e8fa-168">Op een contractregel met een vaste prijs wordt deze waarde gebruikt om het bedrag vóór belasting te genereren op periodieke factureringsmijlpalen.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="9e8fa-169">**Geschatte belasting**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-169">**Estimated Tax**</span></span> | <span data-ttu-id="9e8fa-170">De gebruiker kan dit veld bewerken om het geschatte belastingbedrag op de contractregel in te voeren.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="9e8fa-171">Als een projectgebaseerde contractregel regeldetails heeft, is dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het belastingbedrag in de contractregeldetails.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="9e8fa-172">Als de contractregel regeldetails heeft, kan deze waarde worden gewijzigd door de belastingbedragen op de regeldetails te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="9e8fa-173">Op een contractregel met een vaste prijs wordt deze waarde gebruikt om de belasting te genereren op periodieke factureringsmijlpalen.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="9e8fa-174">**Contractbedrag na belasting**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="9e8fa-175">Het contractregelbedrag na belasting.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-175">The contract line amount after tax.</span></span> <span data-ttu-id="9e8fa-176">Dit veld is alleen-lezen en wordt berekend als **Contractbedrag + belasting**.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="9e8fa-177">Op een contractregel met een vaste prijs wordt deze waarde gebruikt om periodieke factureringsmijlpalen te genereren.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="9e8fa-178">**Niet-overschrijdingslimiet**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="9e8fa-179">De gebruiker kan dit veld bewerken en het is alleen beschikbaar op projectgebaseerde contractregels waarvoor de factureringsmethode is ingesteld als tijd en materiaal.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="9e8fa-180">De gebruiker kan dit veld bewerken.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-180">The user can edit this field.</span></span> <span data-ttu-id="9e8fa-181">Wanneer een werkelijke waarde voor tijd en materiaal verwijst naar deze contractregel voor tijd en materiaal, wordt het bedrag van de werkelijke waarde geëvalueerd tegen de niet-overschrijdingslimiet op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="9e8fa-182">Deze evaluatie wordt voltooid nadat de reeds bestede en toegezegde bedragen zijn verantwoord.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="9e8fa-183">**Klantbudget**</span><span class="sxs-lookup"><span data-stu-id="9e8fa-183">**Customer Budget**</span></span> | <span data-ttu-id="9e8fa-184">Dit veld kan worden bewerkt en wordt gekopieerd van het overeenkomstige waarde op de offerteregel, als het contract is gecreëerd op basis van een offerte,.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="9e8fa-185">Dit veld wordt alleen ter informatie gebruikt en heeft geen invloed op volgende bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="9e8fa-186">Validatieregels voor de opties op het tabblad Algemeen van projectgebaseerde contractregels</span><span class="sxs-lookup"><span data-stu-id="9e8fa-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="9e8fa-187">Regel 1: Als het veld **Opgenomen taken** leeg is of is ingesteld op **Alle projecttaken**, worden alle taken van het project opgenomen op de contractregel.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="9e8fa-188">Regel 2: Als het veld **Opgenomen taken** leeg is of expliciet is ingesteld op **Alle projecttaken**, kunnen een project en een bepaalde transactieklasse slechts worden opgenomen in één projectgebaseerde contractregel van een contract.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="9e8fa-189">Regel 3: Als het veld **Opgenomen taken** is ingesteld op **Alleen geselecteerde projecttaken**, kunnen een project en een bepaalde transactieklasse worden opgenomen in meerdere projectgebaseerde contractregels van een contract.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="9e8fa-190">
                    <strong>Contract</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9e8fa-191">
                    <strong>Contractregel</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="9e8fa-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="9e8fa-193">
                    <strong>Opgenomen taken</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="9e8fa-194">
                    <strong>Tijd opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="9e8fa-195">
                    <strong>Onkosten opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="9e8fa-196">
                    <strong>Materialen opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="9e8fa-197">
                    <strong>Opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="9e8fa-198">
                    <strong>Tarief</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="9e8fa-199">
                    <strong>Geldig/ongeldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="9e8fa-200">
                    <strong>Reden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e8fa-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-201">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-202">CL1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-203">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-204">Leeg</span><span class="sxs-lookup"><span data-stu-id="9e8fa-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-205">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-206">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-207">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-208">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-209">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="9e8fa-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-210">Overtreding van regel 2.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-210">Violation of Rule #2.</span></span> <span data-ttu-id="9e8fa-211">Tijd, onkosten, materialen en vergoedingen voor het P1-project zijn opgenomen op de contractregels CL1 en CL2.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-212">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-213">CL2</span><span class="sxs-lookup"><span data-stu-id="9e8fa-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-214">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-215">Leeg</span><span class="sxs-lookup"><span data-stu-id="9e8fa-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-216">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-217">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-218">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-219">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-220">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-221">CL1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-222">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-223">Leeg</span><span class="sxs-lookup"><span data-stu-id="9e8fa-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-224">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-225">Geen</span><span class="sxs-lookup"><span data-stu-id="9e8fa-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-226">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-227">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-228">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="9e8fa-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-229">Overtreding van regel 2.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-229">Violation of Rule #2.</span></span> <span data-ttu-id="9e8fa-230">Tijd, materialen en vergoedingen voor het P1-project zijn opgenomen op de contractregels CL1 en CL2.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-231">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-232">CL2</span><span class="sxs-lookup"><span data-stu-id="9e8fa-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-233">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-234">Leeg</span><span class="sxs-lookup"><span data-stu-id="9e8fa-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-235">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-236">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-237">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-238">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-239">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-240">CL1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-241">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-242">Leeg</span><span class="sxs-lookup"><span data-stu-id="9e8fa-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-243">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-244">Geen</span><span class="sxs-lookup"><span data-stu-id="9e8fa-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-245">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-246">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-247">Geldig</span><span class="sxs-lookup"><span data-stu-id="9e8fa-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-248">Tijd, materialen en vergoedingen voor het P1-project zijn opgenomen in CL1.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="9e8fa-249">Onkosten voor het P1-project zijn opgenomen in CL2.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="9e8fa-250">Geen overlap in wat wordt opgenomen op elke contractregel en dus geldig.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-251">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-252">CL2</span><span class="sxs-lookup"><span data-stu-id="9e8fa-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-253">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-254">Leeg</span><span class="sxs-lookup"><span data-stu-id="9e8fa-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-255">Geen</span><span class="sxs-lookup"><span data-stu-id="9e8fa-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-256">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-257">Geen</span><span class="sxs-lookup"><span data-stu-id="9e8fa-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-258">Geen</span><span class="sxs-lookup"><span data-stu-id="9e8fa-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-259">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-260">CL1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-261">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-262">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="9e8fa-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-263">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-264">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-265">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-266">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-267">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="9e8fa-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-268">Overtreding van regel 2</span><span class="sxs-lookup"><span data-stu-id="9e8fa-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="9e8fa-269">C1 omvat tijd, materialen, onkosten en vergoedingen voor een subset van taken in project P1.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="9e8fa-270">CL2 omvat tijd, materialen, onkosten en vergoedingen voor het hele project P1 en overlapt daarom met wat is opgenomen in C1.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-271">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-272">CL2</span><span class="sxs-lookup"><span data-stu-id="9e8fa-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-273">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-274">Leeg</span><span class="sxs-lookup"><span data-stu-id="9e8fa-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-275">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-276">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-277">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-278">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-279">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-280">CL1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-281">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-282">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="9e8fa-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-283">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-284">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-285">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-286">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-287">Geldig</span><span class="sxs-lookup"><span data-stu-id="9e8fa-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e8fa-288">Volgens regel 3</span><span class="sxs-lookup"><span data-stu-id="9e8fa-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="9e8fa-289">C1 omvat tijd, onkosten, materialen en vergoedingen voor een subset van taken in project P1.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="9e8fa-290">CL2 omvat tijd, onkosten, materialen en vergoedingen voor een subset van taken in project P1.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="9e8fa-291">De enige aanvullende validatie betreft de subset van taken in CL1, die verschilt van de subset van taken in CL2 om ervoor te zorgen dat er geen overlapping is.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="9e8fa-292">Dit wordt gedaan door het systeem wanneer taken worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9e8fa-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9e8fa-293">C1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9e8fa-294">CL2</span><span class="sxs-lookup"><span data-stu-id="9e8fa-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-295">P1</span><span class="sxs-lookup"><span data-stu-id="9e8fa-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9e8fa-296">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="9e8fa-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-297">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9e8fa-298">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-299">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9e8fa-300">Ja</span><span class="sxs-lookup"><span data-stu-id="9e8fa-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Projectgebaseerde prijsopgaveregels (Pro)
description: Dit onderwerp bevat informatie over het gebruik van op projectgebaseerde prijsopgaveregels voor projectwerk. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074494"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="c873f-104">Projectgebaseerde prijsopgaveregels (Pro)</span><span class="sxs-lookup"><span data-stu-id="c873f-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="c873f-105">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="c873f-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c873f-106">Projectgebaseerde prijsopgaveregels zijn ontworpen om te helpen bij het inschatten van het projectwerk voor een opdracht.</span><span class="sxs-lookup"><span data-stu-id="c873f-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="c873f-107">De structuur van een projectgebaseerde prijsopgaveregel wordt voor projectramingen uitgebreid met de volgende concepten:</span><span class="sxs-lookup"><span data-stu-id="c873f-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="c873f-108">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="c873f-108">Billing Method</span></span>
- <span data-ttu-id="c873f-109">Project- en taaktoewijzing</span><span class="sxs-lookup"><span data-stu-id="c873f-109">Project and Task Mapping</span></span>
- <span data-ttu-id="c873f-110">Inbegrepen transactieklassen</span><span class="sxs-lookup"><span data-stu-id="c873f-110">Included Transaction classes</span></span>
- <span data-ttu-id="c873f-111">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="c873f-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="c873f-112">Instellingen voor toerekenbaarheid</span><span class="sxs-lookup"><span data-stu-id="c873f-112">Chargeability setup</span></span>
- <span data-ttu-id="c873f-113">Schatting met gegevens van prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="c873f-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="c873f-114">Prijsopgaveregelklanten</span><span class="sxs-lookup"><span data-stu-id="c873f-114">Quote line Customers</span></span>

<span data-ttu-id="c873f-115">De volgende tabel bevat informatie over de velden op het tabblad **Algemeen** van projectgebaseerde prijsopgaveregels.</span><span class="sxs-lookup"><span data-stu-id="c873f-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="c873f-116">Deze velden helpen bij het opzetten van de basis voor een gedetailleerde, complete schatting voor projectwerk.</span><span class="sxs-lookup"><span data-stu-id="c873f-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="c873f-117">**Veld**</span><span class="sxs-lookup"><span data-stu-id="c873f-117">**Field**</span></span> | <span data-ttu-id="c873f-118">**Relevantie, doel en richtlijnen**</span><span class="sxs-lookup"><span data-stu-id="c873f-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="c873f-119">**Downstreamimpact**</span><span class="sxs-lookup"><span data-stu-id="c873f-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c873f-120">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="c873f-120">Name</span></span> | <span data-ttu-id="c873f-121">De naam van de prijsopgaveregel waarmee u de afzonderlijke component van de prijsopgave in de raming kunt identificeren.</span><span class="sxs-lookup"><span data-stu-id="c873f-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="c873f-122">Gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-123">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="c873f-123">Billing Method</span></span> | <span data-ttu-id="c873f-124">In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het overeenkomstige veld op de verkoopkansregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="c873f-125">Dit veld bevat de twee belangrijkste contractmodellen die worden ondersteund door Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="c873f-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="c873f-126">- Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="c873f-126">- Fixed price</span></span></br><span data-ttu-id="c873f-127">- Tijd en materiaal.</span><span class="sxs-lookup"><span data-stu-id="c873f-127">- Time and material.</span></span>| <span data-ttu-id="c873f-128">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-129">Project</span><span class="sxs-lookup"><span data-stu-id="c873f-129">Project</span></span> | <span data-ttu-id="c873f-130">Gebruik dit optionele veld om het project te identificeren dat wordt gebruikt om het werk voor deze opdracht af te leveren.</span><span class="sxs-lookup"><span data-stu-id="c873f-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="c873f-131">Wanneer een project wordt toegewezen aan een prijsopgaveregel, is dit handig bij het instellen van toerekenbare taken en ook bij het opnemen van een projectgebaseerde schatting op de prijsopgaveregel als details van de prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="c873f-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="c873f-132">Als een project niet wordt toegewezen aan een projectgebaseerde prijsopgaveregel, moet de schatting handmatig worden gemaakt door elk detail van de prijsopgave te creëren.</span><span class="sxs-lookup"><span data-stu-id="c873f-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="c873f-133">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="c873f-134">Opgenomen taken</span><span class="sxs-lookup"><span data-stu-id="c873f-134">Included Tasks</span></span> | <span data-ttu-id="c873f-135">Geeft aan of deze prijsopgaveregel wordt gebruikt voor alle of enkele projecttaken voor het geselecteerde project.</span><span class="sxs-lookup"><span data-stu-id="c873f-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="c873f-136">Dit veld kan de volgende waarden hebben:</span><span class="sxs-lookup"><span data-stu-id="c873f-136">This field has the following possible values:</span></span></br><span data-ttu-id="c873f-137">- Alle projecttaken</span><span class="sxs-lookup"><span data-stu-id="c873f-137">- All project tasks</span></span></br><span data-ttu-id="c873f-138">- Alleen geselecteerde projecttaken</span><span class="sxs-lookup"><span data-stu-id="c873f-138">- Selected project tasks only</span></span></br><span data-ttu-id="c873f-139">Een lege waarde in dit veld is gelijk aan de optie **Alle projecttaken**.</span><span class="sxs-lookup"><span data-stu-id="c873f-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="c873f-140">Wanneer **Alleen geselecteerde projecttaken** wordt geselecteerd, kunt u vervolgens op de projectpagina in het tabblad **Taakfacturering instellen** specifieke taken selecteren en deze aan de prijsopgaveregel koppelen.</span><span class="sxs-lookup"><span data-stu-id="c873f-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="c873f-141">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-142">Tijd opnemen</span><span class="sxs-lookup"><span data-stu-id="c873f-142">Include Time</span></span> | <span data-ttu-id="c873f-143">Een markering **Ja**/**Nee** geeft aan of tijdtransacties of arbeidskosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c873f-144">Een waarde **Nee** geeft aan of de tijdtransacties of arbeidskosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c873f-145">Een waarde **Ja** geeft aan of de tijdtransacties of arbeidskosten worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c873f-146">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-147">Onkosten opnemen</span><span class="sxs-lookup"><span data-stu-id="c873f-147">Include Expense</span></span> | <span data-ttu-id="c873f-148">Een markering **Ja**/**Nee** geeft aan of onkosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c873f-149">Een waarde **Nee** geeft aan of de onkosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c873f-150">Een waarde **Ja** geeft aan of de onkosten worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c873f-151">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-152">Tarief opnemen</span><span class="sxs-lookup"><span data-stu-id="c873f-152">Include Fee</span></span> | <span data-ttu-id="c873f-153">Een markering **Ja**/**Nee** geeft aan of vergoedingen voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c873f-154">Een waarde **Nee** geeft aan of de vergoedingen niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c873f-155">Een waarde **Ja** geeft aan of de vergoedingen niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c873f-156">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-157">Bedrag van prijsopgave</span><span class="sxs-lookup"><span data-stu-id="c873f-157">Quoted Amount</span></span> | <span data-ttu-id="c873f-158">Dit is het bedrag dat aan de klant wordt geoffreerd voor al het werk dat op deze projectgebaseerde offerteregel wordt voorspeld.</span><span class="sxs-lookup"><span data-stu-id="c873f-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="c873f-159">In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het veld **Klantbudget** op de verkoopkansregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="c873f-160">Wanneer de projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het bedrag in de prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="c873f-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="c873f-161">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-162">Geschatte belasting</span><span class="sxs-lookup"><span data-stu-id="c873f-162">Estimated Tax</span></span> | <span data-ttu-id="c873f-163">Dit is een bewerkbaar veld voor de gebruiker om het geschatte belastingbedrag op de prijsopgaveregel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c873f-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="c873f-164">Wanneer een projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het belastingbedrag in de prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="c873f-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="c873f-165">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-166">Bedrag van prijsopgave na belasting</span><span class="sxs-lookup"><span data-stu-id="c873f-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="c873f-167">Dit veld is het prijsopgaveregelbedrag na belasting en is alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="c873f-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="c873f-168">Het bedrag in dit veld wordt berekend als *Geoffreerd bedrag + belasting*.</span><span class="sxs-lookup"><span data-stu-id="c873f-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="c873f-169">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-170">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="c873f-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="c873f-171">Dit veld kan worden bewerkt en is alleen beschikbaar op projectgebaseerde prijsopgaveregels met de factureringsmethode **Tijd en materiaal**.</span><span class="sxs-lookup"><span data-stu-id="c873f-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="c873f-172">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c873f-173">Klantbudget</span><span class="sxs-lookup"><span data-stu-id="c873f-173">Customer Budget</span></span> | <span data-ttu-id="c873f-174">Dit veld is bewerkbaar en wordt gekopieerd uit het overeenkomstige veld op de verkoopkansregel als de prijsopgave wordt gemaakt op basis van een verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="c873f-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="c873f-175">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c873f-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="c873f-176">Validatieregels voor velden op het tabblad Algemeen van projectgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="c873f-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="c873f-177">**Regel 1** : als het veld **Inbegrepen taken** leeg is, of als het is ingesteld op **Alle projecttaken** , wordt een project opgenomen in de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c873f-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="c873f-178">**Regel 2** : als het veld **Inbegrepen taken** leeg is, of als het is ingesteld op **Alle projecttaken** kunnen een project en een bepaalde transactieklasse alleen worden opgenomen in één projectgebaseerde prijsopgaveregel van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="c873f-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="c873f-179">**Regel 3** : als het veld **Inbegrepen taken** is ingesteld op **Alleen geselecteerde projecttaken** kunnen een project en een bepaalde transactieklasse worden opgenomen in meerdere projectgebaseerde prijsopgaveregels van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="c873f-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="c873f-180">**Regel 4** : als een verkoopkans meerdere prijsopgaven bevat, kunnen er regels van verschillende prijsopgaven zijn die allemaal naar hetzelfde project verwijzen en dezelfde transactieklasse bevatten.</span><span class="sxs-lookup"><span data-stu-id="c873f-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="c873f-181">**Regel 5** : als de prijsopgaven niet tot dezelfde verkoopkans behoren, kunnen ze niet hetzelfde project en dezelfde transactieklasse bevatten.</span><span class="sxs-lookup"><span data-stu-id="c873f-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="c873f-182">
                    <strong>Verkoopkans</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c873f-183">
                    <strong>Offerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c873f-184">
                    <strong>Prijsopgaveregel</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c873f-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="c873f-186">
                    <strong>Opgenomen taken</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c873f-187">
                    <strong>Tijd opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c873f-188">
                    <strong>Onkosten opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c873f-189">
                    <strong>Opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="c873f-190">
                    <strong>Tarief</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="c873f-191">
                    <strong>Geldig/ongeldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="c873f-192">
                    <strong>Reden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c873f-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-193">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-194">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-195">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-196">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-197">Leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-198">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-199">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-200">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-201">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="c873f-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-202">Overtreding van regel 2.</span><span class="sxs-lookup"><span data-stu-id="c873f-202">Violation of Rule #2.</span></span> <span data-ttu-id="c873f-203">Tijd, onkosten en vergoedingen voor het P1-project zijn opgenomen op de prijsopgaveregels QL1 en QL2.</span><span class="sxs-lookup"><span data-stu-id="c873f-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-204">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-205">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-206">QL2</span><span class="sxs-lookup"><span data-stu-id="c873f-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-207">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-208">Leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-209">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-210">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-211">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-212">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-213">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-214">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-215">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-216">Leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-217">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-218">No</span><span class="sxs-lookup"><span data-stu-id="c873f-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-219">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-220">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="c873f-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-221">Overtreding van regel 2.</span><span class="sxs-lookup"><span data-stu-id="c873f-221">Violation of Rule #2.</span></span> <span data-ttu-id="c873f-222">Tijd en vergoedingen voor het P1-project zijn opgenomen op de prijsopgaveregels QL1 en QL2.</span><span class="sxs-lookup"><span data-stu-id="c873f-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-223">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-224">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-225">QL2</span><span class="sxs-lookup"><span data-stu-id="c873f-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-226">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-227">Leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-228">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-229">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-230">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-231">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-232">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-233">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-234">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-235">Leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-236">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-237">No</span><span class="sxs-lookup"><span data-stu-id="c873f-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-238">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-239">Geldig</span><span class="sxs-lookup"><span data-stu-id="c873f-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="c873f-240">Tijd en vergoedingen voor het P1-project zijn opgenomen in QL1.</span><span class="sxs-lookup"><span data-stu-id="c873f-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="c873f-241">Onkosten voor het P1-project zijn opgenomen in QL2.</span><span class="sxs-lookup"><span data-stu-id="c873f-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="c873f-242">Er is geen overlap in wat op elke prijsopgaveregel wordt opgenomen en dus geldig.</span><span class="sxs-lookup"><span data-stu-id="c873f-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-243">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-244">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-245">QL2</span><span class="sxs-lookup"><span data-stu-id="c873f-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-246">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-247">Leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-248">No</span><span class="sxs-lookup"><span data-stu-id="c873f-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-249">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-250">No</span><span class="sxs-lookup"><span data-stu-id="c873f-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-251">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-252">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-253">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-254">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-255">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="c873f-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-256">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-257">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-258">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-259">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="c873f-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-260">Overtreding van regel 2 hierboven</span><span class="sxs-lookup"><span data-stu-id="c873f-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="c873f-261">Q1 omvat tijd, onkosten en vergoedingen voor een subset van taken in project P1.</span><span class="sxs-lookup"><span data-stu-id="c873f-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c873f-262">QL2 omvat tijd, onkosten en vergoedingen voor het hele project P1 en overlapt met wat is inbegrepen in Q1.</span><span class="sxs-lookup"><span data-stu-id="c873f-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-263">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-264">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-265">QL2</span><span class="sxs-lookup"><span data-stu-id="c873f-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-266">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-267">Leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-268">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-269">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-270">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-271">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-272">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-273">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-274">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-275">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="c873f-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-276">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-277">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-278">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-279">Geldig</span><span class="sxs-lookup"><span data-stu-id="c873f-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-280">Volgens regel 3 hierboven,</span><span class="sxs-lookup"><span data-stu-id="c873f-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="c873f-281">Q1 omvat tijd, onkosten en vergoedingen voor een subset van taken in project P1.</span><span class="sxs-lookup"><span data-stu-id="c873f-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c873f-282">QL2 omvat tijd, onkosten en vergoedingen voor een subset van taken in project P1.</span><span class="sxs-lookup"><span data-stu-id="c873f-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c873f-283">De enige aanvullende validatie betreft de subset met taken op QL1 die verschillen van de subset met taken op QL2.</span><span class="sxs-lookup"><span data-stu-id="c873f-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="c873f-284">Dit zorgt ervoor dat er geen overlappingen zijn.</span><span class="sxs-lookup"><span data-stu-id="c873f-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="c873f-285">Dit wordt gedaan door het systeem wanneer taken worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c873f-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-286">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-287">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-288">QL2</span><span class="sxs-lookup"><span data-stu-id="c873f-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-289">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-290">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="c873f-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-291">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-292">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-293">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-294">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-295">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-296">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-297">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-298">Alle projecttaken of leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-299">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-300">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-301">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c873f-302">Geldig</span><span class="sxs-lookup"><span data-stu-id="c873f-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-303">Op basis van regel 5 zijn Q1 en Q2 twee prijsopgaven voor dezelfde verkoopkans, dus ze kunnen beide een schatting geven voor dezelfde componenten van een project.</span><span class="sxs-lookup"><span data-stu-id="c873f-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-304">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-305">KW2</span><span class="sxs-lookup"><span data-stu-id="c873f-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-306">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-307">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-308">Alle projecttaken of leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-309">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-310">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-311">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-312">O1</span><span class="sxs-lookup"><span data-stu-id="c873f-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-313">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-314">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-315">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-316">Alle projecttaken of leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-317">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-318">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-319">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c873f-320">Geldig</span><span class="sxs-lookup"><span data-stu-id="c873f-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c873f-321">Op basis van regel 4 zijn Q1 en Q2 twee prijsopgaven voor verschillende verkoopkansen, dus ze kunnen niet een schatting geven voor dezelfde componenten van hetzelfde project.</span><span class="sxs-lookup"><span data-stu-id="c873f-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c873f-322">O2</span><span class="sxs-lookup"><span data-stu-id="c873f-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c873f-323">KW1</span><span class="sxs-lookup"><span data-stu-id="c873f-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-324">QL1</span><span class="sxs-lookup"><span data-stu-id="c873f-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-325">P1</span><span class="sxs-lookup"><span data-stu-id="c873f-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c873f-326">Alle projecttaken of leeg</span><span class="sxs-lookup"><span data-stu-id="c873f-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-327">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c873f-328">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c873f-329">Ja</span><span class="sxs-lookup"><span data-stu-id="c873f-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c873f-330">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="c873f-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


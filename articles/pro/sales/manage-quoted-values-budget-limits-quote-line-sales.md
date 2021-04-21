---
title: Overzicht van projectgebaseerde prijsopgaveregels
description: Dit onderwerp bevat informatie over het gebruik van op projectgebaseerde prijsopgaveregels voor projectwerk.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858692"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="c7515-103">Overzicht van projectgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="c7515-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="c7515-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="c7515-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c7515-105">Projectgebaseerde prijsopgaveregels zijn ontworpen om te helpen bij het inschatten van het projectwerk voor een opdracht.</span><span class="sxs-lookup"><span data-stu-id="c7515-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="c7515-106">De structuur van een projectgebaseerde prijsopgaveregel wordt voor projectramingen uitgebreid met de volgende concepten:</span><span class="sxs-lookup"><span data-stu-id="c7515-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="c7515-107">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="c7515-107">Billing Method</span></span>
- <span data-ttu-id="c7515-108">Project- en taaktoewijzing</span><span class="sxs-lookup"><span data-stu-id="c7515-108">Project and Task Mapping</span></span>
- <span data-ttu-id="c7515-109">Inbegrepen transactieklassen</span><span class="sxs-lookup"><span data-stu-id="c7515-109">Included Transaction classes</span></span>
- <span data-ttu-id="c7515-110">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="c7515-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="c7515-111">Instellingen voor toerekenbaarheid</span><span class="sxs-lookup"><span data-stu-id="c7515-111">Chargeability setup</span></span>
- <span data-ttu-id="c7515-112">Schatting met gegevens van prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="c7515-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="c7515-113">Prijsopgaveregelklanten</span><span class="sxs-lookup"><span data-stu-id="c7515-113">Quote line Customers</span></span>

<span data-ttu-id="c7515-114">De volgende tabel bevat informatie over de velden op het tabblad **Algemeen** van projectgebaseerde prijsopgaveregels.</span><span class="sxs-lookup"><span data-stu-id="c7515-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="c7515-115">Deze velden helpen bij het opzetten van de basis voor een gedetailleerde, complete schatting voor projectwerk.</span><span class="sxs-lookup"><span data-stu-id="c7515-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="c7515-116">**Veld**</span><span class="sxs-lookup"><span data-stu-id="c7515-116">**Field**</span></span> | <span data-ttu-id="c7515-117">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="c7515-117">**Description**</span></span> | <span data-ttu-id="c7515-118">**Downstreamimpact**</span><span class="sxs-lookup"><span data-stu-id="c7515-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c7515-119">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="c7515-119">Name</span></span> | <span data-ttu-id="c7515-120">De naam van de prijsopgaveregel waarmee u de discrete component kunt identificeren van de prijsopgave die wordt geschat.</span><span class="sxs-lookup"><span data-stu-id="c7515-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="c7515-121">Gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="c7515-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-122">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="c7515-122">Billing Method</span></span> | <span data-ttu-id="c7515-123">In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het overeenkomstige veld op de verkoopkansregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="c7515-124">Dit veld bevat de twee belangrijkste aanbestedingsmodellen die worden ondersteund door Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c7515-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="c7515-125">- Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="c7515-125">- Fixed price</span></span></br><span data-ttu-id="c7515-126">- Tijd en materiaal.</span><span class="sxs-lookup"><span data-stu-id="c7515-126">- Time and material.</span></span>| <span data-ttu-id="c7515-127">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-128">Project</span><span class="sxs-lookup"><span data-stu-id="c7515-128">Project</span></span> | <span data-ttu-id="c7515-129">Gebruik dit optionele veld om het project te identificeren dat wordt gebruikt om het werk voor deze opdracht af te leveren.</span><span class="sxs-lookup"><span data-stu-id="c7515-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="c7515-130">Wanneer een project wordt toegewezen aan een prijsopgaveregel, is dit handig bij het instellen van toerekenbare taken en ook bij het opnemen van een projectgebaseerde schatting op de prijsopgaveregel als details van de prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="c7515-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="c7515-131">Als een project niet wordt toegewezen aan een projectgebaseerde prijsopgaveregel, moet de schatting handmatig worden gemaakt door elk detail van de prijsopgave te creëren.</span><span class="sxs-lookup"><span data-stu-id="c7515-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="c7515-132">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="c7515-133">Opgenomen taken</span><span class="sxs-lookup"><span data-stu-id="c7515-133">Included Tasks</span></span> | <span data-ttu-id="c7515-134">Geeft aan of deze prijsopgaveregel wordt gebruikt voor alle of enkele projecttaken voor het geselecteerde project.</span><span class="sxs-lookup"><span data-stu-id="c7515-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="c7515-135">Dit veld kan de volgende waarden hebben:</span><span class="sxs-lookup"><span data-stu-id="c7515-135">This field has the following possible values:</span></span></br><span data-ttu-id="c7515-136">- Alle projecttaken</span><span class="sxs-lookup"><span data-stu-id="c7515-136">- All project tasks</span></span></br><span data-ttu-id="c7515-137">- Alleen geselecteerde projecttaken</span><span class="sxs-lookup"><span data-stu-id="c7515-137">- Selected project tasks only</span></span></br><span data-ttu-id="c7515-138">Een lege waarde in dit veld is gelijk aan de optie **Alle projecttaken**.</span><span class="sxs-lookup"><span data-stu-id="c7515-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="c7515-139">Wanneer **Alleen geselecteerde projecttaken** wordt geselecteerd op de projectpagina, kunt u op het tabblad **Factureringsinstellingen van taak** specifieke taken selecteren om ze aan deze prijsopgaveregel te koppelen.</span><span class="sxs-lookup"><span data-stu-id="c7515-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="c7515-140">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-141">Tijd opnemen</span><span class="sxs-lookup"><span data-stu-id="c7515-141">Include Time</span></span> | <span data-ttu-id="c7515-142">Een waarde van **Ja**/**Nee** geeft aan of tijdtransacties of arbeidskosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c7515-143">Een waarde **Nee** geeft aan of de tijdtransacties of arbeidskosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c7515-144">Een waarde **Ja** geeft aan of de tijdtransacties of arbeidskosten worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c7515-145">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-146">Onkosten opnemen</span><span class="sxs-lookup"><span data-stu-id="c7515-146">Include Expense</span></span> | <span data-ttu-id="c7515-147">Een waarde van **Ja**/**Nee** geeft aan of onkosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c7515-148">Een waarde **Nee** geeft aan of de onkosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c7515-149">Een waarde **Ja** geeft aan of de onkosten worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c7515-150">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-151">Materiaal opnemen</span><span class="sxs-lookup"><span data-stu-id="c7515-151">Include Material</span></span> | <span data-ttu-id="c7515-152">Een waarde van **Ja**/**Nee** geeft aan of materiaalkosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c7515-153">Een waarde van **Nee** geeft aan dat de materiaalkosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c7515-154">Een waarde van **Ja** geeft aan dat de materiaalkosten wel worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c7515-155">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-156">Tarief opnemen</span><span class="sxs-lookup"><span data-stu-id="c7515-156">Include Fee</span></span> | <span data-ttu-id="c7515-157">Een waarde van **Ja**/**Nee** geeft aan of vergoedingen voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c7515-158">Een waarde van **Nee** geeft aan dat de vergoedingen niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c7515-159">Een waarde van **Ja** geeft aan dat de vergoedingen wel worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c7515-160">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-161">Bedrag van prijsopgave</span><span class="sxs-lookup"><span data-stu-id="c7515-161">Quoted Amount</span></span> | <span data-ttu-id="c7515-162">Dit is het bedrag dat aan de klant in het vooruitzicht wordt gesteld voor al het werk dat op deze projectgebaseerde offerteregel wordt voorspeld.</span><span class="sxs-lookup"><span data-stu-id="c7515-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="c7515-163">In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het veld **Klantbudget** op de verkoopkansregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="c7515-164">Wanneer de projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het bedrag in de prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="c7515-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="c7515-165">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-166">Geschatte belasting</span><span class="sxs-lookup"><span data-stu-id="c7515-166">Estimated Tax</span></span> | <span data-ttu-id="c7515-167">Dit is een bewerkbaar veld voor de gebruiker om het geschatte belastingbedrag op de prijsopgaveregel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c7515-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="c7515-168">Wanneer een projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het belastingbedrag in de prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="c7515-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="c7515-169">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-170">Bedrag van prijsopgave na belasting</span><span class="sxs-lookup"><span data-stu-id="c7515-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="c7515-171">Dit veld is het prijsopgaveregelbedrag na belasting en is alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="c7515-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="c7515-172">Het bedrag in dit veld wordt berekend als *Geoffreerd bedrag + belasting*.</span><span class="sxs-lookup"><span data-stu-id="c7515-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="c7515-173">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-174">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="c7515-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="c7515-175">Dit veld kan worden bewerkt en is alleen beschikbaar op projectgebaseerde prijsopgaveregels met de factureringsmethode **Tijd en materiaal**.</span><span class="sxs-lookup"><span data-stu-id="c7515-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="c7515-176">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c7515-177">Klantbudget</span><span class="sxs-lookup"><span data-stu-id="c7515-177">Customer Budget</span></span> | <span data-ttu-id="c7515-178">Dit veld is bewerkbaar en wordt gekopieerd uit het overeenkomstige veld op de verkoopkansregel als de prijsopgave wordt gemaakt op basis van een verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="c7515-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="c7515-179">Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="c7515-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="c7515-180">Validatieregels voor velden op het tabblad Algemeen van projectgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="c7515-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="c7515-181">**Regel 1**: als het veld **Inbegrepen taken** leeg is, of als het is ingesteld op **Alle projecttaken**, wordt een project opgenomen in de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="c7515-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="c7515-182">**Regel 2**: als het veld **Inbegrepen taken** leeg is, of als het is ingesteld op **Alle projecttaken** kunnen een project en een bepaalde transactieklasse alleen worden opgenomen in één projectgebaseerde prijsopgaveregel van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="c7515-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="c7515-183">**Regel 3**: als het veld **Inbegrepen taken** is ingesteld op **Alleen geselecteerde projecttaken** kunnen een project en een bepaalde transactieklasse worden opgenomen in meerdere projectgebaseerde prijsopgaveregels van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="c7515-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="c7515-184">**Regel 4**: als een verkoopkans meerdere prijsopgaven bevat, kunnen er regels van verschillende prijsopgaven zijn die allemaal naar hetzelfde project verwijzen en dezelfde transactieklasse bevatten.</span><span class="sxs-lookup"><span data-stu-id="c7515-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="c7515-185">**Regel 5**: als de prijsopgaven niet tot dezelfde verkoopkans behoren, kunnen ze niet hetzelfde project en dezelfde transactieklasse bevatten.</span><span class="sxs-lookup"><span data-stu-id="c7515-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="c7515-186">
                    <strong>Verkoopkans</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="c7515-187">
                    <strong>Offerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="c7515-188">
                    <strong>Prijsopgaveregel</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c7515-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="c7515-190">
                    <strong>Opgenomen taken</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="c7515-191">
                    <strong>Tijd opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="c7515-192">
                    <strong>Onkosten opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="c7515-193">
                    <strong>Materiaal opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c7515-194">
                    <strong>Opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="c7515-195">
                    <strong>Tarief</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="c7515-196">
                    <strong>Geldig/ongeldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="c7515-197">
                    <strong>Reden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7515-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-198">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-199">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-200">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-201">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-202">Leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-203">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-204">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-205">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-206">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-207">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="c7515-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-208">Overtreding van regel 2.</span><span class="sxs-lookup"><span data-stu-id="c7515-208">Violation of Rule #2.</span></span> <span data-ttu-id="c7515-209">Tijd, onkosten en vergoedingen voor het P1-project zijn opgenomen op de prijsopgaveregels QL1 en QL2</span><span class="sxs-lookup"><span data-stu-id="c7515-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-210">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-211">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-212">QL2</span><span class="sxs-lookup"><span data-stu-id="c7515-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-213">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-214">Leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-215">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-216">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-217">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-218">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-219">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-220">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-221">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-222">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-223">Leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-224">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-225">Geen</span><span class="sxs-lookup"><span data-stu-id="c7515-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-226">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-227">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-228">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="c7515-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-229">Overtreding van regel 2.</span><span class="sxs-lookup"><span data-stu-id="c7515-229">Violation of Rule #2.</span></span> <span data-ttu-id="c7515-230">Tijd, materiaal en vergoedingen voor het P1-project zijn opgenomen op de prijsopgaveregels QL1 en QL2</span><span class="sxs-lookup"><span data-stu-id="c7515-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-231">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-232">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-233">QL2</span><span class="sxs-lookup"><span data-stu-id="c7515-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-234">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-235">Leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-236">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-237">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-238">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-239">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-240">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-241">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-242">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-243">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-244">Leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-245">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-246">Geen</span><span class="sxs-lookup"><span data-stu-id="c7515-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-247">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-248">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-249">Geldig</span><span class="sxs-lookup"><span data-stu-id="c7515-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-250">Tijd, materiaal en vergoedingen voor het P1-project zijn opgenomen in QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="c7515-251">Onkosten voor het P1-project zijn opgenomen in QL2</span><span class="sxs-lookup"><span data-stu-id="c7515-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="c7515-252">Geen overlap in wat wordt opgenomen op elke prijsopgaveregel en dus geldig.</span><span class="sxs-lookup"><span data-stu-id="c7515-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-253">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-254">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-255">QL2</span><span class="sxs-lookup"><span data-stu-id="c7515-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-256">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-257">Leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-258">Geen</span><span class="sxs-lookup"><span data-stu-id="c7515-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-259">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-260">Geen</span><span class="sxs-lookup"><span data-stu-id="c7515-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-261">Geen</span><span class="sxs-lookup"><span data-stu-id="c7515-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-262">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-263">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-264">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-265">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-266">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="c7515-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-267">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-268">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-269">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-270">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-271">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="c7515-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-272">Overtreding van regel 2</span><span class="sxs-lookup"><span data-stu-id="c7515-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="c7515-273">Q1 omvat tijd, materiaal, onkosten en vergoedingen voor een subset van taken in project P1</span><span class="sxs-lookup"><span data-stu-id="c7515-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="c7515-274">QL2 omvat tijd, onkosten en vergoedingen voor het hele project P1 en overlapt daarom met wat is opgenomen in Q1.</span><span class="sxs-lookup"><span data-stu-id="c7515-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-275">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-276">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-277">QL2</span><span class="sxs-lookup"><span data-stu-id="c7515-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-278">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-279">Leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-280">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-281">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-282">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-283">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-284">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-285">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-286">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-287">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-288">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="c7515-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-289">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-290">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-291">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-292">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-293">Geldig</span><span class="sxs-lookup"><span data-stu-id="c7515-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-294">Volgens regel 3,</span><span class="sxs-lookup"><span data-stu-id="c7515-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="c7515-295">Q1 omvat tijd, materiaal, onkosten en vergoedingen voor een subset van taken in project P1.</span><span class="sxs-lookup"><span data-stu-id="c7515-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c7515-296">QL2 omvat tijd, materiaal, onkosten en vergoedingen voor een subset van taken in project P1.</span><span class="sxs-lookup"><span data-stu-id="c7515-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c7515-297">De enige aanvullende validatie betreft de subset van taken in QL1, die verschilt van de subset van taken in QL2 om ervoor te zorgen dat er geen overlapping is.</span><span class="sxs-lookup"><span data-stu-id="c7515-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="c7515-298">Dit wordt gedaan door het systeem wanneer taken worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c7515-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-299">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-300">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-301">QL2</span><span class="sxs-lookup"><span data-stu-id="c7515-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-302">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-303">Alleen geselecteerde taken</span><span class="sxs-lookup"><span data-stu-id="c7515-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-304">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-305">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-306">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-307">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-308">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-309">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-310">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-311">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-312">Alle projecttaken of leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-313">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-314">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-315">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-316">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-317">Geldig</span><span class="sxs-lookup"><span data-stu-id="c7515-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-318">Per regel 5 zijn Q1 en Q2 twee prijsopgaven voor dezelfde verkoopkans, dus ze kunnen beide een schatting maken voor dezelfde componenten van een project.</span><span class="sxs-lookup"><span data-stu-id="c7515-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-319">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-320">KW2</span><span class="sxs-lookup"><span data-stu-id="c7515-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-321">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-322">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-323">Alle projecttaken of leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-324">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-325">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-326">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-327">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-328">O1</span><span class="sxs-lookup"><span data-stu-id="c7515-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-329">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-330">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-331">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-332">Alle projecttaken of leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-333">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-334">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-335">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-336">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-337">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="c7515-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7515-338">Per regel 4 zijn Q1 en Q2 twee prijsopgaven voor verschillende verkoopkansen, dus ze kunnen niet beide een schatting maken voor dezelfde componenten van hetzelfde project.</span><span class="sxs-lookup"><span data-stu-id="c7515-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c7515-339">O2</span><span class="sxs-lookup"><span data-stu-id="c7515-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c7515-340">KW1</span><span class="sxs-lookup"><span data-stu-id="c7515-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c7515-341">QL1</span><span class="sxs-lookup"><span data-stu-id="c7515-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-342">P1</span><span class="sxs-lookup"><span data-stu-id="c7515-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c7515-343">Alle projecttaken of leeg</span><span class="sxs-lookup"><span data-stu-id="c7515-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c7515-344">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c7515-345">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c7515-346">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c7515-347">Ja</span><span class="sxs-lookup"><span data-stu-id="c7515-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

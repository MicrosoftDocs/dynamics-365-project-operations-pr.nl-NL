---
title: Projectgebaseerde prijsopgaveregels
description: Dit onderwerp bevat informatie over het gebruik van op projectgebaseerde prijsopgaveregels voor projectwerk.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074431"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="891d2-103">Projectgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="891d2-103">Project-based quote lines</span></span>

<span data-ttu-id="891d2-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="891d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="891d2-105">Projectgebaseerde prijsopgaveregels zijn ontworpen om te helpen bij het inschatten van het projectwerk voor een opdracht.</span><span class="sxs-lookup"><span data-stu-id="891d2-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="891d2-106">De structuur van een projectgebaseerde prijsopgaveregel wordt voor projectramingen uitgebreid met de volgende concepten:</span><span class="sxs-lookup"><span data-stu-id="891d2-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="891d2-107">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="891d2-107">Billing Method</span></span>
- <span data-ttu-id="891d2-108">Projecttoewijzing</span><span class="sxs-lookup"><span data-stu-id="891d2-108">Project Mapping</span></span>
- <span data-ttu-id="891d2-109">Inbegrepen transactieklassen</span><span class="sxs-lookup"><span data-stu-id="891d2-109">Included Transaction classes</span></span>
- <span data-ttu-id="891d2-110">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="891d2-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="891d2-111">Instellingen voor toerekenbaarheid</span><span class="sxs-lookup"><span data-stu-id="891d2-111">Chargeability setup</span></span>
- <span data-ttu-id="891d2-112">Schatting met gegevens van prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="891d2-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="891d2-113">Prijsopgaveregelklanten</span><span class="sxs-lookup"><span data-stu-id="891d2-113">Quote line Customers</span></span>

<span data-ttu-id="891d2-114">De volgende tabel bevat informatie over de velden op het tabblad **Algemeen** van projectgebaseerde prijsopgaveregels.</span><span class="sxs-lookup"><span data-stu-id="891d2-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="891d2-115">Deze velden helpen bij het opzetten van de basis voor een gedetailleerde, complete schatting voor projectwerk.</span><span class="sxs-lookup"><span data-stu-id="891d2-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="891d2-116">**Veld**</span><span class="sxs-lookup"><span data-stu-id="891d2-116">**Field**</span></span> | <span data-ttu-id="891d2-117">**Relevantie, doel en richtlijnen**</span><span class="sxs-lookup"><span data-stu-id="891d2-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="891d2-118">**Downstreamimpact**</span><span class="sxs-lookup"><span data-stu-id="891d2-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="891d2-119">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="891d2-119">Name</span></span> | <span data-ttu-id="891d2-120">De naam van de prijsopgaveregel waarmee u de afzonderlijke component van de prijsopgave in de raming kunt identificeren.</span><span class="sxs-lookup"><span data-stu-id="891d2-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="891d2-121">Gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-122">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="891d2-122">Billing Method</span></span> | <span data-ttu-id="891d2-123">In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het overeenkomstige veld op de verkoopkansregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="891d2-124">Dit veld bevat de twee belangrijkste contractmodellen die worden ondersteund door Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="891d2-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="891d2-125">- Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="891d2-125">- Fixed price</span></span></br><span data-ttu-id="891d2-126">- Tijd en materiaal.</span><span class="sxs-lookup"><span data-stu-id="891d2-126">- Time and material.</span></span>| <span data-ttu-id="891d2-127">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-128">Project</span><span class="sxs-lookup"><span data-stu-id="891d2-128">Project</span></span> | <span data-ttu-id="891d2-129">Gebruik dit optionele veld om het project te identificeren dat wordt gebruikt om het werk voor deze opdracht af te leveren.</span><span class="sxs-lookup"><span data-stu-id="891d2-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="891d2-130">Wanneer een project wordt toegewezen aan een prijsopgaveregel, is dit handig bij het instellen van toerekenbare taken en ook bij het opnemen van een projectgebaseerde schatting op de prijsopgaveregel als details van de prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="891d2-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="891d2-131">Als een project niet wordt toegewezen aan een projectgebaseerde prijsopgaveregel, moet de schatting handmatig worden gemaakt door elk detail van de prijsopgave te creëren.</span><span class="sxs-lookup"><span data-stu-id="891d2-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="891d2-132">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-133">Tijd opnemen</span><span class="sxs-lookup"><span data-stu-id="891d2-133">Include Time</span></span> | <span data-ttu-id="891d2-134">Een markering **Ja**/**Nee** geeft aan of tijdtransacties of arbeidskosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="891d2-135">Een waarde **Nee** geeft aan of de tijdtransacties of arbeidskosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="891d2-136">Een waarde **Ja** geeft aan of de tijdtransacties of arbeidskosten worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="891d2-137">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-138">Onkosten opnemen</span><span class="sxs-lookup"><span data-stu-id="891d2-138">Include Expense</span></span> | <span data-ttu-id="891d2-139">Een markering **Ja**/**Nee** geeft aan of onkosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="891d2-140">Een waarde **Nee** geeft aan of de onkosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="891d2-141">Een waarde **Ja** geeft aan of de onkosten worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="891d2-142">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-143">Tarief opnemen</span><span class="sxs-lookup"><span data-stu-id="891d2-143">Include Fee</span></span> | <span data-ttu-id="891d2-144">Een markering **Ja**/**Nee** geeft aan of vergoedingen voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="891d2-145">Een waarde **Nee** geeft aan of de vergoedingen niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="891d2-146">Een waarde **Ja** geeft aan of de vergoedingen niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="891d2-147">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-148">Bedrag van prijsopgave</span><span class="sxs-lookup"><span data-stu-id="891d2-148">Quoted Amount</span></span> | <span data-ttu-id="891d2-149">Dit is het bedrag dat aan de klant wordt geoffreerd voor al het werk dat op deze projectgebaseerde offerteregel wordt voorspeld.</span><span class="sxs-lookup"><span data-stu-id="891d2-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="891d2-150">In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het veld **Klantbudget** op de verkoopkansregel.</span><span class="sxs-lookup"><span data-stu-id="891d2-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="891d2-151">Wanneer de projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het bedrag in de prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="891d2-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="891d2-152">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-153">Geschatte belasting</span><span class="sxs-lookup"><span data-stu-id="891d2-153">Estimated Tax</span></span> | <span data-ttu-id="891d2-154">Dit is een bewerkbaar veld voor de gebruiker om het geschatte belastingbedrag op de prijsopgaveregel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="891d2-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="891d2-155">Wanneer een projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het belastingbedrag in de prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="891d2-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="891d2-156">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-157">Bedrag van prijsopgave na belasting</span><span class="sxs-lookup"><span data-stu-id="891d2-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="891d2-158">Dit veld is het prijsopgaveregelbedrag na belasting en is alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="891d2-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="891d2-159">Het bedrag in dit veld wordt berekend als *Geoffreerd bedrag + belasting*.</span><span class="sxs-lookup"><span data-stu-id="891d2-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="891d2-160">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-161">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="891d2-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="891d2-162">Dit veld kan worden bewerkt en is alleen beschikbaar op projectgebaseerde prijsopgaveregels met de factureringsmethode **Tijd en materiaal**.</span><span class="sxs-lookup"><span data-stu-id="891d2-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="891d2-163">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="891d2-164">Klantbudget</span><span class="sxs-lookup"><span data-stu-id="891d2-164">Customer Budget</span></span> | <span data-ttu-id="891d2-165">Dit veld is bewerkbaar en wordt gekopieerd uit het overeenkomstige veld op de verkoopkansregel als de prijsopgave wordt gemaakt op basis van een verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="891d2-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="891d2-166">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="891d2-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="891d2-167">Validatieregels voor velden op het tabblad Algemeen van projectgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="891d2-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="891d2-168">**Regel 1** : een bepaalde transactieklasse voor het geselecteerde project kan alleen worden opgenomen in één projectgebaseerde regel van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="891d2-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="891d2-169">**Regel 2** : als een verkoopkans meerdere prijsopgaven bevat, kunnen er regels van verschillende prijsopgaven zijn die allemaal naar hetzelfde project verwijzen en dezelfde transactieklasse bevatten.</span><span class="sxs-lookup"><span data-stu-id="891d2-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="891d2-170">**Regel 3** : als de prijsopgaven niet tot dezelfde verkoopkans behoren, kunnen ze niet hetzelfde project en dezelfde transactieklasse bevatten.</span><span class="sxs-lookup"><span data-stu-id="891d2-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="891d2-171">
                    <strong>Verkoopkans</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="891d2-172">
                    <strong>Offerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="891d2-173">
                    <strong>Prijsopgaveregel</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="891d2-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="891d2-175">
                    <strong>Tijd opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="891d2-176">
                    <strong>Onkosten opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="891d2-177">
                    <strong>Opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="891d2-178">
                    <strong>Vergoeding</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="891d2-179">
                    <strong>Geldig/ongeldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="891d2-180">
                    <strong>Reden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891d2-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="891d2-181">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-182">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-183">QL1</span><span class="sxs-lookup"><span data-stu-id="891d2-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-184">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-185">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-186">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-187">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-188">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="891d2-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-189">Overtreding van regel 1.</span><span class="sxs-lookup"><span data-stu-id="891d2-189">Violation of Rule #1.</span></span> <span data-ttu-id="891d2-190">Tijd, onkosten en vergoedingen voor het P1-project zijn opgenomen op beide prijsopgaveregels QL1 en QL2.</span><span class="sxs-lookup"><span data-stu-id="891d2-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="891d2-191">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-192">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-193">QL2</span><span class="sxs-lookup"><span data-stu-id="891d2-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-194">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-195">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-196">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-197">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-197">Yes</span></span> </p>
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
<span data-ttu-id="891d2-198">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-199">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-200">QL1</span><span class="sxs-lookup"><span data-stu-id="891d2-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-201">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-202">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-203">No</span><span class="sxs-lookup"><span data-stu-id="891d2-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-204">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-205">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="891d2-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-206">Overtreding van regel 1.</span><span class="sxs-lookup"><span data-stu-id="891d2-206">Violation of Rule #1.</span></span> <span data-ttu-id="891d2-207">Tijd en vergoedingen voor het P1-project zijn opgenomen op beide prijsopgaveregels QL1 en QL2.</span><span class="sxs-lookup"><span data-stu-id="891d2-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="891d2-208">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-209">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-210">QL2</span><span class="sxs-lookup"><span data-stu-id="891d2-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-211">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-212">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-213">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-214">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-214">Yes</span></span> </p>
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
<span data-ttu-id="891d2-215">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-216">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-217">QL1</span><span class="sxs-lookup"><span data-stu-id="891d2-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-218">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-219">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-220">No</span><span class="sxs-lookup"><span data-stu-id="891d2-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-221">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-222">Geldig</span><span class="sxs-lookup"><span data-stu-id="891d2-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="891d2-223">Tijd en vergoedingen voor het P1-project zijn opgenomen in QL1.</span><span class="sxs-lookup"><span data-stu-id="891d2-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="891d2-224">Onkosten voor het P1-project zijn opgenomen in QL2.</span><span class="sxs-lookup"><span data-stu-id="891d2-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="891d2-225">Er is geen overlap in wat op elke prijsopgaveregel wordt opgenomen en dus is het geldig.</span><span class="sxs-lookup"><span data-stu-id="891d2-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="891d2-226">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-227">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-228">QL2</span><span class="sxs-lookup"><span data-stu-id="891d2-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-229">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-230">No</span><span class="sxs-lookup"><span data-stu-id="891d2-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-231">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-232">No</span><span class="sxs-lookup"><span data-stu-id="891d2-232">No</span></span> </p>
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
<span data-ttu-id="891d2-233">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-234">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-235">QL1</span><span class="sxs-lookup"><span data-stu-id="891d2-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-236">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-237">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-238">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-239">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-240">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="891d2-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-241">Overtreding van regel 1 hierboven</span><span class="sxs-lookup"><span data-stu-id="891d2-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="891d2-242">Q1 omvat tijd, onkosten en vergoedingen voor het hele project P1.</span><span class="sxs-lookup"><span data-stu-id="891d2-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="891d2-243">QL2 omvat tijd, onkosten en vergoedingen voor het hele project P1 en overlapt met wat is inbegrepen in Q1.</span><span class="sxs-lookup"><span data-stu-id="891d2-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="891d2-244">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-245">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-246">QL2</span><span class="sxs-lookup"><span data-stu-id="891d2-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-247">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-248">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-249">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-250">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-250">Yes</span></span> </p>
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
<span data-ttu-id="891d2-251">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-252">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-253">QL1</span><span class="sxs-lookup"><span data-stu-id="891d2-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-254">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-255">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-256">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-257">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="891d2-258">Geldig</span><span class="sxs-lookup"><span data-stu-id="891d2-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-259">Op basis van regel 2 zijn Q1 en Q2 twee prijsopgaven voor dezelfde verkoopkans, dus ze kunnen beide een schatting geven voor dezelfde componenten van een project.</span><span class="sxs-lookup"><span data-stu-id="891d2-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="891d2-260">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-261">KW2</span><span class="sxs-lookup"><span data-stu-id="891d2-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-262">QL1 op Q2</span><span class="sxs-lookup"><span data-stu-id="891d2-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-263">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-264">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-265">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-266">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-266">Yes</span></span> </p>
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
<span data-ttu-id="891d2-267">O1</span><span class="sxs-lookup"><span data-stu-id="891d2-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-268">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-269">QL1</span><span class="sxs-lookup"><span data-stu-id="891d2-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-270">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-271">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-272">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-273">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="891d2-274">Geldig</span><span class="sxs-lookup"><span data-stu-id="891d2-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891d2-275">Op basis van regel 3 zijn Q1 en Q2 twee prijsopgaven voor verschillende verkoopkansen, dus ze kunnen niet een schatting geven voor dezelfde componenten van hetzelfde project.</span><span class="sxs-lookup"><span data-stu-id="891d2-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="891d2-276">O2</span><span class="sxs-lookup"><span data-stu-id="891d2-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="891d2-277">KW1</span><span class="sxs-lookup"><span data-stu-id="891d2-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-278">QL1</span><span class="sxs-lookup"><span data-stu-id="891d2-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-279">P1</span><span class="sxs-lookup"><span data-stu-id="891d2-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-280">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="891d2-281">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="891d2-282">Ja</span><span class="sxs-lookup"><span data-stu-id="891d2-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="891d2-283">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="891d2-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


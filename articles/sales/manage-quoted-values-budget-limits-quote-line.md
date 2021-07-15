---
title: Overzicht van projectprijsopgaveregels
description: Dit onderwerp biedt informatie over het gebruik van projectprijsopgaveregels voor projectwerk.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: c585bbc55119e678a4f75f5dfe8966a436db1a34
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368065"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="6b34d-103">Overzicht van projectprijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="6b34d-103">Project quote lines overview</span></span>

<span data-ttu-id="6b34d-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="6b34d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6b34d-105">Projectgebaseerde prijsopgaveregels zijn ontworpen om te helpen bij het inschatten van het projectwerk voor een opdracht.</span><span class="sxs-lookup"><span data-stu-id="6b34d-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6b34d-106">De structuur van een projectgebaseerde prijsopgaveregel wordt voor projectramingen uitgebreid met de volgende concepten:</span><span class="sxs-lookup"><span data-stu-id="6b34d-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6b34d-107">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="6b34d-107">Billing Method</span></span>
- <span data-ttu-id="6b34d-108">Projecttoewijzing</span><span class="sxs-lookup"><span data-stu-id="6b34d-108">Project Mapping</span></span>
- <span data-ttu-id="6b34d-109">Inbegrepen transactieklassen</span><span class="sxs-lookup"><span data-stu-id="6b34d-109">Included Transaction classes</span></span>
- <span data-ttu-id="6b34d-110">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="6b34d-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6b34d-111">Instellingen voor toerekenbaarheid</span><span class="sxs-lookup"><span data-stu-id="6b34d-111">Chargeability setup</span></span>
- <span data-ttu-id="6b34d-112">Schatting met gegevens van prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="6b34d-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6b34d-113">Prijsopgaveregelklanten</span><span class="sxs-lookup"><span data-stu-id="6b34d-113">Quote line Customers</span></span>

<span data-ttu-id="6b34d-114">De volgende tabel bevat informatie over de velden op het tabblad **Algemeen** van projectgebaseerde prijsopgaveregels.</span><span class="sxs-lookup"><span data-stu-id="6b34d-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6b34d-115">Deze velden helpen bij het opzetten van de basis voor een gedetailleerde, complete schatting voor projectwerk.</span><span class="sxs-lookup"><span data-stu-id="6b34d-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6b34d-116">**Veld**</span><span class="sxs-lookup"><span data-stu-id="6b34d-116">**Field**</span></span> | <span data-ttu-id="6b34d-117">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="6b34d-117">**Description**</span></span> | <span data-ttu-id="6b34d-118">**Downstreamimpact**</span><span class="sxs-lookup"><span data-stu-id="6b34d-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6b34d-119">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="6b34d-119">Name</span></span> | <span data-ttu-id="6b34d-120">De naam van de prijsopgaveregel waarmee u de afzonderlijke component van de prijsopgave in de raming kunt identificeren.</span><span class="sxs-lookup"><span data-stu-id="6b34d-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6b34d-121">Gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-122">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="6b34d-122">Billing Method</span></span> | <span data-ttu-id="6b34d-123">In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het overeenkomstige veld op de verkoopkansregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6b34d-124">Dit veld bevat de twee belangrijkste aanbestedingsmodellen die worden ondersteund door Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6b34d-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6b34d-125">- Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="6b34d-125">- Fixed price</span></span></br><span data-ttu-id="6b34d-126">- Tijd en materiaal.</span><span class="sxs-lookup"><span data-stu-id="6b34d-126">- Time and material.</span></span>| <span data-ttu-id="6b34d-127">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-128">Project</span><span class="sxs-lookup"><span data-stu-id="6b34d-128">Project</span></span> | <span data-ttu-id="6b34d-129">Gebruik dit optionele veld om het project te identificeren dat wordt gebruikt om het werk voor deze opdracht af te leveren.</span><span class="sxs-lookup"><span data-stu-id="6b34d-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6b34d-130">Wanneer een project wordt toegewezen aan een prijsopgaveregel, is dit handig bij het instellen van toerekenbare taken en ook bij het opnemen van een projectgebaseerde schatting op de prijsopgaveregel als details van de prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="6b34d-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6b34d-131">Als een project niet wordt toegewezen aan een projectgebaseerde prijsopgaveregel, moet de schatting handmatig worden gemaakt door elk detail van de prijsopgave te creëren.</span><span class="sxs-lookup"><span data-stu-id="6b34d-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6b34d-132">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-133">Tijd opnemen</span><span class="sxs-lookup"><span data-stu-id="6b34d-133">Include Time</span></span> | <span data-ttu-id="6b34d-134">Een markering **Ja**/**Nee** geeft aan of tijdtransacties of arbeidskosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b34d-135">Een waarde **Nee** geeft aan of de tijdtransacties of arbeidskosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b34d-136">Een waarde **Ja** geeft aan of de tijdtransacties of arbeidskosten worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6b34d-137">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-138">Onkosten opnemen</span><span class="sxs-lookup"><span data-stu-id="6b34d-138">Include Expense</span></span> | <span data-ttu-id="6b34d-139">Een markering **Ja**/**Nee** geeft aan of onkosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b34d-140">Een waarde **Nee** geeft aan of de onkosten niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b34d-141">Een waarde **Ja** geeft aan of de onkosten worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6b34d-142">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-143">Tarief opnemen</span><span class="sxs-lookup"><span data-stu-id="6b34d-143">Include Fee</span></span> | <span data-ttu-id="6b34d-144">Een markering **Ja**/**Nee** geeft aan of vergoedingen voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b34d-145">Een waarde **Nee** geeft aan of de vergoedingen niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6b34d-146">Een waarde **Ja** geeft aan of de vergoedingen niet worden opgenomen in de schatting op deze prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6b34d-147">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-148">Bedrag van prijsopgave</span><span class="sxs-lookup"><span data-stu-id="6b34d-148">Quoted Amount</span></span> | <span data-ttu-id="6b34d-149">Dit is het bedrag dat aan de klant wordt geoffreerd voor al het werk dat op deze projectgebaseerde offerteregel wordt voorspeld.</span><span class="sxs-lookup"><span data-stu-id="6b34d-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6b34d-150">In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het veld **Klantbudget** op de verkoopkansregel.</span><span class="sxs-lookup"><span data-stu-id="6b34d-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6b34d-151">Wanneer de projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het bedrag in de prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="6b34d-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6b34d-152">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-153">Geschatte belasting</span><span class="sxs-lookup"><span data-stu-id="6b34d-153">Estimated Tax</span></span> | <span data-ttu-id="6b34d-154">Dit is een bewerkbaar veld voor de gebruiker om het geschatte belastingbedrag op de prijsopgaveregel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="6b34d-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6b34d-155">Wanneer een projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het belastingbedrag in de prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="6b34d-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6b34d-156">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-157">Bedrag van prijsopgave na belasting</span><span class="sxs-lookup"><span data-stu-id="6b34d-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="6b34d-158">Dit veld is het prijsopgaveregelbedrag na belasting en is alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="6b34d-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6b34d-159">Het bedrag in dit veld wordt berekend als *Geoffreerd bedrag + belasting*.</span><span class="sxs-lookup"><span data-stu-id="6b34d-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6b34d-160">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-161">Niet-overschrijdingslimiet</span><span class="sxs-lookup"><span data-stu-id="6b34d-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="6b34d-162">Dit veld kan worden bewerkt en is alleen beschikbaar op projectgebaseerde prijsopgaveregels met de factureringsmethode **Tijd en materiaal**.</span><span class="sxs-lookup"><span data-stu-id="6b34d-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6b34d-163">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6b34d-164">Klantbudget</span><span class="sxs-lookup"><span data-stu-id="6b34d-164">Customer Budget</span></span> | <span data-ttu-id="6b34d-165">Dit veld is bewerkbaar en wordt gekopieerd uit het overeenkomstige veld op de verkoopkansregel als de prijsopgave wordt gemaakt op basis van een verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="6b34d-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6b34d-166">Deze veldwaarde wordt gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="6b34d-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6b34d-167">Validatieregels voor velden op het tabblad Algemeen van projectgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="6b34d-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6b34d-168">**Regel 1**: een bepaalde transactieklasse voor het geselecteerde project kan alleen worden opgenomen in één projectgebaseerde regel van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="6b34d-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6b34d-169">**Regel 2**: als een verkoopkans meerdere prijsopgaven bevat, kunnen er regels van verschillende prijsopgaven zijn die allemaal naar hetzelfde project verwijzen en dezelfde transactieklasse bevatten.</span><span class="sxs-lookup"><span data-stu-id="6b34d-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6b34d-170">**Regel 3**: als de prijsopgaven niet tot dezelfde verkoopkans behoren, kunnen ze niet hetzelfde project en dezelfde transactieklasse bevatten.</span><span class="sxs-lookup"><span data-stu-id="6b34d-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="6b34d-171">
                    <strong>Verkoopkans</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6b34d-172">
                    <strong>Offerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6b34d-173">
                    <strong>Prijsopgaveregel</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6b34d-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6b34d-175">
                    <strong>Tijd opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6b34d-176">
                    <strong>Onkosten opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6b34d-177">
                    <strong>Opnemen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6b34d-178">
                    <strong>Vergoeding</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="6b34d-179">
                    <strong>Geldig/ongeldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="6b34d-180">
                    <strong>Reden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b34d-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b34d-181">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-182">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-183">QL1</span><span class="sxs-lookup"><span data-stu-id="6b34d-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-184">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-185">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-186">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-187">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-188">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="6b34d-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-189">Overtreding van regel 1.</span><span class="sxs-lookup"><span data-stu-id="6b34d-189">Violation of Rule #1.</span></span> <span data-ttu-id="6b34d-190">Tijd, onkosten en vergoedingen voor het P1-project zijn opgenomen op beide prijsopgaveregels QL1 en QL2.</span><span class="sxs-lookup"><span data-stu-id="6b34d-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b34d-191">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-192">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-193">QL2</span><span class="sxs-lookup"><span data-stu-id="6b34d-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-194">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-195">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-196">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-197">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-197">Yes</span></span> </p>
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
<span data-ttu-id="6b34d-198">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-199">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-200">QL1</span><span class="sxs-lookup"><span data-stu-id="6b34d-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-201">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-202">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-203">Geen</span><span class="sxs-lookup"><span data-stu-id="6b34d-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-204">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-205">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="6b34d-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-206">Overtreding van regel 1.</span><span class="sxs-lookup"><span data-stu-id="6b34d-206">Violation of Rule #1.</span></span> <span data-ttu-id="6b34d-207">Tijd en vergoedingen voor het P1-project zijn opgenomen op beide prijsopgaveregels QL1 en QL2.</span><span class="sxs-lookup"><span data-stu-id="6b34d-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b34d-208">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-209">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-210">QL2</span><span class="sxs-lookup"><span data-stu-id="6b34d-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-211">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-212">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-213">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-214">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-214">Yes</span></span> </p>
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
<span data-ttu-id="6b34d-215">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-216">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-217">QL1</span><span class="sxs-lookup"><span data-stu-id="6b34d-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-218">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-219">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-220">Geen</span><span class="sxs-lookup"><span data-stu-id="6b34d-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-221">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-222">Geldig</span><span class="sxs-lookup"><span data-stu-id="6b34d-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="6b34d-223">Tijd en vergoedingen voor het P1-project zijn opgenomen in QL1.</span><span class="sxs-lookup"><span data-stu-id="6b34d-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="6b34d-224">Onkosten voor het P1-project zijn opgenomen in QL2.</span><span class="sxs-lookup"><span data-stu-id="6b34d-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="6b34d-225">Er is geen overlap in wat op elke prijsopgaveregel wordt opgenomen en dus is het geldig.</span><span class="sxs-lookup"><span data-stu-id="6b34d-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b34d-226">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-227">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-228">QL2</span><span class="sxs-lookup"><span data-stu-id="6b34d-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-229">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-230">Geen</span><span class="sxs-lookup"><span data-stu-id="6b34d-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-231">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-232">Geen</span><span class="sxs-lookup"><span data-stu-id="6b34d-232">No</span></span> </p>
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
<span data-ttu-id="6b34d-233">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-234">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-235">QL1</span><span class="sxs-lookup"><span data-stu-id="6b34d-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-236">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-237">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-238">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-239">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-240">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="6b34d-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-241">Overtreding van regel 1 hierboven</span><span class="sxs-lookup"><span data-stu-id="6b34d-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="6b34d-242">Q1 omvat tijd, onkosten en vergoedingen voor het hele project P1.</span><span class="sxs-lookup"><span data-stu-id="6b34d-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6b34d-243">QL2 omvat tijd, onkosten en vergoedingen voor het hele project P1 en overlapt met wat is inbegrepen in Q1.</span><span class="sxs-lookup"><span data-stu-id="6b34d-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b34d-244">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-245">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-246">QL2</span><span class="sxs-lookup"><span data-stu-id="6b34d-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-247">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-248">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-249">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-250">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-250">Yes</span></span> </p>
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
<span data-ttu-id="6b34d-251">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-252">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-253">QL1</span><span class="sxs-lookup"><span data-stu-id="6b34d-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-254">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-255">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-256">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-257">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6b34d-258">Geldig</span><span class="sxs-lookup"><span data-stu-id="6b34d-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-259">Op basis van regel 2 zijn Q1 en Q2 twee prijsopgaven voor dezelfde verkoopkans, dus ze kunnen beide een schatting geven voor dezelfde componenten van een project.</span><span class="sxs-lookup"><span data-stu-id="6b34d-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b34d-260">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-261">KW2</span><span class="sxs-lookup"><span data-stu-id="6b34d-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-262">QL1 op Q2</span><span class="sxs-lookup"><span data-stu-id="6b34d-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-263">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-264">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-265">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-266">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-266">Yes</span></span> </p>
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
<span data-ttu-id="6b34d-267">O1</span><span class="sxs-lookup"><span data-stu-id="6b34d-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-268">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-269">QL1</span><span class="sxs-lookup"><span data-stu-id="6b34d-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-270">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-271">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-272">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-273">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6b34d-274">Geldig</span><span class="sxs-lookup"><span data-stu-id="6b34d-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b34d-275">Op basis van regel 3 zijn Q1 en Q2 twee prijsopgaven voor verschillende verkoopkansen, dus ze kunnen niet een schatting geven voor dezelfde componenten van hetzelfde project.</span><span class="sxs-lookup"><span data-stu-id="6b34d-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6b34d-276">O2</span><span class="sxs-lookup"><span data-stu-id="6b34d-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6b34d-277">KW1</span><span class="sxs-lookup"><span data-stu-id="6b34d-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-278">QL1</span><span class="sxs-lookup"><span data-stu-id="6b34d-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-279">P1</span><span class="sxs-lookup"><span data-stu-id="6b34d-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-280">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6b34d-281">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6b34d-282">Ja</span><span class="sxs-lookup"><span data-stu-id="6b34d-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6b34d-283">Ongeldig</span><span class="sxs-lookup"><span data-stu-id="6b34d-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]

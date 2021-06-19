---
title: Uitgavenoverzicht van onderzoek naar federale subsidies
description: Dit onderwerp bevat informatie over het uitgavenoverzicht van onderzoek naar federale subsidies.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010060"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c27b6-103">Uitgavenoverzicht van onderzoek naar federale subsidies</span><span class="sxs-lookup"><span data-stu-id="c27b6-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c27b6-104">Volgens Office of Management and budget Circular A-133 zijn agentschappen die overheidsfondsen ontvangen, onderworpen aan auditvereisten, ook wel bekend als eenmalige audits.</span><span class="sxs-lookup"><span data-stu-id="c27b6-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="c27b6-105">Het auditproces wordt gebruikt om op periodiek te rapporteren over de inkomsten en uitgaven van federale subsidies.</span><span class="sxs-lookup"><span data-stu-id="c27b6-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="c27b6-106">Een deel van het auditrapport omvat het uitgavenoverzicht van federale subsidies (SEFA).</span><span class="sxs-lookup"><span data-stu-id="c27b6-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="c27b6-107">Het uitgavenoverzicht van het onderzoek naar federale subsidies omvat de titel en het nummer van de Catalog of Federal Domestic Assistance (CFDA), het nummer van de subsidie, het jaar van de subsidie, de naam van de federale instantie die de fondsen verstrekt en de naam van de doorgifte-entiteit.</span><span class="sxs-lookup"><span data-stu-id="c27b6-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="c27b6-108">Het onderzoek geldt voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="c27b6-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="c27b6-109">Meestal is die periode hetzelfde als de financiële overzichtsperiode, dus een fiscaal jaar.</span><span class="sxs-lookup"><span data-stu-id="c27b6-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="c27b6-110">Het onderzoek heeft betrekking op subsidies met projectiedatums in het geselecteerde datumbereik.</span><span class="sxs-lookup"><span data-stu-id="c27b6-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="c27b6-111">De kolom met het **uitgiftebureau** van het onderzoek toont de subsidieontvanger of, voor een doorgegeven subsidie, het subsidieverstrekker.</span><span class="sxs-lookup"><span data-stu-id="c27b6-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="c27b6-112">Voor een doorgegeven subsidie bevat de kolom **Doorgiftebureau** de naam van de subsidieontvanger.</span><span class="sxs-lookup"><span data-stu-id="c27b6-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="c27b6-113">Als het niet om een doorgegeven subsidie gaat, is de kolom **Doorgiftebureau** leeg.</span><span class="sxs-lookup"><span data-stu-id="c27b6-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="c27b6-114">CFDA-clusters instellen</span><span class="sxs-lookup"><span data-stu-id="c27b6-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="c27b6-115">U moet de CFDA-clusters instellen die kunnen worden gekoppeld aan de CFDA-nummers in het uitgavenoverzicht van het onderzoek naar federale subsidies.</span><span class="sxs-lookup"><span data-stu-id="c27b6-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="c27b6-116">Ga naar **Projectmanagement en financiële administratie \> Instellen \> Subsidies \> CFDA-clusters**.</span><span class="sxs-lookup"><span data-stu-id="c27b6-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="c27b6-117">Selecteer **Nieuw** om een CFDA-cluster (Catalog of Federal Domestic Assistance) te maken.</span><span class="sxs-lookup"><span data-stu-id="c27b6-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="c27b6-118">Voer de clusternaam in.</span><span class="sxs-lookup"><span data-stu-id="c27b6-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="c27b6-119">Selecteer **Opslaan** om uw wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="c27b6-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="c27b6-120">CFDA-nummers instellen</span><span class="sxs-lookup"><span data-stu-id="c27b6-120">Set up CFDA numbers</span></span>

<span data-ttu-id="c27b6-121">U moet de CFDA-nummers instellen die kunnen worden toegevoegd aan subsidies en opgenomen in het uitgavenoverzicht van het onderzoek naar federale subsidies.</span><span class="sxs-lookup"><span data-stu-id="c27b6-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="c27b6-122">Ga naar **Projectmanagement en financiële administratie \> Instellen \> Subsidies \> CFDA-nummers**.</span><span class="sxs-lookup"><span data-stu-id="c27b6-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="c27b6-123">Selecteer **Nieuw** als u een CFDA-nummer wilt maken.</span><span class="sxs-lookup"><span data-stu-id="c27b6-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="c27b6-124">Voer in de kolom **Nummer** het CFDA-nummer in.</span><span class="sxs-lookup"><span data-stu-id="c27b6-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="c27b6-125">Druk de **Tab**-toets.</span><span class="sxs-lookup"><span data-stu-id="c27b6-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="c27b6-126">Voer in de kolom **Beschrijving** de CFDA-titel in.</span><span class="sxs-lookup"><span data-stu-id="c27b6-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="c27b6-127">Druk de **Tab**-toets.</span><span class="sxs-lookup"><span data-stu-id="c27b6-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="c27b6-128">Optioneel: voeg in het veld **Programmacluster** de juiste CFDA-cluster toe.</span><span class="sxs-lookup"><span data-stu-id="c27b6-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="c27b6-129">Selecteer **Opslaan** om uw wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="c27b6-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c27b6-130">Stel in voor welke subsidies moet worden gerapporteerd in het onderzoek naar het uitgavenoverzicht van federale subsidies</span><span class="sxs-lookup"><span data-stu-id="c27b6-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="c27b6-131">Ga naar **Projectmanagement en financiële administratie \> Subsidies \> Subsidies** en selecteer een bestaande subsidie.</span><span class="sxs-lookup"><span data-stu-id="c27b6-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="c27b6-132">Wijs op het sneltabblad **Instellen** in het veld **Catalog of Federal Domestic Assistance** het CFDA-nummer toe.</span><span class="sxs-lookup"><span data-stu-id="c27b6-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="c27b6-133">Het CFDA-nummer van de subsidie bepaalt de CFDA-cluster voor rapportage.</span><span class="sxs-lookup"><span data-stu-id="c27b6-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="c27b6-134">Voer op het sneltabblad **Contactgegevens** de gegevens in van de subsidieverstrekker door deze stappen te volgen:</span><span class="sxs-lookup"><span data-stu-id="c27b6-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="c27b6-135">Voer in het veld **Subsidieontvanger** de klant in die verantwoordelijk is voor de subsidie.</span><span class="sxs-lookup"><span data-stu-id="c27b6-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="c27b6-136">Voor een bestaande subsidie is deze informatie mogelijk al ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="c27b6-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="c27b6-137">Geef aan of de subsidieontvanger de financier is.</span><span class="sxs-lookup"><span data-stu-id="c27b6-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="c27b6-138">Als de subsidieontvanger de financier is, laat u het selectievakje **Doorgeven** uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c27b6-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="c27b6-139">Als een andere klant de financier is en de subsidieontvanger verantwoordelijk is voor het uitgeven en bijhouden van het geld, selecteert u het selectievakje **Doorgeven**.</span><span class="sxs-lookup"><span data-stu-id="c27b6-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="c27b6-140">Als u het selectievakje **Doorgeven** in de vorige stap hebt ingeschakeld, voert u bij **Subsidieverstrekker** de klant in die de subsidie heeft verstrekt.</span><span class="sxs-lookup"><span data-stu-id="c27b6-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="c27b6-141">Het subsidieverstrekker en de subsidieontvanger kunnen niet dezelfde klant zijn.</span><span class="sxs-lookup"><span data-stu-id="c27b6-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="c27b6-142">Dit is een voorbeeld van een doorgegeven subsidie:</span><span class="sxs-lookup"><span data-stu-id="c27b6-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="c27b6-143">De federale overheid financiert een infrastructuurproject voor een staat.</span><span class="sxs-lookup"><span data-stu-id="c27b6-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="c27b6-144">De federale overheid verstrekt het geld aan de staat om te besteden.</span><span class="sxs-lookup"><span data-stu-id="c27b6-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="c27b6-145">In dit geval is de federale overheid de subsidieverstrekker en de staat de subsidieafnemer.</span><span class="sxs-lookup"><span data-stu-id="c27b6-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="c27b6-146">Wanneer u de functie voor het eerst inschakelt, worden de eerste CFDA-nummers ingevoerd met behulp van de bestaande nummers op subsidies.</span><span class="sxs-lookup"><span data-stu-id="c27b6-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="c27b6-147">Subsidies uitsluiten van SEFA-rapportage op basis van het type subsidie</span><span class="sxs-lookup"><span data-stu-id="c27b6-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="c27b6-148">Ga naar **Projectmanagement en financiële administratie \> Instellen \> Subsidies \> Subsidietypes**.</span><span class="sxs-lookup"><span data-stu-id="c27b6-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="c27b6-149">Schakel op het sneltabblad **Standaardinformatie** het selectievakje **Uitsluiten van uitgavenoverzicht van federale subsidies** in.</span><span class="sxs-lookup"><span data-stu-id="c27b6-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="c27b6-150">Selecteer **Opslaan** om uw wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="c27b6-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c27b6-151">Het onderzoek naar het uitgavenoverzicht van federale subsidies uitvoeren</span><span class="sxs-lookup"><span data-stu-id="c27b6-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="c27b6-152">Ga naar **Projectmanagement en financiële administratie \> Rapporten en informatieverzoeken \> Informatieverzoek voor subsidies \> Uitgavenoverzicht van federale subsidies**.</span><span class="sxs-lookup"><span data-stu-id="c27b6-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="c27b6-153">Volg deze stappen in de sectie **Parameters**:</span><span class="sxs-lookup"><span data-stu-id="c27b6-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="c27b6-154">Selecteer in het veld **Datuminterval** de code voor het datuminterval.</span><span class="sxs-lookup"><span data-stu-id="c27b6-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="c27b6-155">Of bepaal het datuminterval in de velden **Begindatum** en **Einddatum**.</span><span class="sxs-lookup"><span data-stu-id="c27b6-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="c27b6-156">Optioneel: als u alleen gefactureerde transacties als omzet in de aanvraag wilt opnemen, stelt u de optie **Alleen gefactureerde omzet opnemen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c27b6-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="c27b6-157">Kolommen</span><span class="sxs-lookup"><span data-stu-id="c27b6-157">Columns</span></span>

<span data-ttu-id="c27b6-158">Het onderzoek naar het uitgavenoverzicht van federale subsidies omvat de volgende kolommen:</span><span class="sxs-lookup"><span data-stu-id="c27b6-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="c27b6-159">Naam van Catalog of Federal Domestic Assistance-cluster</span><span class="sxs-lookup"><span data-stu-id="c27b6-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="c27b6-160">Subsidieverstrekker</span><span class="sxs-lookup"><span data-stu-id="c27b6-160">Grantor agency</span></span>
- <span data-ttu-id="c27b6-161">Doorgiftebureau</span><span class="sxs-lookup"><span data-stu-id="c27b6-161">Pass-through agency</span></span>
- <span data-ttu-id="c27b6-162">Subsidienaam</span><span class="sxs-lookup"><span data-stu-id="c27b6-162">Grant name</span></span>
- <span data-ttu-id="c27b6-163">Subsidie-id</span><span class="sxs-lookup"><span data-stu-id="c27b6-163">Grant ID</span></span>
- <span data-ttu-id="c27b6-164">Id subsidieaanvraag</span><span class="sxs-lookup"><span data-stu-id="c27b6-164">Grant application ID</span></span>
- <span data-ttu-id="c27b6-165">Catalog of Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="c27b6-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="c27b6-166">Betalingsbewijzen</span><span class="sxs-lookup"><span data-stu-id="c27b6-166">Receipts</span></span>
- <span data-ttu-id="c27b6-167">Uitgaven</span><span class="sxs-lookup"><span data-stu-id="c27b6-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
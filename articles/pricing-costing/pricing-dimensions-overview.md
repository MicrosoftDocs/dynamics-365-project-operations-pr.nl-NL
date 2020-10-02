---
title: Overzicht van prijsdimensies
description: Dit onderwerp bevat informatie over de prijsdimensies in Dynamics 365 Project Operations.
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898210"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="31524-103">Overzicht van prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="31524-103">Pricing dimensions overview</span></span>

<span data-ttu-id="31524-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="31524-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="31524-105">De dimensies die worden gebruikt bij personeelszaken om prijzen en kosten in te stellen, vallen in twee categorieën:</span><span class="sxs-lookup"><span data-stu-id="31524-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="31524-106">Mensen</span><span class="sxs-lookup"><span data-stu-id="31524-106">People</span></span>
- <span data-ttu-id="31524-107">Gepland werk</span><span class="sxs-lookup"><span data-stu-id="31524-107">Planned work</span></span>

<span data-ttu-id="31524-108">Hierdoor zijn er twee typen prijsdimensiewaarden beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="31524-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="31524-109">**Optiesets**: dimensies die vaste opsommingen voor een set waarden zijn.</span><span class="sxs-lookup"><span data-stu-id="31524-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="31524-110">**Op entiteiten gebaseerde waarden**: dimensies die een gevarieerde reeks waarden kunnen zijn.</span><span class="sxs-lookup"><span data-stu-id="31524-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="31524-111">Prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="31524-111">Pricing dimensions</span></span>

<span data-ttu-id="31524-112">Dynamics 365 project Operations wordt geleverd met een standaardset prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="31524-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="31524-113">U kunt deze prijsdimensies bekijken door naar **Project Operations** > **Parameters** te gaan.</span><span class="sxs-lookup"><span data-stu-id="31524-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="31524-114">Controleer in de parameterrecord op het tabblad **Op bedrag gebaseerde prijsdimensies** of voor de rol **msdyn_resourcecategory** en de resource-organisatie-eenheid **msdyn_organizationalunit** de velden **Van toepassing op verkoop** en **Van toepassing op kosten** op **Ja** zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="31524-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="31524-115">Als deze velden zijn ingeschakeld, kunt u de prijs en kosten voor elke combinatie van rol en organisatie-eenheid instellen.</span><span class="sxs-lookup"><span data-stu-id="31524-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="31524-116">Als u de prijs of kosten voor uw resources vaststelt met behulp van extra kenmerken, kunt u aangepaste velden, entiteiten en dimensies maken.</span><span class="sxs-lookup"><span data-stu-id="31524-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="31524-117">De prijs van personeelstijd bepalen</span><span class="sxs-lookup"><span data-stu-id="31524-117">Pricing human resource time</span></span>
<span data-ttu-id="31524-118">Hoe een organisatie de prijs van personeelstijd bepaalt, is vaak een belangrijke strategische overweging die rechtstreeks van invloed is op de winstgevendheid van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="31524-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="31524-119">Werk samen met de financiële teams en groepshoofden wanneer uw organisatie klaar is om te bepalen hoe zij facturerings- en kostentarieven voor personeelstijd wil instellen.</span><span class="sxs-lookup"><span data-stu-id="31524-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="31524-120">Een andere overweging voor de prijsbepaling is onder andere de vraag of u velden of entiteiten die momenteel geen prijsdimensies zijn, opnieuw wilt gebruiken, maar ze dan wilt toepassen als een prijsdimensie voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="31524-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="31524-121">Velden, zoals **Transactiecategorie** (**msdyn_transactioncategory**) en **Boekbare resource** (**bookableresource**), zijn voorbeelden van mogelijk geschikte dimensies.</span><span class="sxs-lookup"><span data-stu-id="31524-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="31524-122">Overweeg ook of uw prijsdimensie een tabel of een optieset moet zijn.</span><span class="sxs-lookup"><span data-stu-id="31524-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="31524-123">Als u verwacht dat u meer dan 10 of 12 wijzigingen in de waarden van een dimensie moet aanbrengen en u aanvullende kenmerken voor deze waarden nodig hebt, kunt u een entiteit maken in plaats van een optieset.</span><span class="sxs-lookup"><span data-stu-id="31524-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="31524-124">Voor het onderhouden van een optieset, zoals het toevoegen of verwijderen van waarden, is een beheerder of ontwikkelaar vereist, terwijl het toevoegen van nieuwe rijen aan een tabel kan worden gedaan door de meeste gebruikers.</span><span class="sxs-lookup"><span data-stu-id="31524-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="31524-125">In het volgende voorbeeld worden de factureringstarieven weergegeven die zijn ingesteld op basis van de rol en de organisatie-eenheid waartoe de resource behoort.</span><span class="sxs-lookup"><span data-stu-id="31524-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="31524-126">Kostentarieven zijn meestal gebaseerd op de salarisbandbreedte van de werknemer en de organisatie-eenheid waartoe deze behoort.</span><span class="sxs-lookup"><span data-stu-id="31524-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="31524-127">In dit voorbeeld zien de tabellen met facturerings- en kostentarieven er als volgt uit.</span><span class="sxs-lookup"><span data-stu-id="31524-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="31524-128">**Voorbeeld van factureringstarieven**</span><span class="sxs-lookup"><span data-stu-id="31524-128">**Sample bill rates**</span></span>

| <span data-ttu-id="31524-129">Rol</span><span class="sxs-lookup"><span data-stu-id="31524-129">Role</span></span>        | <span data-ttu-id="31524-130">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="31524-130">Org Unit</span></span>    |<span data-ttu-id="31524-131">Eenheid</span><span class="sxs-lookup"><span data-stu-id="31524-131">Unit</span></span>      |<span data-ttu-id="31524-132">Prijs</span><span class="sxs-lookup"><span data-stu-id="31524-132">Price</span></span>      |<span data-ttu-id="31524-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="31524-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="31524-134">Ontwikkelaar</span><span class="sxs-lookup"><span data-stu-id="31524-134">Developer</span></span>   | <span data-ttu-id="31524-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="31524-135">Contoso US</span></span>  |<span data-ttu-id="31524-136">Hour</span><span class="sxs-lookup"><span data-stu-id="31524-136">Hour</span></span> | <span data-ttu-id="31524-137">200</span><span class="sxs-lookup"><span data-stu-id="31524-137">200</span></span>|<span data-ttu-id="31524-138">USD</span><span class="sxs-lookup"><span data-stu-id="31524-138">USD</span></span>     |
| <span data-ttu-id="31524-139">Ontwikkelaar</span><span class="sxs-lookup"><span data-stu-id="31524-139">Developer</span></span>   | <span data-ttu-id="31524-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="31524-140">Contoso India</span></span> |<span data-ttu-id="31524-141">Hour</span><span class="sxs-lookup"><span data-stu-id="31524-141">Hour</span></span>|   <span data-ttu-id="31524-142">112</span><span class="sxs-lookup"><span data-stu-id="31524-142">112</span></span>|<span data-ttu-id="31524-143">USD</span><span class="sxs-lookup"><span data-stu-id="31524-143">USD</span></span>     |


<span data-ttu-id="31524-144">**Voorbeeld van kostentarieven**</span><span class="sxs-lookup"><span data-stu-id="31524-144">**Sample cost rates**</span></span>

| <span data-ttu-id="31524-145">Salarisbandbreedte</span><span class="sxs-lookup"><span data-stu-id="31524-145">Salary Band</span></span>     | <span data-ttu-id="31524-146">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="31524-146">Org Unit</span></span>    |<span data-ttu-id="31524-147">Eenheid</span><span class="sxs-lookup"><span data-stu-id="31524-147">Unit</span></span>      |<span data-ttu-id="31524-148">Prijs</span><span class="sxs-lookup"><span data-stu-id="31524-148">Price</span></span>      |<span data-ttu-id="31524-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="31524-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="31524-150">Mijn bedrijf_Bandbreedte1</span><span class="sxs-lookup"><span data-stu-id="31524-150">My company_Band1</span></span> | <span data-ttu-id="31524-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="31524-151">Contoso US</span></span>  |<span data-ttu-id="31524-152">Hour</span><span class="sxs-lookup"><span data-stu-id="31524-152">Hour</span></span> | <span data-ttu-id="31524-153">145</span><span class="sxs-lookup"><span data-stu-id="31524-153">145</span></span>|<span data-ttu-id="31524-154">USD</span><span class="sxs-lookup"><span data-stu-id="31524-154">USD</span></span>     |
| <span data-ttu-id="31524-155">Mijn bedrijf_Bandbreedte2</span><span class="sxs-lookup"><span data-stu-id="31524-155">My company_Band2</span></span> | <span data-ttu-id="31524-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="31524-156">Contoso India</span></span> |<span data-ttu-id="31524-157">Hour</span><span class="sxs-lookup"><span data-stu-id="31524-157">Hour</span></span>|   <span data-ttu-id="31524-158">67</span><span class="sxs-lookup"><span data-stu-id="31524-158">67</span></span>|<span data-ttu-id="31524-159">USD</span><span class="sxs-lookup"><span data-stu-id="31524-159">USD</span></span>     |

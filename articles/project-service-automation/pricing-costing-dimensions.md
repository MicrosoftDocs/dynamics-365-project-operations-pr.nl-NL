---
title: Startpagina voor prijs- en kostendimensies
description: Dit onderwerp biedt een overzicht van prijsdimensies.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750736"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="f9a89-103">Startpagina voor prijs- en kostendimensies</span><span class="sxs-lookup"><span data-stu-id="f9a89-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="f9a89-104">De dimensies die worden gebruikt bij personeelszaken om prijzen en kosten in te stellen, vallen in twee categorieën:</span><span class="sxs-lookup"><span data-stu-id="f9a89-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="f9a89-105">Mensen</span><span class="sxs-lookup"><span data-stu-id="f9a89-105">People</span></span>
- <span data-ttu-id="f9a89-106">Gepland werk</span><span class="sxs-lookup"><span data-stu-id="f9a89-106">Planned work</span></span>

<span data-ttu-id="f9a89-107">Hierdoor zijn er twee typen prijsdimensiewaarden beschikbaar in Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="f9a89-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="f9a89-108">**Optiesets** - Dimensies die vaste opsommingen voor een set waarden zijn.</span><span class="sxs-lookup"><span data-stu-id="f9a89-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="f9a89-109">**Op entiteiten gebaseerde waarden** - Dimensies die een gevarieerde set waarden kunnen zijn.</span><span class="sxs-lookup"><span data-stu-id="f9a89-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="f9a89-110">Prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="f9a89-110">Pricing dimensions</span></span>

<span data-ttu-id="f9a89-111">PSA wordt geleverd met een standaardset prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="f9a89-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="f9a89-112">U kunt deze bekijken door naar **Project Service** > **Parameters** te gaan.</span><span class="sxs-lookup"><span data-stu-id="f9a89-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="f9a89-113">Controleer in de parameterrecord op het tabblad **Op bedrag gebaseerde prijsdimensies** of voor de rol **msdyn_resourcecategory** en de resource-organisatie-eenheid **msdyn_organizationalunit** de velden **Van toepassing op verkoop** en **Van toepassing op kosten** op **Ja** zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f9a89-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="f9a89-114">Dit stelt u in staat om de prijs en kosten voor elke combinatie van rol en organisatie-eenheid in te stellen.</span><span class="sxs-lookup"><span data-stu-id="f9a89-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Schermopname van Project Service-parameters waarin 'Van toepassing op verkoop' is gemarkeerd](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="f9a89-116">Als u de kant-en-klare velden van rol en organisatie-eenheid hebt gebruikt als prijsdimensies vóór versie 3 van PSA, is er geen waarneembare wijziging.</span><span class="sxs-lookup"><span data-stu-id="f9a89-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="f9a89-117">U kunt Project Service blijven gebruiken zoals u dat gewend was.</span><span class="sxs-lookup"><span data-stu-id="f9a89-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="f9a89-118">Als u de prijs of kosten voor uw resources vaststelt met behulp van extra kenmerken, kunt u aangepaste velden, entiteiten en dimensies maken.</span><span class="sxs-lookup"><span data-stu-id="f9a89-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="f9a89-119">Zie de volgende onderwerpen voor meer informatie, maar houd er rekening mee dat u de procedures in de onderstaande volgorde moet uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="f9a89-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="f9a89-120">Aangepaste velden en entiteiten maken</span><span class="sxs-lookup"><span data-stu-id="f9a89-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="f9a89-121">Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten</span><span class="sxs-lookup"><span data-stu-id="f9a89-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="f9a89-122">Aangepaste velden instellen als prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="f9a89-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="f9a89-123">Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen</span><span class="sxs-lookup"><span data-stu-id="f9a89-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="f9a89-124">De prijs van personeelstijd bepalen</span><span class="sxs-lookup"><span data-stu-id="f9a89-124">Pricing human resource time</span></span>
<span data-ttu-id="f9a89-125">Hoe een organisatie de prijs van personeelstijd bepaalt, is vaak een belangrijke strategische overweging die rechtstreeks van invloed is op de winstgevendheid van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="f9a89-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="f9a89-126">Werk samen met de financiële teams en groepshoofden wanneer uw organisatie klaar is om te bepalen hoe zij facturerings- en kostentarieven voor personeelstijd wil instellen.</span><span class="sxs-lookup"><span data-stu-id="f9a89-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="f9a89-127">Een andere overweging voor de prijsbepaling is onder andere de vraag of u velden of entiteiten die momenteel geen prijsdimensies zijn, opnieuw wilt gebruiken, maar ze dan wilt toepassen als een prijsdimensie voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="f9a89-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="f9a89-128">Velden, zoals **Transactiecategorie** (**msdyn_transactioncategory**) en **Boekbare resource** (**bookableresource**), zijn voorbeelden van mogelijk geschikte dimensies.</span><span class="sxs-lookup"><span data-stu-id="f9a89-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="f9a89-129">U dient ook te overwegen of uw prijsdimensie een tabel of een optieset moet zijn.</span><span class="sxs-lookup"><span data-stu-id="f9a89-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="f9a89-130">Als u verwacht dat u meer dan 10 of 12 wijzigingen in de waarden van een dimensie moet aanbrengen en u aanvullende kenmerken voor deze waarden nodig hebt, kunt u een entiteit maken in plaats van een optieset.</span><span class="sxs-lookup"><span data-stu-id="f9a89-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="f9a89-131">Voor het onderhouden van een optieset, zoals het toevoegen of verwijderen van waarden, is een beheerder of ontwikkelaar vereist, terwijl het toevoegen van nieuwe rijen aan een tabel kan worden gedaan door de meeste gebruikers.</span><span class="sxs-lookup"><span data-stu-id="f9a89-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="f9a89-132">In het volgende voorbeeld worden de factureringstarieven weergegeven die zijn ingesteld op basis van de rol en de organisatie-eenheid waartoe de resource behoort.</span><span class="sxs-lookup"><span data-stu-id="f9a89-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="f9a89-133">Kostentarieven zijn meestal gebaseerd op de salarisbandbreedte van de werknemer en de organisatie-eenheid waartoe deze behoort.</span><span class="sxs-lookup"><span data-stu-id="f9a89-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="f9a89-134">In dit voorbeeld zien de tabellen met facturerings- en kostentarieven er als volgt uit.</span><span class="sxs-lookup"><span data-stu-id="f9a89-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="f9a89-135">**Voorbeeld van factureringstarieven**</span><span class="sxs-lookup"><span data-stu-id="f9a89-135">**Sample bill rates**</span></span>

| <span data-ttu-id="f9a89-136">Rol</span><span class="sxs-lookup"><span data-stu-id="f9a89-136">Role</span></span>        | <span data-ttu-id="f9a89-137">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="f9a89-137">Org Unit</span></span>    |<span data-ttu-id="f9a89-138">Eenheid</span><span class="sxs-lookup"><span data-stu-id="f9a89-138">Unit</span></span>      |<span data-ttu-id="f9a89-139">Prijs</span><span class="sxs-lookup"><span data-stu-id="f9a89-139">Price</span></span>      |<span data-ttu-id="f9a89-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="f9a89-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f9a89-141">Ontwikkelaar</span><span class="sxs-lookup"><span data-stu-id="f9a89-141">Developer</span></span>   | <span data-ttu-id="f9a89-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f9a89-142">Contoso US</span></span>  |<span data-ttu-id="f9a89-143">Hour</span><span class="sxs-lookup"><span data-stu-id="f9a89-143">Hour</span></span> | <span data-ttu-id="f9a89-144">200</span><span class="sxs-lookup"><span data-stu-id="f9a89-144">200</span></span>|<span data-ttu-id="f9a89-145">USD</span><span class="sxs-lookup"><span data-stu-id="f9a89-145">USD</span></span>     |
| <span data-ttu-id="f9a89-146">Ontwikkelaar</span><span class="sxs-lookup"><span data-stu-id="f9a89-146">Developer</span></span>   | <span data-ttu-id="f9a89-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f9a89-147">Contoso India</span></span> |<span data-ttu-id="f9a89-148">Hour</span><span class="sxs-lookup"><span data-stu-id="f9a89-148">Hour</span></span>|   <span data-ttu-id="f9a89-149">112</span><span class="sxs-lookup"><span data-stu-id="f9a89-149">112</span></span>|<span data-ttu-id="f9a89-150">USD</span><span class="sxs-lookup"><span data-stu-id="f9a89-150">USD</span></span>     |


<span data-ttu-id="f9a89-151">**Voorbeeld van kostentarieven**</span><span class="sxs-lookup"><span data-stu-id="f9a89-151">**Sample cost rates**</span></span>

| <span data-ttu-id="f9a89-152">Salarisbandbreedte</span><span class="sxs-lookup"><span data-stu-id="f9a89-152">Salary Band</span></span>     | <span data-ttu-id="f9a89-153">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="f9a89-153">Org Unit</span></span>    |<span data-ttu-id="f9a89-154">Eenheid</span><span class="sxs-lookup"><span data-stu-id="f9a89-154">Unit</span></span>      |<span data-ttu-id="f9a89-155">Prijs</span><span class="sxs-lookup"><span data-stu-id="f9a89-155">Price</span></span>      |<span data-ttu-id="f9a89-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="f9a89-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f9a89-157">Mijn bedrijf_Bandbreedte1</span><span class="sxs-lookup"><span data-stu-id="f9a89-157">My company_Band1</span></span> | <span data-ttu-id="f9a89-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f9a89-158">Contoso US</span></span>  |<span data-ttu-id="f9a89-159">Hour</span><span class="sxs-lookup"><span data-stu-id="f9a89-159">Hour</span></span> | <span data-ttu-id="f9a89-160">145</span><span class="sxs-lookup"><span data-stu-id="f9a89-160">145</span></span>|<span data-ttu-id="f9a89-161">USD</span><span class="sxs-lookup"><span data-stu-id="f9a89-161">USD</span></span>     |
| <span data-ttu-id="f9a89-162">Mijn bedrijf_Bandbreedte2</span><span class="sxs-lookup"><span data-stu-id="f9a89-162">My company_Band2</span></span> | <span data-ttu-id="f9a89-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f9a89-163">Contoso India</span></span> |<span data-ttu-id="f9a89-164">Hour</span><span class="sxs-lookup"><span data-stu-id="f9a89-164">Hour</span></span>|   <span data-ttu-id="f9a89-165">67</span><span class="sxs-lookup"><span data-stu-id="f9a89-165">67</span></span>|<span data-ttu-id="f9a89-166">USD</span><span class="sxs-lookup"><span data-stu-id="f9a89-166">USD</span></span>     |

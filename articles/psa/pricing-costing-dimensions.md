---
title: Startpagina voor prijs- en kostendimensies
description: Dit onderwerp biedt een overzicht van prijsdimensies.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151292"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="e8ec7-103">Startpagina voor prijs- en kostendimensies</span><span class="sxs-lookup"><span data-stu-id="e8ec7-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e8ec7-104">De dimensies die worden gebruikt om arbeidsprijzen en -kosten in projectgebaseerde organisaties vast te stellen, worden beïnvloed door de volgende kenmerken:</span><span class="sxs-lookup"><span data-stu-id="e8ec7-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="e8ec7-105">Mensen die werk doen dat vergelijkbaar is met hun ervaring, rol of geografie</span><span class="sxs-lookup"><span data-stu-id="e8ec7-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="e8ec7-106">Uit te voeren werkzaamheden die vergelijkbaar zijn met de complexiteit of het tijdstip van de dag</span><span class="sxs-lookup"><span data-stu-id="e8ec7-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="e8ec7-107">Gezien de typische aard van deze kenmerken van het werk en de mensen die nodig zijn om het werk uit te voeren, zijn er twee soorten prijsdimensiewaarden beschikbaar in Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="e8ec7-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="e8ec7-108">**Optiesets**: kenmerken die vaste opsommingen voor een set waarden zijn.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="e8ec7-109">**Op entiteiten gebaseerde waarden**: kenmrken die een gevarieerde reeks waarden kunnen hebben die eindig zijn, maar in de loop van de tijd kunnen veranderen.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="e8ec7-110">Prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="e8ec7-110">Pricing dimensions</span></span>

<span data-ttu-id="e8ec7-111">PSA wordt geleverd met een standaardset prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="e8ec7-112">U kunt deze bekijken door naar **Project Service** > **Parameters** te gaan.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="e8ec7-113">Controleer in de parameterrecord op het tabblad **Op bedrag gebaseerde prijsdimensies** of voor de rol **msdyn_resourcecategory** en de resource-organisatie-eenheid **msdyn_organizationalunit** de velden **Van toepassing op verkoop** en **Van toepassing op kosten** op **Ja** zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="e8ec7-114">Dit stelt u in staat om de prijs en kosten voor elke combinatie van rol en organisatie-eenheid in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Schermopname van Project Service-parameters waarin 'Van toepassing op verkoop' is gemarkeerd](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="e8ec7-116">Als u de kant-en-klare velden van rol en organisatie-eenheid hebt gebruikt als prijsdimensies vóór versie 3 van PSA, is er geen waarneembare wijziging.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="e8ec7-117">U kunt Project Service blijven gebruiken zoals u dat gewend was.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="e8ec7-118">Als u de prijs of kosten voor uw resources vaststelt met behulp van extra kenmerken, kunt u aangepaste velden, entiteiten en dimensies maken.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="e8ec7-119">Zie de volgende onderwerpen voor meer informatie, maar houd er rekening mee dat u de procedures in de onderstaande volgorde moet uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="e8ec7-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="e8ec7-120">Aangepaste velden en entiteiten maken</span><span class="sxs-lookup"><span data-stu-id="e8ec7-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="e8ec7-121">Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten</span><span class="sxs-lookup"><span data-stu-id="e8ec7-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="e8ec7-122">Aangepaste velden instellen als prijsdimensies </span><span class="sxs-lookup"><span data-stu-id="e8ec7-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="e8ec7-123">Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen</span><span class="sxs-lookup"><span data-stu-id="e8ec7-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="e8ec7-124">De prijs van personeelstijd bepalen</span><span class="sxs-lookup"><span data-stu-id="e8ec7-124">Pricing human resource time</span></span>
<span data-ttu-id="e8ec7-125">Hoe een organisatie de prijs van personeelstijd bepaalt, is vaak een belangrijke strategische overweging die rechtstreeks van invloed is op de winstgevendheid van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="e8ec7-126">Werk samen met de financiële teams en groepshoofden wanneer uw organisatie klaar is om te bepalen hoe zij facturerings- en kostentarieven voor personeelstijd wil instellen.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="e8ec7-127">Een andere overweging voor de prijsbepaling is onder andere de vraag of u velden of entiteiten die momenteel geen prijsdimensies zijn, opnieuw wilt gebruiken, maar ze dan wilt toepassen als een prijsdimensie voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="e8ec7-128">Velden, zoals **Transactiecategorie** (**msdyn_transactioncategory**) en **Boekbare resource** (**bookableresource**), zijn voorbeelden van mogelijk geschikte dimensies.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="e8ec7-129">Overweeg ook of uw prijsdimensie een tabel of een optieset moet zijn.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="e8ec7-130">Als u verwacht dat u meer dan 10 of 12 wijzigingen in de waarden van een dimensie moet aanbrengen en u aanvullende kenmerken voor deze waarden nodig hebt, maakt u een entiteit in plaats van een optieset.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="e8ec7-131">Voor het onderhouden van een optieset, zoals het toevoegen of verwijderen van waarden, is een beheerder of ontwikkelaar vereist, terwijl het toevoegen van nieuwe rijen aan een tabel kan worden gedaan door de meeste zakelijke gebruikers.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="e8ec7-132">In het volgende voorbeeld worden de factureringstarieven weergegeven die zijn ingesteld op basis van de rol en de organisatie-eenheid waartoe de resource behoort.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="e8ec7-133">Kostentarieven zijn meestal gebaseerd op de salarisbandbreedte van de werknemer en de organisatie-eenheid waartoe deze behoort.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="e8ec7-134">In dit voorbeeld zien de tabellen met facturerings- en kostentarieven er als volgt uit.</span><span class="sxs-lookup"><span data-stu-id="e8ec7-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="e8ec7-135">**Voorbeeld van factureringstarieven**</span><span class="sxs-lookup"><span data-stu-id="e8ec7-135">**Sample bill rates**</span></span>

| <span data-ttu-id="e8ec7-136">Rol</span><span class="sxs-lookup"><span data-stu-id="e8ec7-136">Role</span></span>        | <span data-ttu-id="e8ec7-137">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="e8ec7-137">Org Unit</span></span>    |<span data-ttu-id="e8ec7-138">Eenheid</span><span class="sxs-lookup"><span data-stu-id="e8ec7-138">Unit</span></span>      |<span data-ttu-id="e8ec7-139">Prijs</span><span class="sxs-lookup"><span data-stu-id="e8ec7-139">Price</span></span>      |<span data-ttu-id="e8ec7-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="e8ec7-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e8ec7-141">Ontwikkelaar</span><span class="sxs-lookup"><span data-stu-id="e8ec7-141">Developer</span></span>   | <span data-ttu-id="e8ec7-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e8ec7-142">Contoso US</span></span>  |<span data-ttu-id="e8ec7-143">Hour</span><span class="sxs-lookup"><span data-stu-id="e8ec7-143">Hour</span></span> | <span data-ttu-id="e8ec7-144">200</span><span class="sxs-lookup"><span data-stu-id="e8ec7-144">200</span></span>|<span data-ttu-id="e8ec7-145">USD</span><span class="sxs-lookup"><span data-stu-id="e8ec7-145">USD</span></span>     |
| <span data-ttu-id="e8ec7-146">Ontwikkelaar</span><span class="sxs-lookup"><span data-stu-id="e8ec7-146">Developer</span></span>   | <span data-ttu-id="e8ec7-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e8ec7-147">Contoso India</span></span> |<span data-ttu-id="e8ec7-148">Hour</span><span class="sxs-lookup"><span data-stu-id="e8ec7-148">Hour</span></span>|   <span data-ttu-id="e8ec7-149">112</span><span class="sxs-lookup"><span data-stu-id="e8ec7-149">112</span></span>|<span data-ttu-id="e8ec7-150">USD</span><span class="sxs-lookup"><span data-stu-id="e8ec7-150">USD</span></span>     |


<span data-ttu-id="e8ec7-151">**Voorbeeld van kostentarieven**</span><span class="sxs-lookup"><span data-stu-id="e8ec7-151">**Sample cost rates**</span></span>

| <span data-ttu-id="e8ec7-152">Salarisbandbreedte</span><span class="sxs-lookup"><span data-stu-id="e8ec7-152">Salary Band</span></span>     | <span data-ttu-id="e8ec7-153">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="e8ec7-153">Org Unit</span></span>    |<span data-ttu-id="e8ec7-154">Eenheid</span><span class="sxs-lookup"><span data-stu-id="e8ec7-154">Unit</span></span>      |<span data-ttu-id="e8ec7-155">Prijs</span><span class="sxs-lookup"><span data-stu-id="e8ec7-155">Price</span></span>      |<span data-ttu-id="e8ec7-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="e8ec7-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e8ec7-157">Mijn bedrijf_Bandbreedte1</span><span class="sxs-lookup"><span data-stu-id="e8ec7-157">My company_Band1</span></span> | <span data-ttu-id="e8ec7-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e8ec7-158">Contoso US</span></span>  |<span data-ttu-id="e8ec7-159">Hour</span><span class="sxs-lookup"><span data-stu-id="e8ec7-159">Hour</span></span> | <span data-ttu-id="e8ec7-160">145</span><span class="sxs-lookup"><span data-stu-id="e8ec7-160">145</span></span>|<span data-ttu-id="e8ec7-161">USD</span><span class="sxs-lookup"><span data-stu-id="e8ec7-161">USD</span></span>     |
| <span data-ttu-id="e8ec7-162">Mijn bedrijf_Bandbreedte2</span><span class="sxs-lookup"><span data-stu-id="e8ec7-162">My company_Band2</span></span> | <span data-ttu-id="e8ec7-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e8ec7-163">Contoso India</span></span> |<span data-ttu-id="e8ec7-164">Hour</span><span class="sxs-lookup"><span data-stu-id="e8ec7-164">Hour</span></span>|   <span data-ttu-id="e8ec7-165">67</span><span class="sxs-lookup"><span data-stu-id="e8ec7-165">67</span></span>|<span data-ttu-id="e8ec7-166">USD</span><span class="sxs-lookup"><span data-stu-id="e8ec7-166">USD</span></span>     |

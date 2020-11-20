---
title: Projectcategorieën configureren
description: In dit onderwerp krijgt u informatie over het instellen van projectcategorieën.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131922"
---
# <a name="configure-project-categories"></a><span data-ttu-id="3ba99-103">Projectcategorieën configureren</span><span class="sxs-lookup"><span data-stu-id="3ba99-103">Configure project categories</span></span>

<span data-ttu-id="3ba99-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="3ba99-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3ba99-105">Project Operations biedt robuuste mogelijkheden voor het categoriseren van omzet en onkosten voor projecten.</span><span class="sxs-lookup"><span data-stu-id="3ba99-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="3ba99-106">Categorieën bieden de mogelijkheid om te rapporteren over projecttransacties, deze te analyseren en het boeken naar het grootboek te stimuleren.</span><span class="sxs-lookup"><span data-stu-id="3ba99-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="3ba99-107">Het volgende diagram illustreert de correlatie tussen transactiecategorieën, gedeelde categorieën en projectcategorieën.</span><span class="sxs-lookup"><span data-stu-id="3ba99-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="3ba99-108">Transactiecategorieën vormen de basisgroepering voor projecttransacties.</span><span class="sxs-lookup"><span data-stu-id="3ba99-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="3ba99-109">Binnen die groepering bestaat er een verzameling gedeelde categorieën die kunnen worden gedeeld tussen toepassingen en modules.</span><span class="sxs-lookup"><span data-stu-id="3ba99-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="3ba99-110">Projectcategorieën zijn het meest gedetailleerde niveau van categorieën.</span><span class="sxs-lookup"><span data-stu-id="3ba99-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="3ba99-111">Projectcategorieën hebben specifiek betrekking op rechtspersonen, modules en toepassingen.</span><span class="sxs-lookup"><span data-stu-id="3ba99-111">Project categories are specific to legal entity, module, and application.</span></span>

![Correlatie tussen transactiecategorieën, gedeelde categorieën en projectcategorieën](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="3ba99-113">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="3ba99-113">Transaction categories</span></span>

<span data-ttu-id="3ba99-114">Transactiecategorieën vertegenwoordigen de basisgroepering voor projecttransacties en zijn niet specifiek gerelateerd aan een bedrijf of transactietype.</span><span class="sxs-lookup"><span data-stu-id="3ba99-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="3ba99-115">Contoso Robotics gebruikt bijvoorbeeld de transactiecategorieën Ontwerp, Reizen, Installatie en Service om projecttransacties te groeperen.</span><span class="sxs-lookup"><span data-stu-id="3ba99-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="3ba99-116">Transactiecategorieën worden gedefinieerd in de Project Operations-module.</span><span class="sxs-lookup"><span data-stu-id="3ba99-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="3ba99-117">Ga naar **Instellingen** \> **Transactiecategorieën** om het formulier te openen.</span><span class="sxs-lookup"><span data-stu-id="3ba99-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="3ba99-118">Maak een nieuwe transactiecategorie door **Nieuw** of **Importeren vanuit Excel** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3ba99-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="3ba99-119">Gedeelde categorieën</span><span class="sxs-lookup"><span data-stu-id="3ba99-119">Shared categories</span></span>

<span data-ttu-id="3ba99-120">In Dynamics 365 wordt het concept Gedeelde categorieën gebruikt om onkosten in verschillende toepassingen te categoriseren, zoals Dynamics 365 Finance, Dynamics 365 Supply Chain en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3ba99-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="3ba99-121">Voor elke gemaakte transactiecategorie worden in Project Operations automatisch vier gerelateerde gedeelde categorieën gemaakt: Uren, Onkosten, Tarieven en Artikel.</span><span class="sxs-lookup"><span data-stu-id="3ba99-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="3ba99-122">U kunt de gedeelde categorieën bekijken en aanpassen door naar **Projectmanagement en financiële administratie** \> **Instellingen** \> **Categorieën** \> **Gedeelde categorieën** te gaan.</span><span class="sxs-lookup"><span data-stu-id="3ba99-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="3ba99-123">Productcategorieën</span><span class="sxs-lookup"><span data-stu-id="3ba99-123">Project categories</span></span>

<span data-ttu-id="3ba99-124">Projectcategorieën staan voor het meest gedetailleerde niveau van categorieconfiguratie en moeten afzonderlijk en voor elk bedrijf worden geconfigureerd door een projectaccountant.</span><span class="sxs-lookup"><span data-stu-id="3ba99-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="3ba99-125">Ga naar **Projectmanagement en financiële administratie** \> **Instellingen** \> **Categorieën** \> **Projectcategorieën**.</span><span class="sxs-lookup"><span data-stu-id="3ba99-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="3ba99-126">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="3ba99-126">Select **New**.</span></span>
3. <span data-ttu-id="3ba99-127">Selecteer de **categorie-id** van de gedeelde categorie die u in de vorige sectie hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3ba99-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="3ba99-128">Met Project Operations kunt u ook alleen die gedeelde categorieën gebruiken die aan transactiecategorieën zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="3ba99-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="3ba99-129">Selecteer een categoriegroep.</span><span class="sxs-lookup"><span data-stu-id="3ba99-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="3ba99-130">Categoriegroepen</span><span class="sxs-lookup"><span data-stu-id="3ba99-130">Category groups</span></span>

<span data-ttu-id="3ba99-131">Categoriegroepen worden gebruikt om eigenschappen, voornamelijk boekingsprofielen, te delen tussen gerelateerde projectcategorieën.</span><span class="sxs-lookup"><span data-stu-id="3ba99-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="3ba99-132">Er moet minimaal één categoriegroep zijn voor elk transactietype en aan elke projectcategorie wordt een groep toegewezen.</span><span class="sxs-lookup"><span data-stu-id="3ba99-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="3ba99-133">De boekingsspecificaties in Project Operations worden gedefinieerd door de profielregels voor projectkosten en -inkomsten, projectcategorieën en categoriegroepen.</span><span class="sxs-lookup"><span data-stu-id="3ba99-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="3ba99-134">U kunt categoriegroepen instellen door naar **Projectmanagement en financiële administratie** \> **Instellingen** \> **Categorieën** \> **Categoriegroepen** te gaan.</span><span class="sxs-lookup"><span data-stu-id="3ba99-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>

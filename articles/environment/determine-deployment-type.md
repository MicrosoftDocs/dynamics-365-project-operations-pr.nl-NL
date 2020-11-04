---
title: Het type implementatie bepalen
description: Dit onderwerp biedt informatie waarmee u het juiste implementatietype van projectactiviteiten voor uw bedrijf kunt bepalen.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074568"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="3dfb3-103">Het type implementatie bepalen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-103">Determine your deployment type</span></span>

<span data-ttu-id="3dfb3-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="3dfb3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3dfb3-105">Nadat u de licentie hebt aangeschaft, begint u hier om het beste implementatiemodel van Dynamics 365 Project Operations te bepalen met behulp van de [begeleide installatiestroom](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="3dfb3-106">Nadat u de begeleide installatiestroom hebt voltooid, wordt u naar de juiste beheerportal geleid om uw installatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="3dfb3-107">Zie de implementatiedetails om de installatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="3dfb3-108">Bestaande klanten van Dynamics die Dynamics 365 Project Service Automation gebruiken</span><span class="sxs-lookup"><span data-stu-id="3dfb3-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="3dfb3-109">Project Operations omvat de mogelijkheden die bij Project Service Automation worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="3dfb3-110">Voor deze klanten wordt in de toekomst een upgradepad vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="3dfb3-111">Bestaande klanten van Dynamics 365 Finance die Projectmanagement en financiële administratie gebruiken</span><span class="sxs-lookup"><span data-stu-id="3dfb3-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="3dfb3-112">Bestaande klanten van Finance die gebruikmaken van de functionaliteit Projectmanagement en financiële administratie, kunnen dit zo blijven doen.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="3dfb3-113">Zie [Project Operations voor scenario's op basis van voorradige artikelen/productieorders](#pma).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="3dfb3-114">Implementatietypen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-114">Deployment types</span></span>
<span data-ttu-id="3dfb3-115">Project Operations ondersteunt meerdere implementatieopties om aan uw vereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="3dfb3-116">Of u nu een nieuwe of bestaande Dynamics 365-klant bent, Project Operations kan uw behoeften ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="3dfb3-117">Onze [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations) helpt u de juiste implementatie te kiezen.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="3dfb3-118">De resultaten leiden u naar een van de volgende implementatietypen:</span><span class="sxs-lookup"><span data-stu-id="3dfb3-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="3dfb3-119">Lite-implementatie – van deal tot pro-formafacturering</span><span class="sxs-lookup"><span data-stu-id="3dfb3-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="3dfb3-120">Project Operations voor scenario's op basis van resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="3dfb3-121">Project Operations voor scenario's op basis van voorradige artikelen/productieorders</span><span class="sxs-lookup"><span data-stu-id="3dfb3-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="3dfb3-122">Project Operations ondersteunt scenario's op basis van voorradige artikelen/productieorders en scenario's op basis van niet-voorradige artikelen/resources in dezelfde omgeving via configuraties op rechtspersoonsniveau.</span><span class="sxs-lookup"><span data-stu-id="3dfb3-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="3dfb3-123">Contoso kan bijvoorbeeld de mogelijkheden voor voorradige artikelen/productieorder gebruiken in de productiefaciliteit in de VS (rechtspersoon = Contoso Manufacturing, Verenigde Staten).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="3dfb3-124">Contoso kan de mogelijkheden voor niet-voorradige artikelen/resource gebruiken in hun servicefaciliteit voor Contoso Robotics Arms in het VK (rechtspersoon = Contoso Robotics Verenigd Koninkrijk).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="3dfb3-125">Vereenvoudigde implementatie - van deal tot pro-formafacturering</span><span class="sxs-lookup"><span data-stu-id="3dfb3-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="3dfb3-126">De Lite-implementatie omvat de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="3dfb3-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="3dfb3-127">Projectplanning met Microsoft Project voor het web</span><span class="sxs-lookup"><span data-stu-id="3dfb3-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="3dfb3-128">Multidimensionale prijzen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="3dfb3-129">Geïntegreerd resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="3dfb3-129">Unified Resource Management</span></span>
- <span data-ttu-id="3dfb3-130">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="3dfb3-130">Time Tracking</span></span>
- <span data-ttu-id="3dfb3-131">Basisonkosten</span><span class="sxs-lookup"><span data-stu-id="3dfb3-131">Basic Expense</span></span>
- <span data-ttu-id="3dfb3-132">Factuurvoorstel</span><span class="sxs-lookup"><span data-stu-id="3dfb3-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3dfb3-133">Installatiestappen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-133">Deployment steps</span></span>
<span data-ttu-id="3dfb3-134">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3dfb3-135">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](lite-preview-subscription-sign-up.md) en [Nieuwe omgeving inrichten](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="3dfb3-136">Project Operations voor scenario's op basis van resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="3dfb3-137">Project Operations biedt voor scenario's voor resources/niet-voorradige artikelen de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="3dfb3-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="3dfb3-138">Projectplanning met Microsoft Project voor het web</span><span class="sxs-lookup"><span data-stu-id="3dfb3-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="3dfb3-139">Multidimensionale prijzen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="3dfb3-140">Geïntegreerd resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="3dfb3-140">Unified Resource Management</span></span>
- <span data-ttu-id="3dfb3-141">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="3dfb3-141">Time Tracking</span></span>
- <span data-ttu-id="3dfb3-142">Basisonkosten</span><span class="sxs-lookup"><span data-stu-id="3dfb3-142">Basic Expense</span></span>
- <span data-ttu-id="3dfb3-143">Volledige onkosten</span><span class="sxs-lookup"><span data-stu-id="3dfb3-143">Full Expense</span></span>
- <span data-ttu-id="3dfb3-144">OCR ontvangst</span><span class="sxs-lookup"><span data-stu-id="3dfb3-144">Receipt OCR</span></span>
- <span data-ttu-id="3dfb3-145">Volledige facturering</span><span class="sxs-lookup"><span data-stu-id="3dfb3-145">Full Invoicing</span></span>
- <span data-ttu-id="3dfb3-146">Omzetverantwoording</span><span class="sxs-lookup"><span data-stu-id="3dfb3-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3dfb3-147">Installatiestappen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-147">Deployment steps</span></span>
<span data-ttu-id="3dfb3-148">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3dfb3-149">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](resource-sign-up-preview-subscription.md) en [Nieuwe omgeving inrichten](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="3dfb3-150">Project Operations voor scenario's op basis van voorradige artikelen/productieorders</span><span class="sxs-lookup"><span data-stu-id="3dfb3-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="3dfb3-151">Projectplanning met structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="3dfb3-151">Project planning using WBS</span></span>
- <span data-ttu-id="3dfb3-152">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="3dfb3-152">Resource Management</span></span>
- <span data-ttu-id="3dfb3-153">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="3dfb3-153">Time Tracking</span></span>
- <span data-ttu-id="3dfb3-154">Volledige onkosten</span><span class="sxs-lookup"><span data-stu-id="3dfb3-154">Full Expense</span></span>
- <span data-ttu-id="3dfb3-155">OCR ontvangst</span><span class="sxs-lookup"><span data-stu-id="3dfb3-155">Receipt OCR</span></span>
- <span data-ttu-id="3dfb3-156">Volledige facturering</span><span class="sxs-lookup"><span data-stu-id="3dfb3-156">Full Invoicing</span></span>
- <span data-ttu-id="3dfb3-157">Omzetverantwoording</span><span class="sxs-lookup"><span data-stu-id="3dfb3-157">Revenue Recognition</span></span>
- <span data-ttu-id="3dfb3-158">Productieorders</span><span class="sxs-lookup"><span data-stu-id="3dfb3-158">Production Orders</span></span>
- <span data-ttu-id="3dfb3-159">Ondersteuning voor materiaal</span><span class="sxs-lookup"><span data-stu-id="3dfb3-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3dfb3-160">Installatiestappen</span><span class="sxs-lookup"><span data-stu-id="3dfb3-160">Deployment steps</span></span>
<span data-ttu-id="3dfb3-161">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3dfb3-162">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) en [Nieuwe omgeving inrichten](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="3dfb3-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 


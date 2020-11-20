---
title: Het type implementatie bepalen
description: Dit onderwerp biedt informatie waarmee u het juiste implementatietype van projectactiviteiten voor uw bedrijf kunt bepalen.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401212"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="7239c-103">Het type implementatie bepalen</span><span class="sxs-lookup"><span data-stu-id="7239c-103">Determine your deployment type</span></span>

<span data-ttu-id="7239c-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="7239c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7239c-105">Nadat u de licentie hebt aangeschaft, begint u hier om het beste implementatiemodel van Dynamics 365 Project Operations te bepalen met behulp van de [begeleide installatiestroom](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7239c-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="7239c-106">Nadat u de begeleide installatiestroom hebt voltooid, wordt u naar de juiste beheerportal geleid om uw installatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="7239c-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="7239c-107">Zie de implementatiedetails om de installatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="7239c-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="7239c-108">Bestaande klanten van Dynamics die Dynamics 365 Project Service Automation gebruiken</span><span class="sxs-lookup"><span data-stu-id="7239c-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="7239c-109">Project Operations omvat de mogelijkheden die bij Project Service Automation worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="7239c-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="7239c-110">In releasewave 1 van 2021 wordt voor deze klanten een upgradepad vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="7239c-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="7239c-111">Bestaande klanten van Dynamics 365 Finance die Projectmanagement en financiële administratie gebruiken</span><span class="sxs-lookup"><span data-stu-id="7239c-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="7239c-112">Bestaande klanten van Finance die de functionaliteit Projectbeheer en financiële administratie gebruiken, kunnen deze gewoon blijven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7239c-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="7239c-113">Zie [Project Operations voor scenario's op basis van voorradige artikelen/productieorders](#pma).</span><span class="sxs-lookup"><span data-stu-id="7239c-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="7239c-114">Implementatietypen</span><span class="sxs-lookup"><span data-stu-id="7239c-114">Deployment types</span></span>
<span data-ttu-id="7239c-115">Project Operations ondersteunt meerdere implementatieopties om aan uw vereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="7239c-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="7239c-116">Of u nu een nieuwe of bestaande Dynamics 365-klant bent, Project Operations kan uw behoeften ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="7239c-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="7239c-117">Onze [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations) helpt u de juiste implementatie te kiezen.</span><span class="sxs-lookup"><span data-stu-id="7239c-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="7239c-118">De resultaten leiden u naar een van de volgende implementatietypen:</span><span class="sxs-lookup"><span data-stu-id="7239c-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="7239c-119">Lite-implementatie – van deal tot pro-formafacturering</span><span class="sxs-lookup"><span data-stu-id="7239c-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="7239c-120">Project Operations voor scenario's op basis van resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="7239c-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="7239c-121">Project Operations voor scenario's op basis van voorradige artikelen/productieorders</span><span class="sxs-lookup"><span data-stu-id="7239c-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="7239c-122">Project Operations ondersteunt scenario's op basis van voorradige artikelen/productieorders en scenario's op basis van niet-voorradige artikelen/resources in dezelfde omgeving via configuraties op rechtspersoonsniveau.</span><span class="sxs-lookup"><span data-stu-id="7239c-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="7239c-123">Contoso kan bijvoorbeeld de mogelijkheden voor voorradige artikelen/productieorder gebruiken in de productiefaciliteit in de VS (rechtspersoon = Contoso Manufacturing, Verenigde Staten).</span><span class="sxs-lookup"><span data-stu-id="7239c-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="7239c-124">Contoso kan de mogelijkheden voor niet-voorradige artikelen/resource gebruiken in hun servicefaciliteit voor Contoso Robotics Arms in het VK (rechtspersoon = Contoso Robotics Verenigd Koninkrijk).</span><span class="sxs-lookup"><span data-stu-id="7239c-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="7239c-125">Vereenvoudigde implementatie - van deal tot pro-formafacturering</span><span class="sxs-lookup"><span data-stu-id="7239c-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="7239c-126">De Lite-implementatie omvat de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="7239c-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="7239c-127">Verkoopproces voor projecten waarbij de voorzieningen van Dynamics 365 Sales-toepassingen worden uitgebreid</span><span class="sxs-lookup"><span data-stu-id="7239c-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="7239c-128">Projectplanning met Microsoft Project voor het web</span><span class="sxs-lookup"><span data-stu-id="7239c-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7239c-129">Multidimensionale prijzen</span><span class="sxs-lookup"><span data-stu-id="7239c-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7239c-130">Geïntegreerd resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="7239c-130">Unified resource management</span></span>
- <span data-ttu-id="7239c-131">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="7239c-131">Time tracking</span></span>
- <span data-ttu-id="7239c-132">Basisonkosten</span><span class="sxs-lookup"><span data-stu-id="7239c-132">Basic expense</span></span>
- <span data-ttu-id="7239c-133">Pro-forma- en klantgerichte facturering</span><span class="sxs-lookup"><span data-stu-id="7239c-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="7239c-134">Installatiestappen</span><span class="sxs-lookup"><span data-stu-id="7239c-134">Deployment steps</span></span>
<span data-ttu-id="7239c-135">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7239c-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7239c-136">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](lite-preview-subscription-sign-up.md) en [Nieuwe omgeving inrichten](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="7239c-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="7239c-137">Project Operations voor scenario's op basis van resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="7239c-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="7239c-138">Project Operations biedt voor scenario's voor resources/niet-voorradige artikelen de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="7239c-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="7239c-139">Verkoopproces voor projecten waarbij de Dynamics 365 Sales-toepassing wordt uitgebreid</span><span class="sxs-lookup"><span data-stu-id="7239c-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="7239c-140">Projectplanning met Microsoft Project voor het web</span><span class="sxs-lookup"><span data-stu-id="7239c-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7239c-141">Multidimensionale prijzen</span><span class="sxs-lookup"><span data-stu-id="7239c-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7239c-142">Geïntegreerd resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="7239c-142">Unified resource management</span></span>
- <span data-ttu-id="7239c-143">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="7239c-143">Time tracking</span></span>
- <span data-ttu-id="7239c-144">Basisonkosten</span><span class="sxs-lookup"><span data-stu-id="7239c-144">Basic expense</span></span>
- <span data-ttu-id="7239c-145">Volledige onkosten</span><span class="sxs-lookup"><span data-stu-id="7239c-145">Full expense</span></span>
- <span data-ttu-id="7239c-146">OCR ontvangst</span><span class="sxs-lookup"><span data-stu-id="7239c-146">Receipt OCR</span></span>
- <span data-ttu-id="7239c-147">Pro-forma- en klantgerichte facturering</span><span class="sxs-lookup"><span data-stu-id="7239c-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="7239c-148">Opbrengstverantwoording voor projecten</span><span class="sxs-lookup"><span data-stu-id="7239c-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7239c-149">Installatiestappen</span><span class="sxs-lookup"><span data-stu-id="7239c-149">Deployment steps</span></span>
<span data-ttu-id="7239c-150">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7239c-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7239c-151">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](resource-sign-up-preview-subscription.md) en [Nieuwe omgeving inrichten](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7239c-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="7239c-152">Project Operations voor scenario's op basis van voorradige artikelen/productieorders</span><span class="sxs-lookup"><span data-stu-id="7239c-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="7239c-153">Projectplanning met structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="7239c-153">Project planning using WBS</span></span>
- <span data-ttu-id="7239c-154">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="7239c-154">Resource Management</span></span>
- <span data-ttu-id="7239c-155">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="7239c-155">Time Tracking</span></span>
- <span data-ttu-id="7239c-156">Volledige onkosten</span><span class="sxs-lookup"><span data-stu-id="7239c-156">Full Expense</span></span>
- <span data-ttu-id="7239c-157">OCR ontvangst</span><span class="sxs-lookup"><span data-stu-id="7239c-157">Receipt OCR</span></span>
- <span data-ttu-id="7239c-158">Volledige facturering</span><span class="sxs-lookup"><span data-stu-id="7239c-158">Full Invoicing</span></span>
- <span data-ttu-id="7239c-159">Omzetverantwoording</span><span class="sxs-lookup"><span data-stu-id="7239c-159">Revenue Recognition</span></span>
- <span data-ttu-id="7239c-160">Productieorders</span><span class="sxs-lookup"><span data-stu-id="7239c-160">Production Orders</span></span>
- <span data-ttu-id="7239c-161">Ondersteuning voor materiaal</span><span class="sxs-lookup"><span data-stu-id="7239c-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7239c-162">Installatiestappen</span><span class="sxs-lookup"><span data-stu-id="7239c-162">Deployment steps</span></span>
<span data-ttu-id="7239c-163">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7239c-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7239c-164">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) en [Nieuwe omgeving inrichten](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7239c-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 


---
title: Implementatietypen
description: Dit onderwerp biedt informatie waarmee u het juiste implementatietype van projectactiviteiten voor uw bedrijf kunt bepalen.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948818"
---
# <a name="deployment-types"></a><span data-ttu-id="5e3f2-103">Implementatietypen</span><span class="sxs-lookup"><span data-stu-id="5e3f2-103">Deployment types</span></span>

<span data-ttu-id="5e3f2-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="5e3f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e3f2-105">Nadat u de licentie hebt aangeschaft, begint u hier om het beste implementatiemodel van Dynamics 365 Project Operations te bepalen met behulp van de [begeleide installatiestroom](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="5e3f2-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="5e3f2-106">Nadat u de begeleide installatiestroom hebt voltooid, wordt u naar de juiste beheerportal geleid om uw installatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="5e3f2-107">Zie de implementatiedetails hieronder om de installatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="5e3f2-108">Bestaande klanten van Dynamics die Dynamics 365 Project Service Automation gebruiken</span><span class="sxs-lookup"><span data-stu-id="5e3f2-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="5e3f2-109">Project Operations omvat de mogelijkheden die bij Project Service Automation worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="5e3f2-110">Voor deze klanten wordt in de toekomst een upgradepad vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="5e3f2-111">Bestaande klanten van Dynamics 365 Finance die Projectmanagement en financiële administratie gebruiken</span><span class="sxs-lookup"><span data-stu-id="5e3f2-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="5e3f2-112">Bestaande klanten van Finance die gebruikmaken van de functionaliteit Projectmanagement en financiële administratie, kunnen dit zo blijven doen.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="5e3f2-113">Zie [Project Operations voor scenario's op basis van voorradige artikelen/productieorders](#pma).</span><span class="sxs-lookup"><span data-stu-id="5e3f2-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="5e3f2-114">Project Operations ondersteunt meerdere implementatieopties om aan uw vereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="5e3f2-115">Of u nu een nieuwe of bestaande Dynamics 365-klant bent, Project Operations kan uw behoeften ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="5e3f2-116">Onze [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations) helpt u de juiste implementatie te kiezen.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="5e3f2-117">De resultaten leiden u naar een van de volgende implementatietypen:</span><span class="sxs-lookup"><span data-stu-id="5e3f2-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="5e3f2-118">Lite-implementatie – van deal tot pro-formafacturering</span><span class="sxs-lookup"><span data-stu-id="5e3f2-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="5e3f2-119">Project Operations voor scenario's op basis van resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="5e3f2-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="5e3f2-120">Project Operations voor scenario's op basis van voorradige artikelen/productieorders</span><span class="sxs-lookup"><span data-stu-id="5e3f2-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="5e3f2-121">Project Operations ondersteunt scenario's op basis van voorradige artikelen/productieorders en scenario's op basis van niet-voorradige artikelen/resources in dezelfde omgeving via configuraties op rechtspersoonsniveau.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="5e3f2-122">Contoso kan bijvoorbeeld capaciteit voor voorradige artikelen/productieorders in hun Amerikaanse productiefaciliteit (Rechtspersoon = Contoso Manufacturing United States) en capaciteit voor niet-voorradige artikelen/resourcegebaseerde artikelen in hun Contoso Robotics Arms-servicefaciliteit in het VK (Rechtspersoon = Contoso Robotics United Kingdom) benutten.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="5e3f2-123"><a name="lite"><a/>Vereenvoudigde implementatie - van deal tot pro-formafacturering</span><span class="sxs-lookup"><span data-stu-id="5e3f2-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="5e3f2-124">De Lite-implementatie omvat de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="5e3f2-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="5e3f2-125">Projectplanning met Microsoft Project voor het web</span><span class="sxs-lookup"><span data-stu-id="5e3f2-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="5e3f2-126">Multidimensionale prijzen</span><span class="sxs-lookup"><span data-stu-id="5e3f2-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="5e3f2-127">Geïntegreerd resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="5e3f2-127">Unified Resource Management</span></span>
- <span data-ttu-id="5e3f2-128">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="5e3f2-128">Time Tracking</span></span>
- <span data-ttu-id="5e3f2-129">Basisonkosten</span><span class="sxs-lookup"><span data-stu-id="5e3f2-129">Basic Expense</span></span>
- <span data-ttu-id="5e3f2-130">Factuurvoorstel</span><span class="sxs-lookup"><span data-stu-id="5e3f2-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="5e3f2-131">Implementatiestappen:</span><span class="sxs-lookup"><span data-stu-id="5e3f2-131">Deployment steps:</span></span>
<span data-ttu-id="5e3f2-132">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="5e3f2-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5e3f2-133">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](lite-preview-subscription-sign-up.md) en [Nieuwe omgeving inrichten](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="5e3f2-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="5e3f2-134"><a name="integrated"><a/>Project Operations voor scenario's op basis van resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="5e3f2-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="5e3f2-135">Project Operations biedt voor scenario's voor resources/niet-voorradige artikelen de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="5e3f2-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="5e3f2-136">Projectplanning met Microsoft Project voor het web</span><span class="sxs-lookup"><span data-stu-id="5e3f2-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="5e3f2-137">Multidimensionale prijzen</span><span class="sxs-lookup"><span data-stu-id="5e3f2-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="5e3f2-138">Geïntegreerd resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="5e3f2-138">Unified Resource Management</span></span>
- <span data-ttu-id="5e3f2-139">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="5e3f2-139">Time Tracking</span></span>
- <span data-ttu-id="5e3f2-140">Basisonkosten</span><span class="sxs-lookup"><span data-stu-id="5e3f2-140">Basic Expense</span></span>
- <span data-ttu-id="5e3f2-141">Volledige onkosten</span><span class="sxs-lookup"><span data-stu-id="5e3f2-141">Full Expense</span></span>
- <span data-ttu-id="5e3f2-142">OCR ontvangst</span><span class="sxs-lookup"><span data-stu-id="5e3f2-142">Receipt OCR</span></span>
- <span data-ttu-id="5e3f2-143">Volledige facturering</span><span class="sxs-lookup"><span data-stu-id="5e3f2-143">Full Invoicing</span></span>
- <span data-ttu-id="5e3f2-144">Omzetverantwoording</span><span class="sxs-lookup"><span data-stu-id="5e3f2-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="5e3f2-145">Implementatiestappen:</span><span class="sxs-lookup"><span data-stu-id="5e3f2-145">Deployment steps:</span></span>
<span data-ttu-id="5e3f2-146">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="5e3f2-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5e3f2-147">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](resource-sign-up-preview-subscription.md) en [Nieuwe omgeving inrichten](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5e3f2-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="5e3f2-148">Project Operations voor scenario's op basis van voorradige artikelen/productieorders</span><span class="sxs-lookup"><span data-stu-id="5e3f2-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="5e3f2-149">Projectplanning met structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="5e3f2-149">Project planning using WBS</span></span>
- <span data-ttu-id="5e3f2-150">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="5e3f2-150">Resource Management</span></span>
- <span data-ttu-id="5e3f2-151">Tijden bijhouden</span><span class="sxs-lookup"><span data-stu-id="5e3f2-151">Time Tracking</span></span>
- <span data-ttu-id="5e3f2-152">Volledige onkosten</span><span class="sxs-lookup"><span data-stu-id="5e3f2-152">Full Expense</span></span>
- <span data-ttu-id="5e3f2-153">OCR ontvangst</span><span class="sxs-lookup"><span data-stu-id="5e3f2-153">Receipt OCR</span></span>
- <span data-ttu-id="5e3f2-154">Volledige facturering</span><span class="sxs-lookup"><span data-stu-id="5e3f2-154">Full Invoicing</span></span>
- <span data-ttu-id="5e3f2-155">Omzetverantwoording</span><span class="sxs-lookup"><span data-stu-id="5e3f2-155">Revenue Recognition</span></span>
- <span data-ttu-id="5e3f2-156">Productieorders</span><span class="sxs-lookup"><span data-stu-id="5e3f2-156">Production Orders</span></span>
- <span data-ttu-id="5e3f2-157">Ondersteuning voor materiaal</span><span class="sxs-lookup"><span data-stu-id="5e3f2-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="5e3f2-158">Implementatiestappen:</span><span class="sxs-lookup"><span data-stu-id="5e3f2-158">Deployment steps:</span></span>
<span data-ttu-id="5e3f2-159">Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="5e3f2-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5e3f2-160">Zie voor deze implementatie [Aanmelden voor preview-abonnementen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) en [Nieuwe omgeving inrichten](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="5e3f2-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 




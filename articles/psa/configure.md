---
title: Project Service Automation configureren
description: Stappen voor het configureren van Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129177"
---
# <a name="configure-project-service"></a><span data-ttu-id="ab34b-103">Project Service configureren</span><span class="sxs-lookup"><span data-stu-id="ab34b-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ab34b-104">Voordat u de automatiseringsmogelijkheden van de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] kunt gebruiken om uw projecten, accounts en resources te beheren dient u enkele configuratiestappen te voltooien om ervoor te zorgen dat de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-oplossing beantwoordt aan de behoeften van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="ab34b-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="ab34b-105">Hieronder vallen de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="ab34b-105">These steps include:</span></span>  
  
-   <span data-ttu-id="ab34b-106">[Tijdseenheden configureren](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="ab34b-107">Configureer de tijdseenheden in de productcatalogus die u als uitgangspunt voor het planning en de facturering van uw projecten wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ab34b-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="ab34b-108">[Valuta´s en wisselkoersen configureren](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="ab34b-109">Setup de valuta die u wilt gebruiken voor uw projecten.</span><span class="sxs-lookup"><span data-stu-id="ab34b-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="ab34b-110">[Organisatie-eenheden maken](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="ab34b-111">Stel de groepen in die uw organisatie gebruikt om zijn zaken, of via geografie, bedrijfsfunctie of andere logische divisie te scheiden.</span><span class="sxs-lookup"><span data-stu-id="ab34b-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="ab34b-112">[Factuurfrequenties configureren](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="ab34b-113">Stel tijdperiodes in die u voor facturering van uw kanten wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ab34b-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="ab34b-114">[Transactiecategorieën configureren](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="ab34b-115">Stel de transactiecategorieën in waar uw adviseurs de factureerbare en niet-factureerbare onkosten kunnen invoeren.</span><span class="sxs-lookup"><span data-stu-id="ab34b-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="ab34b-116">[Onkostencategorieën configureren](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="ab34b-117">Stel de categorieën in waar uw consultants de factureerbare en niet-factureerbare onkosten kunnen invoeren.</span><span class="sxs-lookup"><span data-stu-id="ab34b-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="ab34b-118">[Productcatalogusitems maken](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="ab34b-119">Voeg de producten die u verkoopt aan de productcatalogus toe, zoals softwarelicenties.</span><span class="sxs-lookup"><span data-stu-id="ab34b-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="ab34b-120">[Een prijslijst maken](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="ab34b-121">Configureer andere prijslijsten, afhankelijk van hoeveel u uw kanten wilt berekenen voor elke rol die hun project vereist.</span><span class="sxs-lookup"><span data-stu-id="ab34b-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="ab34b-122">[Resources configureren](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="ab34b-123">Voeg de vaardigheden, bekwaamheden, resourcerollen en andere resourcegegevens toe die u voor uw projecten nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="ab34b-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ab34b-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ab34b-124">See Also</span></span>  
 <span data-ttu-id="ab34b-125">[Overzicht van Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="ab34b-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="ab34b-126">[Project Service Automation configureren](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="ab34b-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="ab34b-127">[Accountmanager-handleiding](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="ab34b-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="ab34b-128">[Projectmanager-handleiding](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="ab34b-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="ab34b-129">[Resourcemanager-handleiding](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="ab34b-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="ab34b-130">Handleiding Tijd, kosten, en samenwerken</span><span class="sxs-lookup"><span data-stu-id="ab34b-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)

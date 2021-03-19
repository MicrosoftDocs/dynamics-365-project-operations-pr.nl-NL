---
title: Handmatig een pro-formafactuur maken - lite
description: Dit onderwerp bevat informatie over het handmatig maken van pro-formafacturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274182"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="f1da5-103">Handmatig een pro-formafactuur maken - lite</span><span class="sxs-lookup"><span data-stu-id="f1da5-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="f1da5-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="f1da5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f1da5-105">In Dynamics 365 Project Operations kunnen pro-formafacturen indien nodig handmatig worden aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="f1da5-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="f1da5-106">U kunt handmatig een pro-formafactuur maken op de lijstpagina **Projectcontracten** of op de detailpagina **Projectcontract**.</span><span class="sxs-lookup"><span data-stu-id="f1da5-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="f1da5-107">Lijstpagina Projectcontracten</span><span class="sxs-lookup"><span data-stu-id="f1da5-107">Project Contracts list page</span></span>

<span data-ttu-id="f1da5-108">Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten en maak facturen voor alle geselecteerde records.</span><span class="sxs-lookup"><span data-stu-id="f1da5-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="f1da5-109">Het systeem controleert welke van de geselecteerde projectcontracten een backlog heeft voor **Gereed voor facturering** die een datum heeft die vóór de datum van vandaag ligt.</span><span class="sxs-lookup"><span data-stu-id="f1da5-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="f1da5-110">Op basis van deze contracten worden conceptpro-formafacturen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f1da5-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="f1da5-111">Als een projectcontract meerdere klanten heeft, kan er één factuur per klant worden gemaakt en meerdere facturen per projectcontract.</span><span class="sxs-lookup"><span data-stu-id="f1da5-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="f1da5-112">Alle gemaakte projectfacturen zijn beschikbaar op de pagina **Factuur** in de sectie **Facturering** van het gebied **Verkoop**.</span><span class="sxs-lookup"><span data-stu-id="f1da5-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="f1da5-113">Detailpagina Projectcontract</span><span class="sxs-lookup"><span data-stu-id="f1da5-113">Project Contract details page</span></span>

<span data-ttu-id="f1da5-114">Een pro-formafactuur kan ook worden gemaakt op basis van de **Projectcontract**-detailpagina.</span><span class="sxs-lookup"><span data-stu-id="f1da5-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="f1da5-115">Het systeem verifieert welk projectcontract een backlog voor **Gereed voor facturering** heeft die een datum heeft die vóór de datum van vandaag ligt.</span><span class="sxs-lookup"><span data-stu-id="f1da5-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="f1da5-116">Op basis van deze contracten worden conceptpro-formafacturen gemaakt op basis van het aantal klanten op elke contractregel.</span><span class="sxs-lookup"><span data-stu-id="f1da5-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="f1da5-117">Als er één pro-formafactuur wordt gemaakt, wordt de pagina **Factuur** geopend.</span><span class="sxs-lookup"><span data-stu-id="f1da5-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="f1da5-118">Als er meerdere facturen worden aangemaakt voor dat projectcontract, opent de lijstpagina **Facturen** om alle gemaakte facturen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f1da5-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
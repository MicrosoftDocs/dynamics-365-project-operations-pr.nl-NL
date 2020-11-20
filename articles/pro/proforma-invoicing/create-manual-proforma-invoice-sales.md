---
title: Handmatig een pro-formafactuur maken - lite
description: Dit onderwerp bevat informatie over het handmatig maken van pro-formafacturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176380"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="d9b0b-103">Handmatig een pro-formafactuur maken - lite</span><span class="sxs-lookup"><span data-stu-id="d9b0b-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="d9b0b-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="d9b0b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d9b0b-105">In Dynamics 365 Project Operations kunnen pro-formafacturen indien nodig handmatig worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="d9b0b-106">U kunt handmatig een pro-formafactuur maken op de lijstpagina **Projectcontracten** of op de detailpagina **Projectcontract**.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="d9b0b-107">Lijstpagina Projectcontracten</span><span class="sxs-lookup"><span data-stu-id="d9b0b-107">Project Contracts list page</span></span>

<span data-ttu-id="d9b0b-108">Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten en maak facturen voor alle geselecteerde records.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="d9b0b-109">Er wordt gecontroleerd welke van de geselecteerde projectcontracten een achterstallige **Gereed voor facturering** heeft die een datum heeft die vóór de datum van vandaag ligt.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="d9b0b-110">Op basis van deze contracten worden conceptpro-formafacturen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="d9b0b-111">Als een projectcontract meerdere klanten heeft, kan er één factuur per klant worden gemaakt en meerdere facturen per projectcontract.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="d9b0b-112">Alle gemaakte projectfacturen zijn beschikbaar op de pagina **Factuur** in de sectie **Facturering** van het gebied **Verkoop**.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="d9b0b-113">Detailpagina Projectcontract</span><span class="sxs-lookup"><span data-stu-id="d9b0b-113">Project Contract details page</span></span>

<span data-ttu-id="d9b0b-114">Een pro-formafactuur kan ook worden gemaakt op de detailpagina **Projectcontract**, waarmee de factuur voor dat specifieke projectcontract wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="d9b0b-115">Er wordt gecontroleerd of het projectcontract een achterstallige **Gereed voor facturering** heeft die een datum heeft die vóór de datum van vandaag ligt.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="d9b0b-116">Op basis van deze contracten worden conceptpro-formafacturen gemaakt op basis van het aantal klanten op elke contractregel.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="d9b0b-117">Als er één pro-formafactuur wordt gemaakt, wordt de pagina **Factuur** geopend.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="d9b0b-118">Als er meerdere facturen zijn gemaakt voor dat projectcontract, dan wordt de lijstpagina **Facturen** geopend om alle gemaakte facturen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>

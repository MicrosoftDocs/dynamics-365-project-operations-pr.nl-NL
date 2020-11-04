---
title: Handmatig een pro-formafactuur maken
description: Dit onderwerp bevat informatie over het handmatig maken van pro-formafacturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074793"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="81ef8-103">Handmatig een pro-formafactuur maken</span><span class="sxs-lookup"><span data-stu-id="81ef8-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="81ef8-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="81ef8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="81ef8-105">In Dynamics 365 Project Operations kunnen pro-formafacturen indien nodig handmatig worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="81ef8-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="81ef8-106">U kunt handmatig een pro-formafactuur maken op de lijstpagina **Projectcontracten** of op de detailpagina **Projectcontract**.</span><span class="sxs-lookup"><span data-stu-id="81ef8-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="81ef8-107">Lijstpagina Projectcontracten</span><span class="sxs-lookup"><span data-stu-id="81ef8-107">Project Contracts list page</span></span>

<span data-ttu-id="81ef8-108">Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten en maak facturen voor alle geselecteerde records.</span><span class="sxs-lookup"><span data-stu-id="81ef8-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="81ef8-109">Er wordt gecontroleerd welke van de geselecteerde projectcontracten een achterstallige **Gereed voor facturering** heeft die een datum heeft die vóór de datum van vandaag ligt.</span><span class="sxs-lookup"><span data-stu-id="81ef8-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="81ef8-110">Op basis van deze contracten worden conceptpro-formafacturen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="81ef8-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="81ef8-111">Als een projectcontract meerdere klanten heeft, kan er één factuur per klant worden gemaakt en meerdere facturen per projectcontract.</span><span class="sxs-lookup"><span data-stu-id="81ef8-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="81ef8-112">Alle gemaakte projectfacturen zijn beschikbaar op de pagina **Factuur** in de sectie **Facturering** van het gebied **Verkoop**.</span><span class="sxs-lookup"><span data-stu-id="81ef8-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="81ef8-113">Detailpagina Projectcontract</span><span class="sxs-lookup"><span data-stu-id="81ef8-113">Project Contract details page</span></span>

<span data-ttu-id="81ef8-114">Een pro-formafactuur kan ook worden gemaakt op de detailpagina **Projectcontract** , waarmee de factuur voor dat specifieke projectcontract wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="81ef8-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="81ef8-115">Er wordt gecontroleerd of het projectcontract een achterstallige **Gereed voor facturering** heeft die een datum heeft die vóór de datum van vandaag ligt.</span><span class="sxs-lookup"><span data-stu-id="81ef8-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="81ef8-116">Op basis van deze contracten worden conceptpro-formafacturen gemaakt op basis van het aantal klanten op elke contractregel.</span><span class="sxs-lookup"><span data-stu-id="81ef8-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="81ef8-117">Als er één pro-formafactuur wordt gemaakt, wordt de pagina **Factuur** geopend.</span><span class="sxs-lookup"><span data-stu-id="81ef8-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="81ef8-118">Als er meerdere facturen zijn gemaakt voor dat projectcontract, dan wordt de lijstpagina **Facturen** geopend om alle gemaakte facturen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="81ef8-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>

---
title: Een resourceaanvraag indienen
description: U kunt een gegenereerde resourcevereiste indienen als een resourceaanvraag. De aanvraag wordt vervolgens verzonden naar een resourcemanager voor vervulling.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014020"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="31c6c-104">Een resourceaanvraag indienen</span><span class="sxs-lookup"><span data-stu-id="31c6c-104">Submit a resource request</span></span>

<span data-ttu-id="31c6c-105">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="31c6c-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="31c6c-106">U kunt een gegenereerde resourcevereiste indienen als een resourceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="31c6c-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="31c6c-107">De aanvraag wordt vervolgens verzonden naar een resourcemanager voor vervulling.</span><span class="sxs-lookup"><span data-stu-id="31c6c-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="31c6c-108">Selecteer in Dynamics 365 Project Operations op de pagina **Projecten** het tabblad **Team** om een lijst met te boeken resources weer te geven.</span><span class="sxs-lookup"><span data-stu-id="31c6c-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="31c6c-109">Selecteer de algemene resource met een resourcevereiste in de lijst en klik vervolgens op **Aanvraag verzenden**.</span><span class="sxs-lookup"><span data-stu-id="31c6c-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="31c6c-110">De aanvraagstatus van het algemene teamlid wordt gewijzigd in **Ingediend**.</span><span class="sxs-lookup"><span data-stu-id="31c6c-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="31c6c-111">Nadat de aanvraag is afgehandeld wordt de algemene resource vervangen door een benoemde resource, als de resourcemanager de aanvraag afhandelt door een benoemde resource te boeken.</span><span class="sxs-lookup"><span data-stu-id="31c6c-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="31c6c-112">Anders, als de resourcemanager een benoemde resource heeft voorgesteld, blijft de algemene resource in het team staan en wordt de status van de aanvraag gewijzigd **Moet worden geëvalueerd**.</span><span class="sxs-lookup"><span data-stu-id="31c6c-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
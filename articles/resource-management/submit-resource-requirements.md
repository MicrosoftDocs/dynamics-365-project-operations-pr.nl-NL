---
title: Een resourceaanvraag indienen
description: U kunt een gegenereerde resourcevereiste indienen als een resourceaanvraag. De aanvraag wordt vervolgens verzonden naar een resourcemanager voor vervulling.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961696"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="71bb3-104">Een resourceaanvraag indienen</span><span class="sxs-lookup"><span data-stu-id="71bb3-104">Submit a resource request</span></span>

<span data-ttu-id="71bb3-105">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="71bb3-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="71bb3-106">U kunt een gegenereerde resourcevereiste indienen als een resourceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="71bb3-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="71bb3-107">De aanvraag wordt vervolgens verzonden naar een resourcemanager voor vervulling.</span><span class="sxs-lookup"><span data-stu-id="71bb3-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="71bb3-108">Selecteer in Dynamics 365 Project Operations op de pagina **Projecten** het tabblad **Team** om een lijst met te boeken resources weer te geven.</span><span class="sxs-lookup"><span data-stu-id="71bb3-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="71bb3-109">Selecteer de algemene resource met een resourcevereiste in de lijst en klik vervolgens op **Aanvraag verzenden**.</span><span class="sxs-lookup"><span data-stu-id="71bb3-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="71bb3-110">De aanvraagstatus van het algemene teamlid wordt gewijzigd in **Ingediend**.</span><span class="sxs-lookup"><span data-stu-id="71bb3-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="71bb3-111">Nadat de aanvraag is afgehandeld wordt de algemene resource vervangen door een benoemde resource, als de resourcemanager de aanvraag afhandelt door een benoemde resource te boeken.</span><span class="sxs-lookup"><span data-stu-id="71bb3-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="71bb3-112">Anders, als de resourcemanager een benoemde resource heeft voorgesteld, blijft de algemene resource in het team staan en wordt de status van de aanvraag gewijzigd **Moet worden geëvalueerd**.</span><span class="sxs-lookup"><span data-stu-id="71bb3-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>

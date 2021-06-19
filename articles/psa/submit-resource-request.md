---
title: Een resourceaanvraag indienen
description: Dit onderwerp bevat informatie over het indienen van een aanvraag voor een projectresource.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013165"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="778e8-103">Een resourceaanvraag indienen</span><span class="sxs-lookup"><span data-stu-id="778e8-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="778e8-104">U kunt een gegenereerde resourcevereiste indienen als een resourceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="778e8-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="778e8-105">De aanvraag wordt vervolgens verzonden naar een resourcemanager voor vervulling.</span><span class="sxs-lookup"><span data-stu-id="778e8-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="778e8-106">Klik in Project Service Automation (PSA) op de pagina **Projecten** op het tabblad **Team** om een lijst met te boeken resources weer te geven.</span><span class="sxs-lookup"><span data-stu-id="778e8-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="778e8-107">Selecteer de algemene resource met een resourcevereiste in de lijst en klik vervolgens op **Aanvraag verzenden**.</span><span class="sxs-lookup"><span data-stu-id="778e8-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Een resourceaanvraag indienen](media/RM-how-to-18.png)

<span data-ttu-id="778e8-109">De aanvraagstatus van het algemene teamlid wordt gewijzigd in **Ingediend**.</span><span class="sxs-lookup"><span data-stu-id="778e8-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="778e8-110">Nadat de aanvraag is vervuld door de resourcemanager wordt de algemene resource vervangen door een benoemde resource, als de resourcemanager de aanvraag vervult door een benoemde resource te boeken.</span><span class="sxs-lookup"><span data-stu-id="778e8-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="778e8-111">Anders blijft de algemene resource in het team staan en wordt de status van de aanvraag gewijzigd **Moet worden geëvalueerd**, als de resourcemanager een benoemde resource heeft voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="778e8-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
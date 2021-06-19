---
title: Kosten- en verkooptarieven voor catalogusproducten instellen - lite
description: Dit onderwerp bevat informatie over het instellen van kosten en verkooptarieven voor artikelen in een productcatalogus.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004311"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="9b73a-103">Kosten- en verkooptarieven voor catalogusproducten instellen - lite</span><span class="sxs-lookup"><span data-stu-id="9b73a-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="9b73a-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="9b73a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9b73a-105">Prijzen instellen voor productcatalogusartikelen in Dynamics 365 Project Operations is hetzelfde als in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9b73a-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="9b73a-106">In Project Operations kunnen producten niet worden geschat of gebruikt voor projecten, dus productcatalogusprijzen hoeven niet te worden ingesteld op projectprijslijsten voor prijsopgaven en contracten.</span><span class="sxs-lookup"><span data-stu-id="9b73a-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="9b73a-107">Gebruik het veld **Productprijs** van een prijsopgave, contract of account om productcatalogusprijzen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="9b73a-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="9b73a-108">Stel geen productcatalogusprijzen in de projectprijslijsten in.</span><span class="sxs-lookup"><span data-stu-id="9b73a-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="9b73a-109">Projectprijslijsten zijn exclusief voor Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9b73a-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="9b73a-110">Toepassingsspecifieke bedrijfslogica kopieert de prijslijsten van een prijsopgave naar een contract.</span><span class="sxs-lookup"><span data-stu-id="9b73a-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="9b73a-111">Het resultaat is een contractspecifieke prijslijst.</span><span class="sxs-lookup"><span data-stu-id="9b73a-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="9b73a-112">De kopieerbewerking kan het proces voor het winnen van de prijsopgave vertragen als de projectprijslijst op de prijsopgave te groot wordt.</span><span class="sxs-lookup"><span data-stu-id="9b73a-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="9b73a-113">Productprijslijsten worden niet gekopieerd om aangepaste prijslijsten voor contracten te maken.</span><span class="sxs-lookup"><span data-stu-id="9b73a-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="9b73a-114">Omdat er geen sprake is van kopiëren, wordt de prestatie van het prijsopgaveproces niet beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="9b73a-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
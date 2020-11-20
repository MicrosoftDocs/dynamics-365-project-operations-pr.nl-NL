---
title: Kosten- en verkooptarieven voor catalogusproducten instellen - lite
description: Dit onderwerp bevat informatie over het instellen van kosten en verkooptarieven voor artikelen in een productcatalogus.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176695"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="e6778-103">Kosten- en verkooptarieven voor catalogusproducten instellen - lite</span><span class="sxs-lookup"><span data-stu-id="e6778-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="e6778-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="e6778-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e6778-105">Het instellen van prijzen voor productcatalogusartikelen in Dynamics 365 Project Operations is hetzelfde als in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e6778-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="e6778-106">Omdat producten niet kunnen worden geschat of gebruikt voor projecten in Project Operations, is het niet nodig om productcatalogusprijzen in te stellen op projectprijslijsten voor offertes en contracten.</span><span class="sxs-lookup"><span data-stu-id="e6778-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="e6778-107">Productcatalogusprijzen moeten worden ingesteld in het veld **Productprijs** van een prijsopgave, contract of account.</span><span class="sxs-lookup"><span data-stu-id="e6778-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="e6778-108">Stel geen productcatalogusprijzen in de projectprijslijsten voor deze entiteiten in.</span><span class="sxs-lookup"><span data-stu-id="e6778-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="e6778-109">Projectprijslijsten zijn exclusief voor Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e6778-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="e6778-110">Er is applicatiespecifieke bedrijfslogica die de prijslijsten van een prijsopgave naar een contract kopieert.</span><span class="sxs-lookup"><span data-stu-id="e6778-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="e6778-111">Het resultaat is een contractspecifieke prijslijst.</span><span class="sxs-lookup"><span data-stu-id="e6778-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="e6778-112">De kopieerbewerking kan het proces voor het winnen van de prijsopgave vertragen als de projectprijslijst op de prijsopgave te groot wordt.</span><span class="sxs-lookup"><span data-stu-id="e6778-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="e6778-113">Productprijslijsten worden niet gekopieerd om aangepaste prijslijsten voor contracten te maken.</span><span class="sxs-lookup"><span data-stu-id="e6778-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="e6778-114">Dit betekent dat productprijslijsten geen invloed hebben op de prestaties van het proces voor het winnen van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="e6778-114">This means that product price lists don't impact the performance of the quote win process.</span></span>

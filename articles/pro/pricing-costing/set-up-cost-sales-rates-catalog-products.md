---
title: Kosten- en verkooptarieven voor catalogusproducten instellen
description: Dit onderwerp bevat informatie over het instellen van kosten en verkooptarieven voor artikelen in een productcatalogus.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074631"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="0b8aa-103">Kosten- en verkooptarieven voor catalogusproducten instellen</span><span class="sxs-lookup"><span data-stu-id="0b8aa-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="0b8aa-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="0b8aa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0b8aa-105">Het instellen van prijzen voor productcatalogusartikelen in Dynamics 365 Project Operations is hetzelfde als in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="0b8aa-106">Omdat producten niet kunnen worden geschat of gebruikt voor projecten in Project Operations, is het niet nodig om productcatalogusprijzen in te stellen op projectprijslijsten voor offertes en contracten.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="0b8aa-107">Productcatalogusprijzen moeten worden ingesteld in het veld **Productprijs** van een prijsopgave, contract of account.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="0b8aa-108">Stel geen productcatalogusprijzen in de projectprijslijsten voor deze entiteiten in.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="0b8aa-109">Projectprijslijsten zijn exclusief voor Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="0b8aa-110">Er is applicatiespecifieke bedrijfslogica die de prijslijsten van een prijsopgave naar een contract kopieert.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="0b8aa-111">Het resultaat is een contractspecifieke prijslijst.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="0b8aa-112">De kopieerbewerking kan het proces voor het winnen van de prijsopgave vertragen als de projectprijslijst op de prijsopgave te groot wordt.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="0b8aa-113">Productprijslijsten worden niet gekopieerd om aangepaste prijslijsten voor contracten te maken.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="0b8aa-114">Dit betekent dat productprijslijsten geen invloed hebben op de prestaties van het proces voor het winnen van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-114">This means that product price lists don't impact the performance of the quote win process.</span></span>

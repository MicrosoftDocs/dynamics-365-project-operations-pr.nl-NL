---
title: Resource-schattingen
description: Dit onderwerp bevat informatie over hoe u schattingen voor resources worden berekend in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074484"
---
# <a name="resource-estimates"></a><span data-ttu-id="32eb0-103">Resource-schattingen</span><span class="sxs-lookup"><span data-stu-id="32eb0-103">Resource estimates</span></span>

<span data-ttu-id="32eb0-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="32eb0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="32eb0-105">Resourceschattingen zijn afkomstig van tijdgefaseerde inspanningen die zijn gedefinieerd in de structuur voor werkspecificatie, samen met de toepasselijke prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="32eb0-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="32eb0-106">Meestal is de berekening **tarief/uur voor elke rol x uur.**</span><span class="sxs-lookup"><span data-stu-id="32eb0-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="32eb0-107">De tijdgefaseerde inspanning voor elke resource wordt opgeslagen in het resourcetoewijzingsrecord.</span><span class="sxs-lookup"><span data-stu-id="32eb0-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="32eb0-108">De prijzen worden opgeslagen in een vooraf gedefinieerde prijslijst.</span><span class="sxs-lookup"><span data-stu-id="32eb0-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="32eb0-109">Eenheidsconversie wordt toegepast op basis van de toepasselijke prijslijst.</span><span class="sxs-lookup"><span data-stu-id="32eb0-109">Unit conversion is applied based on the applicable price list.</span></span>

![Resourceschattingen](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="32eb0-111">Standaardwaarden voor de kostprijs van onkosten en kostenvaluta</span><span class="sxs-lookup"><span data-stu-id="32eb0-111">Default cost price and cost currency</span></span>

<span data-ttu-id="32eb0-112">Kostprijzen worden standaard uit de organisatie-eenheid gehaald.</span><span class="sxs-lookup"><span data-stu-id="32eb0-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="32eb0-113">Standaardfactureringstarief en verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="32eb0-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="32eb0-114">Verkoopprijzen worden één keer per deal toegepast.</span><span class="sxs-lookup"><span data-stu-id="32eb0-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="32eb0-115">De standaardhiërarchie voor de verkoopprijslijst is als volgt:</span><span class="sxs-lookup"><span data-stu-id="32eb0-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="32eb0-116">Organisatie</span><span class="sxs-lookup"><span data-stu-id="32eb0-116">Organization</span></span>
2. <span data-ttu-id="32eb0-117">Klant</span><span class="sxs-lookup"><span data-stu-id="32eb0-117">Customer</span></span>
3. <span data-ttu-id="32eb0-118">Prijsopgave/contract</span><span class="sxs-lookup"><span data-stu-id="32eb0-118">Quote/contract</span></span>

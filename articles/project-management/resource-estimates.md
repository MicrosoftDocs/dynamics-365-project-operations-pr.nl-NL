---
title: Resource-schattingen
description: Dit onderwerp bevat informatie over hoe u schattingen voor resources worden berekend in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127348"
---
# <a name="resource-estimates"></a><span data-ttu-id="3c9c6-103">Resource-schattingen</span><span class="sxs-lookup"><span data-stu-id="3c9c6-103">Resource estimates</span></span>

<span data-ttu-id="3c9c6-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="3c9c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3c9c6-105">Resourceschattingen zijn afkomstig van tijdgefaseerde inspanningen die zijn gedefinieerd in de structuur voor werkspecificatie, samen met de toepasselijke prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="3c9c6-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="3c9c6-106">Meestal is de berekening **tarief/uur voor elke rol x uur.**</span><span class="sxs-lookup"><span data-stu-id="3c9c6-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="3c9c6-107">De tijdgefaseerde inspanning voor elke resource wordt opgeslagen in het resourcetoewijzingsrecord.</span><span class="sxs-lookup"><span data-stu-id="3c9c6-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="3c9c6-108">De prijzen worden opgeslagen in een vooraf gedefinieerde prijslijst.</span><span class="sxs-lookup"><span data-stu-id="3c9c6-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="3c9c6-109">Eenheidsconversie wordt toegepast op basis van de toepasselijke prijslijst.</span><span class="sxs-lookup"><span data-stu-id="3c9c6-109">Unit conversion is applied based on the applicable price list.</span></span>

![Resourceschattingen](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="3c9c6-111">Standaardwaarden voor de kostprijs van onkosten en kostenvaluta</span><span class="sxs-lookup"><span data-stu-id="3c9c6-111">Default cost price and cost currency</span></span>

<span data-ttu-id="3c9c6-112">Kostprijzen worden standaard uit de organisatie-eenheid gehaald.</span><span class="sxs-lookup"><span data-stu-id="3c9c6-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="3c9c6-113">Standaardfactureringstarief en verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="3c9c6-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="3c9c6-114">Verkoopprijzen worden één keer per deal toegepast.</span><span class="sxs-lookup"><span data-stu-id="3c9c6-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="3c9c6-115">De standaardhiërarchie voor de verkoopprijslijst is als volgt:</span><span class="sxs-lookup"><span data-stu-id="3c9c6-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="3c9c6-116">Organisatie</span><span class="sxs-lookup"><span data-stu-id="3c9c6-116">Organization</span></span>
2. <span data-ttu-id="3c9c6-117">Klant</span><span class="sxs-lookup"><span data-stu-id="3c9c6-117">Customer</span></span>
3. <span data-ttu-id="3c9c6-118">Prijsopgave/contract</span><span class="sxs-lookup"><span data-stu-id="3c9c6-118">Quote/contract</span></span>

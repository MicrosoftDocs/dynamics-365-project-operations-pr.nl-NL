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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286512"
---
# <a name="resource-estimates"></a><span data-ttu-id="b0c7b-103">Resource-schattingen</span><span class="sxs-lookup"><span data-stu-id="b0c7b-103">Resource estimates</span></span>

<span data-ttu-id="b0c7b-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="b0c7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b0c7b-105">Resourceschattingen zijn afkomstig van tijdgefaseerde inspanningen die zijn gedefinieerd in de structuur voor werkspecificatie, samen met de toepasselijke prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="b0c7b-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="b0c7b-106">Meestal is de berekening **tarief/uur voor elke rol x uur.**</span><span class="sxs-lookup"><span data-stu-id="b0c7b-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="b0c7b-107">De tijdgefaseerde inspanning voor elke resource wordt opgeslagen in het resourcetoewijzingsrecord.</span><span class="sxs-lookup"><span data-stu-id="b0c7b-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="b0c7b-108">De prijzen worden opgeslagen in een vooraf gedefinieerde prijslijst.</span><span class="sxs-lookup"><span data-stu-id="b0c7b-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="b0c7b-109">Eenheidsconversie wordt toegepast op basis van de toepasselijke prijslijst.</span><span class="sxs-lookup"><span data-stu-id="b0c7b-109">Unit conversion is applied based on the applicable price list.</span></span>

![Resourceschattingen](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="b0c7b-111">Standaardwaarden voor de kostprijs van onkosten en kostenvaluta</span><span class="sxs-lookup"><span data-stu-id="b0c7b-111">Default cost price and cost currency</span></span>

<span data-ttu-id="b0c7b-112">Kostprijzen worden standaard uit de organisatie-eenheid gehaald.</span><span class="sxs-lookup"><span data-stu-id="b0c7b-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="b0c7b-113">Standaardfactureringstarief en verkoopvaluta</span><span class="sxs-lookup"><span data-stu-id="b0c7b-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="b0c7b-114">Verkoopprijzen worden één keer per deal toegepast.</span><span class="sxs-lookup"><span data-stu-id="b0c7b-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="b0c7b-115">De standaardhiërarchie voor de verkoopprijslijst is als volgt:</span><span class="sxs-lookup"><span data-stu-id="b0c7b-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="b0c7b-116">Organisatie</span><span class="sxs-lookup"><span data-stu-id="b0c7b-116">Organization</span></span>
2. <span data-ttu-id="b0c7b-117">Klant</span><span class="sxs-lookup"><span data-stu-id="b0c7b-117">Customer</span></span>
3. <span data-ttu-id="b0c7b-118">Prijsopgave/contract</span><span class="sxs-lookup"><span data-stu-id="b0c7b-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
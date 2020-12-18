---
title: Overzicht van intercompany-facturering
description: Dit onderwerp bevat informatie en voorbeelden over intercompany-facturering voor projecten.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595451"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="d0dc7-103">Overzicht van intercompany-facturering</span><span class="sxs-lookup"><span data-stu-id="d0dc7-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="d0dc7-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="d0dc7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d0dc7-105">Uw organisatie heeft mogelijk meerdere divisies, dochterondernemingen en andere rechtspersonen die producten en diensten aan elkaar leveren voor projecten.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="d0dc7-106">De rechtspersoon die de service of het product levert, wordt de *uitlenende rechtspersoon* genoemd.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="d0dc7-107">De rechtspersoon die de service of het product ontvangt, wordt de *lenende rechtspersoon* genoemd.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="d0dc7-108">De volgende afbeelding toont een typisch scenario waarin twee rechtspersonen, Contoso Robotics USA (de lenende rechtspersoon) en Contoso Robotics UK (de uitlenende rechtspersoon) resources delen om een project voor de klant Adventure Works te leveren.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="d0dc7-109">Voor dit scenario is Contoso Robotics USA gecontracteerd om het werk te leveren aan Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Intercompany-facturering](./media/IntercompanyScenario.png) 

<span data-ttu-id="d0dc7-111">Dynamics 365 Project Operations gebruikt de volgende stroom om intercompany-transacties te verwerken:</span><span class="sxs-lookup"><span data-stu-id="d0dc7-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="d0dc7-112">Resources van de uitlenende rechtspersoon registreren intercompany-tijd- of onkostentransacties door tijd en onkosten te boeken voor projecten in de lenende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="d0dc7-113">De kosten van tijd en uitgaven worden in het uitlenende bedrijf geregistreerd met behulp van de kostprijslijst van het lenende bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="d0dc7-114">Niet-gefactureerde intercompany-verkooptransacties worden in het uitlenende bedrijf geregistreerd met behulp van de kostprijslijst van het lenende bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="d0dc7-115">Niet-gefactureerde inkomsten worden in het lenende bedrijf geregistreerd met behulp van de verkoopprijslijst van het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="d0dc7-116">De klant kan worden gefactureerd wanneer niet-gefactureerde inkomsten worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="d0dc7-117">De klant hoeft niet te wachten tot de intercompany-factuurverwerking is voltooid.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="d0dc7-118">Intercompany-klantfacturen worden periodiek aangemaakt in het uitlenende bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="d0dc7-119">De facturen worden handmatig aangemaakt of middels een periodiek geautomatiseerd proces.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="d0dc7-120">Voor elke lenende rechtspersoon kan één factuur worden aangemaakt of per project kunnen afzonderlijke facturen worden aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="d0dc7-121">Wanneer de intercompany-klantfactuur wordt geboekt in de uitlenende rechtspersoon, wordt de overeenkomstige intercompany-leveranciersfactuur gemaakt in de lenende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="d0dc7-122">De kosten in de openstaande leveranciersfactuur worden bij het boeken van de factuur in de projectsubadministratie geboekt.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="d0dc7-123">Het volgende diagram illustreert de intercompany-facturering in relatie tot boekhoudkundige gebeurtenissen en verwachte boekingen naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="d0dc7-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Intercompany-stroom](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="d0dc7-125">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d0dc7-125">Additional resources</span></span>

- [<span data-ttu-id="d0dc7-126">Intercompany-facturering configureren</span><span class="sxs-lookup"><span data-stu-id="d0dc7-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="d0dc7-127">Intercompany-transacties registreren</span><span class="sxs-lookup"><span data-stu-id="d0dc7-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="d0dc7-128">Intercompany-klant- en leveranciersfacturen maken</span><span class="sxs-lookup"><span data-stu-id="d0dc7-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)

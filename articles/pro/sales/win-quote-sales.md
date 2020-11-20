---
title: Een prijsopgave sluiten - lite
description: Dit onderwerp biedt informatie over het sluiten van een prijsopgave in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175705"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="26eaa-103">Een prijsopgave sluiten - lite</span><span class="sxs-lookup"><span data-stu-id="26eaa-103">Close a quote - lite</span></span>

<span data-ttu-id="26eaa-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="26eaa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26eaa-105">Een projectprijsopgave kan worden afgesloten als Gewonnen of Verloren.</span><span class="sxs-lookup"><span data-stu-id="26eaa-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="26eaa-106">Omdat de functies Activeren en Herzien niet worden ondersteund voor prijsopgaven in Microsoft Dynamics 365 Project Operations kunt u een conceptofferte sluiten.</span><span class="sxs-lookup"><span data-stu-id="26eaa-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="26eaa-107">Een prijsopgave sluiten als gewonnen</span><span class="sxs-lookup"><span data-stu-id="26eaa-107">Close a quote as Won</span></span>

<span data-ttu-id="26eaa-108">Als u een projectprijsopgave afsluit als gewonnen, wordt de status van de prijsopgave ingesteld op Gesloten en de statusreden op Gewonnen.</span><span class="sxs-lookup"><span data-stu-id="26eaa-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="26eaa-109">Als de prijsopgave wordt afgesloten, wordt deze alleen-lezen en wordt een concept-projectcontract gecreëerd dat de informatie bevat.</span><span class="sxs-lookup"><span data-stu-id="26eaa-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="26eaa-110">Omdat een gesloten prijsopgave niet heropend kan worden, een bevestigingsvenster. Er is een bevestigingsvenster voordat de wijzigingen worden doorgevoerd, aangezien een gesloten prijsopgave niet opnieuw kan worden geopend en de wijzigingen onomkeerbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="26eaa-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="26eaa-111">Als de prijsopgave is gekoppeld aan een verkoopkans, worden alle andere projectprijsopgaven voor de verkoopkans automatisch gesloten als Verloren.</span><span class="sxs-lookup"><span data-stu-id="26eaa-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="26eaa-112">Financiële gevolgen van het sluiten van een prijsopgave als Gewonnen</span><span class="sxs-lookup"><span data-stu-id="26eaa-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="26eaa-113">Als er voor een project werkelijke tijd is geregistreerd terwijl dit nog aan een conceptprijsopgave is gehecht, worden alleen de kosten van de tijd of uitgaven geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="26eaa-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="26eaa-114">Nadat een prijsopgave is gesloten als Gewonnen, zal de toepassing de kosten herfactureren door de oudere werkelijke kosten om te keren en nieuwe werkelijke kosten opnieuw te creëren.</span><span class="sxs-lookup"><span data-stu-id="26eaa-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="26eaa-115">De applicatie verwerkt deze werkelijke kosten op basis van de factureringsmethode van de bijbehorende projectcontractregel.</span><span class="sxs-lookup"><span data-stu-id="26eaa-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="26eaa-116">Als de werkelijke kosten verwijzen naar een contractregel voor tijd en materiaal, zal het systeem automatisch overeenkomstige niet-gefactureerde werkelijke verkoopcijfers creëren voor wanneer de offerte wordt gesloten en het projectcontract wordt gecreëerd.</span><span class="sxs-lookup"><span data-stu-id="26eaa-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="26eaa-117">Als de werkelijke kosten verwijzen naar een contractregel met een vaste prijs, stopt de applicatie met het opnieuw verwerken van de werkelijke kosten op basis van de regels voor gesplitste facturering voor de projectcontractklanten.</span><span class="sxs-lookup"><span data-stu-id="26eaa-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="26eaa-118">Een prijsopgave sluiten als verloren:</span><span class="sxs-lookup"><span data-stu-id="26eaa-118">Closing a quote as lost:</span></span>

<span data-ttu-id="26eaa-119">Als u een projectprijsopgave afsluit als verloren, wordt de status van de prijsopgave ingesteld op Gesloten en de statusreden op Verloren.</span><span class="sxs-lookup"><span data-stu-id="26eaa-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="26eaa-120">Als u de prijsopgave sluit, wordt de prijsopgave van het project alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="26eaa-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="26eaa-121">Omdat een gesloten prijsopgave niet opnieuw kan worden geopend, zal een bevestigingsvenster uw wijzigingen bevestigen voordat u een prijsopgave sluit.</span><span class="sxs-lookup"><span data-stu-id="26eaa-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="26eaa-122">Als de projectprijsopgave is gesloten als Verloren een project heeft waarnaar wordt verwezen op een van de regels, wordt dat project ook gemarkeerd als Gesloten en worden alle resourceboekingen vanaf die dag geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="26eaa-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="26eaa-123">In Project Operations heeft het sluiten van een prijsopgave als Gewonnen of Verloren geen invloed op de status van de verkoopkans. Deze blijft open totdat deze handmatig wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="26eaa-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>

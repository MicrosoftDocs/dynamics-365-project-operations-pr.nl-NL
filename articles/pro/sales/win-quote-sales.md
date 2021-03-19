---
title: Een prijsopgave sluiten - lite
description: Dit onderwerp biedt informatie over het sluiten van een prijsopgave in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272265"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="7a970-103">Een prijsopgave sluiten - lite</span><span class="sxs-lookup"><span data-stu-id="7a970-103">Close a quote - lite</span></span>

<span data-ttu-id="7a970-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="7a970-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7a970-105">Een projectprijsopgave kan worden afgesloten als Gewonnen of Verloren.</span><span class="sxs-lookup"><span data-stu-id="7a970-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="7a970-106">Een conceptprijsopgave kan worden gesloten omdat de bewerkingen Activeren en Herzien van prijsopgaven niet worden ondersteund in Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7a970-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="7a970-107">Een prijsopgave sluiten als gewonnen</span><span class="sxs-lookup"><span data-stu-id="7a970-107">Close a quote as Won</span></span>

<span data-ttu-id="7a970-108">Wanneer u een projectprijsopgave als Binnengehaald sluit, wordt de status ingesteld op Gesloten en de reden van status is Binnengehaald.</span><span class="sxs-lookup"><span data-stu-id="7a970-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="7a970-109">Als de prijsopgave wordt afgesloten, wordt deze alleen-lezen en wordt een concept-projectcontract gecreëerd dat de informatie bevat.</span><span class="sxs-lookup"><span data-stu-id="7a970-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="7a970-110">Omdat een gesloten prijsopgave niet heropend kan worden, zal een bevestigingsvenster uw wijzigingen bevestigen.</span><span class="sxs-lookup"><span data-stu-id="7a970-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="7a970-111">Als de prijsopgave is gekoppeld aan een verkoopkans, worden alle andere projectprijsopgaven voor de verkoopkans automatisch gesloten als Verloren.</span><span class="sxs-lookup"><span data-stu-id="7a970-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="7a970-112">Financiële gevolgen van het sluiten van een prijsopgave als Gewonnen</span><span class="sxs-lookup"><span data-stu-id="7a970-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="7a970-113">Als er werkelijke waarden zijn voor tijd van een project terwijl dit nog aan een conceptprijsopgave is gekoppeld, worden alleen de kosten van de tijd of de onkosten geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="7a970-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="7a970-114">Nadat een prijsopgave is gesloten als Gewonnen, zal de toepassing de kosten herfactureren door de oudere werkelijke kosten om te keren en nieuwe werkelijke kosten opnieuw te creëren.</span><span class="sxs-lookup"><span data-stu-id="7a970-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="7a970-115">De applicatie verwerkt deze werkelijke kosten op basis van de factureringsmethode van de bijbehorende projectcontractregel.</span><span class="sxs-lookup"><span data-stu-id="7a970-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="7a970-116">Als de werkelijke kosten verwijzen naar een tijd- en materiaalcontractregel, worden overeenkomstige niet-gefactureerde werkelijke verkoopcijfers gemaakt voor het moment waarop de prijsopgave wordt gesloten en het projectcontract wordt gecreëerd.</span><span class="sxs-lookup"><span data-stu-id="7a970-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="7a970-117">Als de werkelijke kosten verwijzen naar een contractregel met een vaste prijs, stopt de toepassing met het opnieuw verwerken van de werkelijke kosten die zijn gebaseerd op de regels voor gesplitste facturering voor de projectcontractklanten.</span><span class="sxs-lookup"><span data-stu-id="7a970-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="7a970-118">Een prijsopgave sluiten als verloren:</span><span class="sxs-lookup"><span data-stu-id="7a970-118">Closing a quote as lost:</span></span>

<span data-ttu-id="7a970-119">Wanneer u een projectprijsopgave sluit als Gemist, wordt de status ingesteld op Gesloten en de reden van status is Gemist.</span><span class="sxs-lookup"><span data-stu-id="7a970-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="7a970-120">Als u de prijsopgave sluit, wordt de prijsopgave van het project alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="7a970-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="7a970-121">Omdat een gesloten prijsopgave niet opnieuw kan worden geopend, zal een bevestigingsvenster uw wijzigingen bevestigen voordat u een prijsopgave sluit.</span><span class="sxs-lookup"><span data-stu-id="7a970-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="7a970-122">Als de projectprijsopgave die wordt gesloten als Gemist verwijst naar een project op een van de regels, wordt dat project ook gemarkeerd als Gemist.</span><span class="sxs-lookup"><span data-stu-id="7a970-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="7a970-123">Alle resourceboekingen worden vanaf die dag geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="7a970-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="7a970-124">In Project Operations heeft het sluiten van een prijsopgave als Gewonnen of Verloren geen invloed op de status van de verkoopkans. Deze blijft open totdat deze handmatig wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="7a970-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Een projectcontract bevestigen
description: Dit onderwerp bevat informatie over het bevestigen van een contract in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128277"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="f7a3b-103">Een projectcontract bevestigen</span><span class="sxs-lookup"><span data-stu-id="f7a3b-103">Confirm a project contract</span></span>

<span data-ttu-id="f7a3b-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="f7a3b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7a3b-105">Een projectcontract in Dynamics 365 Project Operations kan actief zijn met een reden van **Bevestigd**, of gesloten met een reden van **Verloren**.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="f7a3b-106">Wanneer u een projectcontract bevestigt, wordt de status bijgewerkt van **Concept** naar **Actief** en is de reden van de status **Bevestigd**.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="f7a3b-107">Een actief of gesloten contract kan niet worden bewerkt of heropend.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="f7a3b-108">Financiële gevolgen van het bevestigen van een projectcontract</span><span class="sxs-lookup"><span data-stu-id="f7a3b-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="f7a3b-109">Nadat een projectcontract is bevestigd, worden de kosten opnieuw berekend door de oudere werkelijke kosten om te keren en nieuwe werkelijke kosten opnieuw te maken.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="f7a3b-110">De nieuwe werkelijke kosten worden vervolgens op basis van de factureringsmethode van de bijbehorende projectcontractregel verwerkt.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="f7a3b-111">Als de werkelijke kosten verwijzen naar een contractregel die is ingesteld op Tijd- en materiaalverbruik, worden automatisch bijbehorende niet-gefactureerde werkelijke verkoopcijfers opnieuw gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="f7a3b-112">Als de werkelijke kosten verwijzen naar een contractregel die is ingesteld op Vaste prijs, wordt gestopt met de herverwerking van de werkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="f7a3b-113">De niet te overschrijden limieten, de toerekenbaarheidsinstelling en de instellingen voor prijzen en kosten voor de werkelijke waarden worden geëvalueerd en vervolgens bijgewerkt als onderdeel van het bevestigingsproces.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="f7a3b-114">Een projectcontract sluiten als verloren</span><span class="sxs-lookup"><span data-stu-id="f7a3b-114">Close a project contract as lost</span></span>

<span data-ttu-id="f7a3b-115">Wanneer u een projectcontract als verloren sluit, wordt de contractstatus bijgewerkt naar **Gesloten** en is de statusreden **Verloren**.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="f7a3b-116">Het projectcontract wordt alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-116">The project contract becomes read-only.</span></span> <span data-ttu-id="f7a3b-117">Er wordt een bevestigingsvenster weergegeven voordat de wijzigingen worden doorgevoerd, omdat u een gesloten projectcontract niet opnieuw kunt openen.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="f7a3b-118">Als het projectcontract dat als verloren is gesloten, verwijst naar een project op de bijbehorende regels, wordt dat project ook gemarkeerd als gesloten.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="f7a3b-119">Alle resourceboekingen worden vanaf die dag geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="f7a3b-120">Eventuele niet-gefactureerde werkelijke verkoopcijfers op het projectcontract die nog niet op een factuur staan, worden teruggedraaid.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="f7a3b-121">In Dynamics 365 Project Operations heeft het sluiten van een projectcontract als verloren geen invloed op die status van de gekoppelde verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="f7a3b-122">De verkoopkans blijft open en moet handmatig worden gesloten.</span><span class="sxs-lookup"><span data-stu-id="f7a3b-122">The opportunity will remain open and must be manually closed.</span></span>

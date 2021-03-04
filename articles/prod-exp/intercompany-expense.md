---
title: Intercompany-onkosten
description: Dit onderwerp biedt informatie over het gebruik van intercompany-onkosten om de onkosten van een werkrol toe te wijzen aan de rechtspersoon waarvoor het werk is uitgevoerd.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960826"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="9d604-103">Intercompany-onkosten</span><span class="sxs-lookup"><span data-stu-id="9d604-103">Intercompany expenses</span></span>

<span data-ttu-id="9d604-104">Een werknemer die in dienst is van één rechtspersoon in een organisatie, kan werk verrichten voor een andere rechtspersoon in dezelfde organisatie.</span><span class="sxs-lookup"><span data-stu-id="9d604-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="9d604-105">U kunt intercompany-onkosten gebruiken om de onkosten van een werkrol toe te wijzen aan de rechtspersoon waarvoor het werk werd uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9d604-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="9d604-106">De rechtspersoon die de werknemer in dienst heeft, wordt de uitlenende rechtspersoon genoemd.</span><span class="sxs-lookup"><span data-stu-id="9d604-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="9d604-107">De rechtspersoon waarvoor de werknemer onkosten maakt, wordt de lenende rechtspersoon genoemd.</span><span class="sxs-lookup"><span data-stu-id="9d604-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="9d604-108">Voordat een werkrol intercompany-onkosten kan maken en indienen, moet u intercompany-onkostenregels inschakelen.</span><span class="sxs-lookup"><span data-stu-id="9d604-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="9d604-109">Selecteer in de uitlenende rechtspersoon op de pagina **Parameters voor onkostenbeheer** **Intercompany-onkostenregels toestaan**.</span><span class="sxs-lookup"><span data-stu-id="9d604-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="9d604-110">Belastingboeking voor intercompany-onkosten</span><span class="sxs-lookup"><span data-stu-id="9d604-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d604-111">Voordat u in uw onkostendeclaratie belastinggroepen kunt gebruiken die aan de uitlenende rechtspersoon (bron) zijn gekoppeld in plaats van aan de lenende rechtspersoon (bestemming), moet u de functionaliteit inschakelen in de btw-instellingen van het grootboek.</span><span class="sxs-lookup"><span data-stu-id="9d604-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="9d604-112">Wanneer de parameter **Rechtspersoon voor intercompany-belastingboeking** is ingesteld op **Bron** en **Regels voor btw-heffing toepassen** is ingesteld op **Nee** wordt de belastingcombinatie voor de uitlenende rechtspersoon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9d604-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="9d604-113">Als dezelfde parameter is ingesteld op **Doel**, wordt de belastingcombinatie voor lenende rechtspersoon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9d604-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="9d604-114">Voor rechtspersonen in de Verenigde Staten moet wanneer de parameter is ingesteld op **Bron**, het veld **Te ontvangen verkoopbelasting** ook worden geconfigureerd op de nieuwe pagina **Boekingsgroepen grootboek**.</span><span class="sxs-lookup"><span data-stu-id="9d604-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="9d604-115">Het boekhoudsysteem gebruikt de informatie uit dit veld voor het invoeren van belastinggerelateerde financiële administratie.</span><span class="sxs-lookup"><span data-stu-id="9d604-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="9d604-116">Het gedrag is consistent voor onkostenregels die met of zonder een project zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="9d604-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  

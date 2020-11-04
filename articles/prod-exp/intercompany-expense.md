---
title: Intercompany-onkosten
description: Een werknemer die in dienst is van één rechtspersoon in een organisatie, kan werk verrichten voor een andere rechtspersoon in dezelfde organisatie. In dit geval kunt u de functie voor intercompany-onkosten gebruiken om de onkosten van de werknemer toe te wijzen aan de rechtspersoon waarvoor het werk is uitgevoerd.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074715"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="b3c37-104">Intercompany-onkosten</span><span class="sxs-lookup"><span data-stu-id="b3c37-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3c37-105">Een werknemer die in dienst is van één rechtspersoon in een organisatie, kan werk verrichten voor een andere rechtspersoon in dezelfde organisatie.</span><span class="sxs-lookup"><span data-stu-id="b3c37-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="b3c37-106">In dit geval kunt u de functie voor intercompany-onkosten gebruiken om de onkosten van de werknemer toe te wijzen aan de rechtspersoon waarvoor het werk is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b3c37-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="b3c37-107">De rechtspersoon die de werknemer in dienst heeft, wordt de uitlenende rechtspersoon genoemd.</span><span class="sxs-lookup"><span data-stu-id="b3c37-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="b3c37-108">De rechtspersoon waarvoor de werknemer onkosten maakt, wordt de lenende rechtspersoon genoemd.</span><span class="sxs-lookup"><span data-stu-id="b3c37-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="b3c37-109">Voordat een werknemer onkosten kan aanmaken en indienen voor werk dat wordt uitgevoerd voor een andere rechtspersoon, in de uitlenende rechtspersoon, selecteert u op de pagina **Parameters onkostenbeheer** de optie **Intercompany-onkostenregels toestaan**.</span><span class="sxs-lookup"><span data-stu-id="b3c37-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="b3c37-110">Belastingboeking voor intercompany-onkosten</span><span class="sxs-lookup"><span data-stu-id="b3c37-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3c37-111">Als u in uw onkostendeclaratie belastinggroepen wilt gebruiken die aan de uitlenende (bron) rechtspersoon zijn gekoppeld in plaats van aan de lenende (doel) rechtspersoon, moet u dit configureren in de instelling voor verkoopbelasting in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="b3c37-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="b3c37-112">Als de grootboekparameter **Rechtspersoon voor intercompany-belastingboeking** is ingesteld op **Bron** en **Belastingregels verkoopbelasting toepassen** is ingesteld op **Nee** , wordt de belastingcombinatie voor de uitlenende rechtspersoon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3c37-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="b3c37-113">Als dezelfde parameter is ingesteld op **Doel** , wordt de belastingcombinatie voor lenende rechtspersoon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b3c37-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="b3c37-114">Voor rechtspersonen in de Verenigde Staten moet wanneer de parameter is ingesteld op **Bron** , het veld **Te ontvangen verkoopbelasting** ook worden geconfigureerd op de nieuwe pagina **Boekingsgroepen grootboek**.</span><span class="sxs-lookup"><span data-stu-id="b3c37-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="b3c37-115">Het boekhoudsysteem gebruikt de informatie uit dit veld voor het invoeren van belastinggerelateerde boekhouding.</span><span class="sxs-lookup"><span data-stu-id="b3c37-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="b3c37-116">Het gedrag is consistent voor onkostenregels die met of zonder een project zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="b3c37-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  

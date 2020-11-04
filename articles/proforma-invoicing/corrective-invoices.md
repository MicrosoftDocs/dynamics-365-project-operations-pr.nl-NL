---
title: Gecorrigeerde facturen
description: In dit onderwerp krijgt u informatie over gecorrigeerde factureren.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074732"
---
# <a name="corrected-invoices"></a><span data-ttu-id="2b140-103">Gecorrigeerde facturen</span><span class="sxs-lookup"><span data-stu-id="2b140-103">Corrected invoices</span></span>

<span data-ttu-id="2b140-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="2b140-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2b140-105">Bevestigde facturen kunnen worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="2b140-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="2b140-106">Wanneer u een bevestigde factuur bewerkt, wordt er een concept van de gecorrigeerde factuur gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2b140-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="2b140-107">Omdat wordt aangenomen dat u alle transacties en hoeveelheden van de oorspronkelijke factuur wilt terugboeken, bevat deze gecorrigeerde factuur alle transacties van de oorspronkelijke factuur en zijn alle hoeveelheden op de factuur nul (0).</span><span class="sxs-lookup"><span data-stu-id="2b140-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="2b140-108">Wanneer er transacties zijn die niet hoeven te worden gecorrigeerd, kunt u deze verwijderen uit het concept van de correctiefactuur.</span><span class="sxs-lookup"><span data-stu-id="2b140-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="2b140-109">Als u alleen een gedeeltelijke hoeveelheid wilt terugboeken of retourneren, kunt u het veld Hoeveelheid in de regeldetails bewerken.</span><span class="sxs-lookup"><span data-stu-id="2b140-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="2b140-110">Als u het factuurregeldetail opent, kunt u de oorspronkelijk gefactureerde hoeveelheid bekijken.</span><span class="sxs-lookup"><span data-stu-id="2b140-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="2b140-111">U kunt vervolgens de huidige gefactureerde hoeveelheid bewerken, zodat deze kleiner of groter is dan de oorspronkelijke gefactureerde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="2b140-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="2b140-112">Wanneer u een correctiefactuur bevestigt, wordt de oorspronkelijke gefactureerde werkelijke verkoopwaarde teruggeboekt en wordt er een nieuwe gefactureerde werkelijke verkoopwaarde gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2b140-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="2b140-113">Als de hoeveelheid is verlaagd, zorgt het verschil ervoor dat er ook een nieuwe, niet-gefactureerde werkelijke verkoopwaarde wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2b140-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="2b140-114">Als de oorspronkelijke gefactureerde verkoopwaarde bijvoorbeeld voor acht uur was en het regeldetail van de gecorrigeerde factuur een gereduceerde hoeveelheid van zes uur heeft, wordt de oorspronkelijke gefactureerde verkoopregel teruggeboekt en worden er twee nieuwe werkelijke waarden gemaakt:</span><span class="sxs-lookup"><span data-stu-id="2b140-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="2b140-115">Een gefactureerde werkelijke verkoopwaarde voor zes uur.</span><span class="sxs-lookup"><span data-stu-id="2b140-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="2b140-116">Een niet-gefactureerde werkelijke verkoopwaarde voor de resterende twee uur.</span><span class="sxs-lookup"><span data-stu-id="2b140-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="2b140-117">Deze transactie kan later worden gefactureerd of als niet-factureerbaar worden aangemerkt, afhankelijk van de onderhandelingen met de klant.</span><span class="sxs-lookup"><span data-stu-id="2b140-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>

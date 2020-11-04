---
title: Persoonlijke onkosten in een onkostendeclaratie
description: In dit onderwerp worden de twee methoden uitgelegd voor het verwerken van de persoonlijke onkosten van een werknemer in Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074713"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="06baf-103">Persoonlijke onkosten in een onkostendeclaratie</span><span class="sxs-lookup"><span data-stu-id="06baf-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06baf-104">Tijdens zakenreizen kunnen werknemers soms persoonlijke onkosten in rekening brengen op hun bedrijfscreditcard.</span><span class="sxs-lookup"><span data-stu-id="06baf-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="06baf-105">Als u geen proces definieert voor het verwerken van persoonlijke onkosten, kan het goedkeuringsproces voor onkostendeclaraties worden verstoord wanneer werknemers hun gespecificeerde onkostendeclaraties indienen.</span><span class="sxs-lookup"><span data-stu-id="06baf-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="06baf-106">Er zijn twee methoden om de persoonlijke onkosten van een werknemer te verwerken:</span><span class="sxs-lookup"><span data-stu-id="06baf-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="06baf-107">**Betaald door werknemer** : uw organisatie betaalt geen persoonlijke onkosten die op de factuur van de bedrijfscreditcard staan.</span><span class="sxs-lookup"><span data-stu-id="06baf-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="06baf-108">In plaats daarvan wordt een rapport gemaakt waarop persoonlijke onkosten en bedrijfskosten staan die van de bedrijfscreditcard zijn afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="06baf-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="06baf-109">**Betaald door bedrijf** : uw organisatie betaalt de volledige factuur van de bedrijfscreditcard en schrijft vervolgens de persoonlijke onkosten van de rekening van de werknemer af.</span><span class="sxs-lookup"><span data-stu-id="06baf-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="06baf-110">U kunt de methode selecteren die uw organisatie gebruikt op de pagina **Parameters onkostenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="06baf-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

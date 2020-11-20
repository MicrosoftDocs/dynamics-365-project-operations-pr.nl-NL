---
title: Analyse van projectprijsopgaven
description: Dit onderwerp bevat informatie over de analyse van projectprijsopgaven.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127017"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="3b554-103">Analyse van projectprijsopgaven</span><span class="sxs-lookup"><span data-stu-id="3b554-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3b554-104">Dynamics 365 Project Service Automation analyseert projectprijsopgaven om de winstgevendheid te schatten.</span><span class="sxs-lookup"><span data-stu-id="3b554-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="3b554-105">Ook wordt geanalyseerd hoe goed de prijsopgave is afgestemd op de verwachtingen van de klant over de leverings- of voltooiingsdatum en het budget.</span><span class="sxs-lookup"><span data-stu-id="3b554-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="3b554-106">Winstgevendheidsanalyse</span><span class="sxs-lookup"><span data-stu-id="3b554-106">Profitability analysis</span></span>

<span data-ttu-id="3b554-107">Project Service Automation analyseert de winstgevendheid met behulp van de brutomarge en de aangepaste brutomarge.</span><span class="sxs-lookup"><span data-stu-id="3b554-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="3b554-108">Brutomarges worden berekend met behulp van de volgende formule:</span><span class="sxs-lookup"><span data-stu-id="3b554-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="3b554-109">De aangepaste brutomarges wordt berekend aan de hand van de volgende formule:</span><span class="sxs-lookup"><span data-stu-id="3b554-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="3b554-110">Als de waarden voor brutomarge en aangepaste brutomarge veel verschillen, wordt veel van het werk in de prijsopgave geclassificeerd als niet-toerekenbaar.</span><span class="sxs-lookup"><span data-stu-id="3b554-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="3b554-111">Analyse van klantverwachtingen</span><span class="sxs-lookup"><span data-stu-id="3b554-111">Analysis of customer expectations</span></span>

<span data-ttu-id="3b554-112">U kunt prijsopgaven analyseren en grafieken voor klantverwachtingen genereren over de planning en het budget als u waarden invoert voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="3b554-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="3b554-113">Het veld **Aangevraagde leveringsdatum** in de prijsopgavekoptekst.</span><span class="sxs-lookup"><span data-stu-id="3b554-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="3b554-114">Het veld **Klantbudget** voor elke prijsopgaveregel (voor projectgebaseerde regels en productgebaseerde regels).</span><span class="sxs-lookup"><span data-stu-id="3b554-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="3b554-115">Een analyse van klantverwachtingen over de planning wordt uitgevoerd door de laatste einddatum van het details van de prijsopgaveregel te vergelijken met de gevraagde leveringsdatum voor alle prijsopgaveregels in de prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="3b554-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="3b554-116">Een analyse van klantverwachtingen over het budget wordt uitgevoerd door de som van het totale klantbudget te vergelijken met het prijsopgavebedrag van alle prijsopgaveregels.</span><span class="sxs-lookup"><span data-stu-id="3b554-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>

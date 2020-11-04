---
title: Meerdere fiatteurs voor een onkostendeclaratie
description: Dit onderwerp bevat informatie over onkostendeclaraties die door meerdere personen moeten worden goedgekeurd.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074720"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="96260-103">Meerdere fiatteurs voor een onkostendeclaratie</span><span class="sxs-lookup"><span data-stu-id="96260-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96260-104">Afhankelijk van het goedkeuringsbeleid voor onkosten van uw organisatie kan het zijn dat meer dan één persoon een door een werknemer ingediende onkostendeclaratie moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="96260-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="96260-105">Wanneer u het werkstroomproces instelt voor goedkeuring van onkostennota's, kunt u werkstroomelementen toevoegen die taken of stappen bevatten voor een of meer fiatteurs van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="96260-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="96260-106">U kunt bijvoorbeeld vereisen dat alle onkostendeclaraties eerst worden goedgekeurd door de manager van de werknemer die het rapport heeft ingediend en vervolgens door de coördinator crediteurenadministratie.</span><span class="sxs-lookup"><span data-stu-id="96260-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="96260-107">Als u besluit dat u meerdere fiatteurs van onkostennota's nodig hebt, kunt u de werkstroomelementen op een van de volgende manieren toevoegen:</span><span class="sxs-lookup"><span data-stu-id="96260-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="96260-108">Voeg één goedkeuringselement toe dat één stap bevat.</span><span class="sxs-lookup"><span data-stu-id="96260-108">Add one approval element that has one step.</span></span> <span data-ttu-id="96260-109">De stap kan bijvoorbeeld vereisen dat een onkostennota wordt toegewezen aan een gebruikersgroep en dat deze wordt goedgekeurd door 50 procent van de leden van de gebruikersgroep.</span><span class="sxs-lookup"><span data-stu-id="96260-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="96260-110">Voeg één goedkeuringselement toe dat meerdere stappen bevat.</span><span class="sxs-lookup"><span data-stu-id="96260-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="96260-111">Het goedkeuringselement kan bijvoorbeeld de volgende stappen bevatten:</span><span class="sxs-lookup"><span data-stu-id="96260-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="96260-112">De manager van de medewerker die de onkostennota heeft ingediend, keurt deze goed.</span><span class="sxs-lookup"><span data-stu-id="96260-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="96260-113">De coördinator crediteurenadministrateur verifieert de betalingsbewijzen en de items in de onkostennota.</span><span class="sxs-lookup"><span data-stu-id="96260-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="96260-114">De budgethouder keurt de onkostennota goed.</span><span class="sxs-lookup"><span data-stu-id="96260-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="96260-115">Voeg meerdere goedkeuringselementen toe, die elk één stap hebben.</span><span class="sxs-lookup"><span data-stu-id="96260-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="96260-116">U kunt bijvoorbeeld een afzonderlijk goedkeuringselement toevoegen voor elk van de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="96260-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="96260-117">De manager van de medewerker keurt de onkostennota goed.</span><span class="sxs-lookup"><span data-stu-id="96260-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="96260-118">De budgethouder keurt de onkostennota goed.</span><span class="sxs-lookup"><span data-stu-id="96260-118">The budget owner approves the expense report.</span></span>

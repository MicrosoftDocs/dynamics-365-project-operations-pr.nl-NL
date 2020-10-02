---
title: Onkostenrapporten en meerdere fiatteurs
description: Deze onderwerp biedt informatie over onkostennota's die door meer dan één persoon moeten worden goedgekeurd.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897085"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="4202b-103">Onkostenrapporten en meerdere fiatteurs</span><span class="sxs-lookup"><span data-stu-id="4202b-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="4202b-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="4202b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4202b-105">Afhankelijk van het goedkeuringsbeleid van uw organisatie kan het zijn dat meer dan één persoon een ingediende onkostennota moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="4202b-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="4202b-106">Wanneer u het werkstroomproces instelt voor goedkeuring van onkostennota's, kunt u werkstroomelementen toevoegen die taken of stappen bevatten voor een of meer fiatteurs van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="4202b-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="4202b-107">U kunt bijvoorbeeld eisen dat alle onkostennota's worden goedgekeurd door twee afzonderlijke personen: de manager van de werknemer die het rapport heeft ingediend en de coördinator crediteurenadministratie.</span><span class="sxs-lookup"><span data-stu-id="4202b-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="4202b-108">Als u besluit dat u meerdere fiatteurs van onkostennota's nodig hebt, kunt u de werkstroomelementen op een van de volgende manieren toevoegen:</span><span class="sxs-lookup"><span data-stu-id="4202b-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="4202b-109">Voeg één goedkeuringselement toe dat één stap bevat.</span><span class="sxs-lookup"><span data-stu-id="4202b-109">Add one approval element that has one step.</span></span> <span data-ttu-id="4202b-110">De stap kan bijvoorbeeld vereisen dat een onkostennota wordt toegewezen aan een gebruikersgroep en dat deze wordt goedgekeurd door 50 procent van de leden van de gebruikersgroep.</span><span class="sxs-lookup"><span data-stu-id="4202b-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="4202b-111">Voeg één goedkeuringselement toe dat meerdere stappen bevat.</span><span class="sxs-lookup"><span data-stu-id="4202b-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="4202b-112">Het goedkeuringselement kan bijvoorbeeld de volgende stappen bevatten:</span><span class="sxs-lookup"><span data-stu-id="4202b-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="4202b-113">De manager van de medewerker die de onkostennota heeft ingediend, keurt deze goed.</span><span class="sxs-lookup"><span data-stu-id="4202b-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="4202b-114">De coördinator crediteurenadministrateur verifieert de betalingsbewijzen en de items in de onkostennota.</span><span class="sxs-lookup"><span data-stu-id="4202b-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="4202b-115">De budgethouder keurt de onkostennota goed.</span><span class="sxs-lookup"><span data-stu-id="4202b-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="4202b-116">Voeg meerdere goedkeuringselementen toe, die elk één stap hebben.</span><span class="sxs-lookup"><span data-stu-id="4202b-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="4202b-117">U kunt bijvoorbeeld een afzonderlijk goedkeuringselement toevoegen voor elk van de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="4202b-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="4202b-118">De manager van de medewerker keurt de onkostennota goed.</span><span class="sxs-lookup"><span data-stu-id="4202b-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="4202b-119">De budgethouder keurt de onkostennota goed.</span><span class="sxs-lookup"><span data-stu-id="4202b-119">The budget owner approves the expense report.</span></span>

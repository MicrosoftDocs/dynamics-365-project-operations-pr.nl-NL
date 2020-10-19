---
title: Onkostenschattingen
description: Dit onderwerp biedt informatie over het definiëren of schatten van projectgebaseerde onkosten.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908032"
---
# <a name="expense-estimates"></a><span data-ttu-id="ef732-103">Onkostenschattingen</span><span class="sxs-lookup"><span data-stu-id="ef732-103">Expense estimates</span></span>
<span data-ttu-id="ef732-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="ef732-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ef732-105">Naast resourcegebaseerde bronnen kunnen projectmanagers in Dynamics 365 Project Operations projectgebaseerde onkosten voor elk project definiëren.</span><span class="sxs-lookup"><span data-stu-id="ef732-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="ef732-106">Elk onkostenitem kan worden gekoppeld aan een specifieke projecttaak of onkostencategorie.</span><span class="sxs-lookup"><span data-stu-id="ef732-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="ef732-107">Onkostencategorieën worden doorgaans op organisatieniveau gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ef732-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="ef732-108">De prijzen voor elke onkostencategorie worden doorgaans gedefinieerd in de volgende hiërarchie:</span><span class="sxs-lookup"><span data-stu-id="ef732-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="ef732-109">Organisatie</span><span class="sxs-lookup"><span data-stu-id="ef732-109">Organization</span></span>
- <span data-ttu-id="ef732-110">Klant</span><span class="sxs-lookup"><span data-stu-id="ef732-110">Customer</span></span>
- <span data-ttu-id="ef732-111">Prijsopgave/contract</span><span class="sxs-lookup"><span data-stu-id="ef732-111">Quote/contract</span></span>

<span data-ttu-id="ef732-112">Voer de volgende stappen uit om projectonkosten te bekijken, toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="ef732-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="ef732-113">Ga naar **Projecten** en selecteer het project waaraan u wilt werken.</span><span class="sxs-lookup"><span data-stu-id="ef732-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="ef732-114">Selecteer het tabblad **Projectschattingen** en bekijk de lijst met projectonkosten.</span><span class="sxs-lookup"><span data-stu-id="ef732-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="ef732-115">Selecteer **Nieuwe onkosten** om onkosten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="ef732-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="ef732-116">Of selecteer een onkostenpost die u wilt verwijderen en selecteer vervolgens **Onkosten verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="ef732-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="ef732-117">De volgende kenmerken worden gedefinieerd voor elk onkostenregelitem:</span><span class="sxs-lookup"><span data-stu-id="ef732-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="ef732-118">**Categorie**: de gemeenschappelijke groeperingen die worden gebruikt om alle uitgaven voor een project te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="ef732-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="ef732-119">**Begindatum**: de datum waarop de onkosten naar verwachting worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ef732-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="ef732-120">**Aantal**: het geschatte aantal onkostenitems voor een specifieke categorie.</span><span class="sxs-lookup"><span data-stu-id="ef732-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="ef732-121">**Kostprijs per eenheid**: de eenheidsprijs die wordt gebruikt om de kosten van de onkosten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ef732-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="ef732-122">**Verkoopprijs per eenheid**: de eenheidsprijs die wordt gebruikt om de verkoopprijzen van de onkosten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ef732-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>


---
title: Onkostenschattingen
description: Dit onderwerp biedt informatie over het definiëren of schatten van projectgebaseerde onkosten.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287052"
---
# <a name="expense-estimates"></a><span data-ttu-id="295b0-103">Onkostenschattingen</span><span class="sxs-lookup"><span data-stu-id="295b0-103">Expense estimates</span></span>
<span data-ttu-id="295b0-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="295b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="295b0-105">Behalve het definiëren van op resources gebaseerde schattingen, stelt Dynamics 365 Project Operations projectmanagers in staat om projectgebaseerde onkosten voor elk project te definiëren.</span><span class="sxs-lookup"><span data-stu-id="295b0-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="295b0-106">Elk onkostenitem kan worden gekoppeld aan een specifieke projecttaak of onkostencategorie.</span><span class="sxs-lookup"><span data-stu-id="295b0-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="295b0-107">Onkostencategorieën worden doorgaans op organisatieniveau gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="295b0-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="295b0-108">De prijzen voor elke onkostencategorie worden doorgaans gedefinieerd in de volgende hiërarchie:</span><span class="sxs-lookup"><span data-stu-id="295b0-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="295b0-109">Organisatie</span><span class="sxs-lookup"><span data-stu-id="295b0-109">Organization</span></span>
- <span data-ttu-id="295b0-110">Klant</span><span class="sxs-lookup"><span data-stu-id="295b0-110">Customer</span></span>
- <span data-ttu-id="295b0-111">Prijsopgave/contract</span><span class="sxs-lookup"><span data-stu-id="295b0-111">Quote/contract</span></span>

<span data-ttu-id="295b0-112">Voer de volgende stappen uit om projectonkosten te bekijken, toe te voegen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="295b0-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="295b0-113">Ga naar **Projecten** en selecteer het project waaraan u wilt werken.</span><span class="sxs-lookup"><span data-stu-id="295b0-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="295b0-114">Selecteer het tabblad **Projectschattingen** en bekijk de lijst met projectonkosten.</span><span class="sxs-lookup"><span data-stu-id="295b0-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="295b0-115">Selecteer **Nieuwe onkosten** om onkosten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="295b0-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="295b0-116">Of selecteer een onkostenpost die u wilt verwijderen en selecteer vervolgens **Onkosten verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="295b0-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="295b0-117">De volgende kenmerken worden gedefinieerd voor elk onkostenregelitem:</span><span class="sxs-lookup"><span data-stu-id="295b0-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="295b0-118">**Categorie**: de gemeenschappelijke groeperingen die worden gebruikt om alle uitgaven voor een project te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="295b0-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="295b0-119">**Begindatum**: de datum waarop de onkosten naar verwachting worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="295b0-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="295b0-120">**Aantal**: het geschatte aantal onkostenitems voor een specifieke categorie.</span><span class="sxs-lookup"><span data-stu-id="295b0-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="295b0-121">**Kostprijs per eenheid**: de eenheidsprijs die wordt gebruikt om de kosten van de onkosten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="295b0-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="295b0-122">**Verkoopprijs per eenheid**: de eenheidsprijs die wordt gebruikt om de verkoopprijzen van de onkosten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="295b0-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
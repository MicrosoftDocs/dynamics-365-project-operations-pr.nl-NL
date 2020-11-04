---
title: Prognosemodellen voor projectbudgetten maken
description: In dit onderwerp wordt beschreven hoe u een prognosemodel maakt voor resterende budgetten.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074700"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="43502-103">Prognosemodellen voor projectbudgetten maken</span><span class="sxs-lookup"><span data-stu-id="43502-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43502-104">In dit onderwerp wordt beschreven hoe u een prognosemodel maakt voor resterende budgetten.</span><span class="sxs-lookup"><span data-stu-id="43502-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="43502-105">Voor een project dat onder budgetbeheer valt, worden twee soorten budgetten gebruikt: oorspronkelijk en resterend.</span><span class="sxs-lookup"><span data-stu-id="43502-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="43502-106">Wanneer u een projectbudget maakt, moet u de oorspronkelijke en resterende budgetprognosemodellen opgeven die zijn gemaakt op de pagina **Prognosemodellen**.</span><span class="sxs-lookup"><span data-stu-id="43502-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="43502-107">Projectbudgetten die zijn gebaseerd op de opgegeven modellen worden gemaakt wanneer u het projectbudget vastlegt.</span><span class="sxs-lookup"><span data-stu-id="43502-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="43502-108">Een prognosemodel dat wordt gebruikt voor budgetbeheer, kan geen submodel hebben of als submodel worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="43502-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="43502-109">Selecteer **Projectmanagement en financiële administratie** > **Instellingen** > **Prognoses**  > **Prognosemodellen**.</span><span class="sxs-lookup"><span data-stu-id="43502-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="43502-110">Selecteer **Nieuw** om een nieuw prognosemodel te maken en voer vervolgens een model-id-nummer en een naam voor het nieuwe model in.</span><span class="sxs-lookup"><span data-stu-id="43502-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="43502-111">Stel de optie **Gestopt** in op **Ja** om wijzigingen in de prognoseregels voor het prognosemodel te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="43502-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="43502-112">Als de prognoseregels waaraan het model is gekoppeld, cashflowprognoses in het grootboek moeten genereren, stelt u **Opnemen in cashflowprognoses** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="43502-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="43502-113">Als u de projectdatum als factuurdatum wilt gebruiken, stelt u **Factuurdatum prognose** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="43502-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="43502-114">Selecteer in het veld **Budgettype** een van de volgende modeltypen in:</span><span class="sxs-lookup"><span data-stu-id="43502-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="43502-115">**Oorspronkelijk budget** : gebruik de oorspronkelijke budgetbedragen die zijn vastgelegd toen het oorspronkelijke budget werd gemaakt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="43502-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="43502-116">**Resterend budget** : gebruik de resterende budgetbedragen tijdens de looptijd van het project.</span><span class="sxs-lookup"><span data-stu-id="43502-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="43502-117">De saldi in dit prognosemodel worden verminderd met werkelijke transacties en verhoogd of verlaagd met budgetherzieningen.</span><span class="sxs-lookup"><span data-stu-id="43502-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="43502-118">**Overbrengen** : gebruik de overdrachtsbudgetbedragen voor het project.</span><span class="sxs-lookup"><span data-stu-id="43502-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="43502-119">Overbrengen is een optioneel proces dat kan worden uitgevoerd om ongebruikte budgetbedragen van het ene boekjaar naar het andere over te brengen.</span><span class="sxs-lookup"><span data-stu-id="43502-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="43502-120">Stel indien nodig de volgende opties in:</span><span class="sxs-lookup"><span data-stu-id="43502-120">Set the following options as required:</span></span>

   - <span data-ttu-id="43502-121">Schakel **Factuurdatum prognose** in als u de projectdatum als de factuurdatum wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="43502-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="43502-122">Schakel **Prognose met OHW** in als u een prognose wilt uitvoeren op basis van onderhanden werk (OHW) en selecteer vervolgens het type OHW.</span><span class="sxs-lookup"><span data-stu-id="43502-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="43502-123">U kunt de standaardwaarde voor **Budgettype** van **Geen** behouden of een nieuw type invoeren.</span><span class="sxs-lookup"><span data-stu-id="43502-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="43502-124">Het budgettype kan niet worden gewijzigd nadat u een record hebt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="43502-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="43502-125">Als u het standaardbudgettype wijzigt, zijn alle andere opties niet beschikbaar voor updates en kunt u dit prognosemodel niet opnieuw gebruiken.</span><span class="sxs-lookup"><span data-stu-id="43502-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 


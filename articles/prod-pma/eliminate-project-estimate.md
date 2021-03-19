---
title: Een projectschatting verwijderen
description: Dit onderwerp bevat informatie over het verwijderen van een projectschatting nadat deze is voltooid.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270672"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="a3971-103">Een projectschatting verwijderen</span><span class="sxs-lookup"><span data-stu-id="a3971-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3971-104">Projectschattingen bieden de financiële weergave voor werk dat voor een project wordt geschat en gepland.</span><span class="sxs-lookup"><span data-stu-id="a3971-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="a3971-105">Als u met schattingen voor een project wilt werken, moet u het project aan een schattingsproject koppelen.</span><span class="sxs-lookup"><span data-stu-id="a3971-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="a3971-106">Een schattingsproject wordt altijd gebaseerd op een bestaand project, maar meerdere projecten kunnen verwijzen naar één schattingsproject.</span><span class="sxs-lookup"><span data-stu-id="a3971-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="a3971-107">Aan schattingsprojecten kunnen alleen projecten met een vaste prijs en investeringsprojecten worden gekoppeld, en die projecten moeten tot dezelfde projectgroep behoren als het schattingsproject.</span><span class="sxs-lookup"><span data-stu-id="a3971-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="a3971-108">Als u een schattingsproject wilt verwijderen, moet het voltooid zijn.</span><span class="sxs-lookup"><span data-stu-id="a3971-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="a3971-109">In de volgende stappen wordt uitgelegd hoe u een schatting kunt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="a3971-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="a3971-110">Ga naar **Projectmanagement en financiële administratie** > **Alle projecten** en open het project.</span><span class="sxs-lookup"><span data-stu-id="a3971-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="a3971-111">Selecteer op het tabblad **Beheer** **Schattingen** en selecteer op de pagina **Schatting** **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="a3971-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="a3971-112">Stel de volgende opties in op de pagina **Schatting verwijderen** op het tabblad **Algemeen**:</span><span class="sxs-lookup"><span data-stu-id="a3971-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="a3971-113">**Periodecode**: selecteer de periodecode om de juiste schattingsprojecten te kiezen.</span><span class="sxs-lookup"><span data-stu-id="a3971-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="a3971-114">**Schattingsdatum**: selecteer de juiste schattingsdatum voor verwijdering.</span><span class="sxs-lookup"><span data-stu-id="a3971-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="a3971-115">**Verwijderen met OHW-waarschuwingen**: schakel deze optie in om een melding te geven wanneer een schatting die is gekoppeld aan werk in uitvoering (OHW), wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="a3971-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="a3971-116">Als deze optie niet is ingeschakeld, kan de verwijdering niet worden voortgezet als er niet-geschatte transacties bestaan.</span><span class="sxs-lookup"><span data-stu-id="a3971-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="a3971-117">Deze optie is alleen beschikbaar als verwijdering wordt toegepast op een schattingsproject.</span><span class="sxs-lookup"><span data-stu-id="a3971-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="a3971-118">De optie is niet beschikbaar als u gebruikmaakt van periodieke berichten.</span><span class="sxs-lookup"><span data-stu-id="a3971-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="a3971-119">Deze instelling werkt met de instellingen op het tabblad **Schatting** op de pagina **Projectparameters** in de veldgroep **Verwijdering toestaan als er niet-geschatte transacties bestaan**.</span><span class="sxs-lookup"><span data-stu-id="a3971-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="a3971-120">**Fase instellen op Voltooid**: schakel deze optie in als u de fase van het schattingsproject wilt instellen op **Voltooid** nadat u de verwijdering hebt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a3971-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="a3971-121">**Schattingslijst afdrukken**: selecteer de informatie die moet worden opgenomen wanneer de schattingslijst wordt afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="a3971-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="a3971-122">**Infolog weergeven**: schakel deze optie in om Infolog weer te geven.</span><span class="sxs-lookup"><span data-stu-id="a3971-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="a3971-123">**Boekingsdatum**: kies de boekingsdatum in het grootboek voor de schatting.</span><span class="sxs-lookup"><span data-stu-id="a3971-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="a3971-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3971-124">Select **OK**.</span></span>
5. <span data-ttu-id="a3971-125">Als het verwijderingsproces is voltooid, wordt het verwijderde schattingsproject weergegeven met een negatieve waarde.</span><span class="sxs-lookup"><span data-stu-id="a3971-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="a3971-126">Als u niet van plan was een schatting te verwijderen, kunt u de verwijderde schatting selecteren en **Verwijdering ongedaan maken** selecteren.</span><span class="sxs-lookup"><span data-stu-id="a3971-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
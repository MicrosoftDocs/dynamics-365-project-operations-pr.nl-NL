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
# <a name="create-forecast-models-for-project-budgets"></a>Prognosemodellen voor projectbudgetten maken 

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een prognosemodel maakt voor resterende budgetten. Voor een project dat onder budgetbeheer valt, worden twee soorten budgetten gebruikt: oorspronkelijk en resterend. Wanneer u een projectbudget maakt, moet u de oorspronkelijke en resterende budgetprognosemodellen opgeven die zijn gemaakt op de pagina **Prognosemodellen**. Projectbudgetten die zijn gebaseerd op de opgegeven modellen worden gemaakt wanneer u het projectbudget vastlegt.

> [!NOTE]
> Een prognosemodel dat wordt gebruikt voor budgetbeheer, kan geen submodel hebben of als submodel worden gebruikt.

1. Selecteer **Projectmanagement en financiële administratie** > **Instellingen** > **Prognoses**  > **Prognosemodellen**.
2. Selecteer **Nieuw** om een nieuw prognosemodel te maken en voer vervolgens een model-id-nummer en een naam voor het nieuwe model in. 
3. Stel de optie **Gestopt** in op **Ja** om wijzigingen in de prognoseregels voor het prognosemodel te voorkomen. 
4. Als de prognoseregels waaraan het model is gekoppeld, cashflowprognoses in het grootboek moeten genereren, stelt u **Opnemen in cashflowprognoses** in op **Ja**. 
5. Als u de projectdatum als factuurdatum wilt gebruiken, stelt u **Factuurdatum prognose** in op **Ja**. 
6. Selecteer in het veld **Budgettype** een van de volgende modeltypen in:

   - **Oorspronkelijk budget** : gebruik de oorspronkelijke budgetbedragen die zijn vastgelegd toen het oorspronkelijke budget werd gemaakt en goedgekeurd.
   - **Resterend budget** : gebruik de resterende budgetbedragen tijdens de looptijd van het project. De saldi in dit prognosemodel worden verminderd met werkelijke transacties en verhoogd of verlaagd met budgetherzieningen.
   - **Overbrengen** : gebruik de overdrachtsbudgetbedragen voor het project. Overbrengen is een optioneel proces dat kan worden uitgevoerd om ongebruikte budgetbedragen van het ene boekjaar naar het andere over te brengen.

7. Stel indien nodig de volgende opties in:

   - Schakel **Factuurdatum prognose** in als u de projectdatum als de factuurdatum wilt gebruiken.
   - Schakel **Prognose met OHW** in als u een prognose wilt uitvoeren op basis van onderhanden werk (OHW) en selecteer vervolgens het type OHW. 
   - U kunt de standaardwaarde voor **Budgettype** van **Geen** behouden of een nieuw type invoeren. Het budgettype kan niet worden gewijzigd nadat u een record hebt gewijzigd.     
    > [!NOTE]
    > Als u het standaardbudgettype wijzigt, zijn alle andere opties niet beschikbaar voor updates en kunt u dit prognosemodel niet opnieuw gebruiken. 
   


 

---
title: Projectbudgetten transporteren aan het einde van het fiscale jaar
description: Dit artikel bevat informatie over het overboeken van resterende budgetbedragen naar toekomstige jaren en het maken van budgetregistergegevens.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
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
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074697"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projectbudgetten transporteren aan het einde van het fiscale jaar

[!include [banner](../includes/banner.md)]

Als u aan een meerjarenproject werkt, hebt u mogelijk budget over aan het einde van het fiscaal jaar. U kunt de resterende budgetbedragen overboeken naar een toekomstig jaar, en budgetregistergegevens aanmaken voor de bedragen in de bijbehorende grootboekrekeningen. Bekijk en analyseer de resterende budgetbedragen voordat u de resterende bedragen transporteert.

## <a name="review-and-analyze-remaining-budget-amounts"></a>De resterende budgetbedragen bekijken en analyseren

Voer de volgende stappen uit om de budgetbedragen voor projecten aan het einde van het jaar te bekijken, maar draag de bedragen niet over.

1. Ga naar **Projectmanagement en financiële administratie** > **Periodiek** > **Budgetten** > **Budgetten overboeken**. 
2. Op de pagina **Overdrachtsproces voor projectbudget** verifieert u op het tabblad **Eindejaarsopties** of **Overdracht resterende projectbudgetbedragen** niet is ingeschakeld.
3. Selecteer op het tabblad **Parameters** in het veld **Projectbudgetjaar** het fiscaal jaar waarvoor u het resterende budgetbedrag wilt zien. 
4. Selecteer in het veld **Fiscaal jaar openen** het fiscaal jaar waarvoor u het resterende budgetbedrag wilt zien. 
5. Selecteer **Resterend budget** in het veld **Van prognosemodel**. 
6. Selecteer **Met nul resterend weergeven** om projecten op te nemen die voldoen aan uw geselecteerde criteria en geen resterend budget hebben.  
7. Op het tabblad **Budgetten selecteren** selecteert u **Alle budgetten ophalen** om alle budgetten te laden die voldoen aan uw geselecteerde criteria, en selecteer vervolgens **Verwerken**. 
8. Selecteer **Geselecteerde budgetten ophalen** om een databasequery te ontwerpen die een specifieke set budgetten in het deelvenster laadt.

Selecteer de regel en vervolgens **Budgetdetails weergeven** of **Accounts weergeven** voor meer informatie over een specifieke regel in het deelvenster.

## <a name="carry-forward-remaining-budget-amounts"></a>Resterende budgetbedragen overdragen 

Wanneer u resterende budgetbedragen verwerkt, kunt u transacties in het grootboek maken voor de bedragen die u overdraagt. Als u grootboektransacties wilt maken, voert u de stappen uit in de sectie [Budgetbedragen overdragen en grootboektransacties maken](#carry-forward). 

> [!NOTE]
> Budgetbedragen die worden overgedragen, worden overgebracht naar het prognosemodel dat is geselecteerd op de pagina **Voorspellingsmodellen** als het transportprognosemodel.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Budgetbedragen overdragen en grootboektransacties maken

1.  Selecteer **Projectmanagement en financiële administratie** > **Periodiek** > **Budgetten** > **Budgetten overboeken**. 
2. Selecteer op de pagina **Overdrachtsproces voor projectbudget** de optie **Jaareinde** en schakel vervolgens **Overdracht resterende projectbudgetbedragen** en **Budgetregisterboekingen in het grootboek maken** in. 
3. Op het tabblad **Parameters** , in de veldgroep **Projectparameters** selecteert u het volgende:

   - **Projectbudgetjaar** : selecteer het begin van het fiscaal jaar waarvoor u het resterende budgetbedrag wilt zien. 
   - **Winst en verlies** : maak winst- en verliestransacties in het grootboek. 
   -  **OHW** : maak OHW-transacties in het grootboek.
   -  **Salaris** : maak salaristoewijzingstransacties in het grootboek. 

5. Vul de volgende informatie in de veldgroep **Grootboek** in: 

   - Selecteer in het veld **Fiscaal jaar openen** het fiscaal jaar waarnaar u de resterende budgetbedragen voor de projecten wilt overboeken. De standaardwaarde is één jaar na de waarde in het veld **Projectbudgetjaar**.
   -  In het veld **Overdrachtsperiode** selecteert u de periode waarvoor u de budgetregistergegevens in het grootboek wilt aanmaken. Dit is typisch de eerste periode bij het openen van het fiscaal jaar.

6. Vul de volgende informatie in de veldgroep **Kopiëren van/naar** in:

   - Selecteer in het veld **Van prognosemodel** het prognosemodel voor het projectbudget dat is gekoppeld aan de resterende budgetbedragen die u voor de projecten wilt overboeken. 
   - Selecteer in het veld **Naar grootboekbudgetmodel** het grootboekbudgetmodel dat is gekoppeld aan de budgetbedragen die u wilt overboeken naar het grootboek. 
   -  Selecteer **Verkoopvaluta overboeken** om de verkoopvaluta van het project te gebruiken voor de grootboektransacties die worden gemaakt wanneer u de budgetbedragen voor de projecten overboekt. Als de optie niet wordt geselecteerd, gebruiken de transacties de valuta voor boekhouding. 
   -  Selecteer **Met nul resterend weergeven** om projecten op te nemen die geen resterende budgetbedragen hebben, maar die voldoen aan de andere criteria die u selecteert in de projecten die in het onderste deelvenster worden weergegeven.

7. Op het tabblad **Budgetten selecteren** selecteert u **Alle budgetten ophalen** om alle budgetten te laden die voldoen aan uw geselecteerde criteria. Selecteer **Geselecteerde budgetten ophalen** als u liever een databasequery ontwerpt waarmee een specifieke set projectbudgetten in het deelvenster wordt geladen.
8. Selecteer voor elk project dat u wilt verwerken de optie aan het begin van de regel voor het project.

    > [!TIP]
    > Om alle of de meeste projecten te selecteren, selecteert u het vinkje in de linkerbovenhoek. Om het verwerken van een project uit te sluiten, verwijdert u het vinkje voor dat project.

9. Als u de resterende budgetbedragen voor de geselecteerde projecten wilt overboeken naar het geselecteerde fiscaal jaar en de budgetregistergegevens in het grootboek wilt creëren, selecteert **Verwerken**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Budgetbedragen overdragen zonder grootboektransacties te maken

1. Ga naar **Projectmanagement en financiële administratie** > **Periodiek** > **Budgetten** > **Budgetten overboeken**.
2. Op de pagina **Overdrachtsproces voor projectbudget** selecteert u in het veld **Eindejaarsopties** de optie **Overdracht resterende projectbudgetbedragen**.
3. Selecteer in de groep **Parameters** in het veld **Projectbudgetjaar** het fiscaal jaar waarvoor u het resterende budgetbedragen wilt zien.
4. Vul de volgende informatie in de groep **Kopiëren van/naar** in:

   - Selecteer in het veld **Van prognosemodel** het prognosemodel voor het projectbudget dat is gekoppeld aan de resterende budgetbedragen die u voor de projecten wilt overboeken. 
   - Selecteer **Met nul resterend weergeven** om projecten op te nemen die geen resterend budgetbedragen hebben maar aan andere geselecteerde criteria voldoen.
   - In de groep **Budgetten selecteren** selecteert u **Alle budgetten ophalen** om alle budgetten te laden die voldoen aan uw geselecteerde criteria. Selecteer **Geselecteerde budgetten ophalen** om een databasequery te ontwerpen die een specifieke set project budgetten in het deelvenster laadt.

5. Selecteer voor elk project dat u wilt verwerken de optie aan het begin van de regel voor het project. 
6. Selecteer **Verwerken** om de resterende budgetbedragen voor de geselecteerde projecten over te boeken naar het geselecteerde fiscaal jaar.


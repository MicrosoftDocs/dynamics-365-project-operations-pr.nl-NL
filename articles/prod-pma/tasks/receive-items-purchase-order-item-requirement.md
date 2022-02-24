---
title: Artikelen op inkooporder ontvangen vanuit artikelvereiste
description: In dit onderwerp wordt uitgelegd hoe u artikelen op een inkooporder kunt ontvangen vanuit een artikelvereiste.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074731"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Artikelen op inkooporder ontvangen vanuit artikelvereiste

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u artikelen op een inkooporder kunt ontvangen vanuit een artikelvereiste.

Door een artikelvereiste te gebruiken in plaats van een artikeltransactie, kunt u de levering plannen net voordat het artikel daadwerkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het kader van de handelsovereenkomst en de artikelvereiste opnemen in de productieplanning. 

Deze taak maakt gebruik van de USSI-gegevensset.

1. Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Projecten > Alle projecten**.
2. Selecteer in de lijst de koppeling in de gewenste rij.
3. Selecteer **Plannen** in het actievenster.
4. Selecteer **Artikelvereisten**.
5. Selecteer **Nieuw**.
6. Typ of selecteer in de nieuwe rij een waarde in het veld **Artikelnummer**.
7. Voer een getal in het veld **Hoeveelheid** in.
8. Selecteer **Opslaan**.
9. Selecteer **Beheren** in het actievenster.
10. Selecteer **Functies**.
11. Selecteer **Inkooporder maken**.
12. Schakel het selectievakje **Alles opnemen** in.
13. Typ of selecteer een waarde in het veld **Leveranciersaccount**.
14. Selecteer **OK**.
15. Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Alle inkooporders**.
16. Selecteer in de lijst de koppeling in de gewenste rij.
17. Selecteer **Aankoop** in het actievenster.
18. Selecteer **Bevestigen**.
19. Selecteer **Ontvangen** in het actievenster.
20. Selecteer **Productontvangst**.
21. Typ een waarde in het veld **Productontvangst**.
22. Selecteer **OK**.


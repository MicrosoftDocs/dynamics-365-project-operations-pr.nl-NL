---
title: Artikelen op inkooporder ontvangen vanuit artikelvereiste
description: In dit artikel ziet u hoe u artikelen ontvangt op een inkooporder vanuit een artikelbehoefte.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbe15fac325ad00bdd2f2fc6ddf3ae15df45271
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929530"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Artikelen op inkooporder ontvangen vanuit artikelvereiste

[!include [banner](../../includes/banner.md)]

In dit artikel ziet u hoe u artikelen ontvangt op een inkooporder vanuit een artikelbehoefte.

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
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
# <a name="multiple-approvers-on-an-expense-report"></a>Meerdere fiatteurs voor een onkostendeclaratie

[!include [banner](../includes/banner.md)]

Afhankelijk van het goedkeuringsbeleid voor onkosten van uw organisatie kan het zijn dat meer dan één persoon een door een werknemer ingediende onkostendeclaratie moet goedkeuren. Wanneer u het werkstroomproces instelt voor goedkeuring van onkostennota's, kunt u werkstroomelementen toevoegen die taken of stappen bevatten voor een of meer fiatteurs van onkostennota's. U kunt bijvoorbeeld vereisen dat alle onkostendeclaraties eerst worden goedgekeurd door de manager van de werknemer die het rapport heeft ingediend en vervolgens door de coördinator crediteurenadministratie.

Als u besluit dat u meerdere fiatteurs van onkostennota's nodig hebt, kunt u de werkstroomelementen op een van de volgende manieren toevoegen:

- Voeg één goedkeuringselement toe dat één stap bevat. De stap kan bijvoorbeeld vereisen dat een onkostennota wordt toegewezen aan een gebruikersgroep en dat deze wordt goedgekeurd door 50 procent van de leden van de gebruikersgroep.
- Voeg één goedkeuringselement toe dat meerdere stappen bevat. Het goedkeuringselement kan bijvoorbeeld de volgende stappen bevatten:

    1. De manager van de medewerker die de onkostennota heeft ingediend, keurt deze goed.
    2. De coördinator crediteurenadministrateur verifieert de betalingsbewijzen en de items in de onkostennota.
    3. De budgethouder keurt de onkostennota goed.

- Voeg meerdere goedkeuringselementen toe, die elk één stap hebben. U kunt bijvoorbeeld een afzonderlijk goedkeuringselement toevoegen voor elk van de volgende stappen:

    1. De manager van de medewerker keurt de onkostennota goed.
    2. De budgethouder keurt de onkostennota goed.
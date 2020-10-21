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
# <a name="expense-reports-and-multiple-approvers"></a>Onkostenrapporten en meerdere fiatteurs

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Afhankelijk van het goedkeuringsbeleid van uw organisatie kan het zijn dat meer dan één persoon een ingediende onkostennota moet goedkeuren. Wanneer u het werkstroomproces instelt voor goedkeuring van onkostennota's, kunt u werkstroomelementen toevoegen die taken of stappen bevatten voor een of meer fiatteurs van onkostennota's. U kunt bijvoorbeeld eisen dat alle onkostennota's worden goedgekeurd door twee afzonderlijke personen: de manager van de werknemer die het rapport heeft ingediend en de coördinator crediteurenadministratie.

Als u besluit dat u meerdere fiatteurs van onkostennota's nodig hebt, kunt u de werkstroomelementen op een van de volgende manieren toevoegen:

- Voeg één goedkeuringselement toe dat één stap bevat. De stap kan bijvoorbeeld vereisen dat een onkostennota wordt toegewezen aan een gebruikersgroep en dat deze wordt goedgekeurd door 50 procent van de leden van de gebruikersgroep.
- Voeg één goedkeuringselement toe dat meerdere stappen bevat. Het goedkeuringselement kan bijvoorbeeld de volgende stappen bevatten:

    1. De manager van de medewerker die de onkostennota heeft ingediend, keurt deze goed.
    2. De coördinator crediteurenadministrateur verifieert de betalingsbewijzen en de items in de onkostennota.
    3. De budgethouder keurt de onkostennota goed.

- Voeg meerdere goedkeuringselementen toe, die elk één stap hebben. U kunt bijvoorbeeld een afzonderlijk goedkeuringselement toevoegen voor elk van de volgende stappen:

    1. De manager van de medewerker keurt de onkostennota goed.
    2. De budgethouder keurt de onkostennota goed.

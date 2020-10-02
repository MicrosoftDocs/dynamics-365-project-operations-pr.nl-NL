---
title: Gecorrigeerde facturen
description: In dit onderwerp krijgt u informatie over gecorrigeerde factureren.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898075"
---
# <a name="corrected-invoices"></a>Gecorrigeerde facturen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Bevestigde facturen kunnen worden bewerkt. Wanneer u een bevestigde factuur bewerkt, wordt er een concept van de gecorrigeerde factuur gemaakt. Omdat wordt aangenomen dat u alle transacties en hoeveelheden van de oorspronkelijke factuur wilt terugboeken, bevat deze gecorrigeerde factuur alle transacties van de oorspronkelijke factuur en zijn alle hoeveelheden op de factuur nul (0).

Wanneer er transacties zijn die niet hoeven te worden gecorrigeerd, kunt u deze verwijderen uit het concept van de correctiefactuur. Als u alleen een gedeeltelijke hoeveelheid wilt terugboeken of retourneren, kunt u het veld Hoeveelheid in de regeldetails bewerken. Als u het factuurregeldetail opent, kunt u de oorspronkelijk gefactureerde hoeveelheid bekijken. U kunt vervolgens de huidige gefactureerde hoeveelheid bewerken, zodat deze kleiner of groter is dan de oorspronkelijke gefactureerde hoeveelheid.

Wanneer u een correctiefactuur bevestigt, wordt de oorspronkelijke gefactureerde werkelijke verkoopwaarde teruggeboekt en wordt er een nieuwe gefactureerde werkelijke verkoopwaarde gemaakt. Als de hoeveelheid is verlaagd, zorgt het verschil ervoor dat er ook een nieuwe, niet-gefactureerde werkelijke verkoopwaarde wordt gemaakt. Als de oorspronkelijke gefactureerde verkoopwaarde bijvoorbeeld voor acht uur was en het regeldetail van de gecorrigeerde factuur een gereduceerde hoeveelheid van zes uur heeft, wordt de oorspronkelijke gefactureerde verkoopregel teruggeboekt en worden er twee nieuwe werkelijke waarden gemaakt:

- Een gefactureerde werkelijke verkoopwaarde voor zes uur.
- Een niet-gefactureerde werkelijke verkoopwaarde voor de resterende twee uur. Deze transactie kan later worden gefactureerd of als niet-factureerbaar worden aangemerkt, afhankelijk van de onderhandelingen met de klant.

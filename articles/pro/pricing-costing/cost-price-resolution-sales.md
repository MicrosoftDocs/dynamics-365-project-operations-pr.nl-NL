---
title: Kostprijzen voor schattingen en werkelijke waarden omzetten - lite
description: Dit onderwerp bevat informatie over hoe kostprijzen voor schattingen en werkelijke waarden worden herleid.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764576"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Kostprijzen voor schattingen en werkelijke waarden omzetten - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Om kostprijzen en de kostprijslijst voor schattingen en werkelijke waarden te herleiden, wordt de informatie in de velden **Datum**, **Valuta** en **Contracterende eenheid** van het gerelateerde project gebruikt. Nadat de kostprijslijst is herleid, wordt het kostentarief herleid.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Kostentarieven herleiden voor regels met werkelijke waarden en schattingen voor tijd

Schattingsregels voor Tijd verwijzen naar de details van de prijsopgave- en contractregels voor tijd- en resourcetoewijzingen in een project.

Nadat een kostprijslijst is herleid, worden de velden **Rol** en **Resource-eenheid** op de schattingsregel voor Tijd vergeleken met de rolprijsregels in de prijslijst. Bij deze vergelijking wordt ervan uitgegaan dat u de standaardprijsdimensies voor arbeidskosten gebruikt. Als u het systeem hebt geconfigureerd om velden af te stemmen in plaats van of naast **Rol** en **Resource-eenheid**, dan wordt een andere combinatie gebruikt om een overeenkomende rolprijsregel op te halen. Als een rolprijsregel wordt gevonden met een kostentarief voor de combinatie van **Rol** en **Resource-eenheid**, is dat het standaardkostentarief. Als de waarden voor **Rol** en **Resource-eenheid** niet kunnen worden afgestemd, worden rolprijsregels opgehaald met een overeenkomende rol, maar lege waarden van de **Resource-eenheid**. Als er een overeenkomende rolprijsrecord is, wordt het kostentarief standaard ingesteld op die record. 

> [!NOTE]
> Als u een andere prioriteitstelling van **Rol** en **Resource-eenheid** configureert, of als u andere dimensies heeft die een hogere prioriteit hebben, zal dit gedrag dienovereenkomstig veranderen. Rolprijsrecords worden opgehaald met waarden die overeenkomen met elk van de prijsdimensiewaarden in volgorde van prioriteit, waarbij rijen met null-waarden voor die dimensies als laatste komen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Kostentarieven herleiden voor regels met werkelijke waarden en schattingen voor Onkosten

Schattingsregels voor Onkosten verwijzen naar de details van de prijsopgave- en contractregels voor onkosten en de schattingsregels voor onkosten in een project.

Nadat een kostprijslijst is herleid, gebruikt het systeem een combinatie van de velden **Categorie** en **Eenheid** op de onkostenschattingsregel die moeten worden vergeleken met de regels voor **Categorieprijs** op de herleide prijslijst. Als een categorieprijsregel wordt gevonden met een kostentarief voor de combinatie van **Categorie** en **Eenheid**, wordt het kostentarief standaard ingesteld. Als het systeem de waarden voor **Categorie** en **Eenheid** niet kan vergelijken, of als het een overeenkomende categorieprijsregel kan vinden, maar de prijsmethode niet **Prijs per eenheid** is, wordt het kostentarief standaard nul (0).

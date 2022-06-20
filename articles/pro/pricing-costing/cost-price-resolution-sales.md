---
title: Kostprijzen voor projectschattingen en werkelijke waarden omzetten
description: Dit artikel biedt informatie over hoe kostprijzen bij projectramingen en werkelijke projectwaarden worden opgelost.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c278d8994389145c6dbee7574d2354724d985722
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917524"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Kostprijzen voor projectschattingen en werkelijke waarden omzetten 

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

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Kostentarieven voor werkelijke en schattingsregels voor materiaal omzetten

Schattingsregels voor materiaal verwijzen naar de prijsopgave- en contractregeldetails voor materialen en de materiaalschattingsregels voor een project.

Nadat een kostprijslijst is omgezet, gebruikt het systeem een combinatie van de velden **Product** en **Eenheid** op de schattingsregel voor een materiaalschatting die vervolgens wordt vergeleken met de regels **Prijslijstitems** van de omgezette prijslijst. Als het systeem een productprijsregel vindt met een kostentarief voor de combinatie van de velden **Product** en **Eenheid**, wordt het kostentarief standaard ingesteld. Als de waarden voor **Product** en **Eenheid** niet kunnen worden vergeleken of als er geen overeenkomende prijslijstartikelregel kan worden gevonden, maar de prijsmethode is gebaseerd op Standaardkosten of Huidige kosten en geen van beide is gedefinieerd voor het product, worden de eenheidskosten standaard ingesteld op nul.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

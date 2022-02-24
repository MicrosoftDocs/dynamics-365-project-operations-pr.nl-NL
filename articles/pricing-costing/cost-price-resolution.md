---
title: Kostprijzen voor schattingen en werkelijke waarden herleiden
description: Dit onderwerp bevat informatie over hoe kostprijzen voor schattingen en werkelijke waarden worden herleid.
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877306"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Kostprijzen voor schattingen en werkelijke waarden herleiden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Om kostprijzen en de kostprijslijst voor schattingen en werkelijke waarden te herleiden, wordt de informatie in de velden **Datum**, **Valuta** en **Contracterende eenheid** van het gerelateerde project gebruikt. Nadat de kostprijslijst is herleid, wordt het kostentarief herleid.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Kostentarieven herleiden voor regels met werkelijke waarden en schattingen voor tijd

Schattingsregels voor Tijd verwijzen naar de details van de prijsopgave- en contractregels voor tijd- en resourcetoewijzingen in een project.

Nadat een kostprijslijst is herleid, worden de velden **Rol**, **Bedrijf voor resources** en **Resource-eenheid** op de schattingsregel voor Tijd gebruikt voor afstemming met de rolprijsregels in de prijslijst. Bij deze afstemming wordt ervan uitgegaan dat u standaardprijsdimensies voor arbeidskosten gebruikt. Als u het systeem hebt geconfigureerd om velden af te stemmen in plaats van of naast **Rol**, **Bedrijf voor resources** en **Resource-eenheid**, dan wordt een andere combinatie gebruikt om een overeenkomende rolprijsregel op te halen. Als een rolprijsregel wordt gevonden met een kostentarief voor de combinatie van **Rol**, **Bedrijf voor resources** en **Resource-eenheid**, is dat het standaardkostentarief. Als de combinatie van **Rol**, **Resourcingbedrijf** en **Resourcing-eenheid** niet kan worden gevonden, worden rolprijsregels met een overeenkomende rolwaarde, maar met nulwaarden voor **Resource-eenheid** en **Resourcingbedrijf** opgehaald.​ Nadat een overeenkomende rolprijsrecord met een overeenkomende rolprijswaarde is gevonden, wordt het kostentarief standaard uit die record gehaald. 

> [!NOTE]
> Als u een andere prioriteitstelling van **Rol**, **Bedrijf voor resources** en **Resource-eenheid** configureert, of als u andere dimensies heeft die een hogere prioriteit hebben, zal dit gedrag dienovereenkomstig veranderen. Het systeem haalt rolprijsrecords op met waarden die overeenkomen met elk van de prijsdimensiewaarden in volgorde van prioriteit, waarbij rijen met nulwaarden voor die dimensies als laatste in de prioriteitsvolgorde komen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Kostentarieven herleiden voor regels met werkelijke waarden en schattingen voor Onkosten

Schattingsregels voor Onkosten verwijzen naar de details van de prijsopgave- en contractregels voor onkosten en de schattingsregels voor onkosten in een project.

Nadat een kostprijslijst is herleid, wordt een combinatie van velden **Categorie** en **Eenheid** op de schattingsregel voor Onkosten gebruikt voor afstemming met de regels van **Categorieprijs** in de herleide prijslijst. Als een categorieprijsregel wordt gevonden met een kostentarief voor de combinatie van **Categorie** en **Eenheid**, wordt het kostentarief standaard ingesteld. Als de waarden van **Categorie** en **Eenheid** niet kunnen worden afgestemd of als wel een overeenkomende categorieprijsregel wordt gevonden, maar de prijsmethode niet **Prijs per eenheid** is, wordt het kostentarief standaard ingesteld op nul (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Kostentarieven voor werkelijke en schattingsregels voor materiaal omzetten

Schattingsregels voor materiaal verwijzen naar de prijsopgave- en contractregeldetails voor materialen en de materiaalschattingsregels voor een project.

Nadat een kostprijslijst is omgezet, gebruikt het systeem een combinatie van de velden **Product** en **Eenheid** op de schattingsregel voor een materiaalschatting die vervolgens wordt vergeleken met de regels **Prijslijstitems** van de omgezette prijslijst. Als het systeem een productprijsregel vindt met een kostentarief voor de combinatie van de velden **Product** en **Eenheid**, wordt het kostentarief standaard ingesteld. Als de waarden voor **Product** en **Eenheid** niet kunnen worden vergeleken, worden de eenheidskosten standaard ingesteld op nul. Deze standaardinstelling wordt ook gebruikt als er een overeenkomende prijslijstartikelregel is, maar de prijsmethode is gebaseerd op standaardkosten of huidige kosten die niet voor het product zijn gedefinieerd.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

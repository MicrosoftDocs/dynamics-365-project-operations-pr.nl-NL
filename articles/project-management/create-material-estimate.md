---
title: Financiële schattingen voor materialen in projecten
description: Dit artikel bevat informatie over het definiëren of schatten van projectgebaseerde materialen.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925680"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Financiële schattingen voor materialen in projecten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met Dynamics 365 Project Operations kunnen projectbeheerders projectgebaseerde materiaalkosten voor elk project of elke taak definiëren. Elke materiaalschatting kan worden gekoppeld aan een specifieke projecttaak. Materialen die in projecten worden gebruikt, kunnen toe te voegen producten of producten uit de productcatalogus zijn. Voor elke combinatie van een product en een eenheid kan een prijs worden gedefinieerd in de projectprijslijsten voor verkoop en de projectprijslijsten voor kosten.  

Voer de volgende stappen uit om een projectmateriaalschatting te bekijken, toe te voegen of te verwijderen.

1. Ga naar **Projecten** en selecteer het project dat u wilt bijwerken.
2. Bekijk op het tabblad **Materiaalschattingen** de lijst met projectmateriaalschattingen.
3. Selecteer **Nieuwe materiaalschatting** om een nieuwe materiaalschatting te maken. Of selecteer een materiaalschatting om te verwijderen en selecteer vervolgens **Materiaalschatting verwijderen**​.

De volgende tabel biedt informatie over de velden op de regel **Materiaalschatting** voor een project. 

| **Veld** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- |
| Opdracht | Een lijst met taken in het project. Dit omvat overzichts- en bladknooppunttaken. | Wanneer u een taak selecteert voor een materiaalschattingsregel, heeft dit invloed op de geschatte materiaalkosten en de geschatte materiaalverkoop voor een taak. Als dit veld leeg is, wordt de materiaalschatting alleen op projectniveau bijgehouden en samengevat. |
| Product selecteren |  U kunt opgeven of de schattingsregel voor een bestaand (catalogus)product of een toe te voegen product bedoeld is. | Dit veld bepaalt of u een product uit de catalogus of een in te schrijven product selecteert. |
| Product | De id van het product uit de productcatalogus. Wanneer u een product-id selecteert, wordt de waarde in het veld **Product selecteren** automatisch bijgewerkt naar **Bestaand product**​. De id wordt gebruikt om de kost- en verkoopprijzen uit de prijslijst op te halen. | Er is geen impact op dit veld. |
| Beschrijving van toe te voegen product | Een tekstveld om de productnaam toe te voegen. Dit veld moet worden gebruikt wanneer **Toe te voegen product** is geselecteerd in het veld **Product selecteren**.| Er is geen impact op dit veld. |
| Begindatum | De datum waarop het materiaal naar verwachting wordt gebruikt. | Er is geen impact op dit veld. |
| Eenhedengroep | De standaardwaarde in dit veld is afkomstig uit de standaardeenheidsgroep voor het catalogusproduct. U kunt dit veld bijwerken om een andere eenheidsgroep te selecteren. | Er is geen impact op dit veld. |
| Eenheid | De waarde in dit veld is de standaardeenheid van het geselecteerde product. U kunt dit veld bijwerken om een andere eenheid te selecteren. | Als u de eenheid wijzigt, worden de standaard eenheidsprijs en -kosten ook gewijzigd. |
| Aantal | De geschatte hoeveelheid van het product die in het project wordt gebruikt. | Er is geen impact op dit veld. |
| Kosten per eenheid | De eenheidskosten van de geselecteerde combinatie van product en eenheid zoals ingesteld in de toepasselijke kostprijslijst. | De eenheidskosten worden altijd weergegeven in de kostenvaluta van het project. Als er geen eenheidskosten zijn ingesteld voor de ingestelde combinatie van product en eenheid in de prijslijst, worden de kosten per eenheid standaard 0,00. |
| Prijs per eenheid | De prijs van de geselecteerde combinatie van product en eenheid zoals ingesteld in de toepasselijke verkoopprijslijst. | De eenheidsprijs wordt altijd weergegeven in de verkoopvaluta van het project. Als er geen eenheidsprijs is ingesteld voor de ingestelde combinatie van product en eenheid in de prijslijst, wordt de eenheidsprijs standaard 0,00.|
| Totale kosten | Het kostenbedrag dat wordt berekend als hoeveelheid \* kosten per eenheid.| Het kostenbedrag wordt altijd weergegeven in de kostenvaluta van het project. |
| Totale verkoop | Het verkoopbedrag dat wordt berekend als hoeveelheid \* prijs per eenheid. | Het verkoopbedrag wordt altijd weergegeven in de verkoopvaluta van het project. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]

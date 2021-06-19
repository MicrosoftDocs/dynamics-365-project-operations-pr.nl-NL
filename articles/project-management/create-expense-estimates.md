---
title: Financiële schattingen voor onkosten in projecten
description: Dit onderwerp biedt informatie over het definiëren of schatten van projectgebaseerde onkosten.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 18d8568fae35fc251d9cf48d900b8a436e2e4500
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014155"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Financiële schattingen voor onkosten in projecten
_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met Dynamics 365 Project Operations kunnen projectbeheerders projectgebaseerde onkosten voor elk project of een taak definiëren. Elk onkostenitem kan worden gekoppeld aan een specifieke projecttaak. Onkosten worden onderverdeeld in verschillende onkostencategorieën, die op organisatieniveau worden gedefinieerd. De prijzen en kosten voor elke onkostencategorie worden gedefinieerd in de prijslijst. 

Voer de volgende stappen uit om projectonkosten te bekijken, toe te voegen of te verwijderen.

1. Ga naar **Projecten** en selecteer het project waaraan u wilt werken.
2. Selecteer het tabblad **Projectschattingen** en bekijk de lijst met projectonkosten.
3. Selecteer **Nieuwe onkosten** om onkosten toe te voegen. Of selecteer een onkostenpost die u wilt verwijderen en selecteer vervolgens **Onkosten verwijderen**.

De volgende tabel biedt informatie over de velden op de regel **Onkostenschatting** voor een project. 

| **Veld** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- |
| Opdracht | Een lijst met taken in het project. Dit omvat overzichts- en bladknooppunttaken. | Het selecteren van een taak voor een onkostenschattingsregel heeft invloed op de geschatte onkosten en onkostenverkopen voor een taak. Als dit veld leeg wordt gelaten, wordt de onkostenschatting alleen op projectniveau bijgehouden en samengevat. |
| Categorie | Een lijst met transactiecategorieën waaraan onkostencategorieën in de toepassing zijn gekoppeld. | De keuze voor een categorie bepaalt de prijzen en kosten op de onkostenschattingsregel. |
| Begindatum | De datum waarop de onkosten naar verwachting plaatsvinden. | Er is geen downstreamimpact voor dit veld. |
| Eenhedengroep | De standaardwaarde in dit veld is afkomstig uit de eenheidsgroep die is ingesteld als standaardgroep voor de geselecteerde categorie. U kunt dit veld bijwerken om een andere eenheidsgroep te selecteren. | Er is geen downstreamimpact voor dit veld. |
| Eenheid | De waarde in dit veld is de standaardeenheid van de geselecteerde categorie. U kunt dit veld bijwerken om een andere eenheid te selecteren. | Als u de eenheid wijzigt, worden de standaard eenheidsprijs en -kosten ook gewijzigd. |
| Aantal | Het bedrag van de geschatte kosten die u maakt. | Er is geen downstreamimpact voor dit veld. |
| Kosten per eenheid | De kosten van de geselecteerde combinatie van categorie en eenheid zoals ingesteld in de toepasselijke kostprijslijst | De eenheidskosten worden altijd weergegeven in de kostenvaluta van het project. |
| Prijs per eenheid | De prijs van de geselecteerde combinatie van categorie en eenheid, zoals ingesteld in de toepasselijke verkoopprijslijst. | De eenheidsprijs wordt altijd weergegeven in de verkoopvaluta van het project. |
| Totale kosten | Het kostenbedrag dat wordt berekend als hoeveelheid \* kosten per eenheid.| Het kostenbedrag wordt altijd weergegeven in de kostenvaluta van het project. |
| Totale verkoop | Het verkoopbedrag dat wordt berekend als hoeveelheid \* prijs per eenheid. | Het verkoopbedrag wordt altijd weergegeven in de verkoopvaluta van het project. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]

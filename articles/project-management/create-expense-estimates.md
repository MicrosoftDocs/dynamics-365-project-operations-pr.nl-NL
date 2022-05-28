---
title: Financiële schattingen voor onkosten in projecten
description: Dit onderwerp biedt informatie over het definiëren of schatten van projectgebaseerde onkosten.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589466"
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

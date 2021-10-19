---
title: Overzicht van leveranciersinhoudingen
description: Dit onderwerp biedt een overzicht van de mogelijkheden voor leveranciersinhoudingen.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594577"
---
# <a name="vendor-retention-overview"></a>Overzicht van leveranciersinhoudingen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Uw organisatie wil mogelijk een deel van de betalingen aan leveranciers die aan projecten voor uw organisatie werken, inhouden. Voordat u uw leverancier betaalt, wilt u er bijvoorbeeld zeker van zijn dat de artikelen en services die zij hebben geleverd aan uw verwachtingen voldoen.

Wanneer u met leveranciers onderhandelt over aankopen voor projecten, kunt u de inhoudingstermijnen voor leveranciers opgeven, inclusief het percentage of het bedrag dat moet worden ingehouden. Als de leverancier artikelen en services levert, trekt u het opgegeven inhoudingspercentage of bedrag af van uw betaling aan de leverancier. Wanneer het project is voltooid of een tussenfase bereikt zoals gespecificeerd in het leverancierscontract, geeft u het ingehouden bedrag vrij en maakt u een betaling aan de leverancier.

## <a name="vendor-retention-example"></a>Voorbeeld van leveranciersinhoudingen

Het volgende voorbeeld laat zien hoe een percentage van een leveranciersfactuurbedrag wordt ingehouden op basis van het percentage dat is voltooid voor een project.

Contoso Robotics USA heeft een contract gesloten met de leverancier Fabrikam om 100 uur training te geven voor het apparatuurvernieuwingsproject. De totale contractwaarde bedraagt USD 30.000 met een overeengekomen koopprijs van USD 300 per uur.

De training wordt in drie fasen gegeven met het volgende schema:

- Fase 1: 50 uur, of 50 procent van het project
- Fase 2: 30 uur, of 80 procent van het project in totaal
- Fase 3: 20 uur, of 100 procent van het project

De volgende tabel bevat de inhoudingsvoorwaarden.

| **Percentage geleverde eenheden** | **In te houden percentage** | **Vrij te geven percentage** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

De transacties resulteren in de volgende bedragen:

- Fase 1:
  - Het te betalen bedrag is 50 x 300, ofwel 15.000.
  - 20 procent van het bedrag, oftewel 3000, wordt ingehouden en in een later stadium vrijgegeven.
  - Het bedrag dat aan de verkoper wordt betaald bedraagt 12.000.
- Fase 2:
  - Het te betalen bedrag is 30 x 300, ofwel 9000.
  - 10 procent van het bedrag, oftewel 900, wordt ingehouden.
  - 10 procent van de 3000 die in fase 1 werd ingehouden, oftewel 300, wordt vrijgegeven.
  - Het bedrag dat aan de verkoper wordt betaald bedraagt 8400. Dit bedrag is 9000 min de ingehouden 900 plus de 300 die zijn vrijgegeven uit de inhouding voor Fase 1.
- Fase 3:
  - Het te betalen bedrag is 20 x 300, ofwel 6000.
  - Er wordt geen bedrag ingehouden.
  - Het bedrag dat wordt vrijgegeven is 3600. Dit bedrag bestaat uit de 3000 die werden ingehouden in Fase 1, verminderd met de 300 van Fase 1 die werden vrijgegeven in Fase 2, plus de 900 die werden ingehouden in Fase 2.
  - Het bedrag dat aan de verkoper wordt betaald bedraagt 9600. Dit bedrag bestaat uit het ingehouden bedrag van 3600 plus de 6000 voor voltooiing van Fase 3.

Het totale bedrag dat aan de verkoper wordt betaald nadat de drie fasen zijn voltooid, is 30.000, oftewel het totale bedrag van de inkooporder (15.000 + 9000 + 6000).

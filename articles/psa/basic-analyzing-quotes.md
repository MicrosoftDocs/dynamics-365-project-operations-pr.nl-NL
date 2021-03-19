---
title: Analyse van projectprijsopgaven
description: Dit onderwerp bevat informatie over de analyse van projectprijsopgaven.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291253"
---
# <a name="analysis-of-project-quotes"></a>Analyse van projectprijsopgaven

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analyseert projectprijsopgaven om de winstgevendheid te schatten. Ook wordt geanalyseerd hoe goed de prijsopgave is afgestemd op de verwachtingen van de klant over de leverings- of voltooiingsdatum en het budget.

## <a name="profitability-analysis"></a>Winstgevendheidsanalyse

Project Service Automation analyseert de winstgevendheid met behulp van de brutomarge en de aangepaste brutomarge.

- Brutomarges worden berekend met behulp van de volgende formule:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- De aangepaste brutomarges wordt berekend aan de hand van de volgende formule:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Als de waarden voor brutomarge en aangepaste brutomarge veel verschillen, wordt veel van het werk in de prijsopgave geclassificeerd als niet-toerekenbaar.

## <a name="analysis-of-customer-expectations"></a>Analyse van klantverwachtingen

U kunt prijsopgaven analyseren en grafieken voor klantverwachtingen genereren over de planning en het budget als u waarden invoert voor de volgende velden:

- Het veld **Aangevraagde leveringsdatum** in de prijsopgavekoptekst.
- Het veld **Klantbudget** voor elke prijsopgaveregel (voor projectgebaseerde regels en productgebaseerde regels).

Een analyse van klantverwachtingen over de planning wordt uitgevoerd door de laatste einddatum van het details van de prijsopgaveregel te vergelijken met de gevraagde leveringsdatum voor alle prijsopgaveregels in de prijsopgave.

Een analyse van klantverwachtingen over het budget wordt uitgevoerd door de som van het totale klantbudget te vergelijken met het prijsopgavebedrag van alle prijsopgaveregels.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
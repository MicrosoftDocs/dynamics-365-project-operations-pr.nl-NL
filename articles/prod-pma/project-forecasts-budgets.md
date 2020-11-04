---
title: Projectprognoses en budgetten
description: Microsoft Dynamics 365 Finance biedt projectprognoses en projectbudgetten om uw projecten te beheren en te controleren.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074677"
---
# <a name="project-forecasts-and-budgets"></a>Projectprognoses en budgetten

[!include [banner](../includes/banner.md)]

Er zijn twee manieren voor het beheren en controleren van uw projecten: projectprognoses en projectbudgetten. 

Gebruik projectprognoses als uw organisatie een operationeel perspectief heeft en deze zich richt op de opbrengsten en kosten die worden afgeleid uit specifieke transacties. Gebruik projectbudgettering als uw organisatie zich echter meer richt op de financiële bedragen. 

Zowel projectprognoses als projectbudgetten gebruiken prognosemodellen om de geprojecteerde transactiebedragen vast te leggen. 

Elke methode heeft bepaalde voordelen. U moet de volgende punten in overweging nemen voordat u een methode voor uw organisatie selecteert.

|   Toewijzingsmethode       |           Projectprognoses            |        Projectbudgettering                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Periodetoewijzing**     | U kunt transacties niet expliciet toewijzen aan een boekingsperiode. In plaats daarvan zijn de prognose en de controle van de prognose gebaseerd op de levensduur van het project. Omdat prognoses zijn gebaseerd op een specifieke datum, moet u de periode afleiden uit de datum. | U kunt transacties toewijzen voor het hele project of voor een boekingsperiode. Als u over een periode toewijst, kunt u ongebruikte bedragen meenemen naar de volgende boekingsperiode. |
| **Transacties bekijken**  | U kunt transacties bekijken in de prognoseformulieren, waar u de prognoses voor het hele bedrijf en voor alle projecten ziet, ongeacht de hiërarchie. Als u zich op een bepaald project wilt concentreren, moet u de gegevens filteren.                                       | U kunt gebudgetteerde transacties weergeven voor een enkele projecthiërarchie. Daarom kunt u transactiegegevens voor een bovenliggend project of zijn subprojecten bekijken.                 |
| **Transactievariabelen** | Wanneer u prognosetransacties invoert, kunt u elk kenmerk gebruiken dat bestaat voor een werkelijke transactie. Dit zorgt voor meer detail in de prognose. U kunt bijvoorbeeld details invoeren voor hoeveelheden, werknemers, artikelen of regeleigenschappen.         | Als u budgetgegevens invoert, kunt u alleen bedragen, categorieën en activiteiten gebruiken.                    |
| **Beveiliging**              | Prognoses zijn gebaseerd op transacties die u invoert in de prognoseformulieren en omvatten geen procesbeheersingsmechanisme. Elke werknemer met machtigingen voor een prognoseformulier kan informatie herzien zonder goedkeuring.                                        | Budgettering maakt gebruik van het werkstroomsysteem, dat wijzigingsbeheer mogelijk maakt en u in staat stelt een geschiedenis van de revisies bij te houden.         |
| **Boekingstypen**           | Prognosetransactieboekingen zijn gebaseerd op het aantal eenheden en op kostprijs en eenheidsprijzen voor verkoop.  | Budgetgegevens zijn gebaseerd op bedragen, die zijn opgesplitst in kosten en opbrengsten.                                          |
| **Prognosemodellen**       | Omdat elke prognose aan een model moet worden gekoppeld, kunt u meerdere prognosemodellen maken en ook submodellen instellen.           | Projectbudgettering beperkt de prognosemodellen die worden gebruikt voor budgettering. Minder prognosemodellen kunnen de consistentie in prognoses helpen vergroten.                           |
| **Kostenoverschrijdingen**         | U kunt alleen het invoeren van transacties toestaan of weigeren die een kostenoverschrijding veroorzaken.   | Projectbudgettering biedt gebruikers extra controlemogelijkheden. U kunt waarschuwingen en overschrijdingen toestaan.                    |
| **Besturingselement**               | Prognoseregeling wordt uitgevoerd door gebruik te maken van prognosereductie. Werkelijke bedragen worden zonder audittrail afgetrokken van verwachte transactiesaldi. Dit kan het moeilijker maken om te traceren waar de daadwerkelijke transacties hebben plaatsgevonden.                   | Bij projectbudgetbeheer worden werkelijke bedragen afgetrokken van bedragen in het resterende budget. Dit zorgt voor een duidelijkere audittrail.                                   |

## <a name="project-forecasts"></a>Projectprognoses
Wanneer u projectprognoses gebruikt, kunt u prognosetransacties invoeren in prognoseformulieren voor elk transactietype. Elk kenmerk dat beschikbaar is voor een werkelijke transactie, kan worden gebruikt voor een prognosetransactie, bijvoorbeeld lijnwinstgevendheid, lijnkenmerken, werkers of beschrijvingen. U kunt ook projecteren wanneer u aan een klant factureert nadat u kosten hebt gemaakt. 

Projectprognosetransacties zijn gebaseerd op eenheden en bedragen. 

U moet elke projectprognose aan een prognosemodel koppelen. Wanneer u een prognosetransactie invoert, wordt automatisch een prognosemodel voorgesteld. Het prognosemodel fungeert als een container voor de prognosetransacties. 

U kunt prognosemodellen aanwijzen als submodellen voor een model. Hiermee kunt u prognoses maken per regio, tijdsperiode of afdeling. U kunt de prognosetransacties in een model kopiëren om een nieuw model te maken en u kunt de transacties ook overboeken naar het grootboek. Omdat er een één-op-één relatie is tussen een prognose en een model, stelt elk prognosemodel een apart budget op voor een project. 

Prognosemodellen kunnen prognosevermindering gebruiken als controlemechanisme voor projecten. Bij prognosevermindering verlagen werkelijke transacties de verwachte transactiesaldi. Omdat prognosevermindering echter wordt toegepast op het hoogste project in de hiërarchie, biedt het een beperkt overzicht van wijzigingen in de prognose. Als een werknemer bijvoorbeeld aan een subproject is gekoppeld, worden de werkelijke transacties voor de werknemer naar het bovenliggende project geboekt. Dit kan het moeilijk maken om wijzigingen bij te houden, omdat u niet gemakkelijk kunt bepalen welke transactie in welk deelproject een verlaging van het prognosebedrag heeft veroorzaakt. Daarom is het een goed idee om een kopie van een prognosemodel te maken om de prognosevermindering te gebruiken. U kunt vervolgens rapporten gebruiken om te zien wat oorspronkelijk was voorspeld. 

U kunt projectprognoses herzien, kopiëren, verwijderen of overbrengen naar een grootboekbudget. Er is echter geen procesbeheersing. Elke werknemer met machtiging voor een prognoseformulier kan informatie herzien zonder controle.

-   **Herzien** - U kunt een prognosetransactie herzien in dezelfde formulieren waarin de oorspronkelijke boekingen zijn gemaakt.
-   **Kopiëren of verwijderen** - Wanneer u prognosetransacties kopieert, kopieert u de transactieregels van het ene prognosemodel naar een ander prognosemodel. Wanneer u een prognose verwijdert, verwijdert u de prognosetransacties uit een prognosemodel. Selecteer specifieke transactietypen en datums om het aantal prognosetransacties die worden gekopieerd of verwijderd te beperken. Hiermee kunt u alleen specifieke delen van een prognose kopiëren of verwijderen.
-   **Overboeken** - Wanneer u een projectprognose overboekt naar een grootboekbudget, boekt u de prognosetransacties van een prognosemodel over naar een grootboekbudget. U kunt alle eerder overgeboekte transacties overschrijven in het grootboekbudget waarnaar u uw projectprognose overdraagt.

## <a name="project-budgets"></a>Projectbudgetten
Projectbudgettering is een eenvoudigere methode dan prognoses, hoewel het wel wordt geïntegreerd met prognosemodellen. Het maakt gebruik van een enkel boekingsformulier voor originele budgetdetails en herzieningen, en maakt prognoses mogelijk die alleen zijn gebaseerd op bedrag, categorie of activiteit. 

Bij projectbudgettering moeten alle originele budgetten en revisies ter goedkeuring naar een projectwerkstroom worden gestuurd. Werkstromen geven u meer controle over het proces en creëren een record met wijzigingsgeschiedenis. 

Projectbudgettering lijkt op grootboekbudgettering, maar is sneller en gemakkelijker in te stellen. Veel van de opties in grootboekbudgettering, zoals nummerreeksen of valuta, hoeven voor projecten niet apart te worden ingesteld.

Projectbudgetten worden automatisch gekoppeld aan twee prognosemodellen, één voor het oorspronkelijke budget en één voor het resterende budget. Daarom kunnen rapporten die zijn gebaseerd op prognosemodellen, budgetgegevens gebruiken. Wanneer een projectbudget wordt vastgelegd, maakt het systeem prognosetransacties op basis van de bijbehorende modellen, die worden gebruikt voor rapportage- en controledoeleinden.

## <a name="forecast-models"></a>Prognosemodellen
Prognosemodellen hebben een enkellaagse hiërarchie. Dit betekent dat één projectprognose moet worden gekoppeld aan één prognosemodel.

Als u projectprognoses gebruikt, kunt u modellen identificeren als submodellen. U kunt vervolgens prognoses maken per afdeling, tijdsperiode of regio. U kunt bijvoorbeeld een prognosemodel voor een jaar maken en vervolgens submodellen opstellen voor de regionale prognoses Noordoost, Zuidoost, Noordwest en Zuidwest die regionale hoofden indienen. Door verschillende opties te selecteren in de beschikbare rapporten, kunt u informatie bekijken op totale prognose of op submodel.




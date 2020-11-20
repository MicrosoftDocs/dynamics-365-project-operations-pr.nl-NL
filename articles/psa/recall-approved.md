---
title: Goedgekeurde tijdsvermeldingen of onkostenposten intrekken
description: Dit onderwerp bevat informatie over het intrekken van een eerder goedgekeurde tijds- of onkostentransactie.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120537"
---
# <a name="recall-approved-time-or-expense-entries"></a>Goedgekeurde tijdsvermeldingen of onkostenposten intrekken

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Een lid van het projectteam of een andere persoon die een tijdsvermelding of onkostenpost indient, kan deze tijdsvermelding of onkostenpost intrekken nadat deze is goedgekeurd. Het proces voor het intrekken van een goedgekeurde tijdsvermelding of onkostenpost heeft twee stappen:

1. Een indiener vraagt een intrekking aan.
2. Een fiatteur keurt de intrekking goed.

## <a name="request-a-recall"></a>Een intrekking aanvragen

Volg deze stappen om een intrekking aan te vragen van een goedgekeurde tijdsvermelding of onkostenpost.

1. Ga voor tijdsvermeldingen naar **Projecten** \> **Mijn werk** \> **Tijdsvermelding**.

    –of–

    Ga voor onkostenposten naar **Projecten** \> **Mijn werk** \> **Onkosten**.

2. Selecteer voor tijdsvermeldingen alle tijdsvermeldingen voor een specifieke combinatie van een project en een taak. Of selecteer in het raster de afzonderlijke cellen voor tijd op een specifieke datum voor een specifiek project.

    –of–

    Selecteer voor onkostenposten de rij voor de onkostenpost die u wilt intrekken.

3. Selecteer **Intrekken**. Er wordt een bevestigingsvenster weergegeven. Als de geselecteerde tijdsvermeldingen en onkostenposten al waren goedgekeurd, wordt u gevraagd een reden voor de intrekking in te voeren.
4. Voer een reden voor de intrekking in en selecteer vervolgens **OK** om de bewerking te bevestigen. Het systeem stuurt de persoon die de vermeldingen heeft goedgekeurd, een aanvraag om de intrekking goed te keuren.

> [!NOTE]
> Hoewel goedgekeurde tijdsvermeldingen en onkostenposten kunnen worden ingetrokken als een goedgekeurde tijd of onkostenpost al aan de klant is gefactureerd, kan er geen intrekkingsaanvraag worden gemaakt. Een gebruiker die probeert een intrekkingsaanvraag te maken, ontvangt een bericht waarin wordt gemeld dat de tijdsvermelding of de onkostenpost niet kan worden ingetrokken omdat deze al is gefactureerd.

## <a name="approve-or-reject-a-recall-request"></a>Een intrekkingsaanvraag goedkeuren of afwijzen

Volg deze stappen om een intrekkingsaanvraag goed te keuren of af te wijzen.

1. Ga naar **Projecten** \> **Mijn werk** \> **Goedkeuringen**.
2. Wijzig op lijstpagina **Goedkeuringen** de weergave in **Intrekkingsaanvragen voor goedkeuring**. Er wordt een lijst met ingediende intrekkingsaanvragen weergegeven.
3. Selecteer een of meer vermeldingen en selecteer vervolgens **Goedkeuren** of **Afwijzen**.
4. Als u **Goedkeuren** hebt geselecteerd, ontvangt u een waarschuwingsbericht waarin wordt uitgelegd wat de gevolgen van de goedkeuring zijn. Selecteer **OK** om de bewerking te bevestigen. De intrekkingsaanvraag is goedgekeurd.

    –of–

    Als u **Afwijzen** hebt geselecteerd, wordt de intrekkingsaanvraag afgewezen.

> [!NOTE]
> Wanneer er een intrekking wordt aangevraagd en de intrekking wordt goedgekeurd, controleert het systeem of er factureringsactiviteiten zijn voor de tijdsvermelding of onkostenpost. Als een vermelding al is gefactureerd, of als deze zich op een conceptfactuur bevindt, ontvangt de fiatteur een foutbericht waarin wordt gemeld dat de tijdsvermelding of de onkostenpost niet kan worden goedgekeurd voor intrekking, omdat deze al is gefactureerd.

## <a name="impact-of-a-recall-request"></a>Gevolgen van een intrekkingsaanvraag

Wanneer een goedkeuring wordt ingetrokken, heeft dit zowel operationele als financiële gevolgen.

### <a name="operational-impact"></a>Operationele gevolgen

Als een intrekkingsaanvraag is goedgekeurd, wordt de goedkeuringsrecord gemarkeerd **als** Afgewezen. De status van de vermelding wordt gewijzigd in **Geretourneerd** of **Afgewezen**, afhankelijk van of het een tijdsvermelding of een onkostenpost is.

Het projectteamlid kan posten weergeven, posten bewerken en vervolgens opnieuw indienen of posten volledig verwijderen.

Als een intrekkingsaanvraag wordt afgewezen, behoudt de vermelding de status **Goedgekeurd** en kan de vermelding niet worden bewerkt door het projectteamlid of de fiatteur voor het project.

### <a name="financial-impact"></a>Financiële gevolgen

Als een intrekkingsaanvraag wordt goedgekeurd, worden de corresponderende werkelijke waarden voor kosten en verkoop op de volgende manier bijgewerkt:

- Het veld **Aanpassingsstatus** wordt bijgewerkt naar **Aangepast**.
- Het veld **Factureringsstatus** wordt bijgewerkt naar **Geannuleerd**.

Vervolgens worden er stornoposten gemaakt in de tabel Werkelijke waarden. Om stornoposten te maken, kopieert het systeem de veldwaarden van de oorspronkelijke werkelijke waarden. De enige waarden die niet worden gekopieerd, zijn de hoeveelheidswaarden. In plaats daarvan worden deze waarden omgekeerd. Omgekeerde werkelijke waarden worden gemaakt voor de werkelijke waarden **Kosten** en **Niet-gefactureerde verkoop**. Het veld **Aanpassingsstatus** voor de teruggeboekte werkelijke waarden wordt ingesteld op **Niet aanpasbaar** en het veld **Factureringsstatus** wordt ingesteld op **Geannuleerd**. Door deze wijzigingen wordt bij de vastgelegde uitgaven en de omzetbacklog voor het project niet langer rekening gehouden met de bedragen die deze werkelijke waarden vertegenwoordigen.

Als een intrekkingsaanvraag wordt afgewezen, zijn er geen financiële gevolgen voor het project.

## <a name="changes-to-time-entry-records"></a>Wijzigingen in records voor tijdsvermeldingen

In de volgende afbeelding ziet u de wijzigingen die zich bij goedgekeurde tijdsvermeldingen voordoen wanneer ze worden ingetrokken.

![Statusovergangen van tijdsvermeldingen](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Wijzigingen in records voor onkostenposten

In de volgende afbeelding worden de wijzigingen weergegeven die zich bij goedgekeurde onkostenposten voordoen wanneer ze worden ingetrokken.

![Statusovergangen van onkostenposten](media/ExpenseEntryStateTransitions.png)

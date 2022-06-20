---
title: Eerder goedgekeurde vermeldingen intrekken
description: In dit artikel wordt uitgelegd hoe een projectteamlid de intrekking van eerder ingediende en goedgekeurde tijd-, onkosten- en materiaalgebruiksrecords kan aanvragen, en hoe een projectmanager intrekkingsaanvragen kan goedkeuren of afwijzen.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930358"
---
# <a name="recall-previously-approved-entries"></a>Eerder goedgekeurde vermeldingen intrekken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Een lid van het projectteam die een vermelding voor tijd, onkosten of materiaalgebruik indient, kan deze vermelding intrekken nadat deze is goedgekeurd. Het intrekkingsproces telt twee hoofdstappen:

1. Een indiener vraagt een intrekking aan.
2. Een fiatteur keurt de intrekkingsaanvraag goed.

## <a name="request-a-recall"></a>Een intrekking aanvragen

Volg deze stappen om een intrekking aan te vragen van een goedgekeurde vermelding voor tijd, onkosten of materiaalgebruik.

1. Volg een van deze stappen, afhankelijk van het type vermelding dat u wilt intrekken:

    - Ga voor tijdsvermeldingen naar **Projecten** \> **Mijn werk** \> **Tijdsvermelding** en selecteer alle tijdsvermeldingen voor een specifieke combinatie van een project en een taak. Of selecteer in het raster de afzonderlijke cellen voor tijd op een specifieke datum voor een specifiek project.
    - Ga voor onkostenposten naar **Projecten** \> **Mijn werk** \> **Onkosten** en selecteer de rij voor de onkostenpost die u wilt intrekken.
    - Ga voor materiaalgebruik naar **Projecten** \> **Mijn werk** \> **Logboek voor materiaalgebruik** en selecteer de vermelding voor materiaalgebruik die u wilt intrekken.

2. Selecteer **Intrekken**. Er wordt een bevestigingsvenster weergegeven. Als de geselecteerde vermelding voor tijd, onkosten of materiaalgebruik al waren goedgekeurd, wordt u gevraagd een reden voor de intrekking in te voeren.
3. Voer een reden voor de intrekking in en selecteer vervolgens **OK** om de bewerking te bevestigen. Het systeem stuurt de persoon die de vermeldingen heeft goedgekeurd, een aanvraag om de intrekking goed te keuren.

> [!IMPORTANT]
> U kunt geen intrekkingsaanvraag maken voor een goedgekeurde vermelding voor tijd, onkosten of materiaalgebruik die al aan de klant is gefactureerd. Als u dit probeert, ontvangt u een bericht waarin wordt gemeld dat de vermelding voor tijd, onkosten of materiaalgebruik niet kan worden ingetrokken omdat deze al is gefactureerd. In dit geval kunt u alleen een intrekking van de vermelding aanvragen als een correctiefactuur wordt gebruikt om de klant een volledige creditering of restitutie van de originele factuur te geven.

## <a name="approve-or-reject-a-recall-request"></a>Een intrekkingsaanvraag goedkeuren of afwijzen

Volg deze stappen om een intrekkingsaanvraag goed te keuren of af te wijzen.

1. Ga naar **Projecten** \> **Mijn werk** \> **Goedkeuringen**.
2. Wijzig op lijstpagina **Goedkeuringen** de weergave in **Intrekkingsaanvragen voor goedkeuring**. Er wordt een lijst met ingediende intrekkingsaanvragen weergegeven.
3. Selecteer een of meer vermeldingen en selecteer vervolgens **Goedkeuren** of **Afwijzen**.
4. Als u **Goedkeuren** hebt geselecteerd, ontvangt u een waarschuwingsbericht waarin wordt uitgelegd wat de gevolgen van de goedkeuring zijn. Selecteer **OK** om de bewerking te bevestigen. De intrekkingsaanvraag is goedgekeurd.

    –of–

    Als u **Afwijzen** hebt geselecteerd, wordt de intrekkingsaanvraag afgewezen.

> [!IMPORTANT]
> Wanneer een intrekking wordt goedgekeurd, controleert het systeem, net als bij een aanvraag hiervoor, of er factureringsactiviteiten zijn voor de vermelding voor tijd , onkosten of materiaalgebruik. Als een vermelding al is gefactureerd, of als deze zich op een conceptfactuur bevindt, ontvangt de fiatteur een foutbericht waarin wordt gemeld dat de tijdsvermelding of de onkostenpost niet kan worden goedgekeurd voor intrekking, omdat deze al is gefactureerd. In dit geval kan de fiatteur de intrekking alleen goedkeuren als een correctiefactuur wordt gebruikt om de klant een volledige creditering of restitutie van de originele factuur te verlenen.

## <a name="impact-of-a-recall-request"></a>Gevolgen van een intrekkingsaanvraag

Wanneer een goedkeuring wordt ingetrokken, heeft dit zowel operationele als financiële gevolgen.

### <a name="operational-impact"></a>Operationele gevolgen

Als een intrekkingsaanvraag is goedgekeurd, wordt de goedkeuringsrecord gemarkeerd **als** Afgewezen. De status van de vermelding wordt gewijzigd in **Geretourneerd** of **Afgewezen**, afhankelijk van of het een vermelding voor tijd, onkosten of materiaalgebruik is.

Het projectteamlid kan posten weergeven, posten bewerken en vervolgens opnieuw indienen of vermeldingen volledig verwijderen.

Als een intrekkingsaanvraag wordt afgewezen, behoudt de vermelding de status **Goedgekeurd** en kan de vermelding niet worden bewerkt door het projectteamlid of de fiatteur voor het project.

### <a name="financial-impact"></a>Financiële gevolgen

Als een intrekkingsaanvraag wordt goedgekeurd, worden de corresponderende werkelijke waarden voor kosten en verkoop op de volgende manier bijgewerkt:

- Het veld **Aanpassingsstatus** wordt bijgewerkt naar **Aangepast**.
- Het veld **Factureringsstatus** wordt bijgewerkt naar **Geannuleerd**.

Vervolgens worden er stornoposten gemaakt in de tabel Werkelijke waarden. Om stornoposten te maken, kopieert het systeem de veldwaarden van de oorspronkelijke werkelijke waarden. De enige waarden die niet worden gekopieerd, zijn de hoeveelheidswaarden. In plaats daarvan worden deze waarden omgekeerd. Omgekeerde werkelijke waarden worden gemaakt voor de werkelijke waarden **Kosten** en **Niet-gefactureerde verkoop**. Het veld **Aanpassingsstatus** voor de teruggeboekte werkelijke waarden wordt ingesteld op **Niet-aanpasbaar** en het veld **Factureringsstatus** wordt ingesteld op **Geannuleerd**. Door deze wijzigingen wordt bij de vastgelegde uitgaven en de omzetbacklog voor het project niet langer rekening gehouden met de bedragen die deze werkelijke waarden vertegenwoordigen.

Als een intrekkingsaanvraag wordt afgewezen, zijn er geen financiële gevolgen voor het project.

## <a name="changes-to-time-entry-records"></a>Wijzigingen in records voor tijdsvermeldingen

In de volgende afbeelding ziet u de wijzigingen die optreden bij goedgekeurde tijdsvermeldingen en de overeenkomstige goedkeuringsrecords wanneer ze worden ingetrokken.

![Statusovergangen van tijdsvermeldingen.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Wijzigingen in vermeldingsrecords voor onkosten en materiaalgebruik

In de volgende afbeelding ziet u de wijzigingen die optreden bij goedgekeurde vermeldingen voor onkosten en materiaalgebruik en de overeenkomstige goedkeuringsrecords wanneer ze worden ingetrokken.

![Statusovergangen van onkostenposten.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

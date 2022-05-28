---
title: De goedkeuring van eerder goedgekeurde vermeldingen annuleren
description: In dit onderwerp wordt uitgelegd hoe een projectmanager de goedkeuring van eerder goedgekeurde vermeldingen voor tijd, onkosten of materiaalgebruik kan annuleren.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584774"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>De goedkeuring van eerder goedgekeurde vermeldingen annuleren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Een projectmanager of fiatteur die voorheen vermeldingen voor tijd, onkosten of materiaalgebruik heeft goedgekeurd, kan deze goedkeuring intrekken voor deze vermeldingen. 

Volg deze stappen om de goedkeuring van een eerder goedgekeurde vermelding voor tijd, onkosten of materiaalgebruik te annuleren.

1. Ga naar **Projecten** \> **Mijn werk** \> **Goedkeuringen**.
2. De lijstpagina **Goedkeuringen** toont alle tijdsvermeldingen die wachten op goedkeuring. Wijzig de weergave in **Mijn eerdere goedkeuringen**.
3. Selecteer de tijd-, onkosten- of materiaalgoedkeuringen die u wilt annuleren. Selecteer vervolgens in het actiepaneel de optie **Goedkeuring annuleren**.
4. Selecteer **OK** in het bevestigingsbericht dat verschijnt om de bewerking te bevestigen.

> [!IMPORTANT]
> U kunt de goedkeuring van een eerder goedgekeurde vermelding voor tijd, onkosten en materiaalgebruik die al aan de klant is gefactureerd niet annuleren. Als u dit probeert, ontvangt u een bericht waarin wordt gemeld dat de goedkeuring niet kan worden geannuleerd omdat deze al is gefactureerd. In dit geval kunt u alleen een intrekking van de vermelding aanvragen als een correctiefactuur wordt gebruikt om de klant een volledige creditering of restitutie van de originele factuur te geven.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impact van het annuleren van de goedkeuring van een eerder goedgekeurde vermelding

Wanneer een goedkeuring wordt geannuleerd, heeft dit zowel operationele als financiële gevolgen.

### <a name="operational-impact"></a>Operationele gevolgen

Als de goedkeuring van een vermelding wordt geannuleerd, wordt de goedkeuringsrecord gemarkeerd als **Ingediend**. De status van de vermelding wordt gewijzigd in **Ingediend**. In deze fase kan een projectteamlid de vermelding intrekken zonder een intrekkingsaanvraag in te dienen.

De fiatteur kan de waarden voor **Factureerbare hoeveelheid** en **Factureringstype** wijzigen en vervolgens de vermelding opnieuw goedkeuren.

### <a name="financial-impact"></a>Financiële gevolgen

Als de goedkeuring van een vermelding wordt geannuleerd, worden de corresponderende werkelijke waarden voor kosten en verkoop op de volgende manier bijgewerkt:

- Het veld **Aanpassingsstatus** wordt bijgewerkt naar **Aangepast**.
- Het veld **Factureringsstatus** wordt bijgewerkt naar **Geannuleerd**.

Vervolgens worden er stornoposten gemaakt in de tabel Werkelijke waarden. Om stornoposten te maken, kopieert het systeem de veldwaarden van de oorspronkelijke werkelijke waarden. De enige waarden die niet worden gekopieerd, zijn de hoeveelheidswaarden. In plaats daarvan worden deze waarden omgekeerd. Omgekeerde werkelijke waarden worden gemaakt voor de werkelijke waarden **Kosten** en **Niet-gefactureerde verkoop**. Het veld **Aanpassingsstatus** voor de teruggeboekte werkelijke waarden wordt ingesteld op **Niet-aanpasbaar** en het veld **Factureringsstatus** wordt ingesteld op **Geannuleerd**. Door deze wijzigingen wordt bij de vastgelegde uitgaven en de omzetbacklog voor het project niet langer rekening gehouden met de bedragen die deze werkelijke waarden vertegenwoordigen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

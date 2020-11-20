---
title: De niet-overschrijdingsstatus en validaties beheren
description: Dit onderwerp bevat informatie over de niet-overschrijdingslimietcontroles die worden uitgevoerd in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129987"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>De niet-overschrijdingsstatus en validaties beheren 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

## <a name="not-to-exceed-on-approvals"></a>Niet-overschrijden op goedkeuringen

Wanneer een tijd- of onkostenboeking wordt ingediend, wordt een goedkeuringsrecord aangemaakt. Als de goedkeuring verschuldigd is en gekoppeld is aan een tijd- en materiaalcontractregel, voert het systeem een validatiecontrole voor niet-overschrijding uit op de volgende niveaus:

  - Controleer met de limiet die voor de klant is ingesteld op de projectcontractregel
  - Controleer met de limiet die is ingesteld op de contractregel
  - Controleer met de limiet die is ingesteld voor de klant
  - Controleer met de limiet die is ingesteld op het contract

De controles op elk niveau houden in dat het bedrag van de verkoopwaarde op deze goedkeuring de niet-overschrijdingslimiet op dat niveau niet overschrijdt waarbij rekening wordt gehouden met het bedrag van de reeds geboekte factureringsachterstand en het tot op heden gefactureerde bedrag op dat niveau.

Als de controle slaagt, krijgt de goedkeuring de validatiestatus van **Geslaagd**.

Als de controle mislukt, krijgt de goedkeuring de validatiestatus van **Mislukt**. In de details voor de niet-overschrijdingsvalidatie ziet de gebruiker op welk niveau de validatie is mislukt.

Wanneer de ingediende tijd- of onkostengegevens als niet-toerekenbaar worden beschouwd, wordt de validatiestatus niet-overschrijding ingesteld op **Niet van toepassing** en de validatiedetails op **Niet van toepassing**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Niet-overschrijding op niet-gefactureerde werkelijke verkoopcijfers

Wanneer een tijd- of onkostenboeking wordt goedgekeurd, worden records voor kosten en niet-gefactureerde werkelijke verkopen aangemaakt. Als de niet-gefactureerde werkelijke verkoopwaarde toerekenbaar is en wordt gekoppeld aan een tijd- en materiaalcontractregel, voert de toepassing een validatiecontrole voor niet-overschrijding uit op de volgende niveaus:

  - Controleer met de limiet die voor de klant is ingesteld van de projectcontractregel
  - Controleer met de limiet die is ingesteld op de contractregel
  - Controleer met de limiet die is ingesteld voor de klant
  - Controleer met de limiet die is ingesteld op het contract

De controles op elk niveau zorgen dat het bedrag van de werkelijke verkoopwaarde de niet-overschrijdingslimiet op dat niveau niet overschrijdt waarbij rekening wordt gehouden met het bedrag van de reeds geboekte factureringsachterstand en het tot op heden gefactureerde bedrag op dat niveau.

Als de controle slaagt, krijgt de niet-gefactureerde werkelijke verkoopwaarde de niet-overschrijdingsstatus **Vastgelegd**.

Als de controle mislukt, krijgt de niet-gefactureerde werkelijke verkoopwaarde de niet-overschrijdingsstatus **Mislukt**. In de validatiedetails ziet de gebruiker op welk niveau de validatie is mislukt.

Wanneer de niet-gefactureerde werkelijke verkoop als niet-toerekenbaar of gratis wordt beschouwd, als er geen niet-overschrijdingslimiet is ingesteld op een van de vier niveaus, of als de werkelijke waarde die wordt gecreëerd Kosten, Voorschot, Resource-eenheid of Verkoop binnen organisatie is, moeten de velden **Niet-overschrijdingsstatus** en **Details niet-overschrijdingsvalidatie** worden ingesteld op **Niet van toepassing**.

## <a name="reset-the-not-to-exceed-status"></a>De niet-overschrijdingsstatus opnieuw instellen

U kunt de niet-overschrijdingsstatus in bulk opnieuw instellen. Zo kunnen projectmanagers de niet-overschrijdingsvalidatie aanpassen om voorrang te geven aan facturering van één bepaald werk, tijd of onkosten boven andere die al zijn vastgelegd op basis van het beschikbare niet-overschrijdingsbedrag.

Nadat de niet-overschrijdingsstatus op niet-gefactureerde werkelijke verkopen is gereset, wordt het vastgelegde bedrag verlaagd. De projectmanager kan een andere hoeveelheid werk, tijd of onkosten selecteren die eerder niet zijn geslaagd voor de niet-overschrijdingsvalidatie en deze opnieuw evalueren. Met de verlaging van het vastgelegde bedrag zullen deze werkelijke waarden nu slagen voor de validatie. Dit helpt de projectmanager om meer invloed en controle uit te oefenen op de factureerbare transacties voor die periode.

Als u de niet-overschrijdingsstatus wilt resetten, selecteert u een of meer werkelijke waarden uit de weergave **Backlog voor facturering van tijd en materiaal** of **Werkelijke waarden** en vervolgens **Niet-overschrijdingsstatus opnieuw instellen**.

De niet-overschrijdingsstatus wordt opnieuw ingesteld op **Niet geëvalueerd** op alle relevante geselecteerde werkelijke waarden. Werkelijke waarden waarvan de niet-overschrijdingsstatus opnieuw is ingesteld, zijn niet-gefactureerde werkelijke verkopen die nog niet zijn gefactureerd, niet op een conceptfactuur staan en zijn gemarkeerd als toerekenbaar. Alle andere geselecteerde werkelijke waarden worden genegeerd.

## <a name="reevaluate-not-to-exceed-status"></a>Niet-overschrijdingsstatus opnieuw evalueren

U kunt de niet-overschrijdingsstatus in bulk opnieuw evalueren. Herevaluatie van de niet-overschrijdingsstatus is nuttig wanneer:

  - Er was een heronderhandeling met de klant over de niet-overschrijdingslimieten en de werkelijke waarden moeten opnieuw worden geëvalueerd.
  - De projectmanager wil de facturering van niet-gefactureerde verkoopachterstanden aanpassen door de ene werkhoeveelheid boven de andere te prioriteren.

Als u de niet-overschrijdingsstatus opnieuw wilt evalueren, selecteert u een of meer werkelijke waarden uit de weergave **Backlog voor facturering van tijd en materiaal** of **Werkelijke waarden** en vervolgens **Niet-overschrijdingsstatus opnieuw evalueren**.

Alle relevante geselecteerde werkelijke waarden met een limiet die niet mag worden overschreden, worden geëvalueerd op basis van de ingestelde niet-overschrijdingslimiet. Werkelijke waarden die relevant zijn voor het opnieuw evalueren van de niet-overschrijdingsstatus, zijn niet-gefactureerde werkelijke verkopen die niet zijn gefactureerd, niet op een conceptfactuur staan en zijn gemarkeerd als toerekenbaar. Alle andere geselecteerde werkelijke waarden.

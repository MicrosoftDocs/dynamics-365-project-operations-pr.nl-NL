---
title: Factuurschema's voor projectgebaseerde prijsopgaveregels
description: Dit artikel bevat informatie over het maken van factuurschema's en mijlpalen voor prijsopgaveregels.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1e431bc3586f9fef7a01348555e4ee4e06cc66c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918306"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Factuurschema's voor projectgebaseerde prijsopgaveregels

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Een projectgebaseerde prijsopgaveregel geeft de mogelijkheid om een factuurschema te maken. Dit is optioneel in de prijsopgavefase omdat de toepassing het factureren van een project niet ondersteunt wanneer het is gekoppeld aan een prijsopgaveregel. Facturering is pas toegestaan nadat de prijsopgave is geaccepteerd. De enige downstream-impact van het maken van een factuurschema tijdens de prijsopgavefase, is dat dit factuurschema wordt gekopieerd naar de projectgebaseerde contractregel. Als u tijdens de prijsopgavefase geen factuurschema maakt, kunt u dit doen op de projectmatige contractregel.

Over het algemeen is het doel van factuurschema's om automatisch conceptfacturen voor een projectgebaseerde contractregel te maken. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Een factuurschema voor tijd en materiaal maken voor een projectgebaseerde prijsopgaveregel

Wanneer de factureringsmethode voor een projectgebaseerde prijsopgaveregel Tijd en materiaal is, genereert het systeem een op datum gebaseerd factuurschema. Voer de volgende stappen uit om automatisch een op datum gebaseerd factuurschema te genereren.

1. Ga naar **Instellingen** > **Factuurfrequenties** en stel een factuurfrequentie ins.
2. Open op de pagina **Prijsopgaven** de projectprijsopgave en stel op het tabblad **Samenvatting** een gewenste leverdatum in.
3. Open de prijsopgaveregel met tijd en materiaal waarvoor u een op datum gebaseerd factuurschema wilt maken. 
4. Selecteer op het tabblad **Factuurschema** waarden in de velden **Facturering start** en **Factuurfrequentie**. 
5. Selecteer in het subraster **Factuurschema genereren**.
6. De applicatie genereert het factuurschema terwijl de velden **Uitvoeringsdatum van factuur**, **Einddatum transactie** en **Uitvoeringsstatus** op de volgende manier zijn ingesteld:

    - **Uitvoeringsdatum van factuur** wordt ingesteld op de datum die wordt bepaald op basis van de factuurfrequentie.
    - **Sluitingsdatum van de transactie** is ingesteld op de dag vóór **Uitvoeringsdatum van factuur**.
    - **Uitvoeringsstatus** wordt automatisch ingesteld op **Niet uitvoeren**. Wanneer de taak voor het automatisch maken van facturen wordt uitgevoerd voor een bepaalde datum van factuuruitvoering, wordt dit veld bijgewerkt naar **Uitvoering geslaagd** of **Uitvoering mislukt**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Een factuurschema voor vaste prijs maken voor een projectgebaseerde prijsopgaveregel

Als de projectgebaseerde prijsopgaveregel een **vaste** factureringsmethode heeft, maakt het systeem een op mijlpalen gebaseerd factuurschema. Voer de volgende stappen uit om dit schema automatisch te genereren voor een vaste set mijlpalen die over de kalenderperiode worden verdeeld.

1. Ga naar **Instellingen** > **Factuurfrequenties** en stel een factuurfrequentie ins.
2. Open op de pagina **Prijsopgaven** de projectprijsopgave en stel op het tabblad **Samenvatting** een gewenste leverdatum in.
3. Open de prijsopgaveregel met een vaste prijs waarvoor u een mijlpaalplanning moet maken. 
4. Selecteer op het tabblad **Factuurschema** waarden in de velden **Facturering start** en **Factuurfrequentie**. 
5. Selecteer in het subraster **Periodieke mijlpalen genereren**.
6. De toepassing genereert het factuurschema met een mijlpaalnaam, datum en bedrag.

    - De naam van de mijlpaal wordt ingesteld op de datum die wordt bepaald op basis van de factuurfrequentie.
    - De datum van de mijlpaal wordt ingesteld op de datum die wordt bepaald op basis van de factuurfrequentie.
    - Het mijlpaalbedrag wordt berekend door het prijsopgavebedrag op de projectgebaseerde prijsopgaveregel te delen door het aantal mijlpalen zoals bepaald door de frequentie en het begin van de facturering en de gewenste leverdatums.
    - Als de prijsopgaveregel ook een geschat belastingbedrag heeft, wordt deze waarde evenredig verdeeld over elke mijlpaal bij het genereren van periodieke mijlpalen.

### <a name="manually-create-milestones"></a>Handmatig mijlpalen maken

Mijlpalen met een vaste prijs kunnen ook handmatig worden gegenereerd als ze niet periodiek worden opgesplitst. Handmatig een mijlpaal maken:

Open de prijsopgaveregel met de vaste prijs waarvoor u een mijlpaal wilt maken. Op het tabblad **Factuurschema** selecteert u in het subraster **+ Een nieuwe mijlpaal voor de prijsopgaveregel maken** en voert u de vereiste informatie in op basis van de volgende tabel.

| **Veld** | **Locatie** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Naam van mijlpaal | Snelle invoer | De naam van de mijlpaal. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en aan de factuur |
| Projecttaak | Snelle invoer | Als de mijlpaal is gekoppeld aan een projecttaak, kunt u deze referentie gebruiken om aangepaste logica toe te voegen aan de mijlpaalstatus op basis van de taakstatus. | De toepassing heeft geen downstream-impact van deze verwijzing naar een taak. |
| Datum van mijlpaal | Snelle invoer | Stel de datum in waarop het proces voor het automatisch maken van facturen moet zoeken naar de status van deze mijlpaal waardoor deze in aanmerking komt voor facturering. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en aan de factuur. |
| Factuurstatus | Snelle invoer | Wanneer een mijlpaal wordt gemaakt, wordt deze status altijd ingesteld op **Niet gereed voor facturering**. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en aan de factuur. |
| Regelbedrag | Snelle invoer | Bedrag of waarde van de mijlpaal voor facturering aan de klant. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en aan de factuur. |
| Belastingen | Snelle invoer | Belastingbedrag dat wordt toegepast op de mijlpaal. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en aan de factuur. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
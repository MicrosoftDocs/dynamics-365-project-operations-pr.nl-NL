---
title: Onkostenbeheer configureren
description: In dit artikel worden de overwegingen en beslissingen beschreven die u tijdens het planningsproces moet maken voordat u Onkostenbeheer in Microsoft Dynamics 365 Finance configureert.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960331"
---
# <a name="configure-expense-management"></a>Onkostenbeheer configureren

In dit onderwerp worden de overwegingen en beslissingen beschreven die u tijdens het planningsproces moet maken voordat u Onkostenbeheer configureert. In Onkostenbeheer kunt u informatie opslaan over betalingswijzen, reisaanvragen, onkostendeclaraties, beleid, enzovoort.

Omdat veel van de beslissingen die u neemt wanneer u uw configuratie voor Onkostenbeheer plant, is gebaseerd op de hiërarchie en financiële structuur van uw organisatie, moet u de planningsdocumenten voor deze gebieden raadplegen.

## <a name="intercompany-expenses"></a>Intercompany-onkosten

Wanneer u intercompany-onkosten inschakelt, staat u rechtspersonen en werknemers toe om kosten te maken namens een andere rechtspersoon, en ontvangt u betalingen van de rechtspersoon waarvoor werk wordt uitgevoerd binnen uw organisatie. Een werknemer in rechtspersoon A voltooit bijvoorbeeld een project voor rechtspersoon B, en voor het project worden reisgerelateerde kosten gemaakt. Als intercompany-onkosten worden ingeschakeld, kan de werknemer een onkostendeclaratie indienen waarmee de onkosten naar rechtspersoon B worden geboekt, en de onkosten moeten vervolgens worden betaald door rechtspersoon A. Als uw organisatie geen meerdere rechtspersonen heeft, hoeft u geen intercompany-onkosten in te schakelen.

**Beslissing:** wilt u intercompany-onkosten inschakelen?

## <a name="financial-management"></a>Financieel beheer

Onkostenbeheer is nauw geïntegreerd met het financiële beheer van uw organisatie. Een groot deel van uw configuratie voor Onkostenbeheer wordt gebaseerd op de beslissingen die u hebt genomen over de financiën van uw organisatie. In de volgende secties worden de verschillende gebieden beschreven waarvoor planning en beslissingen nodig zijn, op basis van de financiële beslissingen van uw organisatie en de begeleiding van uw leidinggevende team.

### <a name="per-diems"></a>Dagvergoedingen

U moet de dagvergoedingen voor werknemers definiëren die uw organisatie biedt. Omdat dagvergoedingen doorgaans worden gebruikt om onkosten te dekken, zoals maaltijden, huisvesting en andere incidentele uitgaven, kunt u regels opstellen voor de dagvergoedingen die uw organisatie aanbiedt. Dagvergoedingstarieven kunnen worden gebaseerd op de tijd van het jaar, de reislocatie of beide. Wanneer u een dagvergoedingsregel definieert, kunt u opgeven dat een percentage van het dagvergoedingstarief wordt ingehouden als een werknemer gratis maaltijden of diensten ontvangt. U kunt ook niveaus voor dagvergoedingstarieven definiëren om het minimum en maximum aantal uren in te stellen dat het dagvergoedingstarief op de reis van een werknemer kan worden toegepast.

**Beslissingen:**

- Standaardregels voor dagvergoedingen voor de eerste en laatste dag:

    - Wat is het minimum aantal uren dat een werknemer per dag kan claimen en toch een dagvergoeding kan ontvangen?
    - Is er een verlaging van het bedrag dat wordt aangeboden voor maaltijden voor de eerste dag en de laatste dag? Als er een verlaging is, wat is dan het percentage van de verlaging?
    - Is er een verlaging van het bedrag dat wordt aangeboden voor een hotel voor de eerste en laatste dag? Als er een verlaging is, wat is dan het percentage van de verlaging?
    - Is er een verlaging van het bedrag dat wordt aangeboden voor andere onkosten die worden gemaakt op de eerste en laatste dag? Als er een verlaging is, wat is dan het percentage van de verlaging?

- Standaardregels voor dagvergoedingen:

    - Is er een procentuele verlaging in de dagvergoeding voor elke maaltijd als de maaltijd bijvoorbeeld gratis is? Als er een verlaging is, wat is dan het percentage van de verlaging voor elke maaltijd?
    - Wordt de maaltijdreductie berekend per dag, per reis of op basis van het aantal maaltijden per dag?
    - Moeten bedragen van dagvergoedingen op de reguliere manier worden afgerond of moeten ze naar boven worden afgerond?
    - Worden dagvergoedingen berekend over een periode van 24 uur of op een kalenderdag?

- Dagvergoedingsregels die op locatie worden gebaseerd:

    - Variëren de dagvergoedingstarieven afhankelijk van de locatie? Welke locaties zijn opgenomen?
    - Als dagvergoedingstarieven per locatie verschillen, welk percentagebedrag wordt dan voor elke locatie verstrekt voor de volgende soorten onkosten:

        - Maaltijden
        - Hotel
        - Overige onkosten

### <a name="expense-management-journals-and-accounts"></a>Journalen en rekeningen voor onkostendeclaraties

Voor Onkostenbeheer moet u meerdere journalen en rekeningen gebruiken. U moet bijvoorbeeld beslissen of dezelfde rekening wordt gebruikt voor kasvoorschotten en creditcardgeschillen.

**Beslissingen:**

- Naar welke grootboekjournalen mogen onkostendeclaraties worden geboekt?
- Welke rekening wordt gebruikt voor kasvoorschotten?
- Moeten kasvoorschotten onmiddellijk worden geboekt?

### <a name="payment-methods"></a>Betalingswijzen

Wanneer u werknemers toestaat om onkosten te maken namens uw bedrijf, moet u de betalingswijzen definiëren die werknemers mogen gebruiken. U kunt bijvoorbeeld werknemers toestaan om contant geld of een bedrijfscreditcard te gebruiken. U kunt werknemers ook toestaan persoonlijke creditcards te gebruiken en de werknemers vervolgens vergoeden. U moet de volgende beslissingen nemen voor elke betalingswijze die u toestaat.

**Beslissingen:**

- Welke betalingswijzen zijn toegestaan?
- Wie is de eigenaar van de onkosten van de betalingswijze?
- Is er een tegenrekeningtype? Als er een tegenrekeningtype is, welke is dat dan?
- Als er een tegenrekening is, wat is de rekening dan?
- Als de betalingswijze een creditcard is, mag de betalingswijze dan alleen worden gebruikt bij geïmporteerde transacties?

### <a name="expense-categories-and-shared-categories"></a>Onkostencategorieën en gedeelde categorieën

Wanneer werknemers een onkostendeclaratie maken, moeten alle onkosten die ze registreren, aan een onkostencategorie worden gekoppeld. Onkostencategorieën zijn afgeleid van gedeelde categorieën die kunnen worden gedeeld door de rechtspersonen in uw organisatie. Deze categorieën kunnen ook worden gedeeld in Projectbeheer en financiële administratie, afhankelijk van de manier waarop uw organisatie is gedefinieerd. Op basis van de definitie van uw organisatie en de richtlijnen van het implementatieteam moet u bepalen of de categorieën die worden gebruikt in Onkostenbeheer alleen worden gebruikt in Onkostenbeheer of dat ze moeten worden gedeeld tussen Projectbeheer en financiële administratie en Onkostenbeheer. Deze categorieën kunnen worden gedeeld tussen Project en Onkosten of Project en Productie, maar niet tussen Onkosten en Productie. Voor elke onkostencategorie moet u de volgende beslissingen nemen.

**Beslissingen:**

- Wat is de onkostencategorie? Voorbeelden zijn categorieën voor vluchten, hotel of kilometerstand.
- Kan de onkostencategorie ook worden gebruikt in Projectmanagement en financiële administratie?
- Wat is het onkostentype?
- Wat is de standaard betalingsmethode voor de onkostencategorie?
- Moeten onkosten in de onkostencategorie gespecificeerd worden?
- Wat is de standaard hoofdrekening voor de onkostencategorie?
- Wat is de standaard btw-groep van artikelen voor de onkostencategorie?
- Zijn aanvullende betalingsmethoden toegestaan voor de onkostencategorie? Als aanvullende betalingswijzen zijn toegestaan, welke zijn dat dan?
- Zijn er subcategorieën in deze onkostencategorie? Als er subcategorieën zijn, moet u bovendien de volgende beslissingen nemen:

    - Zijn subcategorieën uitgesloten van belastingteruggave?
    - Wat is de btw-groep van de subcategorieën?

Als de onkostencategorie ook wordt gebruikt in Projectbeheer en financiële administratie, beantwoord dan de overige vragen. Ga anders naar de volgende sectie.

- Welke kostenrekeningen worden gebruikt voor de volgende uitgaven?

    - Kosten
    - Salaristoewijzing
    - OHW - waarde van kostprijs
    - Kosten - artikel
    - OHW - waarde van kostprijs - artikel
    - Opgelopen verlies
    - Opgelopen verlies OHW

- Welke inkomstenrekeningen worden gebruikt voor het volgende?

    - Gefactureerde omzet
    - Toegerekende omzet - verkoopwaarde
    - OHW - verkoopwaarde
    - Opgebouwde opbrengst - productie
    - OHW - productie
    - Opgebouwde opbrengst - winst
    - OHW - winst
    - Opgebouwde opbrengst - abonnement
    - OHW - abonnement

### <a name="taxes"></a>Belastingen

Voor onkostengerelateerde belastingen moet u bepalen wat is opgenomen of ingeschakeld in onkostendeclaraties.

**Beslissingen:**

- Is verkoopbelasting inbegrepen in de onkostenbedragen?
- Moet belastingteruggave voor onkosten worden ingeschakeld?

    > [!NOTE]
    > Als u bij het plannen van het grootboek besloot om Amerikaanse verkoopbelasting toe te passen en belastingregels te gebruiken, kunt u geen belastingteruggave voor onkosten inschakelen. (Als u Amerikaanse verkoopbelasting wilt toepassen en belastingregels wilt gebruiken, stelt u de optie **Belastingregels voor verkoopbelasting toepassen** in op **Ja**.)

## <a name="policies"></a>Beleidsregels

Door beleid voor onkostendeclaraties op te stellen, kunt u uw organisatie helpen tijd en geld te besparen wanneer werknemers namens de organisatie onkosten maken. Beleid helpt ervoor te zorgen dat werknemers binnen budget blijven, alle vereiste informatie verstrekken en alleen geld uitgeven wanneer ze het nodig hebben. U moet de volgende beslissingen nemen voor elk onkostendeclaratiebeleid en elk goedkeuringsbeleid voor onkostendeclaraties dat u opstelt.

**Beslissingen:**

- Wat is de naam van het beleid?
- Waar dient het onkostenbeleid voor?
- Als u eerder hebt besloten intercompany-onkosten in te schakelen, op welke bedrijven in uw organisatie is dit beleid dan van toepassing?
- Wanneer is het beleid van kracht?
- Wanneer verloopt het beleid?
- Wat is de beleidsregel?
- Wat is het resultaat van de beleidsregel?

---
title: Parameters voor onkostenbeheer configureren
description: In dit onderwerp worden de parameters beschreven die het algemene gedrag in Onkostenbeheer bepalen.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8ecbd0abc16d0a29eea47d6bd1653a204a83de4c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897265"
---
# <a name="configure-expense-management-parameters"></a>Parameters voor onkostenbeheer configureren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

In dit onderwerp worden de parameters beschreven die het algemene gedrag in Onkostenbeheer bepalen.

## <a name="general"></a>Algemeen

| Veld                                                    | Beschrijving |
|----------------------------------------------------------|-------------|
| Standaardtarief van kilometervergoeding                                 | Voer het vergoedingstarief voor kilometervergoedingen in. Dit tarief wordt vermenigvuldigd met het aantal kilometers dat voor de onkosten is ingevoerd om het bedrag te berekenen dat wordt vergoed voor de reiskosten. |
| Onkostendoel valideren                                 | Schakel deze optie in om gebruikers te beperken tot een bestaande set waarden die is geconfigureerd in het veld **Doel van onkostennota** wanneer ze onkostennota's maken. |
| Persoonlijke onkosten betaald door                                | Selecteer wie verantwoordelijk is voor het betalen van creditcardtransactiebedragen die als persoonlijk worden gecategoriseerd. |
| Volledige onkostennota weergeven bij drill-back               | Selecteer deze optie om alle onkosten voor een onkostennota weer te geven wanneer de details van het originele document worden bekeken voor een specifiek boekstuk dat is gegenereerd toen de onkostennota werd geboekt. |
| Pre-autorisatie voor reizen is verplicht                 | Selecteer deze optie om te vereisen dat een reisaanvraag wordt ingediend en goedgekeurd voordat een werknemer een onkostennota kan indienen. |
| Verdelingen kunnen vóór het boeken worden bewerkt            | Geef op of de verdelingen van een onkostennota kunnen worden bewerkt voordat deze nota wordt geboekt. |
| Beleid onkostenbeheerbeleid evalueren                     | Geef op wanneer onkosten worden geëvalueerd om te bepalen of een onkostenbeleid is geschonden. Onkosten kunnen worden geëvalueerd voor overtredingen wanneer de onkosteninvoer wordt ingevoerd en opgeslagen of wanneer de onkosten worden ingediend voor goedkeuring. De beleidsregels voor ontvangsten die vereist zijn, worden geëvalueerd wanneer de onkostenregel wordt opgeslagen. |
| Intercompany-onkostenregels toestaan                         | Geef op of onkosten voor andere rechtspersonen kunnen worden ingevoerd in een onkostennota. |
| Wisselkoers bewerken toestaan voor creditcardonkosten | Selecteer deze optie zodat de gebruiker de wisselkoers voor geïmporteerde creditcardonkosten kan bewerken. |
| Hiërarchievelden met meerdere niveaus om weer te geven                  | Selecteer de fiatteursvelden die moeten worden weergegeven als het type werkstroomtoewijzing is ingesteld om een hiërarchie te zijn en de sectie **Hiërarchie** selectie is ingesteld om de goedkeuringshiërarchie met meerdere niveaus voor onkosten te gebruiken. Wanneer de goedkeuringshiërarchie met meerdere niveaus wordt gebruikt voor een werkstroom, worden de geselecteerde velden weergegeven op de onkostennota en kunnen deze worden bewerkt. |
| Creditcardnummer van personeel opgeven                        | Geef op of een nummer van 15 of 16 tekens kan worden ingevoerd en opgeslagen in het veld **Kaart-id** op de pagina **Creditcards** voor een werknemer. |
| Doel voor reisaanvraag valideren                      | Schakel deze optie in om gebruikers te beperken tot een bestaande set waarden die is geconfigureerd in het veld **Doel van onkostennota** wanneer ze reisaanvragen maken. |

## <a name="financial"></a>Financiële dienstverlening

| Veld                                                                                    | Beschrijving |
|------------------------------------------------------------------------------------------|-------------|
| Naam dagelijks journaal grootboek                                                                | Selecteer de naam van het grootboekjournaal waarnaar goedgekeurde onkostennota's moeten worden geboekt. |
| Belastingterugvordering voor onkosten inschakelen                                                        | Selecteer deze optie om belastingterugvordering voor onkosten voor in aanmerking komende uitgaven in te schakelen. Deze optie kan niet worden geselecteerd als Amerikaanse btw- en gebruiksbelastingregels zijn ingeschakeld. |
| Kasvoorschotten onmiddellijk boeken                                                           | Selecteer deze optie om een goedgekeurd kasvoorschot te boeken wanneer het betalings- en overboekingsproces is voltooid. Als deze optie niet is geselecteerd, genereert het betalings- en overboekingsproces een niet-geboekt algemeen journaal. |
| Boekingsdatum corrigeren tijdens boeken                                                   | Selecteer deze optie om de boekingsdatum bij te werken wanneer onkosten worden geboekt, als de huidige periode in de wacht staat of is afgesloten. De boekingsdatum wordt ingesteld op de volgende open periode. |
| De groepering van transacties toestaan op basis van de standaardtegenrekening die is opgegeven in de betalingsmethode       | Selecteer deze optie om de onkostentransacties voor een onkostennota samen te vatten op basis van de tegenrekening die in de betalingsmethode is opgegeven voor de onkosten. |
| Inclusief belasting                                                                             | Selecteer deze optie om standaard btw in het onkostenbedrag op te nemen. |
| Lasten vrijgeven bij sluiten van reisaanvragen                                      | Selecteer deze optie om lasten vrij te geven wanneer een goedgekeurde reisaanvraag wordt gesloten. |
| Indienen van reisaanvraag toestaan bij budgetoverschrijding voor budgetregister en projectbudget | Selecteer deze optie om medewerkers toe te staan reisaanvragen ter goedkeuring in te dienen, ook al overschrijden ze het toegestane budget dat is ingesteld in het budgetregister of het toegestane budget voor een project. |
| Indienen van onkostennota toestaan bij budgetoverschrijding voor budgetregister en projectbudget     | Selecteer deze optie om medewerkers toe te staan onkostennota's ter goedkeuring in te dienen, ook al overschrijden ze het toegestane budget dat is ingesteld in het budgetregister of het toegestane budget voor een project. |
| Goedkeuren van onkostennota alleen toestaan bij budgetoverschrijding voor budgetregister                 | Selecteer deze optie om fiatteurs toe te staan onkostennota's goed te keuren die het toegestane budget overschrijden dat is ingesteld in het budgetregister. |

## <a name="per-diem"></a>Per diem

| Veld                                 | Beschrijving |
|---------------------------------------|-------------|
| Minimum uren voor per diem            | Voer het standaard minimum aantal uren in dat een werknemer op een dag moet werken om in aanmerking te komen voor een dagvergoeding voor reisgerelateerde onkosten. Deze waarde wordt alleen als standaardwaarde gebruikt voor het veld **Minimum aantal uren** voor dagtariefniveaus. |
| Percentage maaltijden                          | Voer het standaardpercentage in van de dagvergoeding voor maaltijden die wordt gebruikt op de eerste en laatste dag van de reisgerelateerde onkosten wanneer het veld **Maaltijdvergoeding berekenen per** is ingesteld op **Maaltijdtype per dag** of **Aantal maaltijden per dag**. De werkdag op de eerste en laatste dag kan korter zijn dan een standaardwerkdag. Daarom kan het bedrag van de dagvergoeding op die dagen afwijken van het standaardbedrag. Als het percentage is ingesteld op **0** (nul), zijn de inhoudingen voor de eerste en laatste dag 0,00. |
| Percentage hotel                         | Voer het standaardpercentage van de dagvergoeding voor hotels in dat wordt gebruikt op de eerste en laatste dag van de reisgerelateerde onkosten. De werkdag op de eerste en laatste dag kan korter zijn dan een standaardwerkdag. Daarom kan het bedrag van de dagvergoeding op die dagen afwijken van het standaardbedrag. Als het percentage is ingesteld op **0** (nul), zijn de inhoudingen voor de eerste en laatste dag 0,00. |
| Ander percentage                         | Voer het standaardpercentage van de dagvergoeding voor diverse onkosten in dat wordt gebruikt op de eerste en laatste dag van de reisgerelateerde onkosten. De werkdag op de eerste en laatste dag kan korter zijn dan een standaardwerkdag. Daarom kan het bedrag van de dagvergoeding op die dagen afwijken van het standaardbedrag. Als het percentage is ingesteld op **0** (nul), zijn de inhoudingen voor de eerste en laatste dag 0,00. |
| Vergoeding in percentage voor ontbijt | Voer het bedrag in waarmee de dagvergoeding wordt verlaagd voor het ontbijt. Als een werknemer bijvoorbeeld een gratis ontbijt krijgt, wilt u misschien het bedrag van de dagvergoeding met 10 procent verlagen. |
| Vergoeding in percentage voor lunch     | Voer het bedrag in waarmee de dagvergoeding wordt verlaagd voor de lunch. Als een werknemer bijvoorbeeld een gratis lunch krijgt, wilt u misschien het bedrag van de dagvergoeding met 15 procent verlagen. |
| Vergoeding in percentage voor diner    | Voer het bedrag in waarmee de dagvergoeding wordt verlaagd voor het diner. Als een werknemer bijvoorbeeld een gratis diner krijgt, wilt u misschien het bedrag van de dagvergoeding met 25 procent verlagen. |
| Maaltijdvergoeding berekenen per           | Geef op hoe het systeem de dagelijkse verlaging voor maaltijden moet berekenen door op te geven of de verlaging is gebaseerd op het maaltijdtype per reis of per dag of op het aantal maaltijden dat per dag is toegestaan. |
| Afronding per dag                     | Selecteer het type afronding dat wordt gebruikt voor dagonkosten. Als u voor normale afronding kiest, worden dagonkosten met een bedrag van 0,50 naar boven afgerond tot 1,00 en worden dagvergoedingen met een bedrag lager dan 0,50 naar beneden afgerond naar 0,00. |
| Dagberekening baseren op          | Geef of een dagvergoeding is gebaseerd op een kalenderdag of een periode van 24 uur. |

## <a name="fax-cover-pages"></a>Faxvoorbladen

| Veld                          | Beschrijving |
|--------------------------------|-------------|
| Instructies                   | Voer de instructies in die werknemers moeten volgen wanneer ze een voorblad maken voor een fax die wordt gebruikt om ontvangstbewijzen te verzenden die betrekking hebben op een onkostennota. Selecteer **Vertalingen** om taalspecifieke tekst in te voeren die wordt weergegeven op basis van de gebruikerstaal. |
| Gebruikers-id (streepjescode-informatie) | Selecteer deze optie om de unieke id van een werknemer op te slaan in de streepjescode die op het voorblad van de fax wordt gebruikt. |
| Streepjescode                       | Selecteer de streepjescode die wordt gebruikt op het voorblad van de fax. Streepjescodes 39 en 128 worden ondersteund in Onkostenbeheer. |

## <a name="anti-corruption"></a>Anti-corruptie

| Veld                                 | Beschrijving |
|---------------------------------------|-------------|
| Anti-corruptieattest weergeven   | Selecteer deze optie om de anti-corruptietekst weer te geven wanneer een onkostennota wordt gemaakt. Specifieke onkostencategorieën kunnen vervolgens worden ingeschakeld waarvoor het anti-corruptieattest voor de onkostennota moet worden geselecteerd. Voor een geschenkcategorie gerelateerd aan de onkosten van een overheidsfunctionaris, kan bijvoorbeeld vereist zijn dat de werknemer bevestigt dat de onkosten voldoen aan het bedrijfsbeleid voor overheidsfunctionarissen. |
| Anti-corruptiebericht voor indiener | Voer de tekst in die moet worden getoond aan een werknemer die een onkostennota maakt. Selecteer **Vertalingen** om taalspecifieke tekst in te voeren die wordt weergegeven op basis van de gebruikerstaal. |
| Anti-corruptiebericht voor fiatteur  | Voer de tekst in die moet worden getoond aan de fiatteur wanneer een onkostennota wordt gemaakt. Selecteer **Vertalingen** om taalspecifieke tekst in te voeren die wordt weergegeven op basis van de gebruikerstaal. |

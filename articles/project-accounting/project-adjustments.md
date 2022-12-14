---
title: Productcorrecties
description: In dit artikel krijgt u informatie over projectcorrecties.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788295"
---
# <a name="project-adjustments"></a>Productcorrecties

_**Van toepassing op:** Project Operations voor scenario's op basis van voorradige artikelen/productieorders_

## <a name="adjustments-overview"></a>Correctieoverzicht

U kunt Microsoft Dynamics 365 Project Operations zodanig configureren dat gebruikers wijzigingen kunnen aanbrengen in geboekte transacties. U kunt projecttransacties afzonderlijk aanpassen of u kunt meerdere transacties tegelijkertijd in een lijst met alle projecttransacties selecteren. Projectcorrecties worden bijvoorbeeld gebruikt om de factureerbare status massaal bij te werken, de kosten opnieuw te berekenen na een configuratiewijziging of financieringsbronnen bij te werken.

Gebruikers hebben op verschillende manieren toegang tot de projectcorrectiefunctionaliteit:

- Door gebruik te maken van de pagina **Transacties aanpassen** die toegankelijk is via **Projectbeheer en financiële administratie** \> **Instelling**.
- Door de knop **Correctie** te gebruiken op de pagina **Geboekte projecttransacties** die toegankelijk is vanaf **Projectbeheer en financiële administratie** \> **Transacties**.
- Door de knop **Aanpassing** te gebruiken op de pagina **Geboekte projecttransacties** in het kader van een project. Deze pagina is toegankelijk via **Projectbeheer en financiële administratie** \> **Alle projecten**.

Om correcties mogelijk te maken, moet u een of meer transactiestatussen inschakelen vanuit **Projectbeheer en financiële administratie** \> **Parameters voor Projectbeheer en financiële administratie** op het tabblad **Algemeen** onder de sectie **Correctie van transactiestatus toestaan**. Voorbeelden van transactiestatussen zijn geboekte transacties, gefactureerde transacties of geëlimineerde transacties. Elke transactiestatus die is ingesteld op **Nee** heeft transacties in die status die niet in het correctieproces verschijnen als selecteerbaar voor correctie.

Een configuratieoptie met de naam **Altijd correctietransactie maken** is momenteel beschikbaar in projectbeheer en de parameters voor financiële administratie. U kunt deze optie uitschakelen om de oorspronkelijke transactie bij te werken in plaats van nieuwe transacties te maken tijdens de correctie in een subset van scenario's. Er is aangekondigd dat deze parameter per 1 maart 2023 is afgeschaft. Na 1 maart 2023 gedraagt het systeem zich altijd alsof de optie is ingeschakeld.

## <a name="adjustments-process-flow"></a>Correctieprocesstroom

De volgende stappen tonen de typische stroom voor het verwerken van correcties.

1. Open de pagina **Projectcorrecties**.
2. Selecteer **Selecteren** om te zoeken naar transacties die voldoen aan de verwachte criteria voor correctie.
3. Selecteer in de lijst met transacties alle transacties of een subset van de transacties voor correctie.
4. Selecteer **Aanpassen** en wijzig de kenmerken op de regel. Als de waarden handmatig zijn opgegeven tijdens het invoeren van transacties, kunt u er ook voor kiezen om standaardsysteemwaarden in te voeren.
5. De lijst met transacties wordt geretourneerd, en er verschijnt een vinkje in de kolom **Correctie in behandeling** om aan te geven waar wijzigingen zijn aangebracht. Alle correcties die wijzigingen in behandeling hebben, worden weergegeven in de onderste helft van de pagina. Daar kunt u aanvullende gedetailleerde wijzigingen aanbrengen die verder gaan dan wat op de vorige pagina werd getoond.
6. Selecteer **Boeken** om de correctietransacties te boeken.

Afhankelijk van de configuratie worden doorgaans nieuwe transacties gemaakt voor de correctie.

- Het veld **Factuurstatus** van de oorspronkelijke transactie is ingesteld op **Aangepast**.
- Er wordt een terugboekingstransactie gemaakt om de oorspronkelijke transactie terug te draaien, en het veld **Status** wordt ingesteld op **Aangepast**.
- Er wordt een nieuwe transactie gemaakt met de wijzigingen die zijn aangebracht tijdens het correctieproces.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Meerdere geboekte projecttransacties tegelijk selecteren voor correcties en creditnota's

Een nieuwe functie die is geïntroduceerd in release 10.0.30 maakt het mogelijk om meerdere transacties tegelijk te selecteren voor correctie vanaf de pagina **Geboekte projecttransacties** .

Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem. Beheerders kunnen de werkruimte **Functiebeheer** gebruiken om de status van de functie te controleren en desgewenst in te schakelen. Zoek in de werkruimte **Functiebeheer** naar **Meerdere geboekte projecttransacties voor correcties en creditnota's selecteren** en selecteer deze optie, gevolgd door **Nu inschakelen**.

Deze functie schakelt het volgende sleutelkenmerk in:

- Het is toegankelijk vanaf de pagina Geboekte transactie binnen een project door de bestaande kop **Correctie** te gebruiken.
- Het maakt een selectie van meerdere rijen mogelijk op de pagina **Geboekte projecttransacties**. U kunt filters toepassen op de lijstpagina en uw records selecteren voordat u met correcties begint.
- De knop **Correctie** wordt uitgeschakeld als een enkele transactie niet kan worden gecorrigeerd, of als u een combinatie van creditnota's en dagboeken samen selecteert in plaats van afzonderlijk.
- Door de toevoeging van de mogelijkheid om meerdere rijen te selecteren, is de link **Toegezegde kosten** in het lint niet langer uitgeschakeld als er meerdere rijen zijn geselecteerd.
- Het voegt het volgende waarschuwingsbericht toe: "U hebt meer dan (geselecteerd aantal) records geselecteerd voor correctie. Doorgaan met deze actie kan even duren. Weet u zeker dat u deze wilt doorgaan met deze actie?

Deze functie verwijdert ook stap 2 uit de processtroom die eerder in dit artikel is beschreven. Daarom worden alle transacties die zijn geselecteerd voordat de pagina **Transacties corrigeren** werd geopend, opgenomen in de lijst met transacties voor correctie. U hoeft de knop **Selecteren** niet te gebruiken om ernaar te zoeken.

> [!NOTE] 
> Zelfs als deze functie is uitgeschakeld, kunt u nog steeds meerdere records selecteren voor correctie. Er blijft echter slechts één record *geselecteerd*, en het dialoogvenster **Transacties selecteren** verschijnt direct nadat u ervoor hebt gekozen om correcties openen.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Correctietransactiestatussen die kunnen worden in- of uitgeschakeld voor correcties

De volgende statussen kunnen worden in- of uitgeschakeld op het tabblad **Algemeen** van de pagina **Parameters voor projectbeheer- en financiële administratie**:

- Geboekt
- Factuurvoorstel
- Gefactureerd
- Geschat
- Geëlimineerd
- Beginsaldo (uur)

## <a name="adjustment-parameters"></a>Correctieparameters

Deze parameters staan vermeld op de pagina **Parameters voor projectbeheer en financiële administratie** op het tabblad **Algemeen** onder de groep **Correctie** en wijzigt gedrag voor hoe correcties worden verwerkt. 

| Parameternaam | Omschrijving |
|----------------|-------------
| Maak altijd een correctietransactie aan | Als deze parameter is ingeschakeld, zal het correctieproces altijd een nieuwe terugboekingstransactie en een nieuwe aangepaste transactie creëren als er sprake is van een financiële of rapportage-impact. Als de parameter is uitgeschakeld, zal het correctieproces de oorspronkelijke transactie bijwerken in plaats van een terugboeking en een nieuwe transactie te creëren voor een scenario als een update van de transactietekst. |
| Veld automatische update | Als deze parameter is ingeschakeld, herberekent het systeem de kostprijs en de verkoopprijs. |
| De correctiedatum gebruiken als nieuw project | Deze parameter wordt gebruikt om transacties naar een toekomstige boekingsperiode te verplaatsen voordat het systeem deze functie ondersteunde. We raden u af om het te gebruiken, omdat het de zakelijke datum van de transactie verandert en in een toekomstige versie wordt afgeschaft. |
| Gesloten activiteiten toestaan | Normaal gesproken kunnen er geen transacties worden gemaakt voor afgesloten activiteiten. Als deze parameter is ingeschakeld, wordt dat gedrag onderdrukt. Daarom kunnen er correcties worden gemaakt voor gesloten activiteiten. |

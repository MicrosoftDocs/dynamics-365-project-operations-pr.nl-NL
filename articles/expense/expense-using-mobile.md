---
title: Mobiele onkosten-app
description: Dit onderwerp bevat informatie over de mobiele werkruimte Onkostenbeheer.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5ab5959fa5c9c5463826a9a792112a93e469de5f
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818177"
---
# <a name="mobile-expense-app"></a>Mobiele onkosten-app

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dit onderwerp bevat informatie over de mobiele werkruimte **Onkostenbeheer**. In deze werkruimte kunnen gebruikers een betalingsbewijs vastleggen en uploaden, zodat ze dit later aan een onkostennota kunnen toevoegen. Gebruikers kunnen ook snel een onkostenregel maken met behulp van een bijgevoegd betalingsbewijs en onkostennota's maken en beheren. Bovendien kunnen fiatteurs de mobiele werkruimte **Onkostenbeheer** gebruiken om onkostennota's te bekijken die aan hen zijn toegewezen en die onkostennota's goed te keuren of af te wijzen.

Deze mobiele werkruimte is bedoeld om te worden gebruikt met de mobiele app Dynamics 365 Unified Ops.

Veel organisaties eisen dat een kopie van een betalingsbewijs wordt toegevoegd aan een reisgerelateerde of zakelijke onkostennota die een werknemer ter vergoeding indient. Met de mobiele werkruimte **Onkostenbeheer** kunnen gebruikers snel nieuwe onkostenregels maken op het mobiele apparaat van hun keuze door een bijgevoegde foto van een betalingsbewijs te gebruiken. Gebruikers kunnen ook een foto van een betalingsbewijs maken en deze later aan een onkostennota toevoegen. Werknemers kunnen ook hun onkostennota's maken en beheren en deze vervolgens ter goedkeuring en vergoeding indienen via hun mobiele apparaat.

In de mobiele werkruimte **Onkostenbeheer** kunt u de volgende taken uitvoeren:

- Een foto maken van een betalingsbewijs. U kunt de foto van het betalingsbewijs uploaden en later toevoegen aan een onkostennota.
- Een bestand uploaden als een vastgelegd betalingsbewijs. U kunt dat bestand later als bijlage aan een onkostennota toevoegen.
- Een nieuwe onkostenregel maken met behulp van een bijgevoegd betalingsbewijs. U kunt het regelitem vervolgens later aan een onkostennota toevoegen en ter goedkeuring en vergoeding indienen.

U kunt ook de volgende functies gebruiken:

- Een nieuwe onkostennota maken.
- Creditcardtransacties en andere eerder gemaakte onkosten toevoegen aan een onkostennota.
- Nieuwe onkosten maken voor een onkostennota.
- Een betalingsbewijs toevoegen aan alle onkosten voor een onkostennota, hetzij door een foto van het betalingsbewijs te maken, hetzij door een bestand te uploaden als een vastgelegd betalingsbewijs.
- Afhankelijk van het onkostenbeleid van het bedrijf, de lijst met gasten toevoegen aan onkosten.
- Afhankelijk van het onkostenbeleid van het bedrijf, onkosten specificeren.
- Een onkostennota indienen ter goedkeuring en vergoeding.
- Onkostennota's waarvoor u een toegewezen fiatteur bent, goedkeuren of afwijzen.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Vereisten als u Dynamics 365 Finance gebruikt

Als Finance is geïmplementeerd voor uw organisatie, moet het systeembeheerder de mobiele werkruimte **Onkostenbeheer** publiceren. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>De mobiele app Dynamics 365 Unified Ops downloaden en installeren
De mobiele app Dynamics 365 Unified Ops downloaden en installeren:

- [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
- [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app
1. Start de app op uw mobiele apparaat.
2. Voer uw URL voor Dynamics 365 in.
4. Wanneer u zich voor het eerst aanmeldt, wordt u om uw gebruikersnaam en wachtwoord gevraagd. Voer uw referenties in.
5. Nadat u zich hebt aangemeld, worden de beschikbare werkruimten voor uw bedrijf weergegeven. Als uw systeembeheerder later een nieuwe werkruimte publiceert, dient u de lijst met mobiele werkruimten te vernieuwen.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Een betalingsbewijs vastleggen met behulp van de mobiele werkruimte Onkostenbeheer

1. Open op uw mobiele apparaat de werkruimte **Onkostenbeheer**.
2. Selecteer **Betalingsbewijs vastleggen**.
3. Selecteer **Foto nemen** of **Afbeelding kiezen**.
4. Volg een van deze stappen:

    - Als u **Foto nemen** hebt geselecteerd, volgt u deze stappen:

        1. U gaat automatisch naar naar de camera van uw mobiele apparaat, zodat u een foto kunt maken van het betalingsbewijs. 
        2. Als u klaar bent met het maken van een foto, selecteert u **OK** om de foto te accepteren.
        3. Optioneel: voer een naam in voor de foto en voer eventuele opmerkingen in.

    - Als u **Afbeelding kiezen** hebt geselecteerd, volgt u deze stappen:

        1. Selecteer een afbeelding in de lijst.
        2. Optioneel: voer een naam in voor de afbeelding en voer eventuele opmerkingen in.

5. Selecteer **Gereed**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Snel betalingsbewijzen vastleggen met behulp van de mobiele werkruimte Onkostenbeheer

1. Open op uw mobiele apparaat de werkruimte **Onkostenbeheer**.
2. Selecteer **Snel onkosten invoeren**.
3. Selecteer de onkostencategorie. U ziet een lijst van onkostencategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) te lezen voor meer informatie. Als uw categorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op onkostencategorie of schakel over naar zoeken op onkostentype.
4. Voer de transactiedatum van de onkosten in.
5. Optioneel: voer de winkel in voor de onkosten.
6. Voer het bedrag van de onkosten in.
7. Selecteer de valuta van de onkosten in. U ziet een lijst van valutacodes die in uw app zijn geladen voor offline gebruik. Standaard worden 400 valuta geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) te lezen voor meer informatie. Als uw valuta niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op valuta of schakel over naar zoeken op naam.
8. Selecteer **Foto nemen** of **Afbeelding kiezen**.
9. Volg een van deze stappen:

    - Als u **Foto nemen** hebt geselecteerd, gaat u automatisch naar naar de camera van uw mobiele apparaat, zodat u een foto kunt maken van het betalingsbewijs. Als u klaar bent met het maken van een foto, selecteert u **OK** om de foto te accepteren.
    - Als u **Afbeelding kiezen** hebt geselecteerd, selecteert u een afbeelding in de lijst.

10. Selecteer **Gereed**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Een onkostennota goedkeuren met behulp van de mobiele werkruimte voor Onkostenbeheer

1. Open op uw mobiele apparaat de werkruimte **Onkostenbeheer**.
2. Bij **Goedkeuringen voor onkosten** wordt het aantal onkostennota's weergegeven die ter goedkeuring aan u zijn toegewezen. Het aantal wordt ongeveer elke 30 minuten bijgewerkt. Selecteer **Goedkeuringen voor onkosten**.

    De lijst van onkostennota's die ter goedkeuring aan u zijn toegewezen, wordt weergegeven.

3. Selecteer een onkostennota om de onkostendetails ervan te bekijken.
4. Selecteer de onkosten om de details ervan te bekijken. De informatie die voor bepaalde kosten wordt weergegeven, bestaat onder andere uit een betalingsbewijs, gastgegevens en specificatiegegevens.
5. Als u terug bent op de pagina **Onkostennota**, selecteert u de optie om de onkostennota goed te keuren of af te wijzen.
6. Voer eventuele opmerkingen in voor de goedkeuringsactie.
7. Selecteer **Gereed**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Een nieuwe onkostennota maken en ter goedkeuring indienen met de mobiele werkruimte voor onkostenbeheer

1. Open op uw mobiele apparaat de werkruimte **Onkostenbeheer**.
2. Selecteer **Onkosten invoeren**.
3. Selecteer **Nieuw rapport** of selecteer een bestaande onkostennota in de lijst.
4. Voer voor nieuwe onkostennota's het doel en eventuele aanvullende informatie in die beschikbaar is. Deze informatie varieert, afhankelijk van de manier waarop het onkostenbeheer voor uw bedrijf is geconfigureerd.
5. Selecteer **Gereed**.
6. Als u bestaande uitgaven, zoals creditcardtransacties, aan de onkostennota wilt toevoegen, selecteert u **Bijvoegen**.
7. Selecteer een of meer onkosten in de lijst.
8. Selecteer **Gereed**.
9. Als u nieuwe onkosten aan een onkostennota wilt toevoegen, selecteert u **Nieuwe onkosten**.
10. Selecteer de categorie voor de onkosten. U ziet een lijst van onkostencategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) te lezen voor meer informatie. Als uw categorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op onkostencategorie of schakel over naar zoeken op onkostentype.
11. Optioneel: voer de winkel in voor de onkosten.
12. Voer de transactiedatum van de onkosten in.
13. Voer het bedrag van de onkosten in.
14. Selecteer de valuta van de onkosten in. U ziet een lijst van valutacodes die in uw app zijn geladen voor offline gebruik. Standaard worden 400 valuta geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) te lezen voor meer informatie. Als uw valuta niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op valuta of schakel over naar zoeken op naam.
15. Selecteer **Gereed**.
16. Als u meer details aan de onkosten wilt toevoegen, selecteert u **Meer details toevoegen**. Welke velden beschikbaar zijn, is afhankelijk van de configuratie van het onkostenbeheer voor uw bedrijf.
17. Als het bedrijfsbeleid een betalingsbewijs voor de onkosten vereist, selecteert u **Betalingsbewijzen** en volgt u deze stappen:

    1. Selecteer **Betalingsbewijs vastleggen** of **Betalingsbewijs bijvoegen**.
    2. Volg een van deze stappen:

        - Als u **Betalingsbewijs vastleggen** hebt geselecteerd, volgt u deze stappen:

            1. Selecteer **Foto nemen** of **Afbeelding kiezen**.
            2. Volg een van deze stappen:

                - Als u **Foto nemen** hebt geselecteerd, volgt u deze stappen:

                    1. U gaat automatisch naar naar de camera van uw mobiele apparaat, zodat u een foto kunt maken van het betalingsbewijs. Als u klaar bent met het maken van een foto, selecteert u **OK** om de foto te accepteren.
                    2. Optioneel: voer een naam in voor de foto en voer eventuele opmerkingen in.

                - Als u **Afbeelding kiezen** hebt geselecteerd, volgt u deze stappen:

                    1. Selecteer een afbeelding in de lijst.
                    2. Optioneel: voer een naam in voor de afbeelding en voer eventuele opmerkingen in.

            3. Selecteer **Gereed**.

        - Als u **Betalingsbewijs bijvoegen** hebt geselecteerd, volgt u deze stappen:

            1. Selecteer een of meer afbeeldingen in de lijst.
            2. Selecteer **Gereed**.

    3. Selecteer de knop **Vorige** om terug te keren naar de onkostendetails.

18. Als het bedrijfsbeleid namen van gasten vereist voor de onkosten, selecteert u **Gasten** en volgt u deze stappen:

    1. Selecteer **Gast**, **Vorige gasten** of **Collega's**.
    2. Volg een van deze stappen:

        - Als u **Gast** hebt geselecteerd, volgt u deze stappen:

            1. Voer de naam van de gast in.
            2. Optioneel: voer de organisatie en/of het land of de regio van de gast in.
            3. Optioneel: voer de functie van de gast in.
            4. Selecteer **Gereed**.

        - Als u **Vorige gasten** hebt geselecteerd, volgt u deze stappen:

            1. Selecteer een of meer vorige gasten in de lijst. U ziet een lijst met vorige gasten die u hebt toegevoegd aan vorige onkostennota's die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) te lezen voor meer informatie. Als uw vorige gast niet in de lijst staat, selecteert u **Zoeken** om de gast online te zoeken. Zoek op naam of schakel over naar zoeken op organisatie, land/regio of functie.
            2. Selecteer **Gereed**.

        - Als u **Collega's** hebt geselecteerd, volgt u deze stappen:

            1. Selecteer een of meer collega's in de lijst. U ziet een lijst van collega's die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) te lezen voor meer informatie. Als uw collega niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op naam of schakel over naar zoeken op bedrijf of functie.
            2. Selecteer **Gereed**.

    3. Selecteer de knop **Vorige** om terug te keren naar de onkostendetails.

19. Als het bedrijfsbeleid vereist dat de onkosten worden gespecificeerd, selecteert u **Specificeren** en volgt u deze stappen:

    1. Selecteer de eerste datum die u wilt specificeren.
    2. Selecteer **Specificatie toevoegen**.
    3. Selecteer de subcategorie voor de onkostenspecificatie. U ziet een lijst van onkostensubcategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) te lezen voor meer informatie. Als uw subcategorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op naam van de onkostensubcategorie.
    4. Voer het transactiebedrag in voor de specificatie.
    5. Bewerk indien nodig de transactiedatum.
    6. Selecteer **Gereed**.
    7. Herhaal de voorgaande stappen totdat u klaar bent met het toevoegen van alle specificaties voor de geselecteerde datum.
    8. Voor extra dagen kunt u de optie **Kopiëren naar volgende dag** selecteren om de specificaties naar de volgende dag te kopiëren. U kunt ook de datum selecteren die u wilt specificeren en vervolgens specificaties toevoegen, zoals u deed voor de eerste datum.
    9. Als u klaar bent met het specificeren van de onkosten, selecteert u de knop **Vorige** om terug te keren naar de onkostendetails.

20. Selecteer de knop **Vorige** om terug te keren naar de pagina **Onkostennota**.
21. Herhaal de voorgaande stappen totdat u klaar bent met het toevoegen van alle onkosten.
22. Selecteer **Verzenden**.
23. Voer eventuele opmerkingen in voor de fiatteur.
24. Selecteer **Gereed**.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Waarom voert de mobiele app voor onkosten de betalingswijze niet standaard in?

Organisaties kunnen de instelling voor **Standaard betalingswijze** voor elke onkostencategorie aanpassen wanneer deze wordt gemaakt. Bovendien kunt u wanneer u betalingswijzes instelt het veld **Standaard betalingswijze** instellen op **Alleen importeren**.

Wanneer **Alleen importeren** is ingeschakeld voor een betalingswijze, wordt de betalingswijze niet standaard ingevoerd. Het veld blijft leeg in onkostencategorieën waar deze betalingswijze is ingesteld. Dit gedrag is consistent binnen zowel de webervaring als de mobiele ervaring.
    
Wanneer **Alleen importeren** niet is ingeschakeld voor een betalingswijze, wordt de ingestelde waarde standaard ingevoerd voor onkostencategorieën waar deze betalingswijze wordt ingesteld. Er is echter een bekend probleem waarbij de standaardwaarde niet wordt ingevoerd in de mobiele app voor onkosten. U kunt dit probleem omzeilen door handmatig een betalingswijze te selecteren voordat u de onkostennota opslaat. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Waarom kan ik geen financiële dimensies toevoegen of bewerken in de mobiele app voor onkosten?

Het invoeren van dimensies en verdelingen wordt niet ondersteund. Om deze beperking te omzeilen, kunt u deze velden standaard laten instellen in de mobiele app door de standaard financiële dimensies per project of werknemer in te stellen.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Waarom zie ik soms een synchronisatiefout in de mobiele app voor onkosten?

Als de onkostenregels niet voldoen aan de beleidsvereisten en de gebruiker de onkostennota indient zonder te reageren op de beleidswaarschuwing, worden de mobiele gegevens niet gesynchroniseerd met de server en treedt er een synchronisatiefout op. Alle onkostennota's die worden ingediend nadat een synchronisatiefout is opgetreden, blijven in de status mislukt en veroorzaken meer synchronisatiefouten. De enige manier om deze situatie op te lossen, is door de synchronisatiemeldingen handmatig te verwijderen. Dit probleem is verholpen door het indienen van onkostennota's te stoppen wanneer beleidswaarschuwingen niet zijn verholpen, zodat synchronisatiefouten worden vermeden.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Waarom wordt project- en categorievalidatie niet correct weergegeven in de mobiele app voor onkosten?

Deze validatie wordt momenteel niet ondersteund. Ondersteuning hiervoor wordt in de toekomst echter mogelijk wel toegevoegd. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Welke documenttypen worden ondersteund in de mobiele app voor onkosten?

De mobiele app voor onkosten ondersteunt alleen afbeeldingen. De app ondersteunt momenteel geen pdf-bestanden of andere documenten.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

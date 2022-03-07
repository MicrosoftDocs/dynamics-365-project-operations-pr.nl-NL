---
title: Mobiele werkruimte voor onkostenbeheer
description: Dit onderwerp bevat informatie over de mobiele werkruimte Onkostenbeheer. In deze werkruimte kunnen gebruikers een betalingsbewijs vastleggen en uploaden, zodat ze dit later aan een onkostennota kunnen toevoegen. Gebruikers kunnen ook snel een onkostenregel maken met behulp van een bijgevoegd betalingsbewijs en onkostennota's maken en beheren.
author: suvaidya
ms.date: 12/01/2017
ms.topic: article
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 0559f881aba2d0a9c65ad123a40803743fc7407bb0d87ac6e8280ee8e30d36b7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001470"
---
# <a name="expense-management-mobile-workspace"></a>Mobiele werkruimte voor onkostenbeheer

Dit onderwerp bevat informatie over de mobiele werkruimte **Onkostenbeheer**. In deze werkruimte kunnen gebruikers een betalingsbewijs vastleggen en uploaden, zodat ze dit later aan een onkostennota kunnen toevoegen. Gebruikers kunnen ook snel een onkostenregel maken met behulp van een bijgevoegd betalingsbewijs en onkostennota's maken en beheren. Bovendien kunnen fiatteurs de mobiele werkruimte **Onkostenbeheer** gebruiken om onkostennota's te bekijken die aan hen zijn toegewezen en die onkostennota's goed te keuren of af te wijzen.


Deze mobiele werkruimte is bedoeld om te worden gebruikt met de mobiele app Dynamics 365 Unified Ops.


## <a name="overview"></a>Overzicht

Veel organisaties eisen dat een kopie van een betalingsbewijs wordt toegevoegd aan een reisgerelateerde of zakelijke onkostennota die een werknemer ter vergoeding indient. Met de mobiele werkruimte **Onkostenbeheer** kunnen gebruikers snel nieuwe onkostenregels maken op het mobiele apparaat van hun keuze door een bijgevoegde foto van een betalingsbewijs te gebruiken. Gebruikers kunnen ook een foto van een betalingsbewijs maken en deze later aan een onkostennota toevoegen. Werknemers kunnen ook hun onkostennota's maken en beheren en deze vervolgens ter goedkeuring en vergoeding indienen via hun mobiele apparaat.


In de mobiele werkruimte **Onkostenbeheer** kunt u de volgende taken uitvoeren:

- Maak een foto van een betalingsbewijs en upload deze naar Dynamics 365 Finance. U kunt die foto later aan een onkostendeclaratie toevoegen.
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

## <a name="prerequisites"></a>Vereisten
De vereisten verschillen, afhankelijk van de versie die is geïmplementeerd voor uw organisatie.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Vereisten als u Dynamics 365 Finance gebruikt 
Als Finance is geïmplementeerd voor uw organisatie, moet het systeembeheerder de mobiele werkruimte **Onkostenbeheer** publiceren. Zie [Mobiele werkruimten publiceren](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace) voor instructies.

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Vereisten als u versie 1611 met platformupdate 3 of hoger gebruikt
Als versie 1611 met platformupdate 3 of hoger is geïmplementeerd voor uw organisatie, moet de systeembeheerder aan de volgende vereisten voldoen. 

<table>
<thead>
<tr class="header">
<th>Vereisten</th>
<th>- Rol</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementeer KB 4019015.</td>
<td>Systeembeheerder</td>
<td>KB 4019015 is een X++-update of een metagegevenshotfix die de mobiele werkruimte <strong>Onkostenbeheer</strong> bevat. Als de systeembeheerder KB 4019015 wil implementeren, moeten deze stappen worden uitgevoerd.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Download de metagegevenshotfix vanuit Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Installeer de metagegevenshotfix</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Maak een implementeerbaar pakket</a> dat de modellen <strong>ApplicationSuite</strong> en <strong>ExpenseMobile</strong> bevat en upload vervolgens het implementeerbare pakket naar LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Pas het implementeerbare pakket toe</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publiceer de mobiele werkruimte <strong>Onkostenbeheer</strong>.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Een mobiele werkruimte publiceren</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>De mobiele app Dynamics 365 for Operations downloaden en installeren
De mobiele app Dynamics 365 Unified Ops downloaden en installeren:

- [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
- [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app
1. Start de app op uw mobiele apparaat.
2. Voer uw URL voor Dynamics 365 in.
4. Wanneer u zich voor het eerst aanmeldt, wordt u om uw gebruikersnaam en wachtwoord gevraagd. Voer uw referenties in.
5. Nadat u zich hebt aangemeld, worden de beschikbare werkruimten voor uw bedrijf weergegeven. Merk op dat als uw systeembeheerder later een nieuwe werkruimte publiceert, u de lijst met mobiele werkruimten moet vernieuwen.


[![Slepen om te vernieuwen.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Een betalingsbewijs vastleggen met behulp van de mobiele werkruimte Onkostenbeheer

1. Open op uw mobiele apparaat de werkruimte **Onkostenbeheer**.
2. Selecteer **Betalingsbewijs vastleggen**.
3. Selecteer **Foto nemen** of **Afbeelding kiezen**.
4. Volg een van deze stappen:

    - Als u **Foto nemen** hebt geselecteerd, volgt u deze stappen:

        1. U gaat automatisch naar naar de camera van uw mobiele apparaat, zodat u een foto kunt maken van het betalingsbewijs. Als u klaar bent met het maken van een foto, selecteert u **OK** om de foto te accepteren.
        2. Optioneel: voer een naam in voor de foto en voer eventuele opmerkingen in.

    - Als u **Afbeelding kiezen** hebt geselecteerd, volgt u deze stappen:

        1. Selecteer een afbeelding in de lijst.
        2. Optioneel: voer een naam in voor de afbeelding en voer eventuele opmerkingen in.

5. Selecteer **Gereed**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Snel betalingsbewijzen vastleggen met behulp van de mobiele werkruimte Onkostenbeheer
1. Open op uw mobiele apparaat de werkruimte **Onkostenbeheer**.
2. Selecteer **Snel onkosten invoeren**.
3. Selecteer de categorie voor de onkosten. U ziet een lijst van onkostencategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) te lezen voor meer informatie. Als uw categorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op onkostencategorie of schakel over naar zoeken op onkostentype.
4. Voer de transactiedatum van de onkosten in.
5. Optioneel: voer de winkel in voor de onkosten.
6. Voer het bedrag van de onkosten in.
7. Selecteer de valuta van de onkosten in. U ziet een lijst van valutacodes die in uw app zijn geladen voor offline gebruik. Standaard worden 400 valuta geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) te lezen voor meer informatie. Als uw valuta niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op valuta of schakel over naar zoeken op naam.
8. Selecteer **Foto nemen** of **Afbeelding kiezen**.
9. Volg een van deze stappen:

    - Als u **Foto nemen** hebt geselecteerd, gaat u automatisch naar naar de camera van uw mobiele apparaat, zodat u een foto kunt maken van het betalingsbewijs. Als u klaar bent met het maken van een foto, selecteert u **OK** om de foto te accepteren.
    - Als u **Afbeelding kiezen** hebt geselecteerd, selecteert u een afbeelding in de lijst.

10. Selecteer **Gereed**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Een onkostennota goedkeuren met behulp van de mobiele werkruimte Onkostenbeheer (als u de update van juli 2017 gebruikt)
1. Open op uw mobiele apparaat de werkruimte **Onkostenbeheer**.
2. Bij **Goedkeuringen voor onkosten** wordt het aantal onkostennota's weergegeven die ter goedkeuring aan u zijn toegewezen. Het aantal wordt ongeveer elke 30 minuten bijgewerkt. Selecteer **Goedkeuringen voor onkosten**.

    De lijst van onkostennota's die ter goedkeuring aan u zijn toegewezen, wordt weergegeven.
    
3. Selecteer een onkostennota om de onkostendetails ervan te bekijken.
4. Selecteer de onkosten om de details ervan te bekijken. De informatie die voor bepaalde kosten wordt weergegeven, bestaat onder andere uit een betalingsbewijs, gastgegevens en specificatiegegevens.
5. Als u terug bent op de pagina **Onkostennota**, selecteert u de optie om de onkostennota goed te keuren of af te wijzen.
6. Voer eventuele opmerkingen in voor de goedkeuringsactie.
7. Selecteer **Gereed**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Een nieuwe onkostennota maken en ter goedkeuring indienen met behulp van de mobiele werkruimte Onkostenbeheer (als u de update van juli 2017 gebruikt)
1. Open op uw mobiele apparaat de werkruimte **Onkostenbeheer**.
2. Selecteer **Onkosten invoeren**.
3. Selecteer **Nieuw rapport** of selecteer een bestaande onkostennota in de lijst.
4. Voer voor nieuwe onkostennota's het doel en eventuele aanvullende informatie in die beschikbaar is. Deze informatie varieert, afhankelijk van de manier waarop het onkostenbeheer voor uw bedrijf is geconfigureerd.
5. Selecteer **Gereed**.
6. Als u bestaande uitgaven, zoals creditcardtransacties, aan de onkostennota wilt toevoegen, selecteert u **Bijvoegen**.
7. Selecteer een of meer onkosten in de lijst.
8. Selecteer **Gereed**.
9. Als u nieuwe onkosten aan een onkostennota wilt toevoegen, selecteert u **Nieuwe onkosten**.
10. Selecteer de categorie voor de onkosten. U ziet een lijst van onkostencategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) te lezen voor meer informatie. Als uw categorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op onkostencategorie of schakel over naar zoeken op onkostentype.
11. Optioneel: voer de winkel in voor de onkosten.
12. Voer de transactiedatum van de onkosten in.
13. Voer het bedrag van de onkosten in.
14. Selecteer de valuta van de onkosten in. U ziet een lijst van valutacodes die in uw app zijn geladen voor offline gebruik. Standaard worden 400 valuta geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) te lezen voor meer informatie. Als uw valuta niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op valuta of schakel over naar zoeken op naam.
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

            3.  Selecteer **Gereed**.

        - Als u **Betalingsbewijs bijvoegen** hebt geselecteerd, volgt u deze stappen:

            1.  Selecteer een of meer afbeeldingen in de lijst.
            2.  Selecteer **Gereed**.

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

            1. Selecteer een of meer vorige gasten in de lijst. U ziet een lijst met vorige gasten die u hebt toegevoegd aan vorige onkostennota's die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) te lezen voor meer informatie. Als uw vorige gast niet in de lijst staat, selecteert u **Zoeken** om de gast online te zoeken. Zoek op naam of schakel over naar zoeken op organisatie, land/regio of functie.
            2. Selecteer **Gereed**.

        - Als u **Collega's** hebt geselecteerd, volgt u deze stappen:

            1. Selecteer een of meer collega's in de lijst. U ziet een lijst van collega's die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) te lezen voor meer informatie. Als uw collega niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op naam of schakel over naar zoeken op bedrijf of functie.
            2. Selecteer **Gereed**.

    3. Selecteer de knop **Vorige** om terug te keren naar de onkostendetails.

19. Als het bedrijfsbeleid vereist dat de onkosten worden gespecificeerd, selecteert u **Specificeren** en volgt u deze stappen:

    1. Selecteer de eerste datum die u wilt specificeren.
    2. Selecteer **Specificatie toevoegen**.
    3. Selecteer de subcategorie voor de onkostenspecificatie. U ziet een lijst van onkostensubcategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars wordt aangeraden [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) te lezen voor meer informatie. Als uw subcategorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op naam van de onkostensubcategorie.
    4. Voer het transactiebedrag in voor de specificatie.
    5. Bewerk indien nodig de transactiedatum.
    6. Selecteer **Gereed**.
    7. Herhaal de voorgaande stappen totdat u klaar bent met het toevoegen van alle specificaties voor de geselecteerde datum.
    8. Voor extra dagen kunt u de optie **Kopiëren naar volgende dag** selecteren om de specificaties naar de volgende dag te kopiëren. U kunt ook de datum selecteren die u wilt specificeren en vervolgens specificaties toevoegen, zoals u deed voor de eerste datum.
    9. Als u klaar bent met het specificeren van de onkosten, selecteert u de knop **Vorige** om terug te keren naar de onkostendetails.

20. Selecteer de knop **Vorige** om terug te keren naar de pagina **Onkostennota**.
21. Herhaal de voorgaande stappen totdat u klaar bent met het toevoegen van alle onkosten.
22. Selecteer **Indienen**.
23. Voer eventuele opmerkingen in voor de fiatteur.
24. Selecteer **Gereed**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
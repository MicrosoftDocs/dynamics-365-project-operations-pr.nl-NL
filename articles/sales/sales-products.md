---
title: Producten
description: Dit onderwerp bevat informatie over de productcatalogus die u kunt gebruiken om klanten informatie te geven over de producten en prijzen die uw organisatie aanbiedt.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5c57b2596e1d480ff59591618f073ceb8f70a289
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574088"
---
# <a name="products"></a>Producten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Producten vormen de ruggengraat van uw bedrijf. De productcatalogus in Dynamics 365 Sales Professional is een verzameling producten met prijsinformatie. Maak het eenvoudiger voor uw verkoopmedewerkers om hun omzet te verhogen door snel een productcatalogus te maken.

## <a name="add-a-product"></a>Een product toevoegen

1.  Zorg dat u de rol Sales Manager Professional of Systeembeheerder hebt, zodat u producten kunt toevoegen in Dynamics 365 Sales Professional.
2.  Selecteer in het siteoverzicht onder **Instellingen** de optie **Producten**.
3.  Selecteer **Product toevoegen** en vul de volgende gegevens in:

    -  **Name**
    -  **Product-id**
    -  **Bovenliggend product**: selecteer een bovenliggende productfamilie voor het product. Als u een onderliggend product in een productfamilie maakt, wordt hier de naam van de bovenliggende productfamilie ingevuld. Dit kan niet worden gewijzigd nadat de record is opgeslagen.
    -  **Geldig van**/**Geldig tot**: geef de geldigheidsperiode voor het product op door een datum te selecteren voor **Geldig van** en **Geldig tot**.
    -  **Eenhedengroep**: selecteer een eenhedengroep. Een eenhedengroep is een verzameling van verschillende eenheden waarin een product wordt verkocht en bepaalt op welke manier afzonderlijke items in grotere hoeveelheden worden gegroepeerd. Als u bijvoorbeeld zaden toevoegt als een product, kunt u een eenhedengroep met de naam "Zaden" maken en de primaire eenheid definiëren als "pakket".
    -  **Standaardeenheid**: selecteer de meest voorkomende eenheid waarin het product wordt verkocht. Eenheden worden de hoeveelheden of de eenheden waarin u uw producten verkoopt in. Bijvoorbeeld, als u zaden als product toevoegt, kunt u deze verkopen in pakken, dozen of pallets. Elk van deze wordt een eenheid van het product. Als de zaden meestal in pakketten worden verkocht, selecteert u pakket als eenheid.
    -  **Standaardprijslijst**: als dit een nieuw product is, is dit veld alleen-lezen. Voordat u een standaardprijslijst selecteert, moet u gegevens in alle vereiste velden invullen en vervolgens de record opslaan. Hoewel de standaardprijslijst niet vereist is, is het raadzaam voor elk product een standaardprijslijst in te stellen nadat u de productrecord hebt opgeslagen. In dat geval kan Sales de standaardprijslijst gebruiken voor het genereren van prijsopgaven, orders en facturen als een klantrecord geen prijslijst bevat.
    -  **Decimalen ondersteund**: voer een geheel getal in tussen 0 en 5. Als het product niet kan worden verdeeld in delen, voert u 0 in. De precisie van het veld **Hoeveelheid** in de prijsopgave, de order of de factuur wordt gevalideerd op basis van de waarde in dit veld als het product geen gekoppelde prijslijst heeft.
    -  **Onderwerp**: u kunt dit product aan een onderwerp koppelen. Met behulp van onderwerpen kunt u producten categoriseren en rapporten filteren.

4.  Selecteer **Opslaan**.
5.  Selecteer op het tabblad **Aanvullende details** in het gedeelte **Prijslijstitems** de optie **Meer opdrachten** en selecteer vervolgens **Nieuw prijslijstitem toevoegen**.
7.  Selecteer op het tabblad **Aanvullende details** in het gedeelte **Productrelatie** de optie **Meer opdrachten** en selecteer vervolgens **Nieuwe productrelatie toevoegen.**
8.  Voer in het formulier **Nieuwe productrelatie** de volgende details in en selecteer **Opslaan en sluiten** op de opdrachtbalk:

    -   **Gerelateerd product**: selecteer een product dat u wilt toevoegen als een gerelateerd product aan de bestaande productrecord waaraan u werkt.
    -   **Type verkooprelatie**: selecteer of u het product wilt toevoegen als product voor up-selling, cross-selling, accessoire of vervangend product.
    -   **Richting**: selecteer of de relatie tussen de producten unidirectioneel of bidirectioneel is. Als u unidirectioneel selecteert, wordt het product dat u selecteert in **Gerelateerd product** weergegeven als aanbeveling voor het bestaande product maar niet omgekeerd.

9.  Selecteer op het formulier Product de optie **Opslaan**.

## <a name="import-products"></a>Producten importeren

U kunt importsjablonen gebruiken om bulkproductgegevens over te brengen naar Dynamics 365 Sales.

## <a name="revise-a-product"></a>Een product herzien

Houd de productvoorraad bijgewerkt door snel naar behoeft eigenschappen voor de producten te herzien en de gegevens opnieuw te publiceren zodat uw verkopenagenten de nieuwste wijzigingen in de voorraad kunnen zien.

1.  Zorg dat u over een van de volgende beveiligingsrollen of soortgelijke machtigingen beschikt: systeembeheerder, systeemaanpasser, verkoopdirecteur, adjunct-directeur van verkoop, adjunct-directeur van marketing, algemeen directeur-bedrijfsleider.
2.  Selecteer **Producten** in het siteoverzicht.
3.  Open een actief product dat u wilt wijzigen en selecteer op de opdrachtbalk de optie **Herzien**.
4.  Selecteer in het dialoogvenster **Herziening bevestigen** de optie **Bevestigen**. Hierdoor verandert de productstatus in **Wordt herzien**.
5.  Nadat u het aanbrengen van wijzigingen hebt voltooid, selecteert u **Publiceren** op de opdrachtbalk.

    > [!TIP]
    > Als u de wijzigingen ongedaan wilt maken en wilt doorgaan met de als laatste actieve versie van het product, selecteert u **Herstellen**. Hiermee wordt de status van het product opnieuw in **Actief** gewijzigd.

## <a name="clone-a-product"></a>Een product klonen 

Als u een nieuw product maakt, kunt u tijd besparen door een bestaand product te klonen. Hiermee maakt u een kopie van de oorspronkelijke record met alle details, behalve de naam en de id.

1.  Zorg dat u over een van de volgende beveiligingsrollen of soortgelijke machtigingen beschikt: systeembeheerder, systeemaanpasser, verkoopdirecteur, adjunct-directeur van verkoop, adjunct-directeur van marketing, algemeen directeur-bedrijfsleider.
2.  Selecteer **Producten** in het siteoverzicht.
3.  Selecteer het product dat u wilt klonen en selecteer op de opdrachtbalk de optie **Klonen**. Er wordt een bevestigingsvenster weergegeven.
4.  Selecteer **Bevestigen**.

Er wordt nu een nieuw productrecord geopend met dezelfde gegevens als het oorspronkelijke record, behalve de naam en de id.

## <a name="retire-a-product"></a>Een product terugtrekken 

Als uw organisatie een product niet meer verkoopt, trekt u het terug zodat het niet meer beschikbaar is voor uw verkopers.

1.  Zorg dat u de rol Systeembeheerder of Sales Professional Manager of gelijkwaardige machtigingen hebt.
2.  Selecteer **Producten** in het siteoverzicht.
3.  Open een actief product dat u buiten gebruik wilt stellen en selecteer op de opdrachtbalk de optie **Buiten gebruik stellen**.
4.  Selecteer in het dialoogvenster **Buitengebruikstelling bevestigen** de optie **Bevestigen**.


## <a name="delete-a-product"></a>Een product verwijderen

Als u wilt stoppen met de verkoop van een product, verwijdert u het.

> [!IMPORTANT]
> U kunt een verwijderde record niet herstellen.

1.  Zorg dat u de rol Systeembeheerder of Sales Professional Manager of gelijkwaardige machtigingen hebt.
2.  Selecteer **Producten** in het siteoverzicht.
3.  Selecteer een productrecord dat u wilt verwijderen en selecteer op de opdrachtbalk de optie **Verwijderen**.
4.  Selecteer **Doorgaan** in het dialoogvenster **Verwijdering bevestigen**.
 
 ## <a name="quantity-factors-for-products"></a>Hoeveelheidsfactoren voor producten

Hoeveelheidsfactoren ondersteunen de verkoop van op abonnementen gebaseerde producten. Voor producten waarop een abonnement kan worden genomen, wordt de hoeveelheid in de prijsopgave- of projectcontractregel uitgedrukt in het aantal gebruikersmaanden.

Meestal wordt de prijs van abonnementssoftware in de catalogus opgeslagen als de prijs per gebruiker per maand. In plaats daarvan kunt u echter andere tijdsvermeldingen gebruiken. Tijdens het verkoopproces is de prijs op de prijsopgaveregel meestal de prijs per gebruiker, per maand die is overeengekomen en waarop korting is gegeven door de IT-verkoopagent. Elke deal heeft een ander aantal gebruikers en een ander aantal abonnementsmaanden. De hoeveelheid die wordt gebruikt om het bedrag van de prijsopgaveregel te berekenen, is het product van het aantal gebruikers en het aantal abonnementsmaanden.

Hoeveelheidsfactoren zijn afhankelijk van productkenmerken. Wanneer u specifieke eigenschappen voor een product configureert, kunt u een subset van deze eigenschappen, of alle eigenschappen, markeren als hoeveelheidsfactoren.

Het systeem zorgt ervoor dat alleen numerieke eigenschappen of producteigenschappen met een numeriek gegevenstype worden gemarkeerd als hoeveelheidsfactoren. Wanneer een product waarvoor hoeveelheidsfactoren zijn geconfigureerd, wordt toegevoegd aan een prijsopgaveregel, wordt het veld **Hoeveelheid** op de prijsopgaveregel een alleen-lezenveld. Nadat u waarden hebt ingevoerd voor producteigenschappen die hoeveelheidsfactoren zijn, wordt de hoeveelheid van de prijsopgaveregel berekend.

Als het bijvoorbeeld de volgende eigenschappen zijn: 

- **Aantal gebruikers**: het aantal gebruikers 
- **Aantal maanden**: het aantal abonnementsmaanden
- **SKU van product** 

De eigenschappen **Aantal gebruikers** en **Aantal maanden** kunnen worden gemarkeerd als hoeveelheidsfactoren door de eigenschappen van de productregel te bewerken. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
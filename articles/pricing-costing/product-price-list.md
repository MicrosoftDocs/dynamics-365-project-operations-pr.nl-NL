---
title: Productprijslijsten
description: Dit onderwerp bevat informatie over de prijslijsten voor het bepalen van catalogusprijzen die worden gebruikt voor projectprijsopgaven en -contracten.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 504aa90bfb478207059b5e2894a3990f9a4a5e9e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074632"
---
# <a name="product-price-lists"></a>Productprijslijsten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Prijslijsten en prijslijstitem-entiteiten ondersteunen productcatalogusprijzen. Deze functionaliteit wordt voornamelijk gebruikt voor op een catalogus gebaseerde regels in projectprijsopgaven en projectcontracten.

Voor projectgebaseerde regels vertegenwoordigt een contract de deal nadat deze is gesloten. Omdat het onderhandelingsproces gewoonlijk voorafgaat aan het sluiten van de deal, wordt de prijs die aan de prijsopgave is gekoppeld, altijd ongewijzigd naar een nieuwe prijslijst gekopieerd en aan het contract gekoppeld. Deze nieuwe prijslijst kan niet buiten het bereik van het contract worden gewijzigd. Deze beperking helpt bij het beschermen van de tariefkaart die is onderhandeld op basis van prijswijzigingen die in de hoofdprijslijst voorkomen.

Producten moeten zo worden ingesteld dat hiervoor standaardkosten en standaardprijslijsten in de productcatalogus aanwezig zijn. Gebruik de lijstprijs, standaardkosten en huidige kosten om de standaardkosten en standaardlijstprijzen te configureren. De standaardlijstprijzen worden alleen op een prijsopgaveregel of projectcontractregel gebruikt als het systeem geen prijslijstregel voor dat product kan vinden in de productprijslijst voor de prijsopgave of het projectcontract.

De kostprijs van productcatalogusregels kan tussen prijsopgaven worden gewijzigd. Deze mogelijkheid is belangrijk, want als u de kosten niet nauwkeurig bijhoudt, kunt u geen operationele winst bepalen voor projectovereenkomsten. De standaardkosten van het product worden standaard gebruikt als de kostprijs. De standaardkostprijs kan echter worden bijgewerkt op de prijsopgaveregel als er een andere kostprijs voor die prijsopgave is.

## <a name="price-list-items"></a>Prijslijstitems

U kunt producten uit een productcatalogus toevoegen aan verschillende prijslijsten. Prijslijstregels voor producten verwijzen altijd naar een specifieke eenheid. Prijzen voor een product in prijslijstitems kunnen worden geconfigureerd als een valutabedrag. Deze prijzen kunnen ook worden geconfigureerd als een functie van de catalogusprijs, huidige kosten of standaardkosten.

Er worden verschillende afrondingsopties ondersteund wanneer prijzen worden geconfigureerd als een functie van de catalogusprijs, standaardkosten of huidige kosten. U kunt niet alleen gebruikmaken van meerdere prijsbepalingsmethoden en afrondingsopties, maar u kunt ook kortingslijsten koppelen aan prijslijstitems. 

Wanneer u een nieuwe aangepaste prijslijst voor een prijsopgave maakt door **Aangepaste prijzen maken** te selecteren op de pagina **Prijsopgave voor projecten** , wordt er een kopie gemaakt van de prijslijst en wordt het veld **Entiteit** in de koptekst van de nieuwe prijslijst ingesteld op **Verkoopentiteit**. Aan de naam van de nieuwe prijslijst worden de naam van de prijsopgave en een timestamp toegevoegd. U kunt ook de naam van de nieuwe prijslijst en de naam van de prijsopgave in aangepaste werkstromen gebruiken om extra controles en goedkeuringen te activeren voor prijsopgaven waarin aangepaste prijzen worden gebruikt.

 
## <a name="default-product-price-list"></a>Standaardproductprijslijst
Elk klantenrecord heeft een veld **Standaardprijslijst** waar u een prijslijst kunt opgeven met prijzen in een valuta die overeenkomt met de valuta van de klant. Er wordt in dit veld niet automatisch een standaardwaarde ingevoerd. Wanneer er een aangepaste prijsafspraak met een specifieke klant bestaat, kunt u dit veld gebruiken om een prijslijst aan die klant te koppelen.

In de entiteiten Verkoopkans, Prijsopgave en Projectcontract wordt de volgende volgorde gebruikt om standaardprijslijsten voor producten in te voeren. Dezelfde volgorde wordt gebruikt voor projectprijslijsten.

1.  Prijsopgave
2.  Kans
3.  Klant
4.  Algemene instellingen 

Standaard worden in het veld **Product** op de prijsopgaveregel alle actieve producten in de productprijslijst van de prijsopgave vermeld. Als een product is gedeactiveerd, of als het een conceptproduct is, wordt het product niet weergegeven, zelfs niet als het in de prijslijst staat. 

Productcatalogusregels worden toegevoegd als factuurregels op de eerste factuur die voor een projectcontract wordt gemaakt. Op een conceptfactuur kunnen deze factuurregels worden verwijderd. In dat geval worden de regels op een volgende factuur weergegeven totdat ze worden gefactureerd of totdat de factuur naar de klant wordt verzonden. U kunt geen deelhoeveelheid van een productfactuurregel factureren. Wanneer de productregels uit het projectcontract worden gefactureerd, worden werkelijke waarden gemaakt. Deze werkelijke waarden zijn echter niet gekoppeld aan de gerelateerde projectentiteit. Met andere woorden: productgebaseerde projectcontractregels zijn onafhankelijk van elk projectgebaseerd gebruik. Het materiaalverbruik van projecten wordt niet bijgehouden.

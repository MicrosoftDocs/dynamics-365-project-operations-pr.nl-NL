---
title: Projectprijslijsten in een prijsopgave beheren
description: In dit onderwerp krijgt u informatie over de entiteit Projectprijslijst.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 4bd4e9cb22bfd6a86fd86e5fc403cb185aab140a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277737"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Projectprijslijsten in een prijsopgave beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations breidt de entiteit Prijslijst in Dynamics 365 Sales uit. 

## <a name="key-entities"></a>Belangrijke entiteiten

Een prijslijst bevat informatie die wordt geleverd door vier verschillende entiteiten:

- **Prijslijst**: in deze entiteit wordt informatie opgeslagen over context, valuta, datumgeldigheid en tijdseenheid voor prijsbepaling. Aan de context is te zien of in de prijslijst kostentarieven of verkooptarieven worden weergegeven. 
- **Valuta**: in deze entiteit wordt de valuta van prijzen in de prijslijst opgeslagen. 
- **Datum**: deze entiteit wordt gebruikt wanneer het systeem een standaardprijs voor een transactie probeert in te voeren. Er wordt een prijslijst geselecteerd met een datumgeldigheid waarbinnen de datum van de transactie valt. Als er meer dan één prijslijst wordt gevonden die geldig is voor de transactiedatum en is gekoppeld aan een verwante prijsopgave, verwant contract of verwante organisatie-eenheid, wordt er standaard geen prijs ingesteld. 
- **Tijd**: in deze entiteit wordt de tijdseenheid opgeslagen waarin prijzen worden weergegeven, zoals dagtarieven of uurtarieven. 

De entiteit Prijslijst heeft drie gerelateerde tabellen waarin prijzen worden opgeslagen:

  - **Rolprijs**: in deze tabel wordt een tarief opgeslagen voor een combinatie van rol- en organisatie-eenheidswaarden en deze tabel wordt gebruikt voor het instellen van op rollen gebaseerde prijzen voor personeel.
  - **Prijs voor transactiecategorie**: in deze tabel worden prijzen per transactiecategorie opgeslagen en deze tabel wordt gebruikt om prijzen voor onkostencategorieën in te stellen.
  - **Prijslijstitems**: in deze tabel worden prijzen voor catalogusproducten opgeslagen.
 
De prijslijst is een tariefkaart. Een tariefkaart is een combinatie van de entiteit Prijslijst en gerelateerde rijen in de tabellen Rolprijs, Prijs voor transactiecategorie en Prijslijstitems.

## <a name="resource-roles"></a>Resourcerollen

De term *resourcerol* verwijst naar een reeks vaardigheden, competenties en certificeringen die een persoon moet hebben om een specifieke reeks taken voor een project uit te voeren.

Voor personeelstijd wordt een prijsopgave gemaakt op basis van de rol die dit personeel vervult in een specifiek project. Voor personeelstijd zijn de kostenberekening en facturering gebaseerd op de rol van de resource. Tijd kan worden geprijsd in elke eenheid in de eenhedengroep **Tijd**.

De eenhedengroep **Tijd** wordt gemaakt wanneer u Project Operations installeert. Deze heeft als standaardeenheid **Uur**. U kunt de kenmerken van de eenhedengroep **Tijd** of de eenheid **Uur** niet verwijderen, hernoemen of bewerken. U kunt echter wel andere eenheden toevoegen aan de eenhedengroep **Tijd**. Als u de eenhedengroep **Tijd** of de eenheid **Uur** probeert te verwijderen, kan dit fouten in de bedrijfslogica veroorzaken.
 
## <a name="transaction-categories-and-expense-categories"></a>Transactiecategorieën en onkostencategorieën

Reis- en andere onkosten die projectconsultants maken, worden aan de klant gefactureerd. De prijsbepaling van onkostencategorieën vindt plaats op basis van prijslijsten. Vliegtickets, hotelovernachtingen en autohuur zijn voorbeelden van onkostencategorieën. Elke prijslijstregel voor onkosten bevat de prijs voor een specifieke onkostencategorie. De volgende drie methoden worden gebruikt om de prijs van onkostencategorieën te bepalen:

- **Tegen kosten**: de onkosten worden gefactureerd aan de klant en er wordt geen opslag toegepast.
- **Opslagpercentage**: het percentage over de werkelijke kosten wordt gefactureerd aan de klant. 
- **Prijs per eenheid**: er wordt een factureringsprijs ingesteld voor elke eenheid van de onkostencategorie. Het bedrag dat wordt gefactureerd aan de klant wordt berekend op basis van het aantal onkosteneenheden dat de consultant rapporteert. Bij Gereden kilometers wordt de prijsstellingsmethode Prijs per eenheid gebruikt. De onkostencategorie Gereden kilometers kan bijvoorbeeld worden geconfigureerd voor 30 euro per dag of 2 euro per kilometer. Wanneer een consultant het aantal gereden kilometers voor een project rapporteert, wordt het factuurbedrag berekend op basis van het aantal kilometers dat de consultant heeft gerapporteerd.
 
## <a name="project-sales-pricing-and-overrides"></a>Prijzen en overschrijvingen van projectverkopen

Voor projectprijsopgaven en -contracten bevat een projectprijslijst een ander patroon voor prijsoverschrijving dan een productprijslijst. Op een op een productcatalogus gebaseerde prijsopgaveregel kunt u de prijs voor rollen en categorieën rechtstreeks op de prijsopgaveregel overschrijven, omdat elke prijsopgaveregel naar exact één catalogusitem verwijst. Op een projectgebaseerde prijsopgaveregel kunt u de prijs echter niet rechtstreeks op de prijsopgaveregel overschrijven voor rollen en categorieën. Gebruik de prijslijst van het project om de twee verschillende overschrijvingspatronen te ondersteunen.

> [!NOTE]
> Het is raadzaam om een aparte prijslijst voor uw projectresources en uw catalogusitems te hanteren vanwege de verschillen in gedrag tussen de twee wanneer u prijzen overschrijft.

Aan elk van de volgende entiteiten kunnen een of meer verkoopprijslijsten worden gekoppeld voor projectprijzen:

- Klant (account) 
- Verkoopkans 
- Prijsopgave 
- Projectcontract

De koppeling van deze entiteiten aan een prijslijst wordt aangegeven door de projectprijslijsten. U kunt een of meer prijslijsten koppelen aan de verkoopentiteiten Klant, Verkoopkans, Prijsopgave en Projectcontract.

Een standaardprojectprijslijst wordt niet automatisch ingevoerd in een klantrecord. U kunt een projectprijslijst echter handmatig aan de klantrecord koppelen. Koppel een projectprijslijst echter alleen handmatig als u een aangepaste prijsafspraak met de klant hebt. 

Wanneer een projectprijslijst aan een verkoopentiteit wordt gekoppeld, wordt de volgende informatie gevalideerd:

- De prijslijst heeft als context **Verkoop**. 
- De prijslijstvaluta komt overeen met de klantvaluta. 

Voor een projectcontract wordt de volgende prioriteitsvolgorde gebruikt om automatisch gerelateerde projectprijslijsten in te stellen:

1. Prijsopgave
2. Kans
3. Klant 
4. Algemene instellingen 

Wanneer een projectprijslijst standaard wordt ingevoerd, controleert het systeem of de valuta overeenkomt met de valuta van de klant en of de standaardprijslijsten die zijn ingevoerd, de context **Verkoop** hebben.

U kunt meerdere projectprijslijsten koppelen aan de entiteiten Klant, Verkoopkans, Prijsopgave en Projectcontract. Deze mogelijkheid ondersteunt datumspecifieke standaardprijzen voor een langlopend projectcontract, waarbij u mogelijk meer dan één prijslijst nodig hebt voor prijsupdates die worden veroorzaakt door inflatie. Als de prijslijsten die u aan de entiteit Klant, Verkoopkans, Prijsopgave of Projectcontract koppelt echter overlappende geldigheidsdatums hebben, zijn de standaardprijzen mogelijk onjuist. Daarom moet u ervoor zorgen dat projectprijslijsten met overlappende geldigheidsdatums niet zijn gekoppeld aan deze entiteiten.

### <a name="deal-specific-price-overrides"></a>Dealspecifieke prijsoverschrijvingen

U kunt dealspecifieke overschrijvingen maken voor geselecteerde prijzen in projectprijslijsten die standaard worden ingevoerd voor een prijsopgave of projectcontract.

Standaard krijgt een projectcontract altijd een kopie van de hoofdverkoopprijslijst in plaats van een directe koppeling naar deze lijst. Dit gedrag zorgt ervoor dat prijsafspraken die zijn gemaakt met een klant voor een werkomschrijving, niet worden gewijzigd als de hoofdprijslijst wordt gewijzigd.

Voor een prijsopgave kunt u echter een hoofdprijslijst gebruiken. U kunt ook een hoofdprijslijst kopiëren en bewerken om een aangepaste prijslijst te maken die alleen van toepassing is op die prijsopgave. Als u een nieuwe prijslijst wilt maken die specifiek is voor een prijsopgave, selecteert u op de pagina **Prijsopgave** de optie **Aangepaste prijzen maken**. U kunt de dealspecifieke projectprijslijst alleen openen vanuit de prijsopgave. 

Wanneer u een aangepaste projectprijslijst maakt, worden alleen de projectonderdelen van de prijslijst gekopieerd. Met andere woorden, er wordt een nieuwe prijslijst gemaakt als een kopie van de bestaande projectprijslijst die is gekoppeld aan de prijsopgave en deze nieuwe prijslijst heeft alleen gerelateerde rolprijzen en transactiecategorieprijzen.
  
## <a name="tracking-costs"></a>Kosten bijhouden

In Project Operations worden kosten voor het gebruik van personeelstijd voor projecten bijgehouden. Daarnaast worden er andere kosten bijgehouden die worden gemaakt tijdens het project, zoals reiskosten.

Net als factuurtarieven worden ook kostentarieven voor personeel ingesteld met behulp van prijslijsten. Dit zijn de belangrijkste verschillen in het gedrag van de kostprijslijst en de verkoopprijslijst:

- Het kostentarief van een resource kan niet worden overschreven voor specifieke projecten, contracten of prijsopgaven. Factuurtarieven kunnen echter per deal worden overschreven als er wijzigingen worden aangebracht die specifiek zijn voor de aard van de deal. 

- De volgende volgorde wordt gebruikt om een kostprijslijst op te lossen:

    1. De kostprijslijst die aan de organisatie-eenheid is gekoppeld.
    2. De kostprijslijst die aan de Project Operations-parameters is gekoppeld. Omdat kostprijslijsten in veel verschillende valuta's kunnen worden gekoppeld aan parameters, wordt de valuta van de contracterende organisatie-eenheid van het project, het contract of de prijsopgave afgestemd op de valuta van de kostprijslijst.
    3. Voor onkosten worden de prijsmethoden Tegen kosten en Opslag over kosten niet toegepast op kostprijslijsten. Zelfs als deze prijsmethoden worden gebruikt voor kostprijslijstregels om transactiecategoriekosten in te stellen, worden deze genegeerd en wordt er geen standaardkostprijs ingevoerd.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Eenhedengroepen en eenheden
description: Dit onderwerp bevat informatie over eenhedengroepen en eenheden.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145577"
---
# <a name="unit-groups-and-units"></a>Eenhedengroepen en eenheden

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Eenhedengroepen en eenheden zijn basisentiteiten in Microsoft Dynamics 365. Een eenheid is één maateenheid en meerdere eenheden kunnen worden gegroepeerd in eenhedengroepen. Een eenhedengroep wordt soms aangeduid als een eenheidsplanning in de gebruikersinterface van Dynamics 365 (UI). 

Hier volgen enkele voorbeelden van eenheden en eenhedengroepen:
 
- **Eenhedengroep**: afstand 
    - **Eenheden**: mijl, kilometer, enzovoort.
- **Eenhedengroep**: tijd
    - **Eenheden**: uur, dag, week, enzovoort. 

Wanneer u meerdere eenheden in een eenhedengroep instelt, moet u ook een conversiefactor hiertussen instellen door de eerste eenheid die u instelt aan te wijzen als de standaard- of primaire eenheid voor de eenhedengroep. 

Wanneer u in een eenhedengroep **Tijd** bijvoorbeeld **Uur** instelt als eerste eenheid, wordt **Uur** aangewezen als de standaardeenheid. Als de volgende eenheid die u instelt **Dag** is, moet u een conversiefactor instellen voor **Dag** naar **Uur**. Als u vervolgens **Week** als derde eenheid toevoegt, moet u een conversiefactor voor **Week** instellen als **Dag** of **Uur**. 

In de volgende afbeelding ziet u een voorbeeld van de instelling voor de eenheid **Dag**, waarbij in het veld **Hoeveelheid** het aantal uren in een dag wordt weergegeven, en de eenheid **Week**, waarbij in het veld **Hoeveelheid** het aantal dagen in een week wordt weergegeven.

> ![Eenhedengroep: informatiepagina](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Eenheden en eenhedengroepen gebruiken

Dynamics 365 Project Service Automation gebruikt eenheden en eenhedengroepen voor het verwerken van schattingen en posten voor zowel onkosten als tijd. 

Voor onkosten heeft elke onkostencategorie een standaardeenhedengroep en -eenheid. Deze waarden worden ingevoerd als standaardwaarden in prijslijstposten voor onkostencategorieën. 

U hebt bijvoorbeeld een onkostencategorie met de naam **Gereden kilometers**. Deze heeft een eenhedengroep met de naam **Afstand** en een standaardeenheid met de naam **Mijl**. Als u de eenhedengroep **Afstand** zo instelt dat deze twee eenheden (**Mijl** en **Kilometer**) heeft, kunt u twee prijzen voor de categorie **Gereden kilometers** in één prijslijst instellen: de prijs per mijl en prijs per kilometer.

| Onkostencategorie  | Eenhedengroep  | Eenheid      | Prijsmethode  | Prijs per eenheid  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Gereden kilometers           | Afstand      | Mijl      | Prijs per eenheid    | 10 USD            |
| Gereden kilometers           | Afstand      | Kilometer | Prijs per eenheid    |  6 USD            |

Wanneer u onkosten invoert voor een project, bepaalt het systeem de prijs op basis van de combinatie van de categorie en de eenheid van de onkosten. 

| Beschrijving van onkosten        | Onkostencategorie  | Eenheid  | Hoeveelheid  | Prijs per eenheid   |
|----------------------------|---------------------|-------|-----------|----------------|
| Afstand naar klantlocatie | Gereden kilometers             | Mijl  | 10        | 10 USD         |

Voor tijd bevat elke prijslijstkop een veld **Standaardeenheid voor tijd**. De waarde wordt ingesteld wanneer u de prijslijstkop maakt. Deze eenheid wordt vervolgens gebruikt om alle op rollen gebaseerde prijzen voor die prijslijst in te stellen.

Schattingsregels voor het veld **Tijd in prijsopgave** kunnen in elke tijdseenheid worden uitgedrukt. Schattingsregels voor projecten en tijdsvermeldingen voor projecten kunnen echter alleen de tijdseenheid **Uur** gebruiken. Als de eenheid van de tijdsvermelding niet overeenkomt met de eenheid in de prijslijstregel voor die rol, converteert het systeem de prijs naar de eenheden die zijn gedefinieerd in de projectschatting of de werkelijke projecttransactie.

In het volgende voorbeeld ziet u hoe PSA de eenhedengroep, eenheden en conversiefactoren gebruikt.
- Eenheden

   - **Eenhedengroep**: tijd 
   - **Eenheden**: uur 
    
    - **Dag** - Conversiefactor: 8 uur       
    - **Week** - Conversiefactor: 40 uur  
        
- Ingestelde prijslijst voor project A:

    - **Naam**: verkoopprijzen VK 2016 
    - **Standaardtijdseenheid**: dag 
    - **Valuta**: GBP

| Rol      | Eenhedengroep | Eenheid | Organisatie-eenheid | Prijs   |
|-----------|------------|------|---------------------|---------|
| Ontwikkelaar | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Tijdsvermelding

In de volgende tabel ziet u de resulterende verkooptransactie die door PSA is gemaakt voor een project van drie uur.


| Project   | Taak    | Rol      | Hoeveelheid | Eenheid  | Prijs per eenheid | Niet-gefactureerd verkoopbedrag |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Project A | Ontwerp  | Ontwikkelaar | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Veelgestelde vragen over tijdseenheden

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Wordt PSA omgezet in verschillende eenheden in het geval van onkosten?
Nr. Eenheidsconversie werkt alleen voor tijd. Voor onkosten wordt de prijs standaard ingesteld op 0,00 als het systeem geen prijs voor de combinatie van de onkostencategorie en eenheid kan vinden.

### <a name="why-does-psa-convert-time-units"></a>Waarom converteert PSA tijdseenheden?
In sommige landen of regio's is er een wettelijke vereiste dat factureringstarieven in dagen worden ingesteld. Prijsonderhandelingen en kortingen tijdens de prijsopgavecyclus worden uitgevoerd met behulp van dagtarieven voor elke factureerbare rol. De planningsschatting en tijdsinvoer worden uitgevoerd in uren. Om dit verschil in tijdseenheden te ondersteunen, converteert PSA tijdseenheden.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Kunnen tijdseenheden worden gewijzigd in projectschattingen?
Nr. Planningsschattingen kunnen momenteel alleen in uren worden uitgevoerd en kunnen niet worden gewijzigd.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Kunnen eenheden en eenhedengroepen worden bewerkt, verwijderd en toegevoegd?
Ja. Met uitzondering van eenhedengroep **Tijd** en de eenheid **Uur** kunnen alle eenheden worden verwijderd of bewerkt en kunnen er nieuwe eenheden worden toegevoegd. In PSA kunnen de eenhedengroep **Tijd** en de eenheid **Uur** niet worden verwijderd. Ze kunnen echter wel worden bijgewerkt met een vertaalde tekst voor het veld **Naam**.

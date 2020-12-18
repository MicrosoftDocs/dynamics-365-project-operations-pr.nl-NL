---
title: Intercompany-facturering configureren
description: Dit onderwerp bevat informatie en voorbeelden over het configureren van intercompany-facturering voor projecten.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595454"
---
# <a name="configure-intercompany-invoicing"></a>Intercompany-facturering configureren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Voer de volgende stappen uit om intercompany-facturering in te stellen voor projecten in Dynamics 365 Project Operations. Intercompany-transacties zijn tijd- en onkostentransacties van een projectcontract die bij één bedrijf of organisatie-eenheid horen, terwijl de resources in het projectcontract deel uitmaken van een ander bedrijf of een andere organisatie-eenheid.

## <a name="example-configure-intercompany-invoicing"></a>Voorbeeld: Intercompany-facturering configureren

In het volgende voorbeeld is Contoso Robotics USA (USPM) de lenende rechtspersoon en Contoso Robotics UK (GBPM) de uitlenende rechtspersoon. 

1. **Configureer intercompany-boekhouding tussen rechtspersonen**. Elk paar van lenende en uitlenende rechtspersonen moet in het grootboek worden geconfigureerd op de pagina [Intercompany-boekhouding](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. Ga in Dynamics 365 Finance naar **Grootboek** > **Boeken instellen** > **Intercompany-boekhouding**. Maak een record met de volgende informatie:

        - **Oorspronkelijk bedrijf** = **GBPM**
        - **Bestemmingsbedrijf** = **USPM**

2. **Configureer de handelsrelatie tussen rechtspersonen**. De klantrecord die de lenende rechtspersoon vertegenwoordigt, moet in de uitlenende rechtspersoon worden aangemaakt. De leverancierrecord die de uitlenende rechtspersoon vertegenwoordigt, moet in de lenende rechtspersoon worden aangemaakt.

     1. Selecteer in Finance de rechtspersoon **GBPM**.
     2. Ga naar **Klanten** > **Klant** > **Alle klanten**. Maak een nieuwe record voor de rechtspersoon **USPM**.
     3. Breid **Naam** uit, filter de records op **Type** en selecteer **Rechtspersonen**. 
     4. Zoek en selecteer de klantrecord voor **Contoso Robotics USA (USPM)**.
     5. Selecteer **Overeenkomstige waarde gebruiken**. 
     6. Selecteer de klantengroep en sla de record op.
     7. Selecteer de rechtspersoon **USPM**.
     8. Ga naar **Leveranciers** > **Leveranciers** > **Alle leveranciers**. Maak een nieuwe record voor de rechtspersoon **GBPM**.
     9. Breid **Naam** uit, filter de records op **Type** en selecteer **Rechtspersonen**. 
     10. Zoek en selecteer de klantrecord voor **Contoso Robotics UK (GBPM)**.
     11. Selecteer **Overeenkomstige waarde gebruiken**, selecteer de leveranciersgroep en sla de record op.
     12. Selecteer in de leveranciersrecord **Algemeen** > **Instellen** > **Intercompany**.
     13. Stel op het tabblad **Handelsrelatie** **Actief** in op **Ja**.
     14. Selecteer het leveranciersbedrijf **GBPM** en selecteer in **Mijn accountrecord** de klantrecord die u eerder in de procedure hebt gemaakt.

3. **Configureer intercompany-instellingen in Projectbeheer en boekhoudparameters**. 

    1. Selecteer de rechtspersoon **USPM** en ga naar **Projectbeheer en boekhouding** > **Instellen** > **Projectbeheer en boekhoudparameters**.
    2. Selecteer op het tabblad **Intercompany** de aanschaffingscategorie die overeenkomt met de leveranciersfacturen die automatisch worden gegenereerd.
    3. Selecteer in **Standaardcategorie** de optie **Intercompany-resources**.
    4. Selecteer de rechtspersoon **GBPM** en ga naar **Projectbeheer en boekhouding** > **Instellen** > **Projectbeheer en boekhoudparameters**.
    5. Selecteer op het tabblad **Intercompany** een standaardprojectcategorie voor elk transactietype. Projectcategorieën worden gebruikt voor belastingconfiguratie wanneer de gefactureerde categorie in intercompany-transacties alleen bestaat in de lenende rechtspersoon. U kunt ervoor kiezen om inkomsten toe te rekenen voor intercompany-transacties. Toerekening vindt plaats wanneer de transacties worden geboekt via het Project Operations-integratiejournaal in de uitlenende rechtspersoon. Het journaal wordt tegengeboekt wanneer de intercompany-factuur wordt geboekt.
    6. In groep **Bij het uitlenen van resources** selecteert u **...** > **Nieuw**. 
    7. Voer in het raster de volgende informatie in:

          - **Lenende rechtspersoon** = **GBPM**
          - **Inkomsten toerekenen** = **Ja**
          - **Standaard urenstaatcategorie** = **Standaard - uur**
          - **Standaard onkostencategorie** = **Standaard - onkosten**

4. **Stel intercompany-rekeningen voor kosten en opbrengsten in in de boekingsinstellingen van grootboek**. De intercompany-opbrengstrekening wordt gecrediteerd wanneer de intercompany-klantfactuur wordt geboekt in de uitlenende rechtspersoon. De intercompany-kostenrekening wordt gedebiteerd wanneer de overeenkomstige leveranciersfactuur in behandeling wordt geboekt in de lenende rechtspersoon. Deze rekeningen worden opgezet in overeenkomstige rechtspersonen. 
      
     1. Selecteer in Finance de lenende rechtspersoon **USPM**. 
     2. Ga naar **Projectbeheer en boekhouding** > **Instellen** > **Boeken** > **Boekingsinstellingen van grootboek**. 
     3. Op het tabblad **Kostenrekeningen** in **Grootboekrekeningtype** selecteert u **Intercompany-kosten**. Maak een nieuwe record met de volgende informatie:
      
        - **Uitlenende rechtspersoon** = **GBPM**
        - **Hoofdrekening** = Selecteer de hoofdrekening voor intercompany-kosten
        
     4. Selecteer de uitlenende rechtspersoon **GBPM**. 
     5. Ga naar **Projectbeheer en boekhouding** > **Instellen** > **Boeken** > **Boekingsinstellingen van grootboek**. 
     6. Op het tabblad **Opbrengstrekeningen** in **Grootboekrekeningtype** selecteert u **Intercompany-opbrengst**. Maak een nieuwe record met de volgende informatie:

        - **Lenende rechtspersoon** = **USPM**
        - **Hoofdrekening** = Selecteer de hoofdrekening voor intercompany-opbrengsten 

5. **Stel verrekenprijzen voor arbeid in**. Intercompany-verrekenprijzen worden geconfigureerd in Project Operations in Dataverse. Configureer [tarieven voor loonkosten](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) en [factureringstarieven voor arbeid](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) voor intercompany-facturering. Verrekenprijzen worden niet ondersteund voor intercompany-onkostentransacties. De intercompany-verkoopprijs zal altijd op dezelfde waarde worden ingesteld als de kostprijs van de resource-eenheid.

      De kosten voor ontwikkelaars in Contoso Robotics UK bedragen 88 GBP per uur. Contoso Robotics UK brengt bij Contoso Robotics USA 120 USD in rekening voor elk uur dat deze resource aan Amerikaanse projecten heeft gewerkt. Contoso Robotics USA zal de klant Adventure Works 200 USD factureren voor het werk dat is verricht door de ontwikkelaarsresource van Contoso Robotics UK.

      1. Ga in Project Operations in Dataverse naar **Verkoop** > **Prijslijst**. Maak een nieuwe kostprijslijst met de naam **Kostentarieven Contoso Robotics UK.** 
      2. Maak in de kostprijslijst een record aan met de volgende gegevens:
         - **Rol** = **Ontwikkelaar**
         - **Kosten** = **88 GBP**
      3. Ga naar **Instellingen** > **Organisatie-eenheden** en voeg deze kostprijslijst toe aan de organisatie-eenheid **Contoso Robotics UK**.
      4. Ga naar **Verkoop** > **Prijslijst**. Maak een kostprijslijst met de naam **Kostentarieven Contoso Robotics USA**. 
      5. Maak in de kostprijslijst een record aan met de volgende gegevens:
          - **Rol** = **Ontwikkelaar**
          - **Bedrijf voor resources** = **Contoso Robotics UK**
          - **Kosten** = **120 USD**
      6. Ga naar **Instellingen** > **Organisatie-eenheden** en voeg de kostprijslijst **Kostentarieven Contoso Robotics USA** toe aan de organisatie-eenheid **Contoso Robotics USA**.
      7. Ga naar **Verkoop** > **Prijslijst**. Maak een verkoopprijslijst met de naam **Factuurtarieven van Adventure Works**. 
      8. Maak in de verkoopprijslijst een record aan met de volgende gegevens:
          - **Rol** = **Ontwikkelaar**
          - **Bedrijf voor resources** = **Contoso Robotics UK**
          - **Factuurtarief** = **200 USD**
      9. Ga naar **Verkoop** > **Projectcontracten** en voeg de prijslijst **Factuurtarieven van Adventure Works** toe aan de Adventure Works-projectprijslijst van het projectcontract.

---
title: Intercompany-facturering configureren
description: Dit onderwerp bevat informatie en voorbeelden over het configureren van intercompany-facturering voor projecten.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9894a405403d4faeb2f02387b03c77a40a6cea3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001150"
---
# <a name="configure-intercompany-invoicing"></a>Intercompany-facturering configureren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Voer de volgende stappen uit om intercompany-facturering in te stellen voor projecten in Dynamics 365 Project Operations. Intercompany-transacties zijn tijd- en onkostentransacties van een projectcontract die bij één bedrijf of organisatie-eenheid horen, terwijl de resources in het projectcontract deel uitmaken van een ander bedrijf of een andere organisatie-eenheid.

## <a name="example-configure-intercompany-invoicing"></a>Voorbeeld: Intercompany-facturering configureren

In het volgende voorbeeld is Contoso Robotics USA (USPM) de lenende rechtspersoon en Contoso Robotics UK (GBPM) de uitlenende rechtspersoon. 

1. **Configureer intercompany-boekhouding tussen rechtspersonen**. Elk paar van lenende en uitlenende rechtspersonen moet in het grootboek worden geconfigureerd op de pagina [Intercompany-boekhouding](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. Ga in Dynamics 365 Finance naar **Grootboek** > **Boeken instellen** > **Intercompany-boekhouding**. Maak een record met de volgende informatie:

        - **Oorspronkelijk bedrijf** = **GBPM**
        - **Bestemmingsbedrijf** = **USPM**

2. **Configureer de handelsrelatie tussen rechtspersonen**. De klantrecord die de lenende rechtspersoon vertegenwoordigt, moet in de uitlenende rechtspersoon worden aangemaakt. De leverancierrecord die de uitlenende rechtspersoon vertegenwoordigt, moet in de lenende rechtspersoon worden aangemaakt.

     1. Selecteer in Finance de rechtspersoon **GBPM**.
     2. Ga naar **Klanten** > **Klant** > **Alle klanten**. Maak een nieuwe record voor de rechtspersoon **USPM**.
     3. Breid **Naam** uit, filter de records op **Type** en selecteer **Rechtspersonen**. 
     4. Zoek en selecteer de klantrecord voor **Contoso Robotics USA (USPM)**.
     5. Selecteer **Overeenkomstige waarde gebruiken**. 
     6. Selecteer de klantengroep **50 - Intercompany-klanten** en sla vervolgens de record op.
     7. Selecteer de rechtspersoon **USPM**.
     8. Ga naar **Leveranciers** > **Leveranciers** > **Alle leveranciers**. Maak een nieuwe record voor de rechtspersoon **GBPM**.
     9. Breid **Naam** uit, filter de records op **Type** en selecteer **Rechtspersonen**. 
     10. Zoek en selecteer de klantrecord voor **Contoso Robotics UK (GBPM)**.
     11. Selecteer **Overeenkomstige waarde gebruiken**, selecteer de leveranciersgroep en sla de record op.
     12. Selecteer in de leveranciersrecord **Algemeen** > **Instellen** > **Intercompany**.
     13. Stel op het tabblad **Handelsrelatie** **Actief** in op **Ja**.
     14. Stel het veld **Klantbedrijf** in op **GBPM** en selecteer in **Mijn accountrecord** de klantrecord die u eerder in de procedure hebt gemaakt.

3. **Configureer intercompany-instellingen in Projectbeheer en boekhoudparameters**. 

    1. Selecteer de rechtspersoon **USPM** en ga naar **Projectbeheer en boekhouding** > **Instellen** > **Projectbeheer en boekhoudparameters**.
    2. Selecteer op het tabblad **Intercompany** de aanschaffingscategorie die overeenkomt met de leveranciersfacturen die automatisch worden gegenereerd.
    3. Selecteer in **Standaardcategorie** de optie **Intercompany-resources**.
    4. Selecteer de rechtspersoon **GBPM** en ga naar **Projectbeheer en boekhouding** > **Instellen** > **Projectbeheer en boekhoudparameters**.
    5. Selecteer op het tabblad **Intercompany** een standaardprojectcategorie voor elk transactietype. Projectcategorieën worden gebruikt voor belastingconfiguratie wanneer de gefactureerde categorie in intercompany-transacties alleen bestaat in de lenende rechtspersoon. U kunt ervoor kiezen om inkomsten toe te rekenen voor intercompany-transacties. Toerekening vindt plaats wanneer de transacties worden geboekt via het Project Operations-integratiejournaal in de uitlenende rechtspersoon. Het journaal wordt tegengeboekt wanneer de intercompany-factuur wordt geboekt.
    6. In groep **Bij het uitlenen van resources** selecteert u **...** > **Nieuw**. 
    7. Voer in het raster de volgende informatie in:

          - **Lenende rechtspersoon** = **USPM**
          - **Inkomsten toerekenen** = **Ja**
          - **Standaard urenstaatcategorie** = **Standaard - uur**
          - **Standaard onkostencategorie** = **Standaard - onkosten**

4. **Stel intercompany-rekeningen voor kosten en opbrengsten in in de boekingsinstellingen van grootboek**. De intercompany-opbrengstrekening wordt gecrediteerd wanneer de intercompany-klantfactuur wordt geboekt in de uitlenende rechtspersoon. De intercompany-kostenrekening wordt gedebiteerd wanneer de overeenkomstige leveranciersfactuur in behandeling wordt geboekt in de lenende rechtspersoon. Deze rekeningen worden opgezet in overeenkomstige rechtspersonen. 
      
     1. Selecteer in Finance de lenende rechtspersoon **USPM**. 
     2. Ga naar **Projectbeheer en boekhouding** > **Instellen** > **Boeken** > **Boekingsinstellingen van grootboek**. 
     3. Op het tabblad **Kostenrekeningen** in **Grootboekrekeningtype** selecteert u **Intercompany-kosten**. Maak een nieuwe record met de volgende informatie:
      
        - **Uitlenende rechtspersoon** = **GBPM**
        - **Hoofdrekening** = Selecteer de hoofdrekening voor intercompany-kosten. Deze instellingen zijn vereist. De instellingen worden gebruikt voor intercompany-stromen in Finance, maar niet voor projectgerelateerde intercompany-stromen. Deze selectie heeft geen impact stroomafwaarts. 
        
     4. Selecteer de uitlenende rechtspersoon **GBPM**. 
     5. Ga naar **Projectbeheer en boekhouding** > **Instellen** > **Boeken** > **Boekingsinstellingen van grootboek**. 
     6. Op het tabblad **Opbrengstrekeningen** in **Grootboekrekeningtype** selecteert u **Intercompany-opbrengst**. Maak een nieuwe record met de volgende informatie:

        - **Lenende rechtspersoon** = **USPM**
        - **Hoofdrekening** = Selecteer de hoofdrekening voor intercompany-opbrengsten. Deze instellingen zijn vereist. De instellingen worden gebruikt voor intercompany-stromen in Finance, maar niet voor projectgerelateerde intercompany-stromen. Deze selectie heeft geen impact stroomafwaarts. 

5. **Stel verrekenprijzen voor arbeid in**. Intercompany-verrekenprijzen worden geconfigureerd in Project Operations in Dataverse. Configureer [tarieven voor loonkosten](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) en [factureringstarieven voor arbeid](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) voor intercompany-facturering. Verrekenprijzen worden niet ondersteund voor intercompany-onkostentransacties. De intercompany-verkoopprijs zal altijd op dezelfde waarde worden ingesteld als de kostprijs van de resource-eenheid.

      De ontwikkelaarskosten bij Contoso Robotics UK bedragen 88 GBP per uur. Contoso Robotics UK factureert Contoso Robotics USA 120 USD voor elk uur dat deze resource aan Amerikaanse projecten heeft gewerkt. Contoso Robotics USA brengt de klant Adventure Works 200 USD in rekening voor het werk dat door de ontwikkelaar van Contoso Robotics UK is uitgevoerd.

      1. Ga in Project Operations in Dataverse naar **Verkoop** > **Prijslijst**. Maak een nieuwe kostprijslijst aan met de naam **Contoso Robotics UK-kostentarieven**. 
      2. Maak in de kostprijslijst een record aan met de volgende gegevens:
         - **Rol** = **Ontwikkelaar**
         - **Kosten** = **88 GBP**
      3. Ga naar **Instellingen** > **Organisatorische eenheden** en voeg deze kostprijslijst toe aan de organisatorische eenheid **Contoso Robotics UK**.
      4. Ga naar **Verkoop** > **Prijslijst**. Maak een kostprijslijst aan met de naam **Contoso Robotics USA-kostentarieven**. 
      5. Maak in de kostprijslijst een record aan met de volgende gegevens:
          - **Rol** = **Ontwikkelaar**
          - **Bedrijf voor resources** = **Contoso Robotics UK**
          - **Kosten** = **120 USD**
      6. Ga naar **Instellingen** > **Organisatorische eenheden** en voeg de kostprijslijst **Contoso Robotics USA cost rates** toe aan de organisatorische eenheid **Contoso Robotics USA**.
      7. Ga naar **Verkoop** > **Prijslijst**. Maak een verkoopprijslijst met de naam **Factuurtarieven van Adventure Works**. 
      8. Maak in de verkoopprijslijst een record aan met de volgende gegevens:
          - **Rol** = **Ontwikkelaar**
          - **Bedrijf voor resources** = **Contoso Robotics UK**
          - **Factuurtarief** = **200 USD**
      9. Ga naar **Verkoop** > **Projectcontracten** en voeg de prijslijst **Factuurtarieven van Adventure Works** toe aan de Adventure Works-projectprijslijst van het projectcontract.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

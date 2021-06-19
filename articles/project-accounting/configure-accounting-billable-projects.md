---
title: Boekhouding configureren voor factureerbare projecten
description: Dit onderwerp biedt informatie over de boekhoudingsopties voor factureerbare projecten.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 413c9821f251fa37f5cfa082281be662d6be670a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012580"
---
# <a name="configure-accounting-for-billable-projects"></a>Boekhouding configureren voor factureerbare projecten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations ondersteunt verschillende boekhoudopties voor factureerbare projecten, waaronder tijd en materiaal en transacties met een vaste prijs.

- **Tijd- en materiaaltransacties** : deze transacties worden gefactureerd naarmate het werk vordert op basis van het verbruik van uren, onkosten, artikelen of vergoedingen voor het project. Deze transactiekosten kunnen worden vergeleken met de opbrengsten van elke transactie en het project wordt gefactureerd naarmate het werk vordert. Projectopbrengsten kunnen ook worden verzameld op het moment dat de transactie plaatsvindt. Tijdens de facturering wordt omzet herkend en wordt, indien van toepassing, verzamelde omzet teruggeboekt.
- **Transacties met een vaste prijs**: deze transacties worden gefactureerd volgens een factureringsschema dat is gebaseerd op het projectcontract. Omzet voor transacties met een vaste prijs kan worden verwerkt bij facturering of periodiek worden berekend en geboekt volgens de methode **Voltooid contract** of **Voltooid percentage**.

Een project wordt als factureerbaar beschouwd wanneer het is gekoppeld aan een of meer contractregels. Een projectcontractregel bepaalt voor zichzelf welke factureringsmethode en transactietypen zijn toegestaan.

Fabrikam Robotics heeft bijvoorbeeld een projectcontract met Adatum Corporation gewonnen voor apparatuuroptimalisatie. Adatum betaalt een vast bedrag van USD 10.000 om gemaakte projectkosten te dekken. Dit is een factureringsmethode voor een vaste prijs. De projecttijd en -kosten worden per gebruik in rekening gebracht. Dit is een factureringsmethode voor tijd en materiaal. Al het werk wordt bijgehouden onder één project met de naam Adatum-apparatuuroptimalisatie.

Een lid van het projectteam dient acht uur werk in voor het project Adatum-apparatuuroptimalisatie. Wanneer de projectmanager deze tijd goedkeurt, wordt de factureringsmethode voor tijd en materiaal gebruikt om werkelijke transacties, een factuur en een account te maken. Deze transactie wordt niet meegenomen in de berekening van de geschatte inkomsten voor vaste prijzen.

Een ander projectteamlid dient een bedrag van USD 2000,00 voor reiskosten in voor het project Adatum-apparatuuroptimalisatie. Wanneer de projectmanager deze kosten goedkeurt, wordt de factureringsmethode voor een vaste prijs gebruikt om werkelijke transacties en een account voor deze projectonkosten te maken. De klant wordt niet op basis van deze transactie gefactureerd. In plaats daarvan worden ze gefactureerd op basis van afzonderlijk geconfigureerde factureringsmijlpalen. Deze onkostentransactie wordt, met schattingen van onkosten, meegenomen in de berekening van de geschatte inkomsten voor vaste prijzen.

Boekhoudprincipes voor projecttransacties worden gedefinieerd in profielen voor projectkosten en -inkomsten. Voor elke projecttransactie bepaalt het systeem het juiste profiel voor projectkosten en -inkomsten door gebruik te maken van de profielregels voor projectkosten en -inkomsten die zijn geconfigureerd.

## <a name="define-project-cost-and-revenue-profiles"></a>Profielen voor projectkosten en -inkomsten opgeven 

Profielen voor projectkosten en -inkomsten bepalen de boekhoudregels voor projecttransacties. Deze profielen worden geconfigureerd in Projectmanagement en financiële administratie. 

Voer de volgende stappen uit om een nieuw profiel voor projectkosten en -inkomsten te maken. 

1. Ga naar **Projectmanagement en financiële administratie** > **Instellingen** > **Boeken** > **Profielen voor projectkosten en -inkomsten**. 
2. Selecteer **Nieuw** om een nieuw profiel voor projectkosten- en inkomsten te maken.
3. Voer in het veld **Naam** de naam en een korte beschrijving van het profiel in.
4. Selecteer in het veld **Factureringsmethode** de optie **Tijd en materiaal** of **Vaste prijs**.
5. Vouw het sneltabblad **Grootboek** uit. Met de velden op dit tabblad worden de boekhoudprincipes gedefinieerd die worden gebruikt wanneer projecttransacties worden gejournaliseerd met behulp van het Project Operations-integratiejournaal en vervolgens worden gefactureerd via het Project-factuurvoorstel.
6. Selecteer de juiste gegevens in de volgende velden op het sneltabblad **Grootboek**:

    - **Kosten boeken - uur**:

       - *Geen grootboek*: de kosten voor tijdtransacties worden niet naar het grootboek geboekt wanneer het Project Operations-integratiejournaal wordt geboekt. De accountant kan kosten echter op een later tijdstip boeken met de functie Kosten boeken.
       - **Saldo**: de kosten voor tijdtransacties worden afgeschreven van het grootboekrekeningtype *OHW - Kostprijs* en toegeschreven aan de *salaristoewijzingsrekening* in Instellingen voor boeking in grootboek. De accountant gebruikt de functie Kosten boeken om deze kosten periodiek van een saldorekening naar een winst- en verliesrekening te verplaatsen.
       - **Winst en verlies**: bij het boeken van het Project Operations-integratiejournaal worden de tijdtransactiekosten gedebiteerd van het grootboekrekeningtype *Kosten* en gecrediteerd aan de *salaristoewijzingsrekening* die is gedefinieerd op het tabblad **Kosten** van de pagina **Instellingen voor boeking in grootboek** (**Projectmanagement en financiële administratie** \> **Instellingen** \> **Boeken** \> **Instellingen voor boeking in grootboek**). Dit is de meest gebruikelijke instelling voor tijd- en materiaaltransacties.
        - *Nooit grootboek*: de kosten voor tijdtransacties worden nooit in het grootboek geboekt.

    - **Kosten boeken – onkosten**:

         - **Saldo**: bij het boeken van het Project Operations-integratiejournaal worden de onkostentransactiekosten gedebiteerd van het grootboekrekeningtype *OHW - kostprijs*, zoals gedefinieerd op het tabblad **Kosten** van de pagina **Instellingen voor boeking in grootboek** en gecrediteerd aan de tegenrekening op de journaalregel. Standaardtegenrekeningen voor onkosten worden gedefinieerd in **Projectmanagement en financiële administratie** > **Instellingen** \> **Boeken** \> **Standaardtegenrekening voor onkosten**. De accountant gebruikt de functie **Kosten boeken** om deze kosten periodiek van de saldorekening naar de winst- en verliesrekening te verplaatsen.
        - **Wint en verlies**: bij het boeken van het Project Operations-integratiejournaal worden de onkostentransactiekosten gedebiteerd van het grootboekrekeningtype *Kosten*, zoals gedefinieerd op het tabblad **Kosten** van de pagina **Instellingen voor boeking in grootboek** en gecrediteerd aan de tegenrekening op de journaalregel. Standaardtegenrekeningen voor onkosten worden gedefinieerd in **Projectmanagement en financiële administratie** \> **Instellingen** \> **Boeken** \> **Standaardtegenrekening voor onkosten**.
      
    - **Kosten boeken - artikel**​:

         - **Saldo**: bij het boeken van het Project Operations-integratiejournaal worden de artikeltransactiekosten afgeschreven van het grootboekrekeningtype *OHW - Kostenwaarde - artikel* zoals gedefinieerd op het tabblad **Kosten** op de pagina **Boekingsinstellingen voor grootboek** en bijgeschreven op de volgende rekening:
    
              - Voor gebruik van documenttype: rekening **Kosten - artikel** in **Boekingsinstellingen voor grootboekboek**​.  
              - Voor aankoop van documenttype: **Integratierekening voor inkoop** in **Projectbeheer en boekhoudkundige parameters**​.
           De accountant gebruikt de functie **Kosten boeken** om deze kosten periodiek van de saldorekening naar de winst- en verliesrekening te verplaatsen.
        - **Winst en verlies**: bij het boeken van het Project Operations-integratiejournaal worden de artikeltransactiekosten afgeschreven van het grootboekrekeningtype *Kosten* zoals gedefinieerd op het tabblad **Kosten** op de pagina **Boekingsinstellingen voor grootboek** en bijgeschreven op de volgende rekening:
         
             - Voor gebruik van documenttype: rekening **Kosten - artikel** in **Boekingsinstellingen voor grootboekboek**​.  
             - Voor aankoop van documenttype: **Integratierekening voor inkoop** in **Projectbeheer en boekhoudkundige parameters**​.
       
    - **Bij facturering op rekening**:

        - **Saldo** : bij het boeken van het Project-factuurvoorstel wordt een transactie op rekening (factureringsmijlpaal) gecrediteerd naar het grootboekrekeningtype *OHW gefactureerd - op rekening*, zoals gedefinieerd op het tabblad **Omzet** op de pagina **Instellingen voor boeking in grootboek** en gedebiteerd van de klantsaldorekening.
         - **Winst en verlies** : bij het boeken van het Project-factuurvoorstel wordt een transactie op rekening (factureringsmijlpaal) gecrediteerd naar het grootboekrekeningtype *Gefactureerde omzet - op rekening*, zoals gedefinieerd op het tabblad **Omzet** op de pagina **Instellingen voor boeking in grootboek** en gedebiteerd van de klantsaldorekening. Klantsaldorekeningen worden gedefinieerd in **Debiteuren** \> **Instellingen** \> **Boekingsprofielen voor klanten**.

   Wanneer u de boekingsprofielen definieert voor factureringsmethoden voor tijd en materiaal, hebt u de mogelijkheid om inkomsten te genereren per transactietype (uur, onkosten, artikel en vergoeding). Als **Omzet toerekenen** is ingesteld op **Ja**, worden niet-gefactureerde verkooptransacties in het Project Operations-integratiejournaal geregistreerd in het grootboek. De verkoopwaarde wordt gedebiteerd van de **OHW - verkoopwaarderekening** en gecrediteerd naar de rekening **Verzamelde omzet - verkoopwaarde** die is ingesteld op de pagina **Instellingen voor boeking in grootboek** op het tabblad **Omzet**. 
  
  > [!NOTE]
  > De optie **Omzet toerekenen** is alleen beschikbaar als het betreffende transactietype **Kosten** wordt geboekt naar de winst- en verliesrekening.
    
7. Vouw het sneltabblad **Schatting** uit. De velden op dit tabblad definiëren de berekeningsinstellingen voor omzetschattingen met een vaste prijs. De velden op dit tabblad zijn alleen van toepassing op profielen voor projectkosten en -inkomsten met de factureringsmethode **Vaste prijs**.
8. Selecteer de juiste gegevens in de volgende velden op het sneltabblad **Schatting**:

    - **Gebruikt principe voor de berekening van projectvoltooiing**:

        - **Voltooid contract**: kostenafstemming en omzetverantwoording vinden pas plaats aan het einde van het project. De kosten worden als OHW in de balans weergegeven totdat het project is voltooid.
        - **Voltooid percentage**: de verzamelde omzet wordt elke periode berekend en naar het grootboek geboekt op basis van het voltooiingspercentage van het project. Er zijn meerdere methoden beschikbaar om het voltooiingspercentage te berekenen. Deze methoden kunnen automatisch zijn op basis van configuratie of handmatig worden uitgevoerd.
        - **Geen OHW**: deze configuratie wordt gebruikt voor projecten met vaste prijzen met een korte tijdspanne en waarbij de facturering en de kosten in dezelfde periode plaatsvinden. In dit geval wordt het veld **Facturering op rekening** op het sneltabblad **Grootboek** automatisch ingesteld op **Winst en verlies** om ervoor te zorgen dat omzet wordt verantwoord bij facturering. Het omzetschattingsproces wordt niet gebruikt voor dit profiel voor projectkosten en -inkomsten.

    - **Methode van overeenkomst**: dit veld bepaalt hoe de berekende verkoopwaarde (verzamelde omzet) naar het grootboek wordt geboekt.

        - Met de methode **Verkoopwaarde** wordt de verkoopwaarde door kosten en omzet te matchen en deze vervolgens als één bedrag te boeken.
        - Op basis van de methode **Productie en winst** wordt de verkoopwaarde opgesplitst in gerealiseerde kosten en berekende winst. Deze worden apart geboekt.

    - **Kostensjablonen**: sta toe dat projecttransacties worden gegroepeerd op basis van transactietype en projectcategorie, en definieer berekeningsregels voor het voltooiingspercentage voor deze groepen.
    - **Periodecodes**: definieer de frequentie waarmee omzetschattingen worden berekend voor een bepaald profiel voor projectkosten en -inkomsten.
    - **Categorieën voor schatting**: wordt gebruikt voor het boeken van verkoopwaarde (verzamelde omzet) naar projecttransacties. Configureer eerst de speciale projectcategorie voor een transactietype **Tarief** en stel vervolgens de vlag **Schatting** in voor deze projectcategorie. Kies vervolgens, afhankelijk van de geselecteerde methode van overeenkomst, deze projectcategorie voor **Verkoop** of **Winst** in het profiel voor projectkosten en -inkomsten.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Voorbeeldconfiguraties voor profielen voor projectkosten en -inkomsten

Tijd en materialen - geen OHW

![Kosten- en inkomstenprofiel: Tijd en materialen - geen OHW](media/time-material-no-wip.png)

Tijd en materialen - geen OHW (omzet)

![Kosten- en inkomstenprofiel: Tijd en materialen - OHW](media/time-material-with-wip.png)

Vaste prijs – Geen OHW

![Kosten- en inkomstenprofiel: Vaste prijs - geen OHW](media/fixed-price-no-wip.png)

Vaste prijs - voltooid contract

![Kosten- en inkomstenprofiel: Vaste prijs - voltooid contract](media/fixed-price-completed-contract.png)

Vaste prijs - voltooiingspercentage

![Kosten- en inkomstenprofiel: Vaste prijs - voltooiingspercentage](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Voorbeelden van boekhoudkundige gebeurtenissen voor voorbeeldprofielen voor projectkosten en -inkomsten.

| Boekhoudkundige gebeurtenis                  | Tijd en materiaal - Geen OHW                       | Tijd en materiaal - OHW                                                                                           | Vaste prijs - geen OHW                                            | Vaste prijs - Voltooid contract                                                                            | Vaste prijs - Voltooiingspercentage                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Tijdtransacties journaliseren    | Debet - Kosten <br>Krediet - Salaristoewijzing          | Debet - Kosten <br>Krediet - Salaristoewijzing <br>Debet - Verkoopwaarde OHW <br>Krediet - Verkoopwaarde toegerekende omzet                | Debet - Kosten <br>Krediet - Salaristoewijzing                         | Debet - Kosten <br>Krediet - Salaristoewijzing                                                                    | Debet - Kosten <br>Krediet - Salaristoewijzing                       |
| Onkostentransacties journaliseren | Debet - Kosten <br>Krediet - Tegenrekening voor onkosten | Debet - Kosten <br>Krediet - Tegenrekening voor onkosten <br>Debet - Verkoopwaarde OHW <br>Krediet - Verkoopwaarde toegerekende omzet      | Debet - Kosten <br>Krediet - Tegenrekening voor onkosten                 | Debet - Kosten<br> Krediet - Tegenrekening voor onkosten                                                            | Debet - Kosten <br>Krediet - Tegenrekening voor onkosten               |
| Klant factureren                | Debet - Klantsaldo <br>Krediet - Gefactureerde omzet | Debet - Klantsaldo <br>Krediet - Gefactureerde omzet <br>Krediet - Verkoopwaarde OHW Debet - Verkoopwaarde toegerekende omzet | Debet - Klantsaldo <br>Krediet - Gefactureerde omzet - op rekening | Debet - Klantsaldo <br>Krediet - OHW - Gefactureerd op rekening                                                  | Debet - Klantsaldo <br>Krediet - OHW - Gefactureerd op rekening    |
| Geschatte omzet boeken             | Niet van toepassing                                   | Niet van toepassing                                                                                                    | Niet van toepassing                                                  | Debet - Kostprijs OHW <br>Krediet - Kosten                                                                         | Debet - OHW - Verkoopwaarde <br>Krediet - Verkoopwaarde toegerekende omzet |
| Verwijderen                         | Niet van toepassing                                   | Niet van toepassing                                                                                                    | Niet van toepassing                                                  | Krediet - Kostprijs OHW <br>Debet - Kosten <br>Krediet - Toegerekende omzet - Verkoopwaarde <br>Debet - OHW gefactureerd op rekening | Debet - OHW - Gefactureerd op rekening <br>Krediet - Verkoopwaarde OHW     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Profielregels voor projectkosten en -inkomsten configureren

Profielregels voor projectkosten en -inkomsten bepalen welk profiel voor projectkosten- en inkomsten moet worden gebruikt bij het verwerken van factureerbare projecttransacties. Definieer de regels via **Projectmanagement en financiële administratie** \> **Instellingen** \> **Boeken** \> **Profielregels voor projectkosten en -inkomsten**.

Regels kunnen worden gedefinieerd per projectcontract, projectgroep of specifiek project. Het systeem kiest altijd eerst de regel met de hoogste granulariteit.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

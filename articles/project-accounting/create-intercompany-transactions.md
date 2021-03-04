---
title: Intercompany-transacties maken
description: Dit onderwerp bevat informatie over het maken van intercompany-transacties.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a9d34d69ff59f0cb470bb852d8a80ecaedf6544
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595453"
---
# <a name="create-intercompany-transactions"></a>Intercompany-transacties maken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Intercompany-transacties zijn tijd- en onkostentransacties van een projectcontract die bij één bedrijf of organisatie-eenheid horen, terwijl de resources in het projectcontract deel uitmaken van een ander bedrijf of een andere organisatie-eenheid.

Wanneer een intercompany-transactie is goedgekeurd, worden de volgende werkelijke transacties gemaakt

| **Transactietype** | **Toegepaste prijslijst** | **Transactievaluta** |
| --- | --- | --- |
| Kosten | Kostprijslijst van contracterende eenheid | Valuta op de prijsregel |
| Niet-gefactureerde verkoop. Dit wordt alleen gemaakt voor werkelijke waarden die zijn gekoppeld aan een contractregel met het factureringstype, de tijd en het materiaal. | Prijslijst voor projectverkoop in contract | Contractvaluta |
| Kosten van resource-eenheid | Kostprijslijst van resource-eenheid | Valuta op de prijsregel |
| Verkopen interorganisatorische eenheid | Kostprijslijst van contracterende eenheid | Valuta op de prijsregel |

De kosten, de resource-eenheidskosten en de prijs en valuta voor verkooptransacties tussen de verschillende organisatie-eenheden worden bepaald door **organisatorische eenheid**. Dit is belangrijk om te onthouden wanneer u besluit hoe u bedrijven en organisatie-eenheden in uw implementatie wilt structureren.

Wanneer u verkoopkans-, prijsopgave-, projectcontract- en projectrecords maakt, controleert het systeem of de valuta van de contracterende eenheid overeenkomt met de valuta voor boekhouding van het bedrijf. Als ze niet hetzelfde zijn, kunnen deze records niet worden gemaakt. De valuta van de organisatie-eenheid wordt gedefinieerd in Dynamics 365 Project Operations via **Dataverse** > **Instellingen** > **Organisatie-eenheden**. De valuta voor boekhouding van een bedrijf wordt gedefinieerd in Dynamics 365 Finance via **Grootboek** > **Grootboek instellen** > **Grootboek**. De valuta wordt gesynchroniseerd met uw Dataverse-omgeving met behulp van de grootboektoewijzing voor Twee keer wegschrijven.

Het systeem creëert in de volgende situaties de resource-eenheidskosten en de werkelijke verkoopcijfers tussen de organisatie-eenheden:

  - Wanneer de resource-eenheid verschilt van de contracterende eenheid
  - Wanneer het resourcebedrijf verschilt van het contracterende bedrijf

Alleen transacties die een ander resourcebedrijf hebben dan het contracterende bedrijf, worden overgedragen aan de Dynamics 365 Finance-omgeving voor extra boekhouding.

De boekhouding voor de werkelijke projectwaarden wordt vastgelegd in het Project Operations-integratiejournaal in Finance. Het systeem maakt de volgende journaalregels.

| **Transactietype** | **Rechtspersoon** | **Maakt een projecttransactie bij het boeken** | **Financiële dimensies zijn afkomstig uit** | **Standaard btw-groep voor facturering en btw-groep voor factuurartikel** |
| --- | --- | --- | --- | --- |
| Kosten | Wordt niet toegevoegd aan het integratiejournaal | n.v.t. | n.v.t. | n.v.t. |
| Niet-gefactureerde verkoop | Het integratiejournaal voor de lenende rechtspersoon | Ja | Project | **Btw-groep facturering**: gebaseerd op de **contractklant** <br/> **Btw-groep voor factuurartikel**: van de huidige projectcategorie voor de rechtspersoon op de journaalregel |
| Kosten van resource-eenheid | Het integratiejournaal voor de uitlenende rechtspersoon | Geen | Intercompany-klant | **Btw-groep facturering**: gebaseerd op de **intercompany-klant** <br/> **Btw-groep voor factuurartikel**: van de huidige projectcategorie voor de rechtspersoon op de journaalregel |
| Interorganisatorische verkopen | Het integratiejournaal voor de uitlenende rechtspersoon | Geen | Intercompany-klant | **Btw-groep facturering**: gebaseerd op de **intercompany-klant** <br/> **Btw-groep voor factuurartikel**: van de huidige projectcategorie voor de rechtspersoon op de journaalregel |

### <a name="example-intercompany-transactions"></a>Voorbeeld: Intercompany-transacties

Elsje Hulsegge, ontwikkelaar werkzaam bij GBPM, registreert 10 uur werk voor een USPM Adventure Works-project, dat is goedgekeurd door de projectmanager. Ontwikkelaarskosten in GBPM zijn 88 GBP per uur. GBPM factureert USPM 120 USD per ontwikkelaaruur. USPM factureert de klant Adventure Works 200 USD voor het werk dat door de GBPM-resource is gedaan. Voor meer informatie raadpleegt u [Intercompany-facturering configureren](configure-intercompany-invoicing.md).

1. Ga in Project Operations naar **Resources** en selecteer **Elsje Hulsegge** in de lijst. Selecteer **GBPM** op het tabblad **Planning** in het veld **Bedrijf**.
2. Ga naar **Verkoop** > **Klanten** en selecteer **Nieuw** om een nieuw klantrecord voor Adventure Works te maken.
    1. Stel het bedrijf in op **USPM**.
    2. Stel **Relatietype** in op **Klant**.
    3. Selecteer **Klantengroep 10 - Binnenland**.
    4. Stel de valuta in op **USD**.
    5. Sla de record op.
3. Ga naar **Verkoop** > **Projectcontracten** en maak een nieuw projectcontract voor Adventure Works.
    1. Stel het bedrijf dat eigenaar is in op **USPM** en de contracterende eenheid op **Contoso Robotics US**.
    2. Selecteer Adventure Works als klant.
    3. Selecteer een productprijslijst en sla de record op.
    4. Maak op het tabblad **Contractregels** een nieuwe contractregel. Stel een naam in en selecteer **Tijd en materiaal** als factureringsmethode.
    5. Maak een nieuw project en koppel dit aan deze contractregel.
4. Log in als de resource **Elsje Hulsegge**. Ga naar **Projecten** > **Tijdinvoer** en maak een tijdregistratie voor het Adventure Works-project.
5. Log in als de projectmanager. Ga naar **Projecten** > **Goedkeuringen**, en keur de tijdinvoertransactie goed die door Elsje Hulsegge is geregistreerd.
6. Navigeer naar het Adventure Works-project en selecteer **Gerelateerd** > **Werkelijke waarden**. De volgende werkelijke transacties worden gemaakt.

| **Transactietype** | **Prijs** | **Transactievaluta** | **Bedrag** |
| --- | --- | --- | --- |
| Kosten | 120 | USD | 1200 |
| Niet-gefactureerde verkoop | 200 | USD | 2000 |
| Kosten van resource-eenheid | 88 | GBP | 880 |
| Verkopen interorganisatorische eenheid | 120 | USD | 1200 |

7. Log in als USPM-accountant. Open het Finance-exemplaar van Project Operations en selecteer het bedrijf **USPM**. 
8. Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Project Operations op Customer Engagement** > **Importeren uit fasering** en selecteer de uitvoering van het periodieke proces. Met dit periodieke proces wordt het Project Operations-integratiejournaal gevuld.
9. Ga naar **Projectbeheer en boekhouding** > **Journalen** > **Project Operations-integratiejournaal** en bekijk de journaalregels. Het systeem maakt de volgende regel.

    | **Transactietype** | **Prijs** | **Transactievaluta** | **Bedrag** |
    | --- | --- | --- | --- |
    | Niet-gefactureerde verkoop | 200 | USD | 2000 |

    Als het systeem is ingesteld om inkomsten toe te rekenen voor dit project, wordt het volgende geboekt:

    - Debet: Project - OHW-verkoopwaarde 200 USD
    - Credit: Project - Toegerekende inkomsten 200 USD

    Deze niet-gefactureerde verkoop is nu klaar voor facturering. De factuur voor de klant Adventure Works kan indien nodig financieel worden geboekt.

10. Log in als **GBPM**-accountant. Open het Finance-exemplaar van Project Operations en open het bedrijf **GBPM**. 
11. Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Project Operations op Customer Engagement** > **Importeren uit fasering** en voer het periodieke proces uit om het Project Operations-integratiejournaal te vullen.
12. Ga naar **Projectbeheer en boekhouding** > **Journalen** > **Project Operations-integratiejournaal** en bekijk de regels. Het systeem maakt de volgende regels.

    | **Transactietype** | **Prijs** | **Transactievaluta** | **Bedrag** |
    | --- | --- | --- | --- |
    | Kosten van resource-eenheid | 88 | GBP | 880 |
    | Verkopen interorganisatorische eenheid | 120 | USD | 1200 |

    Het boeken van deze records resulteert in de volgende boekstuktransacties:

    - Debet: projectkosten 88 GBP
    - Credit: salaristoewijzing 88 GBP

    Als het systeem is ingesteld om intercompany-inkomsten toe te rekenen voor dit project, wordt het volgende geboekt:

    - Debet: Project - OHW-verkoopwaarde 120 USD
    - Credit: Project - Toegerekende inkomsten 120 USD

    Het systeem is nu klaar om een intercompany-klantfactuur te creëren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
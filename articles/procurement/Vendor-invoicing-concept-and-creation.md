---
title: Leveranciersfacturen maken
description: In dit artikel wordt het concept van leveranciersfacturen beschreven en wordt uitgelegd hoe u ze maakt in Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475411"
---
# <a name="create-vendor-invoices"></a>Leveranciersfacturen maken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Om de in dit artikel beschreven functionaliteit te gebruiken, moet u de functie **Verwerking van werkelijke waarden van subcontracten met Project Operations voor op resources gebaseerde scenario's inschakelen** in de werkruimte **Functiebeheer**.

Leveranciersfacturering in Microsoft Dynamics 365 Project Operations kan worden gebruikt om kosten van leveringen van diensten en/of materialen op een voltooid project door leveranciers vast te leggen.

Wanneer diensten en/of materialen worden uitbesteed aan een leverancier, vormt een subcontract de contractuele overeenkomst met die leverancier. Naarmate de leverancier de diensten levert, of de materialen worden ontvangen en gebruikt voor projecttaken, worden de kosten op het project geregistreerd. De leverancier stuurt dan periodiek facturen. Deze facturen zijn geverifieerd en afgestemd op kosten die op het project zijn vastgelegd. Nadat het verificatieproces is voltooid, wordt de leveranciersfactuur bevestigd en vrijgegeven voor betaling.

## <a name="scenarios-for-use"></a>Scenario's voor gebruik

Leveranciersfacturen in Project Operations kunnen worden gebruikt om twee verschillende scenario's te ondersteunen:

- Klanten gebruiken de volledige uitbestedingservaringen.
- Klanten maken geen gebruik van de volledige uitbestedingservaringen, maar willen een uniform beeld van de kosten van projecten in Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klanten gebruiken de volledige uitbestedingservaringen

Ervaringen met leveranciersfacturen bieden een manier om tijdsvermeldingen, materiaalgebruik en onkostenposten die verwijzen naar uitbestede componenten te verifiëren en af te stemmen met leveranciersfactuurregels. Dit proces kan worden gebruikt om de juistheid van de leveranciersfactuurregels te verifiëren. Nadat het verificatieproces is voltooid en de leveranciersfactuur is bevestigd, boekt het systeem de werkelijke waarden terug die zijn vastgelegd door goedgekeurde logboeken voor tijd, onkosten en materiaalgebruik en maakt dan nieuwe werkelijke kosten aan met behulp van de leveranciersfactuurregels.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klanten maken geen gebruik van de volledige uitbestedingservaringen, maar willen een uniform beeld van de kosten van projecten in Project Operations

Als u het uitbestedingsproces bijhoudt in een systeem van derden, kunt u kosten van dat systeem van derden vastleggen in Project Operations door leveranciersfacturen te maken die niet naar subcontracten verwijzen. Op deze manier hebben uw projectmanagers één uniform overzicht van alle kosten van een bepaald project.

## <a name="create-vendor-invoices-in-project-operations"></a>Leveranciersfacturen in Project Operations maken

Leveranciersfacturen worden gemaakt in Dynamics 365 Finance, met behulp van de module **Leveranciers**. U kunt leveranciersfacturen niet rechtstreeks in Dataverse maken.

### <a name="set-up-vendor-invoice-verification"></a>Verificatie van leveranciersfacturen instellen

Als de leveranciersfactuur bedoeld is voor een subcontract in Dataverse, moet u de parameter **Handmatige verificatie door PM is vereist** inschakelen. De instelling van de optie bepaalt of de leveranciersfactuur automatisch moet worden bevestigd in Dataverse, of dat handmatige bevestiging vereist is. De kop van elke factuur van een projectleverancier bevat een optie met dezelfde naam. Standaard is de optie in de koptekst van alle projectleveranciersfacturen ingesteld op de waarde die u hier instelt. U kunt de waarde echter naar wens bijwerken in de koptekst van afzonderlijke leveranciersfacturen.

Als de optie is ingesteld op **Ja**, heeft de leveranciersfactuur die is gemaakt in Finance en wordt gesynchroniseerd met Dataverse de status **Concept**. De factuur moet vervolgens worden gevalideerd en geverifieerd door de projectmanager en bevestigd voordat deze wordt verwerkt en geboekt naar de specifieke project- en grootboekrekeningen in Finance.

Als de optie is ingesteld op **Nee**, wordt de leveranciersfactuur automatisch bevestigd. U hoeft verder niets te doen.

Voer de volgende stappen uit om verificatie van leveranciersfacturen in te stellen.

1. Ga in Finance naar **Projectmanagement en financiële administratie** \> **Instellen** \> **Parameters voor Projectmanagement en financiële administratie**.
1. Stel op het tabblad **Financiële dienstverlening** de optie **Handmatige verificatie door PM is vereist** in op **Ja** als verificatie van de leveranciersfacturen van onderaannemers volgens bedrijfsbeleid vereist is. Als verificatie door de projectmanager niet vereist is in Dataverse, laat u de optieset ingesteld op **Nee**. Standaard wordt de instelling gebruikt op de pagina **Leveranciersfacturen in behandeling**.

> [!NOTE]
> Leveranciersfacturen die zijn gemaakt voor subcontracten in Dataverse, kunnen alleen correct worden verwerkt als de optie **Handmatige verificatie door PM is vereist** is ingesteld op **Ja**. Werkelijke kosten voor tijd, materiaal en onkosten die door onderaannemers worden gemaakt, kunnen door de projectmanager alleen handmatig worden gekoppeld aan leveranciersfactuurregels als deze optie is ingesteld op **Ja**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Een inkoopintegratieaccount voor leveranciersfacturen instellen

Wanneer een leveranciersfactuur wordt geboekt in Finance for Project Operations – Geïntegreerde omgeving (niet-voorraad), worden financiële gegevens geboekt naar het integratieaccount voor inkoop. Het systeem genereert de werkelijke waarden in Dataverse voor de geboekte factuur. Deze werkelijke waarden worden in Finance geboekt met behulp van het projectintegratiejournaal. Bij het boeken van het projectintegratiejournaal worden de werkelijke kosten geboekt en wordt de rekening voor inkoopintegratie teruggeboekt.

Volg deze stappen om een inkoopintegratieaccount voor leveranciersfacturen in te stellen.

1. Ga in Finance naar **Projectmanagement en financiële administratie** \> **Instellen** \> **Parameters voor Projectmanagement en financiële administratie**.
1. Selecteer op het tabblad **Project Operations inschakelen in Dynamics 365 Customer Engagement** de optie **Materialen** \> **Inkoopintegratieaccount**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Leveranciersfacturen voor onderaannemers maken en boeken

Wanneer een boekhouder een factuur van de onderaannemer ontvangt, wordt in Finance een nieuwe factuur gemaakt.

1. Ga in Finance naar **Leveranciers** \> **Facturen** \> **Openstaande leveranciersfacturen**.
1. Selecteer in het **actievenster** de optie **Nieuw** om een leveranciersfactuur te maken.
1. Selecteer op de factuurkoptekst, in het veld **Factuuraccount**, de optie **Onderaannemer**.
1. Selecteer de factuurdatum.
1. Stel op het tabblad **Header** de optie **Handmatige verificatie door PM is vereist** in op **Ja**. De standaardinstelling van deze optie komt van de pagina **Parameters voor Projectmanagement en financiële administratie**. Het kan echter op leveranciersfactuurniveau worden gewijzigd.
1. Selecteer op het sneltabblad **Factuurregel** de optie **Regel toevoegen** om een regel voor een leveranciersfactuur te maken.
1. Selecteer de inkoopcategorie die is gemaakt voor subcontractregels en voer de eenheidsprijs, meeteenheid en hoeveelheid in.
1. Selecteer in de sectie voor leveranciersfactuurregels op het tabblad **Project** het project waarmee de onderaannemer de factuur voor het subcontract deelt.
1. Selecteer de projectcategorie. Het kan elk type **Item**, **Onkosten**, **Materialen** of **Uren** zijn.
1. Selecteer de rol alleen als de geselecteerde projectcategorie van het type **Uur** is.
1. Selecteer **Boeken** om de leveranciersfactuur te boeken.

U kunt ook een leveranciersfactuur maken door naar **Leveranciers** \> **Facturen** \> **Openstaande leveranciersfacturen** te gaan en **Nieuw** te selecteren.

Wanneer de leveranciersfactuur is geboekt, wordt deze beschikbaar in Dataverse voor verificatie en verwerking door de projectmanager.

## <a name="vendor-invoice-processing-in-dataverse"></a>Leveranciersfacturen verwerken in Dataverse

In de leveranciersfactuur die is gemaakt in Dataverse, zijn sommige veldwaarden afkomstig van de leveranciersfactuur die is vastgelegd in Finance. Andere waarden zijn standaardwaarden die afkomstig zijn uit het subcontract.

De volgende velden en gerelateerde records worden gekopieerd van het subcontract naar de koptekst van de leveranciersfactuur:

- Valuta
- Contracterende eenheid
- Betalingsvoorwaarden

Op de leveranciersfactuurregels gebruikt Project Operations de volgende veldwaarden om de standaard subcontract- en subcontractregelreferentie in te voeren:

- Transactieklasse
- - Rol
- Transactiecategorie
- Productvelden
- Project
- Opdracht

> [!NOTE]
> Subcontractregels met een vaste prijs worden niet ondersteund in Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

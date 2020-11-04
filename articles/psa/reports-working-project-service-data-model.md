---
title: Werken met het gegevensmodel van Project Service Automation
description: Dit onderwerp legt uit hoe u werkt met het gegevensmodel.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 19e999e16a5bf6321a5a61208c8654f7870e6007
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074749"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Werken met het gegevensmodel van Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation breidt andere app-entiteiten uit en introduceert eigen entiteiten in het gegevensmodel Common Data Service. In dit onderwerp worden enkele entiteiten beschreven die u tegenkomt in typische scenario's voor PSA-rapportage.

## <a name="reporting-on-opportunities"></a>Rapportage over verkoopkansen

Project Service Automation breidt de entiteit Dynamics 365 Sales-entiteit **Verkoopkans** uit door velden toe te voegen die projectgebaseerde scenario's mogelijk maken. Deze velden worden aangeduid met een schemanaam die wordt voorafgegaan door **msdyn**\_. Een nieuw veld dat belangrijk is voor het rapporteren van PSA-verkoopkansen is **Ordertype**. De waarde **Werkgebaseerd** in dit veld geeft aan dat de verkoopkans een PSA-verkoopkans is. Andere velden die aan de entiteit zijn toegevoegd, zijn onder andere **Aanbestedende organisatie** , waarin de organisatie wordt geregistreerd die de verkoopkans houdt, en **Accountmanager** , waarin de naam van de accountmanager wordt vastgelegd die verantwoordelijk is voor de verkoopkans.

De entiteit **Verkoopkansregel** bevat ook velden die zijn gerelateerd aan Project Service. **Factureringsmethode** geeft aan of de verkoopkansregel moet worden gefactureerd op basis van tijd en materiaal of op basis van vaste prijs, en in **Project** wordt de naam vastgelegd van het project dat de verkoopkans steunt. Andere velden die u kunt gebruiken in rapporten worden gebruikt voor kosten en bedragen in het budget van de klant voor het regelitem.

## <a name="reporting-on-quotes"></a>Rapporteren over prijsopgaven

PSA breidt de Verkoop-entiteit **Prijsopgave** uit door projectgerelateerde velden toe te voegen. Door **Ordertype** worden PSA-prijsopgaven onderscheiden van niet-PSA-prijsopgaven. De waarde **Werkgebaseerd** in dit veld geeft aan dat de prijsopgave een PSA-prijsopgave is. Andere velden die relevant kunnen zijn voor rapportage over PSA-prijsopgaven zijn bedragvelden, zoals **Toerekenbare kosten** , **Niet-toerekenbare kosten** , **Brutomarge** , **Schattingen** en **Budget**. Andere nuttige velden geven aan of de prijsopgave winstgevend is, of deze op tijd wordt voltooid en of deze voldoet aan de budgetverwachtingen van de klant.

PSA breidt ook de entiteit **Prijsopgaveregel** uit. Eén van de veldven die PSA toevoegt, is **Factureringsmethode** , waarmee wordt aangegeven hoe de prijsopgaveregel wordt gefactureerd (tijd en materiaal of vaste prijs). In andere velden die aan de entiteit zijn toegevoegd, wordt het gerelateerde project vastgelegd dat de prijsopgaveregel, de facturering, de kosten en het budget steunt.

PSA voegt ook nieuwe aan prijsopgaven gerelateerde entiteiten toe aan het Dynamics 365-gegevensmodel. Hieronder volgen een aantal voorbeelden:

- **Detail van prijsopgaveregel** : deze entiteit bevat de gegevens voor projectschattingen van de prijsopgaveregel. Deze bevat twee records voor elke prijsopgaveregel. In een van de records worden de kosten en kostendetails van de prijsopgaveregel opgeslagen en in de andere record het verkoopbedrag en de verkoopdetails van de prijsopgaveregel.
- **Factuurschema voor prijsopgaveregels** : deze entiteit bevat het factuurschema voor de prijsopgaveregel. Deze planning wordt gegenereerd op basis van de factureringsfrequentie die is toegewezen aan de prijsopgaveregel.
- **Mijlpaal van prijsopgaveregels** : deze entiteit bevat de factureringsmijlpalen voor regels voor prijsopgaven met vaste-prijsbasis.
- **Opsplitsing van analyse van prijsopgaveregels** : deze entiteit bevat de financiële gegevens van de prijsopgaveregel. Deze details kunnen nuttig zijn voor rapportage over verkopen waarvoor een prijsopgave is gemaakt en geschatte kostenbedragen via verschillende dimensies.

Andere entiteiten die PSA aan prijsopgaven toevoegt, zijn **Prijslijst voor projecten van prijsopgaveregel** , **Resourcecategorie voor prijsopgaveregels** en **Transactiecategorie voor prijsopgaveregels**.

![Diagram met prijsopgave, prijsopgaveregel en projectrelaties](media/PS-Reporting-image2.png "Diagram met prijsopgave, prijsopgaveregel en projectrelaties")

## <a name="reporting-on-project-contracts"></a>Rapporteren over projectcontracten

PSA breidt de Verkoop-entiteit **Order** uit die wordt gebruikt wanneer projectcontracten worden geregistreerd. Er wordt een belangrijk nieuw veld **Ordertype** toegevoegd dat het contract identificeert als een PSA-projectcontract in plaats van een verkooporder. De waarde **Werkgebaseerd** in dit veld geeft aan dat de order een PSA-order is. In andere nieuwe velden die aan de entiteit **Order** worden toegevoegd, worden gegevens vastgelegd over de kosten, de PSA-contractstatus en de organisatie die eigenaar is van het contract.

PSA breidt ook de entiteit **Verkooporderregel** uit. Tot de velden die worden toegevoegd, behoren velden waarin de factureringsmethode (tijd en materialen of vaste prijs), bedragen in het klantbudget en het onderliggende project worden vastgelegd.

PSA voegt ook nieuwe entiteiten toe die zijn ontworpen voor projectcontracten. Hieronder volgen een aantal voorbeelden:

- **Detail van projectcontractregels** : deze entiteit bevat de details op regelniveau, die zijn samengevoegd tot het contractregelbedrag. Deze kunnen zo gedetailleerd zijn als regelitems die worden gegenereerd op basis van een projectplanning op taakniveau.
- **Factuurschema voor contractregels** : deze entiteit bevat het factuurschema dat wordt gegenereerd op basis van de factuurfrequentie die is toegewezen aan de contractregel.
- **Contractmijlpalen** : deze entiteit bevat de factureringsmijlpalen voor contractregels met vaste prijs als factureringsvoorwaarde hebben.

Andere entiteiten die PSA aan contracten toevoegt, zijn **Prijslijst voor projecten van projectcontractregels** , **Resourcecategorie voor projectcontractregels** en **Transactiecategorie voor projectcontractregels**.

![Diagram met order, orderregel en projectrelaties](media/PS-Reporting-image3.png "Diagram met order, orderregel en projectrelaties")

## <a name="reporting-on-projects"></a>Rapporteren over projecten

De entiteit **Projecten** en de gerelateerde entiteiten worden alleen in PSA gebruikt. **Project** is de entiteit op het hoogste niveau, waarmee het werk en de kosten van de activiteiten wordt vastgelegd. Hier is een lijst van de gerelateerde entiteiten:

- **Projectteamlid** : deze entiteit bevat details over de boekbare resources die aan het project zijn toegewezen. Deze resources kunnen algemene boekbare resources zijn, of ze kunnen benoemde boekbare resources zijn die worden ingevoerd door de projectmanager of die worden gegenereerd vanuit de projectplanning.
- **Projecttaak** : deze entiteit bevat de taken waaruit het projectplan of de projectplanning bestaat.
- **Resourcetoewijzing** : deze entiteit bevat de taaktoewijzingen voor de boekbare resource.
- **Resourcevereiste** : deze entiteit bevat de vereisten voor alle algemene leden van het resourceteam.
- **Schattingen** en **Schattingsregel** : deze entiteiten hebben een koptekst/regelrelatie en bevatten onkostenschattingen voor het project. Taakschattingen worden opgeslagen in de entiteit **Resourceschatting**.

![Diagram met resourcevereiste en projectrelaties](media/PS-Reporting-image4.png "Diagram met resourcevereiste en projectrelaties")

## <a name="reporting-on-resources"></a>Rapporteren over resources

Projectresources gebruiken de entiteiten voor **Boekbare resources** uit Universal Resource Scheduling (URS), die worden gedeeld met andere apps zoals Microsoft Dynamics 365 Field Service. Hier volgt een lijst met de entiteiten die u mogelijk moet gebruiken wanneer u rapporteert over projectresources:

- **Boekbare resource** : deze entiteit vertegenwoordigt de gebruiker, contactpersoon, algemene resource, account, groep of apparatuur die wordt gebruikt in het projectteam.
- **Kenmerken van boekbare resources** : deze entiteit omvat de vaardigheden, certificeringen of opleiding van de resource. De kenmerken kunnen beoordelingswaarden hebben, die worden gedefinieerd door het beoordelingsmodel.
- **Categorie van boekbare resources** : deze entiteit vertegenwoordigt de rol van de boekbare resource.
- **Boekingen van boekbare resources** : deze entiteit vertegenwoordigt de tijd die is geboekt voor projecten voor de resource. Elke boeking heeft zowel een koptekstentiteit als regelentiteiten en elke regel heeft een status die de status van de boeking vertegenwoordigt.

![Diagram met eigenschappen van boekbare resources en relaties](media/PS-Reporting-image5.png "Diagram met eigenschappen van boekbare resources en relaties")

## <a name="reporting-on-actual-transactions"></a>Rapporteren over werkelijke transacties

Wanneer u een urenstaat of onkostendeclaratie goedkeurt, of een contract factureert in PSA, wordt de zakelijke transactie vastgelegd in de entiteit **Werkelijke waarde**. Deze entiteit kan dienen als basis voor bijna alle rapporten in PSA die met Finance te maken hebben. In de entiteit **Werkelijke waarde** worden de kosten en verkooptransacties vastgelegd voor de zakelijke gebeurtenis. Hierin worden ook veel relevante kenmerken vastgelegd.

Wanneer u met de entiteit **Werkelijke waarde** werkt, is het belangrijk dat u begrijpt welke transactie of transacties worden geregistreerd in de entiteit en wanneer de transacties worden geregistreerd. Hier is de gebruikelijke stroom wanneer u met tijdvermeldingen werkt (de stroom voor de vermelding onkosten is vergelijkbaar):

1. Wanneer de tijdsvermelding wordt opgeslagen, worden geen records gemaakt in de entiteit **Werkelijke waarde**.
2. Wanneer de tijdsvermelding wordt ingediend worden geen records gemaakt in de entiteit **Werkelijke waarde**.
3. Wanneer de tijdsvermelding is goedgekeurd, wordt één record gemaakt in de entiteit **Werkelijke waarde**. Er kan ook nog een tweede record worden gemaakt. In de eerste record worden de kosten van de tijdsvermelding opgeslagen. In de tweede record wordt het niet-gefactureerde verkoopbedrag van de tijdsvermelding opgeslagen. De tweede record is afhankelijk van of er aan het project een klant, een prijsopgave of een contractregel is toegewezen.

    | Documentdatum | Transactietype | Transactieklasse | Klant         | Contract   | Resource:     | Resourcerol | Factureringstype | Hoeveelheid | Prijs per eenheid | Bedrag |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3-2-18        | Kosten             | Time              | Alpine Ski House | Alpine CRM | Dana Plant | Projectmanager   | Toerekenbaar   | 8.0      | 50.00      | 400.00 |
    | 3-2-18        | Niet-gefactureerde verkoop   | Time              | Alpine Ski House | Alpine CRM | Dana Plant | Projectmanager   | Toerekenbaar   | 8.0      | 100.00     | 800.00 |

    Deze twee records zijn afzonderlijke records die wel aan elkaar gerelateerd zijn. Ze zijn noch debets noch credits.

4. Als een contract aan het project is gekoppeld, worden er nog twee records gemaakt in de entiteit **Werkelijke waarde** wanneer de tijdsvermelding wordt gefactureerd. Eerst wordt een negatief bedrag voor de niet-gefactureerde verkooprecord gemaakt. Deze record keert in wezen de niet-gefactureerde verkoop om. Als tweede wordt een transactie voor de gefactureerde verkoop gemaakt. Nogmaals, deze records zijn afzonderlijke, maar gerelateerde records, niet debets en credits.

    | Documentdatum | Transactietype | Transactieklasse | Klant         | Contract   | Resource:     | Resourcerol | Factureringstype | Hoeveelheid | Prijs per eenheid | Bedrag   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4-2-18        | Niet-gefactureerde verkoop   | Time              | Alpine Ski House | Alpine CRM | Dana Plant | Projectmanager   | Toerekenbaar   | - 8,0    | 100.00     | - 800,00 |
    | 4-2-18        | Gefactureerde verkoop     | Time              | Alpine Ski House | Alpine CRM | Dana Plant | Projectmanager   | Toerekenbaar   | 8.0      | 100.00     | 800.00   |

In de entiteitsrecords **Transactieoorsprong** wordt de oorsprong van de record **Werkelijke waarde** vastgelegd en in de record **Transactieverbinding** de gerelateerde records voor de record **Werkelijke waarde**. Bovendien bevat de record **Werkelijke waarde** verwijzingen naar het project, het projectcontract (de order), de boekbare resource en de klant.

![Diagram met transactieverbinding, oorsprong en werkelijke relaties](media/PS-Reporting-image6.png "Diagram met transactieverbinding, oorsprong en werkelijke relaties")

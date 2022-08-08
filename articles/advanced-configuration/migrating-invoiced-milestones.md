---
title: Volledig gefactureerde factureringsmijlpalen migreren bij cutover
description: In dit artikel wordt uitgelegd uit hoe u mijlpalen voor facturering met een vaste prijs kunt migreren die vóór de datum van inwerkingtreding aan de klant zijn gefactureerd voor openstaande projectcontracten.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028696"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Volledig gefactureerde factureringsmijlpalen migreren bij cutover

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

## <a name="scenario"></a>Scenario

Contoso gaat live met Microsoft Dynamics 365 Project Operations voor scenario's op basis van resources/niet-voorradige artikelen. Als onderdeel van de cutover-activiteiten moet het implementatieteam open projectcontracten migreren vanuit het oude systeem. Sommige van de projectcontracten bevatten contractregels die de methode voor facturering op basis van vaste prijs gebruiken en die al gedeeltelijk aan de eindklant zijn gefactureerd. Het implementatieteam moet deze factureringsmijlpalen migreren als **Klantfactuur geboekt**, omdat ze moeten worden opgenomen in de totale contractwaarde voor doeleinden van opbrengsttoerekening. Klantsaldi in Klanten en Grootboek mogen echter niet worden beïnvloed.

## <a name="solution"></a>Oplossing

### <a name="prerequisites"></a>Vereisten

- Dynamics 365 Finance 10.0.24 of hoger moet zijn geïnstalleerd.
- De omgeving waarin de migratiestappen worden voltooid, moet zich in de onderhoudsmodus bevinden. Er mogen geen andere activiteiten worden uitgevoerd terwijl de mijlpalen worden gemigreerd.
- De migratiestappen moeten precies worden gevolgd zoals hier beschreven en kunnen alleen worden gebruikt voor de cutover-activiteit. Microsoft ondersteunt geen ander gebruik van deze mogelijkheid.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Een cutover-versie maken van de toewijzing voor twee keer wegschrijven van contractregelmijlpalen voor Project Operations-integratie 

1. Zorg ervoor dat de doeltoewijzing voor de entiteit **Contractregelmijlpalen voor Project Operations-integratie** up-to-date is. 

    1. Ga in Financiën naar **Gegevensbeheer** \> **Gegevensentiteiten** en selecteer de entiteit **Contractregelmijlpalen voor Project Operations-integratie**. 
    2. Selecteer **Doeltoewijzingen wijzigen**. 
    3. Selecteer op de pagina **Fasering aan doel toewijzen** de optie **Toewijzing genereren** en bevestig vervolgens dat u de toewijzing wilt genereren.

2. Stop en vernieuw de toewijzing voor twee keer wegschrijven van **Contractregelmijlpalen voor Project Operations-integratie** (**msdyn\_contractlinescheduleofvalues**). 

    1. Ga naar **Gegevensbeheer** \> **twee keer wegschrijven**, selecteer de toewijzing en open de details. 
    2. Selecteer **Stop** en wacht tot het systeem de toewijzing stopt. 
    3. Selecteer **Tabellen vernieuwen**.

3. Voeg een toewijzing toe voor de transactiestatus.

    1. Selecteer **Toewijzing toevoegen**.
    2. Selecteer op de nieuwe regel, in de kolom **Apps voor financiën en bedrijfsactiviteiten** het veld **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Selecteer in de kolom **Microsoft Dataverse** de optie **msdyn\_invoicestatus \[Factuurstatus\]**.
    4. Selecteer in de kolom **Toewijzingstype** de pijl naar rechts (**\>**).
    5. Selecteer in het dialoogvenster dat verschijnt, in het veld **Synchronisatierichting** de optie **Dataverse naar apps voor financiën en bedrijfsactiviteiten**.
    6. Selecteer **Transformatie toevoegen**.
    7. Selecteer in het veld **Transformatietype** de optie **ValueMap**.
    8. Selecteer **Waardetoewijzing toevoegen**.
    9. Voer in het linkerveld **4** in. Voer in het rechterveld **192350001** in. 
    10. Selecteer **Opslaan**, en sluit vervolgens het dialoogvenster.

4. Selecteer **Opslaan als** om de versie van de toewijzing voor twee keer wegschrijven op te slaan. 
5. Selecteer in het deelvenster **Tabel toevoegen**, in het veld **Uitgever** de optie **Standaarduitgever**.
6. Voer in het veld **Versie** de versie in.
7. Voer in het veld **Beschrijving** een opmerking in over deze cutover-versie van de toewijzing. 
8. Selecteer **Save**.
9. Start de toewijzing.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Gefactureerde mijlpalen migreren naar de Dataverse-omgeving

1. Maak in de Dataverse-omgeving van Project Operations mijlpalen met een factuurstatus **Gereed voor facturering**. Migreer op dit moment geen mijlpalen die nog niet zijn gefactureerd.

    > [!NOTE]
    > Voordat u de factureringsmijlpalen migreert, moet u ervoor zorgen dat de financiële dimensies die zijn gerelateerd aan de projectcontractregel, zijn ingesteld op de verwachte waarden. Financiële dimensies kunnen niet worden bewerkt nadat de migratie is voltooid.

2. Nadat alle mijlpalen zijn gemigreerd, stopt u de volgende toewijzingen voor twee keer wegschrijven:

    - Mijlpalen voor projectcontractregels voor Project Operations-integratie (msdyn\_contractlinescheduleofvalues)
    - Werkelijke waarden voor integratie van Project Operations (msdyn\_actuals)
    - Projectfactuurvoorstel V2 (facturen)

    Volg deze stappen om de toewijzingen te stoppen:

    1. Ga in Finance naar **Gegevensbeheer** \> **twee keer wegschrijven**, selecteer een toewijzing en open de details.
    2. Selecteer **Stop** en wacht totdat het systeem de toewijzing stopt.

3. Maak en bevestig in de Dataverse-omgeving van Project Operations pro forma -facturen voor de factureringsmijlpalen. 

    1. Ga in het siteoverzicht naar de projectcontracten, selecteer de contracten en selecteer vervolgens **Facturen maken**.
    2. Nadat de facturen zijn gemaakt, opent u ze vanuit het menu **Facturen** in het siteoverzicht en selecteert u vervolgens **Bevestigen**.

    Met deze stap worden de vereiste records in de Dataverse-omgeving gemaakt. Het heeft echter geen invloed op financiën en klanten, omdat de eerder genoemde toewijzingen voor twee keer wegschrijven zijn stopgezet.

4. Nadat alle pro forma-facturen zijn bevestigd, zet u alle toewijzingen voor twee keer wegschrijven terug naar hun oorspronkelijke staat.

    1. Werk de versie van de toewijzing voor twee keer wegschrijven van **Contractregelmijlpalen voor Project Operations-integratie** (**msdyn\_contractlinescheduleofvalues**) bij naar de oorspronkelijke waarde. 
    2. Selecteer de toewijzing voor twee keer wegschrijven in de lijst met toewijzingen, selecteer **Versie van tabeltoewijzing** en selecteer vervolgens de oorspronkelijke versie van de tabeltoewijzing.
    3. Selecteer **Save**.
    4. Start de volgende toewijzingen voor twee keer wegschrijven opnieuw:

        - Mijlpalen voor projectcontractregels voor Project Operations-integratie (msdyn\_contractlinescheduleofvalues)
        - Werkelijke waarden voor integratie van Project Operations (msdyn\_actuals)
        - Projectfactuurvoorstel V2 (facturen)

De mijlpalen zijn nu gemigreerd en het systeem is gereed voor de volgende stappen in de cutover-activiteit.

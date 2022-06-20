---
title: Instelling en configuratie van gegevensintegratie in Project Operations
description: Dit artikel bevat informatie over het instellen en configureren van toewijzingen voor tweemaal wegschrijven in Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914534"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Instelling en configuratie van gegevensintegratie in Project Operations

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel bevat informatie over integratie van twee keer wegschrijven in Project Operations voor instellings- en configuratie-entiteiten.

## <a name="project-contracts-contract-lines-and-projects"></a>Projectcontracten, contractregels en projecten

Projectcontracten, contractregels en projecten worden gemaakt in Dataverse en gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten voor extra boekhouding. De records in deze entiteiten kunnen alleen worden gemaakt en verwijderd in Dataverse. Boekhoudkenmerken zoals standaardwaarden voor btw-groepen en financiële dimensies kunnen echter aan deze records worden toegevoegd in de apps voor financiën en bedrijfsactiviteiten.

  ![Concepten voor projectcontractintegratie.](./media/1ProjectContract.jpg)

Potentiële klanten, verkoopkansen en offertes worden bijgehouden in Dataverse en niet gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten omdat er geen downstream-boekhouding aan deze activiteit is gekoppeld.

De projectcontractfunctionaliteit in Dataverse maakt een projectcontractrecord in apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing **Kopteksten van projectcontracten (verkooporders)**. Bij het opslaan van een projectcontract in Dataverse wordt het aanmaken van een record van een klantentiteit voor een projectcontract gestart. Dit record wordt gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing **Bron van projectfinanciering (msdyn\_projectcontractssplitbillingrules)**. Deze kaart synchroniseert ook toevoegingen, updates en verwijderingen van klanten in projectcontracten. Gesplitste factureringspercentages tussen projectcontractklanten worden alleen beheerst in Dataverse en niet gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten.

Nadat een projectcontract is gemaakt in Dataverse, kan de projectaccountant de boekhoudkenmerken voor dit projectcontract bijwerken in apps voor financiën en bedrijfsactiviteiten door naar **Projectbeheer en financiële administratie** > **Projectcontracten** > **Instellingen** > **Standaardboekhouding weergeven** te gaan. De accountant kan operationele projectcontractkenmerken, zoals gevraagde leveringsdatum en contractbedrag, bekijken door de projectcontract-id te selecteren in apps voor financiën en bedrijfsactiviteiten, waardoor de gerelateerde projectcontractrecord wordt geopend in Dataverse.

De projectentiteit wordt gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing **Projecten V2 (msdyn\_projects)**. De projectaccountant kan:

  - Bekijk projecten in apps voor financiën en bedrijfsactiviteiten door naar **Projectbeheer en financiële administratie** > **Alle projecten** te gaan. 
  - Werk boekhoudkenmerken voor het project in apps voor financiën en bedrijfsactiviteiten bij door naar **Projectbeheer en financiële administratie** > **Alle projecten** > **Instellingen** > **Standaardboekhouding weergeven** te gaan.  
  - Bekijk operationele projectkenmerken, zoals geschatte begin- en einddatums, door de project-id te selecteren in apps voor financiën en bedrijfsactiviteiten, waarmee de gerelateerde projectrecord wordt geopend in Dataverse.

Een project wordt aan een projectcontract gekoppeld via de entiteit **Projectcontractregel**.

Projectcontractregels in Dataverse maken een factureringsregel voor projectcontracten in apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing **Projectcontractregels (salesorderdetails)**. De factureringsmethode definieert het type factureringsregel voor projectcontracten in apps voor financiën en bedrijfsactiviteiten:

  - Projectcontractregels met een factureringsmethode voor tijd en materiaal creëren een factureringsregel voor tijd en materiaaltype.
  - Contractregels voor factureringsmethode met een vaste prijs creëren een factureringsregel voor mijlpalen.

Projectcontractregels kunnen worden beoordeeld door de projectaccountant in apps voor financiën en bedrijfsactiviteiten door naar **Projectbeheer en financiële administratie** > **Projectcontracten** > **Instellingen** > **Standaardboekhouding weergeven** te gaan en de details op het tabblad **Contractregels** te bekijken. De accountant kan op dit tabblad ook standaard financiële dimensies instellen voor de contractregels voor de factureringsmethode met een vaste prijs.

## <a name="billing-milestones"></a>Factureringsmijlpalen

Projectcontractregels die de factureringsmethode tegen een vaste prijs gebruiken, worden gefactureerd via factureringsmijlpalen. Factureringsmijlpalen worden gesynchroniseerd om transacties op rekening in apps voor financiën en bedrijfsactiviteiten te projecteren met behulp van de tabeltoewijzing **Mijlpalen van contractregels voor integratie van projectbewerkingen (msdyn\_contractlinescheduleofvalues)**.

  ![Integratie van factureringsmijlpalen.](./media/2Milestones.jpg)

De accountant kan transacties op rekening bekijken en de boekhoudkundige kenmerken voor die transacties aanpassen door naar **Projectmanagement en boekhouding** > **Projectcontracten** > **Bijhouden** > **Transacties op rekening** of **Projectmanagement en boekhouding** > **Alle projecten** > **Bijhouden** > **Transacties op rekening** te gaan.

Wanneer u voor het eerst een factureringsmijlpaal maakt voor een bepaalde projectcontractregel, maakt het systeem automatisch een project voor een geschatte omzet met een vaste prijs voor het project dat aan deze contractregel is gekoppeld. Projecten met een geschatte opbrengst tegen een vaste prijs kunnen worden bekeken door naar **Projectmanagement en boekhouding** > **Projecten met omzetschattingen met een vaste prijs** te gaan.

### <a name="project-tasks"></a>Projecttaken

Projecttaken worden uitsluitend voor referentiedoeleinden gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten via de tabeltoewijzing **Projecttaken (msdyn\_projectstasks)**. Het maken, bijwerken en verwijderen van bewerkingen wordt niet ondersteund via apps voor financiën en bedrijfsactiviteiten.

  ![Integratie van projecttaken.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projectresources

De entiteit **Projectresourcerollen** entiteit wordt uitsluitend voor referentiedoeleinden gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing **Projectresourcerollen voor alle bedrijven (bookableresourcecategories)**. Omdat resourcerollen in Dataverse niet bedrijfsspecifiek zijn, maakt het systeem automatisch respectievelijke bedrijfsspecifieke resourcerollenrecords in apps voor financiën en bedrijfsactiviteiten voor alle rechtspersonen die zijn opgenomen in het integratiebereik voor dubbel wegschrijven.

![Integratie van resourcerollen.](./media/5Resources.jpg)

Projectresources in Project Operations worden onderhouden in Dataverse en worden niet gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten.

### <a name="transaction-categories"></a>Transactiecategorieën

Transactiecategorieën worden bijgehouden in Dataverse en gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing **Projecttransactiecategorieën (msdyn\_transactioncategories)**. Nadat de transactiecategorierecord is gesynchroniseerd, maakt het systeem automatisch vier gedeelde categorierecords. Elke record komt overeen met een transactietype in apps voor financiën en bedrijfsactiviteiten en koppelt deze aan de transactiecategorierecord.

![Integratie van transactiecategorieën.](./media/4TransactionCategories.jpg)

Het gebruik van transactiecategorieën voor schattingen en werkelijke waarden vereist dat de projectaccountant of systeembeheerder overeenkomstige projectcategorieën in elke rechtspersoon maakt. Zie [Projectcategorieën configureren](../project-accounting/configure-project-categories.md) voor meer informatie.

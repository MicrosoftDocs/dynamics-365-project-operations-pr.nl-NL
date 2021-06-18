---
title: Instelling en configuratie van gegevensintegratie in Project Operations
description: Deze onderwerp biedt informatie over het instellen en configureren van 'Twee keer wegschrijven'-kaarten in Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001060"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Instelling en configuratie van gegevensintegratie in Project Operations

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp biedt informatie over integratie van twee keer wegschrijven in Project Operations voor instellings- en configuratie-entiteiten.

## <a name="project-contracts-contract-lines-and-projects"></a>Projectcontracten, contractregels en projecten

Projectcontracten, contractregels en projecten worden gemaakt in Dataverse en gesynchroniseerd met Finance and Operations-apps voor extra financiële administratie. De records in deze entiteiten kunnen alleen worden gemaakt en verwijderd in Dataverse. Boekhoudkundige kenmerken zoals standaardwaarden voor btw-groepen en financiële dimensies kunnen echter aan deze records worden toegevoegd in de Finance and Operations-apps.

  ![Concepten voor projectcontractintegratie](./media/1ProjectContract.jpg)

Potentiële klanten, verkoopkansen en prijsopgaven voor verkoop worden bijgehouden in Dataverse en niet gesynchroniseerd met Finance and Operations-apps omdat er geen stroomafwaartse financiële administratie aan deze activiteit is gekoppeld.

De functionaliteit voor projectcontracten in Dataverse maakt een projectcontractrecord aan in Finance and Operations-apps met behulp van de tabeltoewijzing **Projectcontractkoppen (salesorders)**. Bij het opslaan van een projectcontract in Dataverse wordt het aanmaken van een record van een klantentiteit voor een projectcontract gestart. Deze record wordt gesynchroniseerd met Finance and Operations-apps met behulp van de tabeltoewijzing **Bron voor projectfinanciering (msdyn\_projectcontractssplitbillingrules)**. Deze kaart synchroniseert ook toevoegingen, updates en verwijderingen van klanten in projectcontracten. Gesplitste factureringspercentages tussen projectcontractklanten worden alleen bijgehouden in Dataverse en niet gesynchroniseerd met Finance and Operations-apps.

Nadat een projectcontract is gemaakt in Dataverse kan de projectaccountant de boekhoudkundige kenmerken voor dit projectcontract bijwerken in Finance and Operations-apps door naar **Projectmanagement en boekhouding** > **Projectcontracten** > **Instellingen** > **Standaardboekhouding weergeven** te gaan. De accountant kan de kenmerken van het operationele projectcontract bekijken, zoals de gewenste opleverdatum en het contractbedrag door de projectcontract-id te selecteren in Finance and Operations-apps waarmee de gerelateerde projectcontractrecord wordt geopend in Dataverse.

De projectentiteit wordt gesynchroniseerd met Finance and Operations-apps met behulp van de tabeltoewijzing **Projecten V2 (msdyn\_projects)**. De projectaccountant kan:

  - Projecten beoordelen in Finance and Operations-apps door naar **Projectmanagement en boekhouding** > **Alle projecten** te gaan. 
  - Werk boekhoudkundige kenmerken voor het project bij in Finance and Operations-apps door naar **Projectmanagement en boekhouding** > **Alle projecten** > **Instellingen** > **Standaardboekhouding weergeven** te gaan.  
  - Bekijk operationele projectkenmerken, zoals geschatte begin- en einddatums, door de project-id te selecteren in Finance and Operations-apps waardoor de gerelateerde projectrecord wordt geopend in Dataverse.

Een project wordt aan een projectcontract gekoppeld via de entiteit **Projectcontractregel**.

Projectcontractregels in Dataverse maken een factureringsregel voor projectcontracten aan in Finance and Operations-apps met behulp van de tabeltoewijzing **Projectcontractregels (salesorderdetails)**. De factureringsmethode definieert het type factureringsregel voor projectcontracten in Finance and Operations-apps:

  - Projectcontractregels met een factureringsmethode voor tijd en materiaal creëren een factureringsregel voor tijd en materiaaltype.
  - Contractregels voor factureringsmethode met een vaste prijs creëren een factureringsregel voor mijlpalen.

Projectcontractregels kunnen worden beoordeeld door de projectaccountant in Finance and Operations-apps door naar **Projectmanagement en boekhouding** > **Projectcontracten** > **Instellingen** > **Standaardboekhouding weergeven** te gaan en de details te bekijken op het tabblad **Contractregels**. De accountant kan op dit tabblad ook standaard financiële dimensies instellen voor de contractregels voor factureringsmethode tegen een vaste prijs.

## <a name="billing-milestones"></a>Factureringsmijlpalen

Projectcontractregels die de factureringsmethode tegen een vaste prijs gebruiken, worden gefactureerd via factureringsmijlpalen. Factureringsmijlpalen worden gesynchroniseerd om transacties op rekening te projecteren in Finance and Operations-apps met behulp van de tabeltoewijzing **Mijlpalen voor integratiecontractregels in Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integratie van factureringsmijlpalen](./media/2Milestones.jpg)

De accountant kan transacties op rekening bekijken en de boekhoudkundige kenmerken voor die transacties aanpassen door naar **Projectmanagement en boekhouding** > **Projectcontracten** > **Bijhouden** > **Transacties op rekening** of **Projectmanagement en boekhouding** > **Alle projecten** > **Bijhouden** > **Transacties op rekening** te gaan.

Wanneer u voor het eerst een factureringsmijlpaal maakt voor een bepaalde projectcontractregel, maakt het systeem automatisch een project voor een geschatte omzet met een vaste prijs voor het project dat aan deze contractregel is gekoppeld. Projecten met een geschatte opbrengst tegen een vaste prijs kunnen worden bekeken door naar **Projectmanagement en boekhouding** > **Projecten met omzetschattingen met een vaste prijs** te gaan.

### <a name="project-tasks"></a>Projecttaken

Projecttaken worden uitsluitend voor referentiedoeleinden gesynchroniseerd met Finance and Operations-apps via de tabeltoewijzing **Projecttaken (msdyn\_projecttasks)**. De bewerkingen voor maken, bijwerken en verwijderen worden niet ondersteund via Finance and Operations-apps.

  ![Integratie van projecttaken](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projectresources

De entiteit **Rollen van projectresources** wordt uitsluitend voor referentiedoeleinden gesynchroniseerd met Finance and Operations-apps via de tabeltoewijzing **Projectresourcerollen voor alle bedrijven (bookableresourcecategories)**. Omdat resourcerollen in Dataverse niet bedrijfsspecifiek zzijn, maakt het systeem automatisch respectievelijke bedrijfsspecifieke resourcerollenrecords aan in Finance and Operations-apps voor alle juridische entiteiten die zijn opgenomen in het integratiebereik voor twee keer wegschrijven.

![Integratie van resourcerollen](./media/5Resources.jpg)

Projectresources in Project Operations worden onderhouden in Dataverse en worden niet gesynchroniseerd met Finance and Operations-apps.

### <a name="transaction-categories"></a>Transactiecategorieën

Transactiecategorieën worden onderhouden in Dataverse en gesynchroniseerd met Finance and Operations-apps via de tabeltoewijzing **Projecttransactiecategorieën (msdyn\_transactioncategories)**. Nadat de transactiecategorierecord is gesynchroniseerd, maakt het systeem automatisch vier gedeelde categorierecords. Elke record komt overeen met een transactietype in Finance and Operations-apps en koppelt deze aan de transactiecategorierecord.

![Integratie van transactiecategorieën](./media/4TransactionCategories.jpg)

Het gebruik van transactiecategorieën voor schattingen en werkelijke waarden vereist dat de projectaccountant of systeembeheerder overeenkomstige projectcategorieën in elke rechtspersoon maakt. Zie [Projectcategorieën configureren](../project-accounting/configure-project-categories.md) voor meer informatie.

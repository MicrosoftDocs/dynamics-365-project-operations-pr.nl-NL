---
title: Functiewijzigingen van Project Service Automation naar Project Operations
description: Dit artikel biedt een overzicht van de functiewijzigingen van Project Service Automation naar Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925344"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Functiewijzigingen van Project Service Automation naar Project Operations

De upgrade van Dynamics 365 Project Service Automation naar Dynamics 365 Project Operations Lite wordt in drie fasen geleverd. Dit artikel biedt informatie over de belangrijkste wijzigingen die u kunt verwachten wanneer de upgrade is voltooid.

| Levering van de upgrade | Fase 1 <br>(Januari 2022) | Fase 2 <br>(Wave van april 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Geen afhankelijkheid van de structuur voor werkspecificatie (WBS) voor projecten. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| De structuur voor werkspecificatie is inbegrepen in de momenteel ondersteunde limieten van Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| De structuur voor werkspecificatie buiten de momenteel ondersteunde limieten van Project Operations, inclusief ondersteuning voor de Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projectbeheer

De belangrijkste wijzigingen in de gebruikerservaring zullen zich voordoen op het gebied van projectplanning. Project Operations past een nieuwe, moderne ervaring toe voor het beheren van een structuur voor werkspecificatie (WBS) door gebruik te maken van de planningsmogelijkheden die worden geboden door [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Verschillen in de planningservaring

De volgende tabel biedt een overzicht van de planningsverschillen tussen Project Service Automation en Project Operations.

|  Plannen     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projectsjablonen - Mogelijkheid om projectsjablonen te definiëren en toe te passen wanneer een project wordt gemaakt  |  &nbsp;    | :heavy_check_mark: |
| Integratie van structuur voor werkspecificatie (WBS) van projecten met desktopclient   |    &nbsp;  | :heavy_check_mark: |
| Beperkingen - Begin niet eerder dan, eindig niet later dan  | :heavy_check_mark: |   &nbsp;  |
| Mijlpalen - Taken zonder duur   | :heavy_check_mark:  |  &nbsp;  |
| Resourcegestuurde taken respecteren de beschikbaarheid van toegewezen resources   | :heavy_check_mark: |  &nbsp;    |
| Tijdgefaseerde bewerking - Bewerk plannen en werk van dag tot dag   |   &nbsp;  | :heavy_check_mark: |
| Automatische/handmatige planning - Gebruik de Project-planningsengine om taken automatisch of handmatig te plannen |  &nbsp; | :heavy_check_mark:  |
| Bewerk grote projecten rechtstreeks in de gebruikersinterface: er geldt geen limiet voor de grootte van bewerkbare plannen  | Limiet van 500 taken  | :heavy_check_mark:       |
| Percentage voltooid - Markeer taakvoortgang   | :heavy_check_mark:  |  &nbsp;  |
| [Modi voor projectplanning](../project-management/scheduling-modes.md) - Definieer het project als vaste eenheden, vaste inspanning of vaste duur | :heavy_check_mark: | &nbsp; |
| Tijdlijn - Bouw en pas de tijdlijnweergave aan om planningsdetails te visualiseren en te communiceren met belanghebbenden. | :heavy_check_mark:  | &nbsp; |
| Inspanningsgestuurde taken - Ondersteuning in planningsengine voor het plannen van een taak als inspanningsgestuurd  | :heavy_check_mark:  | &nbsp; |
| Dialoogvenster **Taakinformatie** - Sla taakdetails op met behulp van een dialoogvenster | :heavy_check_mark:  |  &nbsp;  |
| Slepen en neerzetten - Voer meervoudige selectie van taken uit en wijzig hun positie in de structuur voor werkspecificatie | :heavy_check_mark: | &nbsp;  |
| Flexibele permanente weergaven - Definieer gedetailleerdere weergaven van taakkenmerken   | :heavy_check_mark:  | &nbsp; |
| De structuur voor werkspecificatie sorteren en filteren  | :heavy_check_mark:  | &nbsp; |
| Weergave van borden voor projectlevering zonder gebruik van het watervalmodel  | :heavy_check_mark:   | &nbsp; |
| Tijdlijnweergave - Interactief Gantt-diagram dat wordt gebruikt om de structuur voor werkspecificatie te visualiseren en bewerken   | :heavy_check_mark:  | &nbsp; |
| Toetsenbordsneltoetsen - Gebruik sneltoetsen voor veelvoorkomende bewerkingen, zoals inspringen of invoegen  | :heavy_check_mark:  |  &nbsp; |
| Ongedaan maken op meerdere niveaus - Voer wat-als-analyses uit om de impact van wijzigingen volledig te begrijpen door een hele reeks bewerkingen ongedaan te maken en opnieuw toe te passen | :heavy_check_mark: | &nbsp; |
| Knippen/kopiëren/plakken - Werk samen aan planningsontwikkeling door planningsdetails tussen toepassingen te kopiëren en te plakken  | :heavy_check_mark: | &nbsp; |
| Checklijsten voor taken - Voeg tot 20 checklijstitems toe aan een taak   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projectplanning

De pagina **Project** in Project Operations vertoont een aanzienlijk aantal verschillen met de pagina **Project** in Project Service Automation.

De volgende acties zijn verwijderd van de pagina **Projecten** als onderdeel van de fase 1-upgrade:

  - **Openen in MS Project**
  - **Sjabloon maken**
  - **Koppeling met MS Project ongedaan maken**

De pagina **Project** in Project Operations bevat de volgende nieuwe tabbladen.

- **Materiaalschattingen**
- **Factureringsinstellingen van taak**

Het tabblad **Status** is verwijderd en het veld **Status** bevindt zich nu op het tabblad **Samenvatting** met de planningsmodus van het project.

   ![Updates voor de pagina Project.](media/projectform.png)

Het tabblad **Planning** is hernoemd naar het tabblad **Taak** en bevat de nieuwe projectplanningservaring met Project for the Web.

   ![Tabblad Nieuwe projecttaken.](media/tasktab.png)

## <a name="scheduling-modes"></a>Planningsmodi

Project Operations heeft een nieuwe functie geïntroduceerd, [Planningsmodi](../project-management/scheduling-modes.md). Alle bestaande Project Service Automation-projecten worden standaard ingesteld op **Vaste duur** in Project Operations. De standaardinstelling voor nieuwe projecten kan echter worden beheerd door naar **Instellingen** > **Parameters** > **Parameter** > **Planningsmodus** te gaan.

   ![Projectparameterinstellingen voor planningsmodus.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Limieten voor projectplanning

Project Operations vertrouwt op Project for the Web voor alle projectplanningsactiviteiten. Project for the Web beheert de structuur voor werkspecificatie met behulp van de limieten in de volgende tabel.

| **Veld**                                          | **Limiet**             |
|----------------------------------------------------|-----------------------|
| Maximum aantal taken voor een project                  | 500                   |
| Maximale duur voor een project               | 3650 dagen (10 jaar)  |
| Maximum aantal resources voor een project              | 300                   |
| Maximum aantal koppelingen (alleen opvolgend) voor een project | 600                   |
| Maximum aantal aangepaste velden voor een project          | 10                    |
| Maximaal hiërarchieniveau                            | 10 niveaus             |
| Maximum aantal koppelingen (opvolgend + voorgaand)            | 20                    |
| Maximale duur van bladtaak                      | 1250 dagen             |
| Maximale duur van een samenvattingstaak                 | 3650 dagen (10 jaar)  |
| Maximum aantal toegewezen resources aan een taak               | 20 resources          |
| Ondersteunde datumbereik voor een taak                    | 01-01-2000 - 31-12-2149 |
| Controlelijstonderdelen                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Uitbreidbaarheid en ontwikkeling van projectplanning

Nadat u een upgrade naar Project Operations hebt uitgevoerd, moet u de API's voor projectplanning gebruiken om bewerkingen voor maken, bijwerken en verwijderen uit te voeren op de volgende entiteiten:

|   Naam van entiteit           |   Logische naam van entiteit       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projecttaak            | msdyn_projecttask           |
| Afhankelijkheid van projecttaken | msdyn_projecttaskdependency |
| Resourcetoewijzing     | msdyn_resourceassignment    |
| Projectbucket          | msdyn_projectbucket         |
| Projectteamlid     | msdyn_projectteam           |

Zie [API's voor projectplanning gebruikenom bewerkingen uit te voeren met planningsentiteiten](../project-management/schedule-api-preview.md) voor implementatiebegeleiding als u momenteel aanpassingen hebt waarbij deze entiteiten betrokken zijn.

## <a name="data-model-changes"></a>Wijzigingen in gegevensmodel

Als onderdeel van Upgradefase 1 zijn er wijzigingen in het gegevensmodel. Deze wijzigingen zijn voornamelijk veldwijzigingen in bestaande entiteiten. In fase 1 vindt in de entiteiten **msydn_project** en **msdyn_projectteam** een aantal aanpassingen plaats. 

> [!IMPORTANT]
> Met het voltooien van toekomstige upgradefasen wordt deze sectie bijgewerkt met extra entiteiten.

De volgende velden zijn vervangen door nieuwe velden.

|   Entity          |   Oude logische naam   |   Nieuwe logische naam    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

De volgende velden zijn toegevoegd.

|   Entity          |   Logische naam                               |   Beschrijving |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Geeft de totale werkelijke verkoopwaarden van kosten voor het project weer. Uitsluitend voor gebruik in Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Geeft de totale werkelijke materiaalkosten voor het project weer. Uitsluitend voor gebruik in Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Geeft de totale werkelijke verkoopwaarden van materiaal weer voor het project. Uitsluitend voor gebruik in Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | De contractregel die aan dit project is gekoppeld. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Dit is een intern systeemveld dat wordt gebruikt voor **Project kopiëren** gerelateerd aan de correlatie-id. Uitsluitend voor gebruik in Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Dit is een intern systeemveld dat wordt gebruikt voor **Project kopiëren** gerelateerd aan de sessie-id. Uitsluitend voor gebruik in Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Laatste synchronisatie van algemeen xRM-revisietoken van de projectplanningsservice. |
| msdyn_project     | msdyn_msprojectdocument                      | Het Microsoft Project-document dat bij het project behoort. |
| msdyn_project     | msdyn_plannedmaterialcost                    | De totale geplande materiaalkosten voor het project. Uitsluitend voor gebruik in Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | De totale geplande verkoopwaarden voor materiaal voor het project. Uitsluitend voor gebruik in Project Service Automation. |
| msdyn_project     | msdyn_program                                | Het programma waaraan dit project is gerelateerd. |
| msdyn_project     | msdyn_quotelineproject                       | De prijsopgaveregel die aan dit project is gekoppeld. |
| msdyn_project     | msdyn_replaylogheader                        | De koptekst voor opnieuw afspelen van logboeken. |
| msdyn_project     | msdyn_schedulemode                           | De standaardplanningsmodus die wordt gebruikt voor alle taken in het project.  |
| msdyn_project     | msdyn_taskearlieststart                      | De vroegste begindatum van een taak in het project.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Het projectteamlid van waaruit dit projectteamlid is gekopieerd. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Geeft aan of de resourcevereiste moet worden gemaakt voor een nieuw gemaakt algemeen teamlid.  |
| msdyn_projectteam | msdyn_deletestatus                           | De verwijderingsstatus van het teamlid om bij te houden of er een verwijderingsaanvraag naar de projectplanningsservice is verzonden, en of met succes en binnen het verwachte tijdvenster een respons is teruggestuurd. |
| msdyn_projectteam | msdyn_effortcompleted                        | Houdt de inspanning bij die door het teamlid is besteed aan de eigen opdrachten. |
| msdyn_projectteam | msdyn_effortremaining                        | Houdt de inspanning bij die nog door het teamlid aan de opdrachten moet worden besteed. |
| msdyn_projectteam | msdyn_markedvooreletiontimer                 | De wachttijd vanaf het moment dat het teamlid een verwijderingsaanvraag naar de projectplanningsservice verzendt totdat het teamlid daadwerkelijk wordt verwijderd in Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | De timestamp die moet worden vastgelegd wanneer de verwijderingsaanvraag voor het teamlid naar de projectplanningsservice wordt verzonden. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Geeft het projectteamlid weer van waaruit dit projectteamlid is gekopieerd.  |

## <a name="project-templates"></a>Projectsjablonen

Project Operations biedt geen ondersteuning voor projectsjablonen. U kunt echter veel van de kernfunctionaliteit repliceren met behulp van de [API voor project kopiëren](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Ondersteuning voor desktop-invoegtoepassingen

In de eerste 2 fasen van de upgrade is geen ondersteuning voor de Microsoft Project Desktop-invoegtoepassing beschikbaar. In fase 3 kunnen klanten met projecten die groter zijn dan de momenteel ondersteunde limieten van Project for the Web de desktop-invoegtoepassing gebruiken.

## <a name="editing-resource-assignment-contours"></a>Contouren voor resourcetoewijzing bewerken

De mogelijkheid om de contouren van resourcetoewijzingen te bewerken, komt beschikbaar met fase 2 van de upgrade.

## <a name="billing-and-pricing"></a>Facturering en prijzen

De volgende nieuwe functies zijn toegevoegd in Project Operations. Deze functies zijn additief van aard en hebben geen invloed op het gegevensmodel van Project Service Automation.

- [Materiaalgebruik voor projecten en projecttaken registreren](../material/material-usage-log.md)
- [Toeleveringscontractbeheer](../pro/subcontracting/managing-subcontracts-overview.md)
- [Vooruitbetalingen en op voorschot gebaseerde contracten](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Contract voor niet-overschrijdingsstatus en validaties](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Taakgebaseerde facturering](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Verouderde onderdelen

In de volgende tabellen worden alle verouderde velden beschreven die na de upgrade naar de oplossing voor verouderde onderdelen worden verplaatst. Zie [Verouderde elementen van Dynamics 365 Project Service Automation 3x naar Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution) voor meer informatie en een koppeling naar de oplossing.

### <a name="invoicedetail"></a>invoicedetail

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Velden                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |


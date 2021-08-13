---
title: Wijzigingen in entiteiten, besturingselementen en de gebruikersinterface (Project Service Automation 3.x)
description: In dit onderwerp worden oplossingswijzigingen voor Microsoft Dynamics Project Service Automation 3.x beschreven.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 86b51e58189a62f15a5ded039e9265733a0d9d4a7c7bf8d18ac46aadf1d2a931
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987340"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Wijzigingen in entiteiten, besturingselementen en de gebruikersinterface (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


In Microsoft Dynamics Project Service Automation (PSA) 3.x zijn veel wijzigingen aangebracht in de entiteiten, besturingselementen, weergaven en de gebruikersinterface aangebracht. Dit onderwerp bevat informatie over deze belangrijke wijzigingen.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relaties tussen bovenliggende en onderliggende items voor entiteiten voor verkoopdocumenten, details van verkoopdocumentregels
In eerdere versies van Dynamics 365 Project Service Automation (PSA) dan versie 3.0 werden sommige van de relaties tussen entiteiten voor verkoopdocumenten, verkoopdocumentregels en details van verkoopdocumentregels geïmplementeerd via tekenreeksvelden die een tekenreeksweergave van de GUID van de gerelateerde entiteit bevatten. Dit werd veroorzaakt door platformbeperkingen die aanzienlijke aangepaste code op de server- en clientzijden van de oplossing vereisten om die relaties op een vergelijkbare manier als normale Dynamics CRM-entiteitsrelaties te laten werken en tekenreeksvelden te laten fungeren als opzoekvelden.

PSA 3.0 is bijgewerkt om de nieuwe entiteitsrelaties tussen de entiteiten voor verkoopdocumenten en verkoopdocumentregels te gebruiken.

Omdat opzoekvelden nu kunnen worden gebruikt om verwijzingen naar entiteiten aan te geven, zijn de velden die de tekenreekswaarde van de GUID van de gerelateerde entiteit in eerdere versies bevatten niet meer nodig en daarom afgeschaft. De aangepaste client- en servercode die de relaties gedefinieerd door verouderde tekenreeksvelden verwerkt, is ook afgeschaft.

### <a name="entity-schema-changes"></a>Wijzigingen in entiteitsschema
De volgende tabel bevat een één-op-één-lijst van de afgeschafte tekenreeksvelden en de nieuwe opzoekvelden voor de entiteiten. 

 Entiteit |   Afgeschaft veld (tekenreeks) | Nieuw veld (opzoeken)
--- | --- | ---
invoicedetail (Factuurregel) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Werkelijk) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Factuurschema voor projectcontractregels) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Mijlpaal voor projectcontractregels) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Feit) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Factuurregeldetail) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Journaalregel) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Resourcecategorie voor projectcontractregels) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Detail van projectcontractregels) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Transactiecategorie voor projectcontractregels) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Transactieclassificatie voor projectcontractregels) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Factuurschema voor prijsopgaveregels) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Resourcecategorie voor prijsopgaveregels) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Mijlpaal van prijsopgaveregels) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Detail van prijsopgaveregel) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Transactiecategorie voor prijsopgaveregels) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Transactieclassificatie voor prijsopgaveregels) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Orderregel) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Afgeschafte aangepaste weergaven en besturingselementen
De volgende aangepaste weergaven en besturingselementen, en de bijbehorende artefacten, zijn afgeschaft.

- De weergave Toerekenbaarheid.
- Aangepaste rasterbesturingselementen voor het weergeven van prijsopgaveregeldetails op de pagina **Projectgegevens** voor de prijsopgaveregel.
- Aangepaste rasterbesturingselementen voor het weergeven van contractregeldetails van projecten op de pagina **Projectgegevens** voor de verkooporderregel.

> [!NOTE]
> Zie voor de volledige lijst met afgeschafte resources [Afgeschafte webresources in Project Service Automation v3. x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Unified Client Interface-appmodule
Door de introductie van UCI-appmodules (Unified Client Interface) app-modules zijn de PSA-siteoverzichtitems uit het systeem verwijderd.  
Functionaliteit met betrekking tot het schakelen tussen formulieren voor verkoopkansen, prijsopgaven, orders en facturen is afgeschaft aangezien deze niet meer nodig is omdat de UCI-appmodule alleen PSA-versies van de formulieren bevat.  

De volgende webresources zijn afgeschaft:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Zie voor de volledige lijst met afgeschafte resources [Afgeschafte webresources in Project Service Automation v3. x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
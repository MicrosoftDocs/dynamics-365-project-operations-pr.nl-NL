---
title: Integratie van projectschattingen en werkelijke waarden
description: Dit onderwerp biedt informatie over integratie van twee keer wegschrijven in Project Operations voor projectschattingen en werkelijke waarden.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006285"
---
# <a name="project-estimates-and-actuals-integration"></a>Integratie van projectschattingen en werkelijke waarden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp biedt informatie over integratie van twee keer wegschrijven in Project Operations voor projectschattingen en werkelijke waarden.

## <a name="project-estimates"></a>Projectschattingen

Schattingen van arbeid, kosten en materiaal voor projecten worden gemaakt en bijgehouden in Microsoft Dataverse en gesynchroniseerd met Finance and Operations-apps voor boekhoudkundige doeleinden. Bewerkingen voor maken, bijwerken en verwijderen worden niet ondersteund via de Finance and Operations-apps.

Voor het maken van schattingen is een geldige boekhoudkundige configuratie voor het project vereist. Voor projecten die aan contractregels zijn gekoppeld, moet een geldig projectkosten- en opbrengstenprofiel worden gedefinieerd in de projectkosten- en -opbrengstenprofielregels. Zie [Boekhouding voor factureerbare projecten configureren](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules) voor meer informatie.

## <a name="labor-estimates"></a>Schattingen voor arbeid

Arbeidsschattingen worden gemaakt door de projectmanager of resourcemanager die ook een algemene of benoemde resource aan de projecttaak toewijst. Records voor resourcetoewijzingen kunnen worden bekeken op het tabblad **Resourcetoewijzingen** op de pagina **Projectdetails** in Dataverse. Records voor resourcetoewijzing in Dataverse maken records voor urenprognose in Finance and Operations-apps via **Project Operations-integratie-entiteit voor uurschattingen (msdyn\_resourceassignments)**.

   ![Integratie van schattingen voor arbeid.](./Media/DW4LaborEstimates.png)

Twee keer wegschrijven synchroniseert records voor resourcetoewijzing met de opslagtabel (**ProjCDSEstimateHoursImport**) en gebruikt vervolgens bedrijfslogica om records voor urenprognose te maken en bij te werken (**ProjForecastEmpl**).

De projectaccountant beoordeelt de records voor prognose-uren die zijn gemaakt in Finance and Operations-apps door naar **Projectmanagement en boekhouding** > **Alle projecten** > **Plan** > **Uurprognoses** te gaan.

## <a name="expense-estimates"></a>Onkostenschattingen

Onkostenschattingen worden gemaakt door de projectmanager op het tabblad **Onkostenschattingen** op de pagina **Projectdetails** in Dataverse. Onkostenschattingsrecords worden opgeslagen in de entiteit **Schattingsregel** in Dataverse. Deze schattingsrecords hebben een transactieklasse, **Onkosten**, en worden gesynchroniseerd met uitgavenprognoserecords in Finance and Operations-apps via **Project Operations-integratie-entiteit voor onkostenschattingen (msdyn\_estimatelines)**.

   ![Integratie van schattingen voor onkosten.](./Media/DW4ExpenseEstimates.png)

Twee keer wegschrijven synchroniseert records voor onkostenschatting met de opslagtabel **ProjCDSEstimateExpenseImport** en gebruikt vervolgens bedrijfslogica om records voor onkostenprognose te maken en bij te werken (**ProjForecastCost**). In schattingregels worden records voor verkoopschatting en kostenschatting afzonderlijk opgeslagen. De bedrijfslogica in Finance and Operations-apps vult één record Onkostenprognose met behulp van dit detail in de opslagtabel.

De projectaccountant kan records voor onkostenprognose beoordelen in Finance and Operations-apps door naar **Projectmanagement en boekhouding** > **Alle projecten** > **Plan** > **Onkostenprognoses** te gaan.

## <a name="material-estimates"></a>Materiaalschattingen

Materiaalschattingen worden gemaakt door de projectmanager op het tabblad **Materiaalschattingen** op de pagina **Projectdetails** in Dataverse. Materiaalschattingsrecords worden opgeslagen in de entiteit **Schattingsregel** in Dataverse. Deze schattingsrecords hebben de transactieklasse, **Materiaal**, en worden gesynchroniseerd met artikelprognoserecords in Finance and Operations-apps via **Project-integratietabel voor materiaalschattingen (msdyn\_estimatelines)**.

   ![Integratie van schattingen voor materiaal.](./Media/DW4MaterialEstimates.png)

Twee keer wegschrijven synchroniseert records voor materiaalschatting met de opslagtabel **ProjForecastSalesImpor** en gebruikt vervolgens bedrijfslogica om records voor artikelprognose te maken en bij te werken (**ForecastSales**). In schattingregels worden records voor verkoopschatting en kostenschatting afzonderlijk opgeslagen. De bedrijfslogica in Finance and Operations-apps vult één artikelprognoserecord met behulp van dit detail in de opslagtabel.

De projectaccountant kan records voor artikelprognose beoordelen in Finance and Operations-apps door naar **Projectmanagement en boekhouding** > **Alle projecten** > **Plan** > **Artikelprognoses** te gaan.

## <a name="project-actuals"></a>Werkelijke waarden voor projecten

Werkelijke waarden voor projecten worden gemaakt in Dataverse, gebaseerd op tijd, onkosten, materiaal en factureringsactiviteiten. Alle operationele kenmerken van deze transacties, waaronder hoeveelheid, kostprijs, verkoopprijs en project, worden vastgelegd in deze Dataverse-entiteit. Zie [Werkelijke waarden](../actuals/actuals-overview.md) voor meer informatie. Werkelijke records worden gesynchroniseerd met Finance and Operations-apps met behulp van de tabeltoewijzing voor twee keer wegschrijven **Werkelijke waarden voor Project Operations-integratei (msdyn\_actuals)** voor stroomafwaartse financiële administratie.

   ![Integratie van werkelijke waarden.](./Media/DW4Actuals.png)

De tabeltoewijzing **Werkelijke waarden voor Project Operations-integratie** synchroniseert alle records van de entiteit **Werkelijke waarden** in Dataverse, met het kenmerk **Synchronisatie overslaan (uitsluitend voor intern gebruik)** ingesteld op **Onwaar**. Deze kenmerkwaarde wordt automatisch ingesteld in Dataverse bij het maken van de record. Voorbeelden waarbij dit kenmerk is ingesteld op **Waar** zijn:

  - Werkelijke projectkosten voor intercompany-transacties. Zie [Intercompany-transacties maken](../project-accounting/create-intercompany-transactions.md) voor meer informatie. Deze records worden overgeslagen omdat het systeem de werkelijke projectkosten opnieuw maakt in Finance and Operations-apps bij het boeken van de intercompany-leveranciersfactuur.
  - Negatieve niet-gefactureerde verkooprecords die zijn gemaakt bij bevestiging van de proformafactuur. Deze records worden overgeslagen omdat het subgrootboek voor het project in Finance and Operations-apps de niet-gefactureerde verkooprecord bij facturering niet omkeert, maar de status wijzigt in volledig gefactureerd.

De tabeltoewijzing voor twee keer wegschrijven synchroniseert de werkelijke records met de opslagtabel, **ProjCDSActualsImport**. Deze records worden verwerkt door het periodieke proces **Importeren uit opslagtabel** bij het maken van journaalregels voor Project Operations-integratie en voorstelregels voor projectfacturen. Zie [Integratiejournaal in Project Operations](../project-accounting/project-operations-integration-journal.md) voor meer informatie.

Dataverse legt ook de verbanden tussen de daadwerkelijke transacties van het project vast in de entiteit **Transactieverbinding**. Zie [Werkelijke waarden aan originele records koppelen](../actuals/linkingactuals.md) voor meer informatie. Koppelingen tussen daadwerkelijke transacties worden ook gesynchroniseerd met Finance and Operations-apps met behulp van de tabeltoewijzing voor twee keer wegschrijven, **Integratie-entiteit voor projecttransactierelaties (msdyn\_transactionconnections)** voor meer informatie. Deze records worden gebruikt door het periodieke proces, **Importeren uit opslagtabel**, bij het maken van journaalregels voor Project Operations-integratie en voorstelregels voor projectfacturen.

Bij het boeken van een Project Operations-integratiedagboek en een projectfactuurvoorstel wordt een update in de respectievelijke records in de opslagtabel, **ProjCDSActualsImport**, geactiveerd. Het systeem registreert en legt de volgende boekhoudkundige kenmerken voor werkelijke transacties vast:

- Bedrag in valuta voor boekhouding
- Wisselkoers
- Boekstuknummer
- Bedrag van omzetbelasting

De tabeltoewijzing **Werkelijke waarden voor Project Operations-integratie** werkt respectievelijke actuele records in Dataverse bij met deze informatie.

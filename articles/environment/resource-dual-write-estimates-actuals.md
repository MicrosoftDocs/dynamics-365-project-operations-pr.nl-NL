---
title: Integratie van projectschattingen en werkelijke waarden
description: Dit artikel bevat informatie over integratie van twee keer wegschrijven in Project Operations voor projectschattingen en werkelijke projectwaarden.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914580"
---
# <a name="project-estimates-and-actuals-integration"></a>Integratie van projectschattingen en werkelijke waarden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel bevat informatie over integratie van twee keer wegschrijven in Project Operations voor projectschattingen en werkelijke projectwaarden.

## <a name="project-estimates"></a>Projectschattingen

Ramingen voor werkuren, onkosten en materialen voor projecten worden gemaakt en onderhouden in Microsoft Dataverse en gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten voor boekhoudkundige doeleinden. Bewerkingen voor maken, bijwerken en verwijderen worden niet ondersteund via de apps voor financiën en bedrijfsactiviteiten.

Voor het maken van schattingen is een geldige boekhoudkundige configuratie voor het project vereist. Voor projecten die aan contractregels zijn gekoppeld, moet een geldig projectkosten- en opbrengstenprofiel worden gedefinieerd in de projectkosten- en -opbrengstenprofielregels. Zie [Boekhouding voor factureerbare projecten configureren](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules) voor meer informatie.

## <a name="labor-estimates"></a>Schattingen voor arbeid

Arbeidsschattingen worden gemaakt door de projectmanager of resourcemanager die ook een algemene of benoemde resource aan de projecttaak toewijst. Records voor resourcetoewijzingen kunnen worden bekeken op het tabblad **Resourcetoewijzingen** op de pagina **Projectdetails** in Dataverse. Met resourcetoewijzingsrecords in Dataverse worden uurprognoserecords gemaakt in apps voor financiën en bedrijfsactiviteiten met **Project Operations-integratie-entiteit voor uurramingen (msdyn\_resourceassignments)**.

   ![Integratie van schattingen voor arbeid.](./Media/DW4LaborEstimates.png)

Twee keer wegschrijven synchroniseert records voor resourcetoewijzing met de opslagtabel (**ProjCDSEstimateHoursImport**) en gebruikt vervolgens bedrijfslogica om records voor urenprognose te maken en bij te werken (**ProjForecastEmpl**).

De projectaccountant beoordeelt prognose-uurrecords die zijn gemaakt in apps voor financiën en bedrijfsactiviteiten door naar **Projectbeheer en financiële administratie** > **Alle projecten** > **Plannen** > **Uurprognoses** te gaan.

## <a name="expense-estimates"></a>Onkostenschattingen

Onkostenschattingen worden gemaakt door de projectmanager op het tabblad **Onkostenschattingen** op de pagina **Projectdetails** in Dataverse. Onkostenschattingsrecords worden opgeslagen in de entiteit **Schattingsregel** in Dataverse. Deze prognoserecords hebben een transactieklasse, **Onkosten**, en worden gesynchroniseerd met onkostenprognoserecords in apps voor financiën en bedrijfsactiviteiten met behulp van **Project Operations integratie-entiteit voor kostenramingen (msdyn\_estimatelines)**.

   ![Integratie van schattingen voor onkosten.](./Media/DW4ExpenseEstimates.png)

Twee keer wegschrijven synchroniseert records voor onkostenschatting met de opslagtabel **ProjCDSEstimateExpenseImport** en gebruikt vervolgens bedrijfslogica om records voor onkostenprognose te maken en bij te werken (**ProjForecastCost**). In schattingregels worden records voor verkoopschatting en kostenschatting afzonderlijk opgeslagen. De bedrijfslogica in apps voor financiën en bedrijfsactiviteiten vult één onkostenprognoserecord met dit detail in de verzameltabel.

De projectaccountant kan onkostenprognoserecords in apps voor financiën en bedrijfsactiviteiten beoordelen door naar **Projectbeheer en financiële administratie** > **Alle projecten** > **Plannen** > **Kostenprognoses** te gaan.

## <a name="material-estimates"></a>Materiaalschattingen

Materiaalschattingen worden gemaakt door de projectmanager op het tabblad **Materiaalschattingen** op de pagina **Projectdetails** in Dataverse. Materiaalschattingsrecords worden opgeslagen in de entiteit **Schattingsregel** in Dataverse. Deze prognoserecords hebben de transactieklasse **Materiaal** en worden gesynchroniseerd met artikelprognoserecords in apps voor financiën en bedrijfsactiviteiten met behulp van **Project Operations integratie-entiteit voor materiaalschattingen (msdyn\_estimatelines)**.

   ![Integratie van schattingen voor materiaal.](./Media/DW4MaterialEstimates.png)

Twee keer wegschrijven synchroniseert records voor materiaalschatting met de opslagtabel **ProjForecastSalesImpor** en gebruikt vervolgens bedrijfslogica om records voor artikelprognose te maken en bij te werken (**ForecastSales**). In schattingregels worden records voor verkoopschatting en kostenschatting afzonderlijk opgeslagen. De bedrijfslogica in apps voor financiën en bedrijfsactiviteiten vult één artikelprognoserecord met dit detail in de verzameltabel.

De projectaccountant kan artikelprognoserecords in apps voor financiën en bedrijfsactiviteiten beoordelen door naar **Projectbeheer en financiële administratie** > **Alle projecten** > **Plannen** > **Artikelprognoses** te gaan.

## <a name="project-actuals"></a>Werkelijke waarden voor projecten

Werkelijke waarden voor projecten worden gemaakt in Dataverse, gebaseerd op tijd, onkosten, materiaal en factureringsactiviteiten. Alle operationele kenmerken van deze transacties, waaronder hoeveelheid, kostprijs, verkoopprijs en project, worden vastgelegd in deze Dataverse-entiteit. Zie [Werkelijke waarden](../actuals/actuals-overview.md) voor meer informatie. Werkelijke records worden gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing voor twee keer wegschrijven **Integratie van werkelijke waarden in Project Operations (msdyn\_actuals)** voor downstream-boekhouding.

   ![Integratie van werkelijke waarden.](./Media/DW4Actuals.png)

De tabeltoewijzing **Werkelijke waarden voor Project Operations-integratie** synchroniseert alle records van de entiteit **Werkelijke waarden** in Dataverse, met het kenmerk **Synchronisatie overslaan (uitsluitend voor intern gebruik)** ingesteld op **Onwaar**. Deze kenmerkwaarde wordt automatisch ingesteld in Dataverse bij het maken van de record. Voorbeelden waarbij dit kenmerk is ingesteld op **Waar** zijn:

  - Werkelijke projectkosten voor intercompany-transacties. Zie [Intercompany-transacties maken](../project-accounting/create-intercompany-transactions.md) voor meer informatie. Deze records worden overgeslagen omdat het systeem de werkelijke projectkosten opnieuw maakt in apps voor financiën en bedrijfsactiviteiten wanneer de intercompany-leveranciersfactuur wordt geboekt.
  - Negatieve niet-gefactureerde verkooprecords die zijn gemaakt bij bevestiging van de proformafactuur. Deze records worden overgeslagen omdat de projectsubadministratie in apps voor financiën en bedrijfsactiviteiten de niet-gefactureerde verkooprecord bij facturering niet ongedaan maakt, maar de status wijzigt in volledig gefactureerd.

De tabeltoewijzing voor twee keer wegschrijven synchroniseert de werkelijke records met de opslagtabel, **ProjCDSActualsImport**. Deze records worden verwerkt door het periodieke proces **Importeren uit opslagtabel** bij het maken van journaalregels voor Project Operations-integratie en voorstelregels voor projectfacturen. Zie [Integratiejournaal in Project Operations](../project-accounting/project-operations-integration-journal.md) voor meer informatie.

Dataverse legt ook de verbanden tussen de daadwerkelijke transacties van het project vast in de entiteit **Transactieverbinding**. Zie [Werkelijke waarden aan originele records koppelen](../actuals/linkingactuals.md) voor meer informatie. Koppelingen tussen daadwerkelijke transacties worden ook gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten met behulp van de toewijzingstabel voor twee keer wegschrijven **Integratie-entiteit voor projecttransactierelaties (msdyn\_transactionconnections)**. Deze records worden gebruikt door het periodieke proces, **Importeren uit opslagtabel**, bij het maken van journaalregels voor Project Operations-integratie en voorstelregels voor projectfacturen.

Bij het boeken van een Project Operations-integratiedagboek en een projectfactuurvoorstel wordt een update in de respectievelijke records in de opslagtabel, **ProjCDSActualsImport**, geactiveerd. Het systeem registreert en legt de volgende boekhoudkundige kenmerken voor werkelijke transacties vast:

- Bedrag in valuta voor boekhouding
- Wisselkoers
- Boekstuknummer
- Bedrag van omzetbelasting

De tabeltoewijzing **Werkelijke waarden voor Project Operations-integratie** werkt respectievelijke actuele records in Dataverse bij met deze informatie.

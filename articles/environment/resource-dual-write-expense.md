---
title: Integratie van onkostenbeheer
description: Dit artikel bevat informatie over de integratie van onkostendeclaraties in Project Operations met behulp van twee keer wegschrijven.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e11f1cfd714212691146eed59bcfb5b5facd750c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029203"
---
# <a name="expense-management-integration"></a>Integratie van onkostenbeheer

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel bevat informatie over de integratie van onkostendeclaraties in Project Operations [volledige onkostenimplementatie](../expense/expense-overview.md) met behulp van twee keer wegschrijven.

## <a name="expense-categories"></a>Onkostencategorieën

Bij een volledige onkostenimplementatie worden onkostencategorieën gemaakt en onderhouden in apps voor financiën en bedrijfsactiviteiten. Voer de volgende stappen uit om een nieuwe onkostencategorie te maken:

1. Maak in Microsoft Dataverse een categorie **Transactie**. Integratie van twee keer wegschrijven synchroniseert deze transactiecategorie met apps voor financiën en bedrijfsactiviteiten. Zie [Projectcategorieën configureren](/dynamics365/project-operations/project-accounting/configure-project-categories) en [Integratie van instellings- en configuratiegegevens in Project Operations](resource-dual-write-setup-integration.md) voor meer informatie. Als resultaat van deze integratie ,aalt het systeem vier gedeelde categorierecords in apps voor financiën en bedrijfsactiviteiten.
2. Ga in Finance naar **Onkostenbeheer** > **Instellingen** > **Gedeelde categorieën** en selecteer een gedeelde categorie met een transactieklasse **Onkosten**. Stel de parameter **Kan worden gebruikt in Onkosten** in op **Waar** en definieer het te gebruiken onkostentype.
3. Maak met behulp van deze gedeelde categorierecord een nieuwe onkostencategorie door naar **Onkostenbeheer** > **Instellingen** > **Onkostencategorieën** te gaan en **Nieuw** te selecteren. Wanneer de record is opgeslagen, gebruikt twee keer wegschrijven de tabeltoewijzing **Exportentiteit voor projectonkostencategorieën voor integratie van Project Operations (msdyn\_expensecategories)** om deze record te synchroniseren met Dataverse.

  ![Integratie van onkostencategorieën.](./media/DW6ExpenseCategories.png)

Onkostencategorieën in apps voor financiën en bedrijfsactiviteiten zijn bedrijfs- of rechtspersoonspecifiek. Er zijn afzonderlijke, corresponderende, rechtspersoonspecifieke records in Dataverse. Wanneer een projectmanager een kostenschatting maakt, kan deze geen onkostencategorieën selecteren die zijn gemaakt voor een project dat eigendom is van een ander bedrijf dan het bedrijf dat eigenaar is van het project waaraan hij of zij werkt. 

## <a name="expense-reports"></a>Onkostendeclaraties

Onkostenrapporten worden gemaakt en goedgekeurd in apps voor financiën en bedrijfsactiviteiten. Zie [Onkostendeclaraties maken en verwerken in Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/) voor meer informatie. Nadat de onkostendeclaratie is goedgekeurd door de projectmanager, wordt deze naar het grootboek geboekt. In project Operations worden projectgerelateerde onkostendeclaratieregels geboekt met behulp van speciale boekingsregels:

  - Projectgerelateerde kosten (inclusief niet-terugvorderbare belasting) worden niet onmiddellijk naar het account voor projectkosten in het grootboek geboekt, maar in plaats daarvan naar het integratieaccount voor onkosten. Dit account wordt geconfigureerd in **Projectmanagement en boekhouding** > **Instellingen** > **Projectbeheer en boekhoudkundige parameters**, tabblad **Project Operations in Dynamics 365 Customer Engagement**.
  - Twee keer wegschrijven synchroniseert naar Dataverse via tabeltoewijzing **Exportentiteit voor projectonkosten voor integratie van Project Operations (msdyn\_expenses)**.
  - Btw-subgrootboek, subgrootboek voor leveranciers en andere financiële boekingen worden geregistreerd zoals van toepassing op het moment dat de onkostendeclaratie wordt geboekt.

  ![Integratie van onkostendeclaraties.](./media/DW6ExpenseReports.png)

Wanneer een record wordt weggeschreven naar de entiteit **Onkosten** in Dataverse, activeert het systeem het geautomatiseerde goedkeuringsproces van de record. Indien nodig kan de status van het geautomatiseerde goedkeuringsproces worden bekeken in Dataverse door naar **Geavanceerde instellingen** > **Systeem** > **Systeemtaken** te gaan. Nadat de goedkeuring is voltooid, worden records voor onkostentransactieklassen gemaakt in de entiteit **Werkelijke waarden**.

Werkelijke, aan onkosten gerelateerde waarden worden vervolgens verwerkt met behulp van de tabeltoewijzing voor twee keer wegschrijven **Werkelijke waarden voor integratie van Project Operations (msdyn\_actuals)**. Zie [Schattingen en werkelijke waarden voor projecten](resource-dual-write-estimates-actuals.md) voor meer informatie .

Het periodieke proces, **Importeren uit opslagtabel** maakt aan onkostendeclaraties gerelateerde journaalregels in het journaal voor Project Operations Integration. De tegenrekening wordt standaard ingesteld op het integratieaccount voor onkosten. Het boekingsintegratiejournaal wist het rekeningsaldo voor de onkostentransactie en verplaatst het onkostenbedrag naar het account voor projectkosten. Het systeem maakt ook subadministratietransacties voor projecten voor downstream facturering en opbrengstentoerekening.

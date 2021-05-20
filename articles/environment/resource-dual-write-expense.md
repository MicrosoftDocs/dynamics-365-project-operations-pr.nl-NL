---
title: Integratie van onkostenbeheer
description: Dit onderwerp biedt informatie over integratie van onkostenrapporten in Project Operations via twee keer wegschrijven.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c347f14f3a479eb4aec951cfe4094c5581bce32
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955733"
---
# <a name="expense-management-integration"></a>Integratie van onkostenbeheer

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp biedt informatie over integratie van onkostenrapporten in Project Operations [volledige onkostenimplementatie](../expense/expense-overview.md) via twee keer wegschrijven.

## <a name="expense-categories"></a>Onkostencategorieën

Bij een volledige onkostenimplementatie worden onkostencategorieën gemaakt en onderhouden in Finance and Operations-apps. Voer de volgende stappen uit om een nieuwe onkostencategorie te maken:

1. Maak in Microsoft Dataverse een categorie **Transactie**. Integratie met twee keer wegschrijven synchroniseert deze transactiecategorie met Finance and Operations-apps. Zie [Projectcategorieën configureren](/dynamics365/project-operations/project-accounting/configure-project-categories) en [Integratie van instellings- en configuratiegegevens in Project Operations](resource-dual-write-setup-integration.md) voor meer informatie. Als resultaat van deze integratie maakt het systeem vier gedeelde categorierecords in Finance and Operations-apps.
2. Ga in Finance naar **Onkostenbeheer** > **Instellingen** > **Gedeelde categorieën** en selecteer een gedeelde categorie met een transactieklasse **Onkosten**. Stel de parameter **Kan worden gebruikt in Onkosten** in op **Waar** en definieer het te gebruiken onkostentype.
3. Maak met behulp van deze gedeelde categorierecord een nieuwe onkostencategorie door naar **Onkostenbeheer** > **Instellingen** > **Onkostencategorieën** te gaan en **Nieuw** te selecteren. Wanneer de record is opgeslagen, gebruikt twee keer wegschrijven de tabeltoewijzing **Exportentiteit voor projectonkostencategorieën voor integratie van Project Operations (msdyn\_expensecategories)** om deze record te synchroniseren met Dataverse.

  ![Integratie van onkostencategorieën](./media/DW6ExpenseCategories.png)

Onkostencategorieën in Finance and Operations-apps zijn specifiek voor het bedrijf of de rechtspersoon. Er zijn afzonderlijke, corresponderende, rechtspersoonspecifieke records in Dataverse. Wanneer een projectmanager een kostenschatting maakt, kan deze geen onkostencategorieën selecteren die zijn gemaakt voor een project dat eigendom is van een ander bedrijf dan het bedrijf dat eigenaar is van het project waaraan hij of zij werkt. 

## <a name="expense-reports"></a>Onkostendeclaraties

Onkostendeclaraties worden gemaakt en goedgekeurd in Finance and Operations-apps. Zie [Onkostendeclaraties maken en verwerken in Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/) voor meer informatie. Nadat de onkostendeclaratie is goedgekeurd door de projectmanager, wordt deze naar het grootboek geboekt. In project Operations worden projectgerelateerde onkostendeclaratieregels geboekt met behulp van speciale boekingsregels:

  - Projectgerelateerde kosten (inclusief niet-terugvorderbare belasting) worden niet onmiddellijk naar het account voor projectkosten in het grootboek geboekt, maar in plaats daarvan naar het integratieaccount voor onkosten. Dit account wordt geconfigureerd in **Projectmanagement en boekhouding** > **Instellingen** > **Projectbeheer en boekhoudkundige parameters**, tabblad **Project Operations in Dynamics 365 Customer Engagement**.
  - Twee keer wegschrijven synchroniseert naar Dataverse via tabeltoewijzing **Exportentiteit voor projectonkosten voor integratie van Project Operations (msdyn\_expenses)**.
  - Btw-subgrootboek, subgrootboek voor leveranciers en andere financiële boekingen worden geregistreerd zoals van toepassing op het moment dat de onkostendeclaratie wordt geboekt.

  ![Integratie van onkostendeclaraties](./media/DW6ExpenseReports.png)

Wanneer een record wordt weggeschreven naar de entiteit **Onkosten** in Dataverse, activeert het systeem het geautomatiseerde goedkeuringsproces van de record. Indien nodig kan de status van het geautomatiseerde goedkeuringsproces worden bekeken in Dataverse door naar **Geavanceerde instellingen** > **Systeem** > **Systeemtaken** te gaan. Nadat de goedkeuring is voltooid, worden records voor onkostentransactieklassen gemaakt in de entiteit **Werkelijke waarden**.

Werkelijke, aan onkosten gerelateerde waarden worden vervolgens verwerkt met behulp van de tabeltoewijzing voor twee keer wegschrijven **Werkelijke waarden voor integratie van Project Operations (msdyn\_actuals)**. Zie [Schattingen en werkelijke waarden voor projecten](resource-dual-write-estimates-actuals.md) voor meer informatie .

Het periodieke proces, **Importeren uit opslagtabel** maakt aan onkostendeclaraties gerelateerde journaalregels in het journaal voor Project Operations Integration. De tegenrekening wordt standaard ingesteld op het integratieaccount voor onkosten. Het boekingsintegratiejournaal wist het rekeningsaldo voor de onkostentransactie en verplaatst het onkostenbedrag naar het account voor projectkosten. Het systeem maakt ook subadministratietransacties voor projecten voor downstream facturering en opbrengstentoerekening.

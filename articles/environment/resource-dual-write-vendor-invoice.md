---
title: Integratie van leveranciersfacturen
description: Dit artikel biedt informatie over integratie van leveranciersfacturen in Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d1e41638b6fe827e9e577860a78a84a9948053e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912050"
---
# <a name="vendor-invoice-integration"></a>Integratie van leveranciersfacturen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Projectgerelateerde inkoop in Dynamics 365 Project Operations kan worden opgenomen door naar **Leveranciers** > **Facturen** > **In behandeling zijnde leveranciersfacturen** te gaan en een in behandeling zijnde leveranciersfactuur te gebruiken. Zie [Niet-voorradige materialen aanschaffen via een in behandeling zijnde leveranciersfactuur](../procurement/pending-vendor-invoices.md) voor meer informatie.

> [!IMPORTANT]
> Voordat u de functionaliteit gebruikt die in dit artikel wordt beschreven, moet u de vereiste configuraties doornemen en toepassen. Zie [Niet-voorradige materialen en in behandeling zijnde leveranciersfacturen inschakelen](../procurement/configure-materials-nonstocked.md) voor meer informatie.

In project Operations worden projectgerelateerde leveranciersfacturen geboekt met behulp van speciale boekingsregels:

- Projectgerelateerde kosten (inclusief niet-terugvorderbare belasting) worden niet onmiddellijk geboekt naar het projectkostenaccount in het grootboek. In plaats daarvan worden de kosten geboekt naar het **account voor inkoopintegratie**. Dit account wordt geconfigureerd in **Projectmanagement en boekhouding** > **Instellingen** > **Projectbeheer en boekhoudkundige parameters** op het tabblad **Project Operations in Dynamics 365 Customer Engagement**.
- Twee keer wegschrijven synchroniseert details van leveranciersfacturen naar Microsoft Dataverse met behulp van de volgende tabeltoewijzingen:

     - **Entiteit voor exporteren van leverancierfacturen in Project Operations-integratieprojecten (msdyn_projectvendorinvoices)**: deze tabeltoewijzing synchroniseert informatie in de koptekst van de leveranciersfactuur. Alleen leveranciersfacturen met ten minste één regel die een project-id bevat, worden gesynchroniseerd met Dataverse.
     - **Entiteit voor exporteren van leverancierfactuurregels in Project Operations-integratieprojecten (msdyn_projectvendorinvoicelines)**: deze tabeltoewijzing synchroniseert informatie in leveranciersfactuurregels. Alleen regels die een project-id bevatten, worden gesynchroniseerd met Dataverse.

     > [!NOTE]
     > Details van leveranciersfacturen in Dataverse zijn niet bewerkbaar.

Belastingsubadministratie, leverancierssubadministratie en andere financiële boekingen worden vastgelegd zoals van toepassing in Dynamics 365 Finance wanneer de leveranciersfactuur wordt geboekt.

![Integratie van leveranciersfacturen.](media/DW7VendorInvoice.png)

Wanneer records worden weggeschreven naar een entiteit **Leveranciersfactuur** in Dataverse begint een geautomatiseerd goedkeuringsproces voor de records. Indien nodig kan de status van het geautomatiseerde goedkeuringsproces worden bekeken in Dataverse door naar **Geavanceerde instellingen** > **Systeem** > **Systeemtaken** te gaan. Nadat de goedkeuring is voltooid, worden records voor materiaaltransactieklassen gemaakt in de entiteit **Werkelijke waarden**.

Werkelijke, aan materiaal gerelateerde waarden worden vervolgens verwerkt met behulp van de tabeltoewijzing voor twee keer wegschrijven **Werkelijke waarden voor integratie van Project Operations (msdyn_actuals)**. Zie [Schattingen en werkelijke waarden voor projecten](resource-dual-write-estimates-actuals.md) voor meer informatie .

Het periodieke proces, **Importeren uit opslagtabel** maakt aan leveranciersfacturen gerelateerde journaalregels voor Project Operations Integration. De tegenrekening wordt standaard ingesteld op het inkoopintegratieaccount. Nadat het integratiejournaal is geboekt, wordt het rekeningsaldo voor de leveranciersfactuurtransactie gewist en wordt het regelbedrag naar het account voor projectkosten verplaatst. Tevens worden subadministratietransacties voor projecten gemaakt voor downstream facturering en opbrengstentoerekening.

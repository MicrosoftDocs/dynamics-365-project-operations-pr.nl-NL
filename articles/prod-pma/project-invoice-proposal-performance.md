---
title: Prestaties van projectfactuurvoorstellen
description: Dit onderwerp biedt informatie over prestatieverbeteringen voor projectfactuurvoorstellen.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b6df8baf1013720778308ce536b037dec4775f040d2925a47508fb373900f81
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005700"
---
# <a name="project-invoice-proposal-performance"></a>Prestaties van projectfactuurvoorstellen

[!include [banner](../includes/banner.md)]

Wanneer u een nieuw factuurvoorstel maakt, kunt u prestatieproblemen tegenkomen naarmate het aantal projecten en subprojecten toeneemt. Om de prestaties te verbeteren, is er een functie beschikbaar die de tijd verkort die nodig is om een nieuw factuurvoorstel te maken voor geboekte projecttransacties.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Prestatieverbetering voor projectfactuurvoorstellen inschakelen
Voer de volgende stappen uit om de functie voor prestatieverbetering van projectfactuurvoorstellen in te schakelen.

1.  Ga naar **Functiebeheer** > **Alle**. Zoek in de lijst met functies naar **Prestatieverbetering voor projectfactuurvoorstellen**.
2.  Selecteer **Nu inschakelen**.
3.  Vernieuw de browser en maak een nieuw factuurvoorstel.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Prestatieverbetering voor projectfactuurvoorstellen uitschakelen
Voer de volgende stappen uit om de functie voor prestatieverbetering van projectfactuurvoorstellen uit te schakelen.

1.  Ga naar **Functiebeheer** > **Alle**. Zoek in de lijst met functies naar **Prestatieverbetering voor projectfactuurvoorstellen**.
2.  Selecteer **Uitschakelen**.
3.  Vernieuw de browser.

> [!NOTE]
> Factuurvoorstelprestaties kunnen niet worden toegepast wanneer factureringsregels zijn ingeschakeld.
> 
> Tijdens het batchproces om factuurvoorstellen te maken, splitst het aantal subtakende taken in een maximum aantal op basis van het aantal contracten met factureerbare transacties, ongeacht wat u hebt ingevoerd. Als u bijvoorbeeld **3** invoert voor het aantal subtaken voor het maken van factuurvoorstellen in batch en er zijn slechts twee contracten met factureerbare transacties, worden er slechts twee subtaken gemaakt.

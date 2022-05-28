---
title: Overzicht van bestede uren van resource
description: Dit onderwerp bevat informatie over de bestede uren van resources in Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e24bbb33cdf34426d4e7fff21b68fcaea2fcef5e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587120"
---
# <a name="resource-utilization-overview"></a>Overzicht van bestede uren van resource

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Resources kunnen een doelwaarde voor factureerbare bestede uren hebben. Dit doel voor bestede uren is gedefinieerd als een kenmerk voor de standaardrol van een resource, of is ingesteld in de record van de individuele boekbare resource. Berekeningen van bestede uren zijn gebaseerd op de werkelijke uren die resources hebben gerapporteerd door middel van goedgekeurde tijdsvermeldingen.

De volgende formules worden gebruikt om het gebruik te berekenen:

  - Factureerbare uren = Factureerbare werkelijke uren ÷ Resourcecapaciteit
  - Niet-factureerbare uren = Werkelijke tijd met factureringstype-ID = Niet-factureerbaar, Complementair of Niet beschikbaar ÷ Resourcecapaciteit
  - Intern = Werkelijke tijd zonder verkoopcontract ÷ Resourcecapaciteit
  - Resourcecapaciteit = Werkuren van resource – Afwezig – Niet-werkdagen

De weergave **Bestede uren van resource** vindt u in het deelvenster **Resources**.

Elke cel in het raster vertegenwoordigt het het percentage factureerbare uren van de resource in een periode, zoals een dag, week of maand. De volgende formules worden gebruikt voor de kleur van de cellen:

  - **Groen**: factureerbare bestede uren >= doel voor bestede uren van resource
  - **Geel**: doel voor bestede uren - 20 <= factureerbare bestede uren < doel voor bestede uren
  - **Rood**: factureerbare bestede uren < doel voor bestede uren – 20

Omdat de weergave **Bestede uren van resource** is gebaseerd op het planbord, kunt u met de filtermogelijkheden van het planbord uw resultaten filteren.

Het raster vereist dat u een doelwaarde voor bestede uren instelt voor de rol of voor de individuele resource. Dit kunt u doen in **Resources** > **Resourcerollen**.

Daarnaast moet een standaardrol worden toegewezen aan elke boekbare resource. Ga naar **Resources** > **Resources**. Controleer op het tabblad **Project Service** of een resourerol is gedefinieerd en of het veld **Is standaard** is ingesteld op **Ja**. U kunt extra rollen toevoegen waar **Is standaard** = **Nee**. De rol waar **Is standaard** = **Ja**, wordt gebruikt voor het evalueren van de bestede uren van de resource ten opzichte van het doel voor die rol.

Op het tabblad **Project Service** kunt u ook een afzonderlijk doel voor bestede uren voor de resource instellen. De berekening van de bestede uren gebruikt vervolgens die doelwaarde om te het doel van de resource te evalueren, in plaats van het doel van de standaardrol van de resource.

De bestede uren worden alleen voor een resource weergegeven als die resource goedgekeurde, factureerbare tijd heeft in de periode die wordt weergegeven in het raster.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
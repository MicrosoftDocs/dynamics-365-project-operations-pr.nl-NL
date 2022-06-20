---
title: Resourcecapaciteit synchroniseren
description: Dit artikel bevat informatie over het synchroniseren van de capaciteit van een resource in kalenders en projecten.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b684833ffae83b7cedfc73ee96a8aa8ddd4ec57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920698"
---
# <a name="synchronize-resource-capacity"></a>Resourcecapaciteit synchroniseren

[!include [banner](../includes/banner.md)]

De processen voor resourcesynchronisatie helpen garanderen dat informatie voor de agenda en de basisagenda naar beneden stroomt in de resourceplanning van het project. Als de agenda wordt gewijzigd, voeren de processen de vereiste updates uit in de planning van projectresources. De processen helpen ook de prestaties te verbeteren, omdat de resourcegegevens van de agenda van tevoren wordt gesynchroniseerd. Daarom vinden updates van gegevens over resourceplanning sneller plaats. We raden u aan de processen als batch te plannen in plaats van een voor een. Anders bestaat het risico dat iemand de inclusieve datums vergeet waarop de gegevens voor het laatst zijn gesynchroniseerd. Als geen inclusieve datums worden gebruikt, kunnen er hiaten ontstaan tijdens de synchronisatie van de datum.

![Agendasynchronisatie.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Samenvoegen van resourcecapaciteit synchroniseren

Het synchronisatieproces is ontworpen om alle agendagegevens van resources te synchroniseren. Deze informatie omvat basisagendagegevens over eventuele wijzigingen in de capaciteitstabel van de resourceagenda van het project. Als er nieuwe resources aan het project worden toegevoegd, zorgt synchronisatie ervoor dat de bijgewerkte agendagegevens beschikbaar zijn. Deze synchronisatie kan op elk moment worden uitgevoerd.

We raden u aan een batch te gebruiken. De opties zijn beschikbaar tijdens het synchroniseren van capaciteitsreserveringen.

1. Selecteer **Projectmanagement en financiële administratie** &gt; **Periodiek** &gt; **Capaciteitssynchronisatie** &gt; **Samenvoegen van resourcecapaciteit synchroniseren**.
2. Stel de opties in de volgende tabel in.

    | Optie      | Beschrijving |
    |-------------|-------------|
    | Periodecode | Selecteer desgewenst de intervalcode van de grootboekdatum om de begin- en einddatums in te stellen voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit. |
    | Begindatum  | Voer de begindatum in voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit. |
    | Einddatum    | Voer de einddatum in voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit. |

[![Synchronisatieproces.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
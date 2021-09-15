---
title: Resources voor subcontractregels
description: In dit onderwerp wordt uitgelegd hoe u de toegewezen resources opgeeft die door de leverancier worden geleverd voor een specifieke subcontractregel voor tijd.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323365"
---
# <a name="subcontract-line-resources"></a>Resources voor subcontractregels

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In Dynamics 365 Project Operations kan een leverancier resources opgeven die worden gebruikt om de resourcecapaciteit te leveren die wordt ingekocht op de subcontractregel voor tijd.

## <a name="create-subcontract-line-resources"></a>Resources voor subcontractregels maken

Voer de volgende stappen uit om resources voor subcontractregels te maken.

1. Selecteer in het navigatievenster de optie **Subcontracten** en open het subcontract waarmee u wilt werken.
2. Open de subcontractregel voor tijd waarop u leveranciersresources wilt opgeven.
3. Selecteer op het tabblad **Resources voor subcontractregels** in het subraster **+ Nieuwe resource voor subcontractregels**.
4. Voer op de pagina **Nieuwe mijlpaal voor subcontractregels** de vereiste informatie in en selecteer **Opslaan en sluiten**.

In de volgende tabel worden de velden in de resource voor subcontractregels uitgelegd.

| Veld |  Beschrijving |
| ----- | ------------ |
| Boekbare resource | Selecteer een boekbare resource van het type Contractmedewerker die u als resource op de subcontractregel wilt gebruiken. Als u nog geen boekbare resource voor de contractmedewerker hebt gemaakt, laat u dit veld leeg. Er wordt een boekbare resource gemaakt wanneer u de record opslaat.  |
| Contact | Als het veld **Boekbare resource** leeg is, kunt u uw subcontractregelresource maken van een bestaande contactpersoon. Gebruik de zoekfunctie om de lijst met actieve contactpersonen in het systeem te bekijken. Selecteer een contactpersoon voor de leverancier van dit subcontract. De contactpersoon die u selecteert, wordt gevalideerd wanneer u de record opslaat. Als de geselecteerde contactpersoon geen geldige contactpersoon is, wordt uw record niet opgeslagen. Als er geen boekbare resource is voor de geselecteerde contactpersoon, wordt door het systeem een boekbare resource gemaakt voor de geselecteerde contactpersoon voordat de subcontractregelresource wordt gemaakt. |
| Gebruiker | Als het veld **Boekbare resource** leeg is, kunt u een subcontractregelresource maken door een actieve contactpersoon te selecteren. Gebruik de zoekfunctie om de lijst met actieve gebruikers in het systeem te bekijken. Als er geen boekbare resource is voor de geselecteerde gebruiker, wordt door het systeem een boekbare resource gemaakt voor de geselecteerde gebruiker voordat de subcontractregelresource wordt gemaakt. |
| Begindatum | De datum waarop de toewijzing van de onderaannemer begint. Als deze resource is geboekt voor een periode die vóór dit datumbereik valt, wordt er een waarschuwing weergegeven. |
| Einddatum | De datum waarop de toewijzing van de onderaannemer eindigt. Als deze resource is geboekt voor een periode die na dit datumbereik valt, wordt er een waarschuwing weergegeven. |
| Inspanning | Het totale aantal werkuren dat de onderaannemer aan deze subcontractregel besteedt. Er wordt een waarschuwing weergegeven als deze resource wordt geboekt voor ander werk dan is toegewezen in dit subcontract. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

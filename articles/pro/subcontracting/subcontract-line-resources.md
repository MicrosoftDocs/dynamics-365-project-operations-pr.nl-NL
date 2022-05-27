---
title: Resources voor subcontractregels
description: In dit onderwerp wordt uitgelegd hoe u de toegewezen resources opgeeft die door de leverancier worden geleverd voor een specifieke subcontractregel voor tijd.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 96bce2d6797c124331ce0174b16804ff8dfec993
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576080"
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
4. Voer op de pagina **Resource voor nieuwe subcontractregel** de vereiste informatie in en selecteer vervolgens **Opslaan en sluiten**.

In de volgende tabel worden de velden in de resource voor subcontractregels uitgelegd.

| Veld | Beschrijving | Functionele impact |
| ----- | ----------- | ----------------- |
| Boekbare resource | Selecteer een boekbare resource van het type **Contractmedewerker** die u als resource op de subcontractregel wilt gebruiken.| Als u geen boekbare resource voor de contractmedewerker hebt gemaakt, laat u dit veld leeg. Er wordt een boekbare resource gemaakt wanneer u de record opslaat.  |
| Contact | U kunt uw subcontractregelresource maken op basis van een bestaande contactpersoon. Gebruik de zoekfunctie om de lijst met actieve contactpersonen in het systeem te bekijken. Selecteer een contactpersoon voor de leverancier van dit subcontract. Als de contactpersoon die u hebt geselecteerd geen geldige contactpersoon is voor de leverancier in het subcontract, wordt de resourcerecord van de subcontractregel niet opgeslagen.| Als er geen boekbare resource is voor de geselecteerde contactpersoon, wordt door het systeem een boekbare resource gemaakt voor de geselecteerde contactpersoon voordat de subcontractregelresource wordt gemaakt. |
| Gebruiker | U kunt een resource voor een subcontractregel maken door een actieve gebruiker te selecteren. Gebruik de zoekfunctie om de lijst met actieve gebruikers in het systeem te bekijken.| Als er geen boekbare resource is voor de geselecteerde gebruiker, wordt door het systeem een boekbare resource gemaakt voor de geselecteerde gebruiker voordat de subcontractregelresource wordt gemaakt. |
| Begindatum | De datum waarop de toewijzing van de onderaannemer begint.| Als deze resource is geboekt voor een periode die vóór dit datumbereik valt, wordt er een waarschuwing weergegeven. |
| Einddatum | De datum waarop de toewijzing van de onderaannemer eindigt.| Als deze resource is geboekt voor een periode die na dit datumbereik valt, wordt er een waarschuwing weergegeven. |
| Inspanning | Het totale aantal inspanningsuren dat de gecontracteerde werknemer aan deze subcontractregel zal besteden.| Als deze resource wordt geboekt voorbij de inspanning die is toegewezen aan dit subcontract, wordt er een waarschuwing weergegeven. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

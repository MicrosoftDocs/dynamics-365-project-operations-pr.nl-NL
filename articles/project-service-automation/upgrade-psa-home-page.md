---
title: Startpagina upgraden
description: Dit onderwerp laat zien waar u belangrijke informatie vindt over de nieuwe en gewijzigde functies in Dynamics 365 Project Service Automation en het proces voor het upgraden naar de nieuwste versie.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750790"
---
# <a name="upgrade-home-page"></a>Startpagina upgraden

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Upgrade uitvoeren van PSA-versie 2.x of 1.x naar versie 3.x

### <a name="new-instances"></a>Nieuwe exemplaren

Vanaf 17 mei 2019 wordt standaard versie 3.x geïnstalleerd wanneer Project Service Automation is geselecteerd tijdens het inrichten van een nieuw exemplaar.

### <a name="existing-instances"></a>Bestaande exemplaren

Voorheen moesten klanten die een exemplaar van PSA versie 2.x hebben en wilden upgraden naar versie 3.x met de op Unified Client Interface (UCI) gebaseerde versie van PSA, contact opnemen met Microsoft Ondersteuning en de details van hun exemplaar opgeven, zodat de ondersteuning het exemplaar kon upgraden naar versie 3.x. Vanaf 1 maart 2020 kunnen klanten die een exemplaar van PSA versie 2.x hebben en moeten upgraden naar versie 3.x, hun exemplaren rechtstreeks vanuit de beheerportal upgraden zonder contact op te nemen met Microsoft Ondersteuning.  

> [!NOTE]
> PSA versie 3.x bevat belangrijke wijzigingen. Het is gebouwd op de Unified Interface-framework om een verbeterde gebruikerservaring te bieden. Het nieuwe ontwerp van de app levert een consistente, uniforme gebruikersinterface die een responsief ontwerp volgt voor een optimale weergave op elke schermgrootte of elk apparaat. Er zijn ook nog andere wijzigingen doorgevoerd in de toepassing. Er zijn wijzigingen in prijzen, boeken en toewijzen van resources, tijd, onkosten en goedkeuringen.

We adviseren u om de volgende taken te voltooien voordat u begint met het upgradeproces:

- Controleer of zowel Dynamics 365 Field Service als Project Service Automation op het geïdentificeerde exemplaar zijn geïnstalleerd. Als beide oplossingen zijn geïnstalleerd, moet u beide upgraden voordat u het normale gebruik van het exemplaar kunt hervatten.
- Lees de volgende onderwerpen zorgvuldig door. Als u zich bewust bent van en inzicht hebt in de wijzigingen tussen versies, zal dat u helpen bij het upgradeproces. Deze onderwerpen bevatten informatie over de belangrijkste wijzigingen in PSA, samen met overwegingen en aanbevelingen voor het plannen van de upgrade naar versie 3 x.

    - [Wat is er nieuw of gewijzigd in Project Service Automation versie 3](whats-new-changed-v3.md)
    - [Overwegingen voor de upgrade van Project Service Automation versie 2.x of 1.x naar versie 3](upgrade-v3.md)

- Upgrade uw sandbox-exemplaar om de wijzigingen in uw implementatie te evalueren voordat u uw productie-exemplaar bijwerkt.

Nadat u de eerder genoemde onderwerpen hebt bekeken en gereed bent om een upgrade uit te voeren naar PSA versie 3.x of de op UCI gebaseerde versie, dient u een verzoek in bij Microsoft Ondersteuning om de upgrade beschikbaar te maken vanuit Beheercentrum. Geef in uw aanvraag de details van uw exemplaar op.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Oudere versies van PSA (PSA versie 2.x) in een nieuw exemplaar

Vanaf 17 mei 2019 hebben alle nieuwe exemplaren UCI als de standaardclient. Voor de afstemming met deze wijziging worden PSA versie 3.x en Field Service versie 8.x standaard ingericht, omdat deze versies zijn ontworpen om te werken met de UCI-client.

Vanaf 1 maart 2020 kunnen klanten met Dynamics PSA geen nieuwe omgevingen meer maken met oudere versies van PSA, bijvoorbeeld PSA versie 2.x of lager. Elke nieuwe omgeving krijgt alleen versie 3.x van PSA.

> [!NOTE]
> Voor de beste ervaring wanneer u oudere versies van de Field Service- en PSA-toepassingen gebruikt, gaat u naar de pagina **Systeeminstellingen** en selecteert u voor het veld **Alleen de nieuwe Unified Interface gebruiken (aanbevolen)** de optie **Nee** omdat deze versies niet zijn ontworpen om correct te worden geladen in UCI. Nadat u UCI hebt uitgeschakeld, kunt u deze versies van Field Service en PSA openen en uitvoeren met de oude webclient. Zie [Alleen Unified Interface inschakelen](../admin/enable-unified-interface-only.md) voor instructies over het uitschakelen van de UCI-client.

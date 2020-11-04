---
title: Projectgebaseerde verkoopkansregels (Pro)
description: In dit onderwerp krijgt u informatie over projectgebaseerde verkoopkansregels. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074489"
---
# <a name="project-based-opportunity-lines-pro"></a>Projectgebaseerde verkoopkansregels (Pro)

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Projectgebaseerde verkoopkansregels zijn alleen beschikbaar in projectgebaseerde verkoopkansen. Voor projectgebaseerde verkoopkansrecords is het veld **Type** ingesteld op **Werkgebaseerd**.

Projectgebaseerde verkoopkansregels zijn de regelitems die met behulp van een project aan de klant worden geleverd. Een project kan echter niet worden gekoppeld aan een projectgebaseerde verkoopkansregel. Projecten kunnen worden gekoppeld aan regelitems uit de fase **Prijsopgave** en gaan naar de volgende fase omdat de verkoopkans zich doorgaans in een vroeg stadium van de levenscyclus van een deal bevindt. Het bepalen met hoeveel projecten het werk voor de klant wordt opgeleverd, is een beslissing die later in de verkoopfase wordt genomen. U kunt de verkoopkansfase gebruiken om de verschillende leveringscomponenten voor de klant te identificeren. De beslissingen over het werkelijke aantal projecten dat wordt gebruikt om deze componenten te leveren, kunnen vooruit worden geschoven totdat er meer informatie over het werk zelf bekend is.

Hieronder staan de velden op een projectgebaseerde verkoopkansregel:

| **Veld** | **Locatie** | **Relevantie, doel en richtlijnen** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Producttype | Tabblad Algemeen (verborgen) | Selecteer een van de volgende opties:</br>- Projectgebaseerde service (alleen beschikbaar als Dynamics 365 Project Operations is geïnstalleerd)</br>- Product (alleen beschikbaar als Project Operations en Dynamics 365 Sales zijn geïnstalleerd) | De waarde van dit veld is ingesteld op **Projectgebaseerde service** wanneer u een projectgebaseerde verkoopkansregel maakt vanuit het projectgebaseerde regelraster van de verkoopkans. <br> Als u deze waarde wijzigt of overschrijft, wordt de projectfunctionaliteit niet ingeschakeld voor uw projectgebaseerde regelitems. |
| Kans | Tabblad Algemeen | Dit veld is alleen-lezen en verwijst naar de bovenliggende verkoopkansrecord waartoe dit regelitem behoort. | Er is geen downstreamimpact van dit veld. |
| Meetcriterium | Tabblad Algemeen | Dit bewerkbare tekstveld kan worden gebruikt om een korte identiteit aan het regelitem te geven. | Deze waarde wordt overgedragen naar de prijsopgaveregel wanneer u een prijsopgave maakt vanuit deze verkoopkans. |
| Klantbudget | Tabblad Algemeen | Dit bewerkbare valutaveld kan worden gebruikt om het bedrag bij te houden dat de klant bereid is te besteden voor dit regelitem. | Deze waarde wordt overgedragen naar het bijbehorende veld op de prijsopgaveregel wanneer u een prijsopgave maakt vanuit deze verkoopkans. |
| Factureringsmethode | Tabblad Algemeen | Dit bewerkbare veld kan de volgende waarden hebben:</br>- Tijd en materiaal</br>- Vaste prijs | Deze waarde wordt overgedragen naar het bijbehorende veld op de prijsopgaveregel wanneer u een prijsopgave maakt vanuit deze verkoopkans. Nadat de prijsopgaveregel is gemaakt, is het veld vergrendeld en kan het niet worden gewijzigd. Wijs deze veldwaarde zo nauwkeurig mogelijk toe. Als u de waarde van dit veld op de prijsopgaveregel moet wijzigen, verwijdert u de prijsopgaveregel en maakt u deze opnieuw. |

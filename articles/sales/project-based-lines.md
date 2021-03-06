---
title: Projectgebaseerde verkoopkansregels
description: In dit onderwerp krijgt u informatie over het werken met projectgebaseerde verkoopkansregels.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b255d607ac8180c249a9b9831db6f8d0cd3937b
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898390"
---
# <a name="project-based-opportunity-lines"></a>Projectgebaseerde verkoopkansregels

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_


Projectgebaseerde verkoopkansregels zijn alleen beschikbaar in projectgebaseerde verkoopkansen. Voor projectgebaseerde verkoopkansrecords is het veld **Type** ingesteld op **Werkgebaseerd**.

Projectgebaseerde verkoopkansregels zijn de regelitems die met behulp van een project aan de klant worden geleverd. Een project kan echter niet worden gekoppeld aan een projectgebaseerde verkoopkansregel. Projecten kunnen worden gekoppeld aan regelitems uit de fase **Prijsopgave** en verder omdat de verkoopkans zich doorgaans in een vroeg stadium van een deal bevindt. Het bepalen met hoeveel projecten het werk voor de klant wordt opgeleverd, is een beslissing die later in de verkoopfase wordt genomen. Gebruik de verkoopkansfase om de verschillende leveringscomponenten voor de klant te identificeren. De beslissingen over het werkelijke aantal projecten dat wordt gebruikt om deze componenten te leveren, kunnen vooruit worden geschoven totdat er meer informatie over het werk zelf bekend is.

Hieronder staan de velden op een projectgebaseerde verkoopkansregel:

| **Veld** | **Locatie** | **Relevantie, doel en richtlijnen** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Producttype | Tabblad Algemeen (verborgen) | Dit is een veld uit de optieset. Als Dynamics 365 Project Operations is geïnstalleerd, is **Projectgebaseerde service** een van de beschikbare opties.  | De waarde van dit veld is ingesteld op **Projectgebaseerde service** wanneer u de projectgebaseerde verkoopkansregel maakt vanuit het projectgebaseerde regelraster van de verkoopkans. <br> Als u deze waarde wijzigt of overschrijft, wordt de projectfunctionaliteit niet ingeschakeld voor uw projectgebaseerde regelitems. |
| Kans | Tabblad Algemeen | Dit veld is alleen-lezen en verwijst naar de bovenliggende verkoopkansrecord waartoe dit regelitem behoort. | Er is geen downstreamimpact van dit veld. |
| Meetcriterium | Tabblad Algemeen | Dit is een bewerkbaar tekstveld dat kan worden gebruikt om een korte identiteit aan dit regelitem te geven. | Deze waarde wordt overgedragen naar de prijsopgaveregel wanneer u een prijsopgave maakt vanuit deze verkoopkans |
| Klantbudget | Tabblad Algemeen | Dit bewerkbare valutaveld kan worden gebruikt om het bedrag bij te houden dat de klant bereid is te besteden voor dit regelitem. | Deze waarde wordt overgedragen naar het bijbehorende veld op de prijsopgaveregel wanneer u een prijsopgave maakt vanuit deze verkoopkans |
| Factureringsmethode | Tabblad Algemeen | Dit bewerkbare veld kan de volgende waarden hebben:</br>- Tijd en materiaal</br>- Vaste prijs | Deze waarde wordt overgedragen naar het bijbehorende veld op de prijsopgaveregel wanneer u een prijsopgave maakt vanuit deze verkoopkans. Nadat de prijsopgaveregel is gemaakt, is het veld vergrendeld en kan het niet worden gewijzigd. Wijs deze veldwaarde zo nauwkeurig mogelijk toe. Als u de waarde van dit veld op de prijsopgaveregel moet wijzigen, verwijdert u de prijsopgaveregel en maakt u deze opnieuw. |

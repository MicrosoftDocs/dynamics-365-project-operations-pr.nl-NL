---
title: Projecten met omzetschattingen met een vaste prijs
description: Dit onderwerp bevat informatie over opbrengsten met een vaste prijs in projecten.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531402"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projecten met omzetschattingen met een vaste prijs 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Wanneer u een projectcontractregel maakt met de volgende kenmerken in Dynamics 365 Project Operations voor Microsoft Dataverse, maakt het systeem automatisch een project met een geschatte omzet met een vaste prijs. De gegevens in dit project worden gebaseerd op het volgende:

  - Een factureringsmethode met een vaste prijs.
  - Een gekoppeld project.
  - Er is minstens één mijlpaal gedefinieerd op het tabblad **Factuurschema** op de pagina **Projectcontractregel**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Projecten met omzetschattingen met een vaste prijs beoordelen
Voer de volgende stappen uit om projecten met een geschatte omzet met een vaste prijs te bekijken:

1. Ga in de Dynamics 365 Finance-omgeving naar **Projectbeheer en boekhouding** > **Projecten** > **Projecten met omzetschattingen met een vaste prijs**.
2. Selecteer het project dat u wilt bekijken en dubbelklik op de **Schattingsproject-id** om de record te openen en de details van het project te bekijken.
3. Vouw het tabblad **Project** uit. U ziet één project in het raster **Geselecteerde projecten**. Het systeem gebruikt dit als standaardproject omdat dit het project is dat is gekoppeld aan de projectcontractregel. 
4. Als u de koppeling wilt wijzigen, selecteert u aanvullende projecten en voegt u ze toe aan het raster **Geselecteerde projecten**. Als er meerdere projecten zijn geselecteerd in dit raster, worden het projectpercentage van voltooiing en omzetramingen samen berekend voor alle geselecteerde projecten.

  Projectkosten, inkomstenprofiel, kostensjabloon en de periodecode kunnen handmatig worden ingesteld. Als ze niet handmatig worden ingesteld, worden de standaardwaarden gebruikt van de eerste schattingsberekening voor het project met behulp van de regels die zijn geconfigureerd voor projectkosten- en opbrengstprofielen.


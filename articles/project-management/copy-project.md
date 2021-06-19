---
title: Een project kopiëren
description: In dit onderwerp krijgt u informatie over het kopiëren van projecten in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091248"
---
# <a name="copy-a-project"></a>Een project kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met Dynamics 365 Project Operations kunt u snel nieuwe projecten bouwen door **Project kopiëren** te selecteren op het formulier **Projecten**. Als u een project wilt kopiëren, opent u het project dat u wilt kopiëren en selecteert u vervolgens **Project kopiëren**. Met de actie wordt het volgende gekopieerd:

- Projecteigenschappen 
- Structuur voor werkspecificatie
- Projectteamleden
- Projectschattingen
- Projectonkostenschattingen
- Materiaalschattingen project

## <a name="project-properties"></a>Projecteigenschappen

Wanneer het project wordt gekopieerd, worden de waarden in de volgende velden gekopieerd:

- Meetcriterium
- Beschrijving
- Klant
- Agendasjabloon
- Valuta
- Contracterende eenheid
- Projectmanager
- Status
- Algehele projectstatus
- Opmerkingen 
- Schattingen
- Geschatte begindatum: dit is de datum waarop het project op basis van de kopie is gemaakt.
- Geschatte einddatum: deze datum wordt aangepast op basis van de begindatum van het nieuwe project dat op basis van de kopie is gemaakt.
- Inspanning (uren)
- Geschatte arbeidskosten
- Geschatte onkosten
- Geschatte materiaalkosten

> [!NOTE]
> Het kopiëren van het project is een langdurige operatie. Projectrecords, de bijbehorende relevante kenmerken en veel gerelateerde entiteiten worden ook gekopieerd. Vanwege de langdurige aard van de bewerking, wordt de doelprojectpagina, nadat het kopiëren is gestart, vergrendeld voor bewerking totdat de kopieerbewerking is voltooid.

## <a name="work-breakdown-structure"></a>Structuur voor werkspecificatie

Wanneer het project wordt gekopieerd, wordt de volledige voor de resource geladen structuur voor werkspecificatie gekopieerd. Benoemde resources worden vervangen door algemene resource. Als de benoemde resources niet dezelfde werkuren heeft als de algemene resource, wordt de planning opnieuw berekend en kan de duur van de taak veranderen.

## <a name="project-team-members"></a>Projectteamleden

Wanneer een projectteam wordt gekopieerd uit het bronproject, worden de algemene resources gekopieerd. Algemene resourcetoewijzingen worden ook onderhouden, net zoals in het bronproject. Benoemde resources worden omgezet in algemene teamleden.

## <a name="estimates"></a>Schattingen

Wanneer het project wordt gekopieerd, worden resource-, onkosten- en materiaalramingsregels gekopieerd uit het bronproject. 

Zie voor informatie over het programmatisch openen van Project kopiëren [Projectsjablonen ontwikkelen met Project kopiëren](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]

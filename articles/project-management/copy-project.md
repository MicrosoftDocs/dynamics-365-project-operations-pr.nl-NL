---
title: Een project kopiëren
description: Dit onderwerp biedt informatie over het kopiëren van projecten in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074505"
---
# <a name="copy-a-project"></a>Een project kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met Dynamics 365 Project Operations kunt u snel nieuwe projecten maken door **Project kopiëren** in het formulier **Projecten** te selecteren. Als u een project wilt kopiëren, opent u het project dat u wilt kopiëren en selecteert u vervolgens **Project kopiëren**. Met de actie kopieert u het volgende:

- Projecteigenschappen
- De structuur voor werkspecificatie
- Projectteamleden
- Projectschattingen
- Projectonkostenschattingen

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
- Geschatte begindatum
- Einddatum
- Inspanning (uren)
- Geschatte arbeidskosten
- Geschatte onkosten

## <a name="work-breakdown-structure"></a>Structuur voor werkspecificatie

Wanneer het project wordt gekopieerd, wordt de volledige voor de resource geladen structuur voor werkspecificatie gekopieerd. Benoemde resources worden vervangen door algemene resource. Als de benoemde resources niet dezelfde werkuren heeft als de algemene resource, wordt de planning opnieuw berekend en kan de duur van de taak veranderen.

## <a name="project-team-members"></a>Projectteamleden

Wanneer een projectteam wordt gekopieerd uit het bronproject, worden de algemene resources gekopieerd. Algemene resourcetoewijzingen worden ook onderhouden, net zoals in het bronproject. Benoemde resources worden omgezet in algemene teamleden.

## <a name="estimates"></a>Schattingen

Wanneer het project wordt gekopieerd, worden zowel resource- als kostenramingsregels uit het bronproject gekopieerd. 

Zie voor informatie over het programmatisch openen van Project kopiëren [Projectsjablonen ontwikkelen met Project kopiëren](dev-copy-project.md).

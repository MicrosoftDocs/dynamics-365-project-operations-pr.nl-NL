---
title: Een project kopiëren
description: Dit onderwerp biedt informatie over het kopiëren van projecten in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908033"
---
# <a name="copy-a-project"></a>Een project kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met Dynamics 365 Project Operations kunt u snel nieuwe projecten bouwen met behulp van de actie **Project kopiëren** in het formulier **Projecten**. Als u een project wilt kopiëren, selecteert u een project en vervolgens **Kopiëren**. Met de actie kopieert u het volgende:

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
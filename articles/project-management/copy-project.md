---
title: Een project kopiëren
description: Dit artikel biedt informatie over het kopiëren van projecten in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925758"
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
- Projectchecklijsten
- Projectbuckets

## <a name="project-properties"></a>Projecteigenschappen

Wanneer het project wordt gekopieerd, worden de waarden in de volgende velden gekopieerd.

| Veld | Niet-voorradige materialen voor Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Beschrijving | :heavy_check_mark: | :heavy_check_mark: | |
| klant | :heavy_check_mark: | :heavy_check_mark: | |
| Agendasjabloon | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuta | :heavy_check_mark: | :heavy_check_mark: | |
| Contracterende eenheid | :heavy_check_mark: | :heavy_check_mark: | |
| Bedrijf dat eigenaar is | :heavy_check_mark: | | |
| Projectmanager | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| -Status | :heavy_check_mark: | :heavy_check_mark: | |
| Algehele projectstatus | :heavy_check_mark: | :heavy_check_mark: | |
| Opmerkingen  | :heavy_check_mark: | :heavy_check_mark: | |
| Schattingen | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Geschatte begindatum</p><p><strong>Opmerking:</strong> in dit veld wordt de datum gespecificeerd waarop het project is gemaakt op basis van de kopie. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Geschatte voltooiingsdatum</p><p><strong>Opmerking:</strong> de datum in dit veld wordt aangepast op basis van de begindatum van het nieuwe project dat op basis van de kopie is gemaakt.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Inspanning (uren) | :heavy_check_mark: | :heavy_check_mark: | |
| Geschatte arbeidskosten | :heavy_check_mark: | :heavy_check_mark: | |
| Geschatte onkosten | :heavy_check_mark: | :heavy_check_mark: | |
| Geschatte materiaalkosten | | :heavy_check_mark: | |

> [!NOTE]
> Het kopiëren van het project is een langdurige operatie. Projectrecords, de bijbehorende relevante kenmerken en veel gerelateerde entiteiten worden ook gekopieerd. Vanwege de langdurige aard van de bewerking, wordt de doelprojectpagina, nadat het kopiëren is gestart, vergrendeld voor bewerking totdat de kopieerbewerking is voltooid.

## <a name="work-breakdown-structure"></a>Structuur voor werkspecificatie

Wanneer het project wordt gekopieerd, wordt de volledige voor de resource geladen structuur voor werkspecificatie gekopieerd. Benoemde resources worden vervangen door algemene resource. Als de benoemde resources niet dezelfde werkuren hebben als de generieke resource, wordt de planning opnieuw berekend en kan de duur van taken veranderen.

## <a name="project-team-members"></a>Projectteamleden

Wanneer een projectteam wordt gekopieerd uit het bronproject, worden de algemene resources gekopieerd. Algemene resourcetoewijzingen worden ook onderhouden, net zoals in het bronproject. Benoemde resources worden omgezet in algemene teamleden.

> [!NOTE]
> Teamleden en opdrachten worden niet gekopieerd in Project for the Web.

## <a name="estimates"></a>Schattingen

Wanneer het project wordt gekopieerd, worden resource-, onkosten- en materiaalramingsregels gekopieerd uit het bronproject. 

Zie voor informatie over het programmatisch openen van Project kopiëren [Projectsjablonen ontwikkelen met Project kopiëren](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Prijsopgaven en contracten

Prijsopgaven en contracten zijn niet gekoppeld aan het bestemmingsproject.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

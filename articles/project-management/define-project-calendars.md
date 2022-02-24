---
title: Projectkalenders definiëren
description: Dit onderwerp biedt informatie over hoe u een agendasjabloon op een project kunt toepassen om de projectplanning bij te houden.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981294"
---
# <a name="define-project-calendars"></a>Projectkalenders definiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Als u een project wilt maken en beheren, moet u een agendasjabloon op het project toepassen. De agendasjabloon definieert de volgende projectkenmerken:

- Werkuren, inclusief begin- en eindtijd
- Werkdagen
- Agenda-uitzonderingen zoals niet-werkdagen

De agendasjabloon die op een project wordt toegepast, is een kopie van de agendasjabloon die is gedefinieerd in de instellingen van uw organisatie.

> [!NOTE]
> Als u de agendasjabloon wijzigt, worden die wijzigingen niet doorgevoerd in de werktijden van het project. Als u de werktijden van het project wilt wijzigen, moet een nieuwe sjabloon worden toegepast.

Als u een agendasjabloon voor uw organisatie wilt maken, zijn er twee belangrijke vereisten:

- Definieer de gewenste werkuren van de sjabloon met behulp van een nieuwe of bestaande boekbare resource.
- Maak een nieuwe agendasjabloon en koppel de sjabloon aan de boekbare resource.

**De werkuren van de sjabloon definiëren**

1. Ga naar **Resources** \> **Resources**.
2. Maak een nieuwe resource om naar te verwijzen in de agendasjabloon of selecteer een bestaande resource.
3. Selecteer het tabblad **Werkuren** van de resource en voer de instructies uit in [Werkuren instellen voor een resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) om de agendaregels te configureren.

**Een nieuwe agendasjabloon maken**

1. Ga naar **Instellingen** \> **Agendasjabloon**.
2. Selecteer **Nieuw** en voer een naam, beschrijving en sjabloonresource in.

> [!NOTE]
> Wanneer in een agendasjabloon naar een resource wordt verwezen, wordt een kopie van de agenda van de resource aan de agendasjabloon gekoppeld. Als de werkuren van de gekopieerde sjabloon veranderen, worden die wijzigingen niet doorgevoerd in de agendasjabloon.

U kunt nu de werksjabloon aan een sjabloon voor een projectkalender koppelen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]


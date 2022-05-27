---
title: Projectkalenders definiëren
description: Dit onderwerp biedt informatie over hoe u een agendasjabloon op een project kunt toepassen om de projectplanning bij te houden.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e31fcaf039ae214394b08b60b5d41987dc648e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578932"
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
3. Selecteer het tabblad **Werkuren** van de resource en voer de instructies uit in [Werkuren instellen voor een resource](/dynamics365/field-service/set-work-hours-resource) om de agendaregels te configureren.

**Een nieuwe agendasjabloon maken**

1. Ga naar **Instellingen** \> **Agendasjabloon**.
2. Selecteer **Nieuw** en voer een naam, beschrijving en sjabloonresource in.

> [!NOTE]
> Wanneer in een agendasjabloon naar een resource wordt verwezen, wordt een kopie van de agenda van de resource aan de agendasjabloon gekoppeld. Als de werkuren van de gekopieerde sjabloon veranderen, worden die wijzigingen niet doorgevoerd in de agendasjabloon.

U kunt nu de werksjabloon aan een sjabloon voor een projectkalender koppelen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]


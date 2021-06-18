---
title: Integratie van twee keer wegschrijven in Project Operations
description: Dit onderwerp geeft een overzicht van integratie van twee keer wegschrijven in Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998675"
---
# <a name="project-operations-dual-write-integration-overview"></a>Overzicht van integratie van twee keer wegschrijven in Project Operations

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Project Operations gebruikt [mogelijkheden voor twee keer wegschrijven](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) om gegevens te synchroniseren tussen Microsoft Dataverse en Dynamics 365 Finance.

De volgende afbeelding laat zien hoe gegevens worden gesynchroniseerd als onderdeel van deze integratie tussen Dataverse en Finance.

![Overzicht van gegevensstromen in Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations in Dataverse biedt een moderne gebruikersinterface (UI) en eenvoudige uitbreidbaarheid zonder code/met weinig code met behulp van Power Platform-mogelijkheden. Projectmanagers, resourcemanagers, projectteamleden en andere frontoffice-persona's voeren hun activiteiten uit in Project Operations op Dataverse.

Project Operations in Finance biedt ondersteuning voor projectadministratie en opbrengstentoerekening. Project Operations wordt aangesloten op het financiële raamwerk in Finance voor het berekenen van omzetbelasting, valutakoersen, rapportage van financiële dimensies en meer. De ervaringen van de projectaccountant zijn voornamelijk gebaseerd op Finance.

Project Operations-integratie bestaat uit de volgende onderdeelintegratie:


- [Integratie van instellings- en configuratiegegevens in Project Operations](resource-dual-write-setup-integration.md) 
- [Projectschattingen en werkelijke waarden](resource-dual-write-estimates-actuals.md)
- [Projectfacturen](resource-dual-write-project-invoice.md)
- [Onkostenbeheer](resource-dual-write-expense.md)
- [Leveranciersfactuur](resource-dual-write-vendor-invoice.md)

---
title: Belangrijke concepten bij onderaanneming
description: In dit artikel worden enkele belangrijke concepten uitgelegd die van toepassing zijn op onderaanneming in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e75f2cf9c1092604e43e5cb60dda0e2a1b7dcd64
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262163"
---
# <a name="key-concepts-in-subcontracting"></a>Belangrijke concepten bij onderaanneming


_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In het artikel worden enkele belangrijke concepten uitgelegd waarvan u op de hoogte moet zijn voordat u de functionaliteit voor onderaanneming gaat gebruiken in Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Contracterende eenheid op het subcontract

De contracterende eenheid vertegenwoordigt de afdeling of praktijk die eigenaar is van de oplevering van het uiteindelijke project. De contracterende eenheid is ook de afdeling die de contractrelatie met de verkoper aangaat.

## <a name="purchase-currency"></a>Aankoopvaluta

In Project Operations is de aankoopvaluta de valuta waarin het subcontract is opgesteld. Het is ook de valuta waarin de kosten van onderaannemers voor een project worden vastgelegd. De aankoopvaluta kan verschillen van de projectvaluta en de projectvaluta kan op zijn beurt verschillen van de verkoopvaluta.

## <a name="billing-methods-on-subcontract-lines"></a>Factureringsmethoden op subcontractregels

Voor projecten zijn er doorgaans contractmodellen op basis van vaste vergoedingen en verbruik. Project Operations ondersteunt deze factureringsmethoden in de verkoop- en aankoopcontext. Voor een aankoop werken de factureringsmethoden op de volgende manier:

- **Tijd en materiaal**: wanneer een subcontractregel gebruikmaakt van de factureringsmethode **Tijd en materiaal**, worden de tijdskosten voor het project geregistreerd terwijl onderaannemers aan dat project werken en tijd registreren. Deze kostentransacties van onderaannemers worden vervolgens vergeleken met de regelitems op leveranciersfacturen. In dit model kunnen projectmanagers die Project Operations gebruiken, leveranciersfactuurregels afstemmen en verifiëren met de tijd van onderaannemers die is vastgelegd en goedgekeurd. Nadat de verificatie is voltooid, worden eerdere werkelijke kosten die zijn vastgelegd na goedkeuring, teruggedraaid en worden nieuwe werkelijke kosten gemaakt op basis van de leveranciersfactuur voor het project.
- **Vaste prijs**: in dit contractmodel met vaste vergoedingen zijn leveranciersfacturen gebaseerd op vaste mijlpalen. Resources van onderaannemers kunnen echter ook tijd rapporteren. De tijd wordt vervolgens beoordeeld en goedgekeurd door de projectmanager. Na goedkeuring worden in Project Operations tijdelijke werkelijke kosten voor het project vastgelegd. Nadat de leverancier een factuur voor een mijlpaal heeft verzonden, kan de projectmanager eerder geregistreerde werkelijke kosten vergelijken met de mijlpaal. Wanneer de verificatie is voltooid, worden de werkelijke kosten teruggeboekt en worden de op mijlpalen gebaseerde kosten geregistreerd.

## <a name="project-price-lists-on-subcontracts"></a>Projectprijslijsten bij subcontracten

Projectprijslijsten zijn prijslijsten die worden gebruikt om aankoopprijzen in te stellen voor tijd, onkosten en andere projectgerelateerde onderdelen. Er kunnen meerdere prijslijsten zijn, die elk hun eigen subcontract met ingangsdatum kunnen hebben in Project Operations. Project Operations ondersteunt geen overlappende ingangsdatums op projectprijslijsten voor een subcontract.

## <a name="transaction-classes-on-subcontracts"></a>Transactieklassen bij subcontracten

Project Operations ondersteunt vier soorten transactieklassen:

- Tijd
- Onkosten
- Materiaal
- Tarief

Aankoopkosten kunnen alleen worden geschat en gemaakt voor transactieklassen **Tijd**, **Kosten** en **Materiaal**. **Tarief** is een transactieklasse met alleen inkomsten en is niet beschikbaar in de inhoud van de aankoop.

## <a name="purchase-pricing-dimensions"></a>Dimensies voor aankoopprijzen

Met prijsdimensies kunt u bepalen welke kenmerken worden gebruikt voor het instellen van aankoopprijzen en standaardtransacties op tijd. Met betrekking tot aankoop ondersteunt Project Operations alleen sets met vaste dimensies voor het instellen van aankoopprijzen en standaardinstellingen. Voor het instellen van aankoopprijzen en het in gebreke blijven van subcontractregels en -tijdtransacties, zijn de kenmerken **Rol** en **Boekbare resource**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

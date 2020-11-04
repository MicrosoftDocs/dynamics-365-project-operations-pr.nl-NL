---
title: Toerekenbare onderdelen van een projectgebaseerde contractregel configureren
description: Dit onderwerp bevat informatie over opgenomen, toerekenbare en niet-toerekenbare onderdelen op contractregels.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074501"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Toerekenbare onderdelen van een projectgebaseerde contractregel configureren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Een projectgebaseerde contractregel heeft het concept van opgenomen, toerekenbare en niet-toerekenbare onderdelen.

Op opgenomen onderdelen is het volgende van toepassing: de factureringsmethode, klantsplitsingen, niet te overschrijden limieten en factuurfrequentie-instellingen die zijn gedefinieerd op de projectgebaseerde contractregel.

Een subset van de opgenomen onderdelen kan worden gemarkeerd als toerekenbaar door het veld **Factureringstype** bij te werken.

Toerekenbare onderdelen kunnen worden gedefinieerd voor rollen en transactiecategorieën.

Voor de contractregel van een project is de toerekenbaarheid die is gedefinieerd voor een rol alleen van toepassing op de transactieklasse **Tijd**. Als het veld **Tijd opnemen** is ingesteld op **Nee** op een contractregel van een project, is het tabblad **Toerekenbare rollen** niet beschikbaar.

Toerekenbaarheid die is gedefinieerd voor transactiecategorieën voor een projectcontractregel is alleen van toepassing op de transactieklasse **Onkosten**. Als het veld **Onkosten opnemen** is ingesteld op **Nee** op een contractregel van een project, is het tabblad **Toerekenbare categorieën** niet beschikbaar.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Een rol bijwerken als toerekenbaar of niet-toerekenbaar

Een rol kan toerekenbaar of niet-toerekenbaar op een specifieke projectgebaseerde contractregel zijn.

Werk het factureringstype voor een rol bij op het tabblad **Toerekenbare rollen** van een projectgebaseerde contractregel in het subraster **Toerekenbare categorieën** in het veld **Factureringstype**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar

Een transactiecategorie kan toerekenbaar of niet-toerekenbaar zijn op een specifieke projectgebaseerde contractregel.

Werk het factureringstype voor een transactie bij op het tabblad **Toerekenbare categorieën** van een projectgebaseerde contractregel in het subraster **Toerekenbare categorieën** in het veld **Factureringstype**.

### <a name="resolve-chargeability"></a>Toerekenbaarheid oplossen

Een schatting of een werkelijke waarde die is gemaakt voor tijd, wordt alleen als toerekenbaar beschouwd als tijd is opgenomen op de contractregel, en als de rol is geconfigureerd als toerekenbaar op de contractregel.

Een schatting of een werkelijke waarde die is gemaakt voor onkosten, wordt alleen als toerekenbaar beschouwd als onkosten is opgenomen op de contractregel, en als de transactiecategorieën is geconfigureerd als toerekenbaar op de contractregel.

| Bevat tijd | Bevat onkosten | - Rol | Categorie | Opdracht |
| --- | --- | --- | --- | --- |
| Ja | Ja | Toerekenbaar | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Toerekenbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Toerekenbaar |
| Ja | Ja | Niet-toerekenbaar | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Toerekenbaar |
| Ja | Ja | Niet-toerekenbaar | Niet-toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Niet-toerekenbaar |
| Geen | Ja | Kan niet worden ingesteld | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet beschikbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Toerekenbaar |
| Geen | Ja | Kan niet worden ingesteld | Niet-toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet beschikbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Niet-toerekenbaar |
| Ja | Geen | Toerekenbaar | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Toerekenbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Niet beschikbaar |
| Ja | Geen | Niet-toerekenbaar | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar </br> Factureringstype voor een werkelijke waarde van onkosten: Niet beschikbaar |

---
title: Toerekenbare componenten van een projectgebaseerde contractregel configureren - lite
description: Dit onderwerp bevat informatie over het toevoegen van niet-toerekenbare onderdelen aan contractregels in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513873"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Toerekenbare componenten van een projectgebaseerde contractregel configureren - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een projectgebaseerde contractregel heeft *opgenomen* onderdelen en *toerekenbare* onderdelen.

Opgenomen onderdelen zijn onderdelen waarop het volgende van toepassing is:

  - Factureringsmethode en klantsplitsingen
  - Niet-overschrijdingslimieten 
  - Factuurfrequentie-instellingen die zijn gedefinieerd op de projectgebaseerde contractregel

Een subset van de opgenomen onderdelen kan worden gemarkeerd als toerekenbaar met het veld **Factureringstype**. Het veld **Factureringstype** is een optieset die de volgende waarden toestaat in de context van een contractregel:

  - Toerekenbaar
  - Niet-toerekenbaar

Toerekenbare onderdelen kunnen worden gedefinieerd voor taken, rollen en transactiecategorieën.

Toerekenbaarheid wordt gedefinieerd voor taken van een projectcontractregel en is van toepassing op alle transactieklassen die op de regel zijn opgenomen. Als het veld **Taken opnemen** op een contractregel leeg is of is ingesteld op **Geheel project**, is het tabblad **Toerekenbare taken** niet beschikbaar.

Toerekenbaarheid die is gedefinieerd voor rollen voor een projectcontractregel is alleen van toepassing op de transactieklasse **Tijd**. Als het veld **Tijd opnemen** op een contractregel is ingesteld op **Nee**, is het tabblad **Toerekenbare rollen** niet beschikbaar.

Toerekenbaarheid die is gedefinieerd voor transactiecategorieën voor een projectcontractregel is alleen van toepassing op de transactieklasse **Onkosten**. Als het veld **Onkosten opnemen** is ingesteld op **Nee**, is het tabblad **Toerekenbare categorieën** niet beschikbaar.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Een projecttaak bijwerken als toerekenbaar of niet-toerekenbaar

Een projecttaak kan op een specifieke contractregel toerekenbaar of niet-toerekenbaar zijn, waardoor de volgende instellingen mogelijk zijn:

Als een projectgebaseerde contractregel **Tijd** bevat en een bepaalde taak, **T1**, ermee is verbonden als toerekenbaar. Als er een tweede contractregel is die **Onkosten** bevat, kunt u de T1-taak op de contractregel als niet-toerekenbaar koppelen. Het resultaat is dat alle tijd die voor de taak is geregistreerd, toerekenbaar is en dat alle onkosten niet-toerekenbaar zijn.

Het factureringstype van een taak kan worden geconfigureerd op het tabblad **Toerekenbare taken** van de contractregel door het veld **Factureringstype** op het takensubraster van de contractregel bij te werken. U kunt ook het veld **Factureringstype** op het subraster Factureringsinstellingen van de projecttaak bijwerken dat de contractregels toont die aan een taak zijn gekoppeld.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Een rol bijwerken als toerekenbaar of niet-toerekenbaar

Een rol kan toerekenbaar of niet-toerekenbaar op een specifieke contractregel zijn.

Het factureringstype van een rol kan worden geconfigureerd op het tabblad **Toerekenbare rollen** van een contractregel. Werk hiervoor het veld **Factureringstype** bij in het subraster **Toerekenbare rollen**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar

Een transactiecategorie kan toerekenbaar of niet-toerekenbaar zijn op een specifieke contractregel.

Het factureringstype van een transactiecategorie kan worden geconfigureerd op het tabblad **Toerekenbare categorieën** van een projectgebaseerde contractregel. Werk hiervoor het veld **Factureringstype** bij in het subraster **Toerekenbare categorieën**.

### <a name="resolve-chargeability"></a>Toerekenbaarheid oplossen

Een schatting of een werkelijke waarde die is gemaakt voor tijd, wordt alleen als toerekenbaar beschouwd als **Tijd** is opgenomen op de contractregel, en als **Taak** en **Rol** zijn geconfigureerd als toerekenbaar op de contractregel.

Een schatting of een werkelijke waarde die is gemaakt voor onkosten, wordt alleen als toerekenbaar beschouwd als **Onkosten** is opgenomen op de contractregel, en als de categorieën **Taak** en **Transactie** zijn geconfigureerd als toerekenbaar op de contractregel.


| Bevat Tijd | Bevat Onkosten | Bevat Taken | - Rol           | Categorie       | Opdracht                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ja           | Ja              | Geheel project | Toerekenbaar     | Toerekenbaar     | Facturering voor een werkelijke waarde van Tijd: **Toerekenbaar** </br> Factureringstype voor een werkelijke waarde van Onkosten: **Toerekenbaar**           |
| Ja           | Ja              | Geselecteerde taken | Toerekenbaar     | Toerekenbaar     | Facturering voor een werkelijke waarde van Tijd: **Toerekenbaar** </br> Factureringstype voor een werkelijke waarde van Onkosten: **Toerekenbaar**           |
| Ja           | Ja              | Geselecteerde taken | Niet-toerekenbaar | Toerekenbaar     | Facturering voor een werkelijke waarde van Tijd: **Niet-toerekenbaar** </br> Factureringstype voor een werkelijke waarde van Onkosten: **Toerekenbaar**       |
| Ja           | Ja              | Geselecteerde taken | Toerekenbaar     | Toerekenbaar     | Facturering voor een werkelijke waarde van Tijd: **Niet-toerekenbaar** </br> Factureringstype voor een werkelijke waarde van Onkosten: **Niet-toerekenbaar** |
| Ja           | Ja              | Geselecteerde taken | Niet-toerekenbaar | Toerekenbaar     | Facturering voor een werkelijke waarde van Tijd: **Niet-toerekenbaar** </br> Factureringstype voor een werkelijke waarde van Onkosten: **Niet-toerekenbaar** |
| Ja           | Ja              | Geselecteerde taken | Niet-toerekenbaar | Niet-toerekenbaar | Facturering voor een werkelijke waarde van Tijd: **Niet-toerekenbaar** </br> Factureringstype voor een werkelijke waarde van Onkosten: **Niet-toerekenbaar** |
| Geen            | Ja              | Geheel project | Kan niet worden ingesteld   | Toerekenbaar     | Facturering voor een werkelijke waarde van Tijd: **Niet beschikbaar**</br>Factureringstype voor een werkelijke waarde van Onkosten: **Toerekenbaar**          |
| Geen            | Ja              | Geheel project | Kan niet worden ingesteld   | Niet-toerekenbaar | Facturering voor een werkelijke waarde van Tijd: **Niet beschikbaar**</br> Factureringstype voor een werkelijke waarde van Onkosten: **Niet-toerekenbaar**     |
| Ja           | Geen               | Geheel project | Toerekenbaar     | Kan niet worden ingesteld   | Facturering voor een werkelijke waarde van Tijd: **Toerekenbaar** </br> Factureringstype voor een werkelijke waarde van Onkosten: **Niet beschikbaar**        |
| Ja           | Geen               | Geheel project | Niet-toerekenbaar | Kan niet worden ingesteld   | Facturering voor een werkelijke waarde van Tijd: **Niet-toerekenbaar** </br>Factureringstype voor een werkelijke waarde van Onkosten: **Niet beschikbaar**   |

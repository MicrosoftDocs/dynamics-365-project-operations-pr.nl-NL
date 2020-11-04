---
title: Niet-toerekenbare onderdelen van een projectgebaseerde contractregel configureren
description: Dit onderwerp bevat informatie over het toevoegen van niet-toerekenbare onderdelen aan contractregels in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d665a6351d2315d185e64e4eb6b0b8859f7bbc4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074471"
---
# <a name="configuring-chargeable-components-of-a-project-based-contract-line"></a>Niet-toerekenbare onderdelen van een projectgebaseerde contractregel configureren

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

Toerekenbaarheid wordt gedefinieerd voor taken van een projectcontractregel en is van toepassing op alle transactieklassen die op de regel zijn opgenomen. Als het veld **Taken opnemen** op een contractregel leeg is of is ingesteld op **Geheel project** , is het tabblad **Toerekenbare taken** niet beschikbaar.

Toerekenbaarheid die is gedefinieerd voor rollen voor een projectcontractregel is alleen van toepassing op de transactieklasse **Tijd**. Als het veld **Tijd opnemen** op een contractregel is ingesteld op **Nee** , is het tabblad **Toerekenbare rollen** niet beschikbaar.

Toerekenbaarheid die is gedefinieerd voor transactiecategorieën voor een projectcontractregel is alleen van toepassing op de transactieklasse **Onkosten**. Als het veld **Onkosten opnemen** is ingesteld op **Nee** , is het tabblad **Toerekenbare categorieën** niet beschikbaar.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Een projecttaak bijwerken als toerekenbaar of niet-toerekenbaar

Een projecttaak kan op een specifieke contractregel toerekenbaar of niet-toerekenbaar zijn, waardoor de volgende instellingen mogelijk zijn:

Als een projectgebaseerde contractregel **Tijd** bevat en een bepaalde taak, **T1** , ermee is verbonden als toerekenbaar. Als er een tweede contractregel is die **Onkosten** bevat, kunt u de T1-taak op de contractregel als niet-toerekenbaar koppelen. Het resultaat is dat alle tijd die voor de taak is geregistreerd, toerekenbaar is en dat alle onkosten niet-toerekenbaar zijn.

Het factureringstype van een taak kan worden geconfigureerd op het tabblad **Toerekenbare taken** van de contractregel door het veld **Factureringstype** op het subraster van de contractregeltaken bij te werken. U kunt ook het veld **Factureringstype** in het subraster van de taak bijwerken in Factureringsinstellingen van een project waarin de contractregels worden weergegeven die aan een taak zijn gekoppeld.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Een rol bijwerken als toerekenbaar of niet-toerekenbaar

Een rol kan toerekenbaar of niet-toerekenbaar op een specifieke contractregel zijn.

Het factureringstype van een rol kan worden geconfigureerd op het tabblad **Toerekenbare rollen** van een contractregel. Werk hiervoor het veld **Factureringstype** in het subraster **Toerekenbare rollen** bij.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar

Een transactiecategorie kan toerekenbaar of niet-toerekenbaar zijn op een specifieke contractregel.

Het factureringstype van een transactiecategorie kan worden geconfigureerd op het tabblad **Toerekenbare categorieën** van een projectgebaseerde contractregel. Werk hiervoor het veld **Factureringstype** in het subraster **Toerekenbare categorieën** bij.

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

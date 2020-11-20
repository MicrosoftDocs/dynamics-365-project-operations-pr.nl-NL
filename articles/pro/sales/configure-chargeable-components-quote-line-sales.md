---
title: De toerekenbare componenten van een prijsopgaveregel configureren - lite
description: Dit onderwerp bevat informatie over het instellen van toerekenbare en niet-toerekenbare onderdelen op een projectgebaseerde prijsopgaveregel.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177100"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>De toerekenbare componenten van een prijsopgaveregel configureren - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een projectgebaseerde prijsopgaveregel heeft het concept van *opgenomen* onderdelen en *toerekenbare* onderdelen.

Op opgenomen onderdelen is het volgende van toepassing:

  - Factureringsmethode en klantsplitsingen
  - Niet-overschrijdingslimieten 
  - Factuurfrequentie-instellingen die zijn gedefinieerd op de projectgebaseerde prijsopgaveregel

Een subset van de opgenomen onderdelen kan worden gemarkeerd als toerekenbaar met het veld **Factureringstype**. Het veld **Factureringstype** is een optieset die de volgende waarden toestaat in de context van een prijsopgaveregel:

  - Toerekenbaar
  - Niet-toerekenbaar

Toerekenbare onderdelen kunnen worden gedefinieerd voor taken, rollen en transactiecategorieën.

Toerekenbaarheid wordt gedefinieerd voor de taken van een prijsopgaveregel en is van toepassing op alle transactieklassen die op die regel zijn opgenomen. Als het veld **Taken opnemen** is ingesteld op **Geheel project** of is leeg gelaten, is het tabblad **Toerekenbare taken** niet beschikbaar.

Toerekenbaarheid die is gedefinieerd voor rollen voor een prijsopgaveregel is alleen van toepassing op de transactieklasse **Tijd**. Als het veld **Tijd opnemen** is ingesteld op **Nee** op een prijsopgaveregel van een project, is het tabblad **Toerekenbare rollen** niet beschikbaar.

Toerekenbaarheid die is gedefinieerd voor transactiecategorieën voor een prijsopgaveregel is alleen van toepassing op de transactieklasse **Onkosten**. Als het veld **Onkosten opnemen** is ingesteld op **Nee** op een prijsopgaveregel van een project, is het tabblad **Toerekenbare categorieën** niet beschikbaar.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Een projecttaak bijwerken als toerekenbaar of niet-toerekenbaar

Een projecttaak kan in de context van een projectgebaseerde prijsopgaveregel toerekenbaar of niet-toerekenbaar zijn, waardoor de volgende instellingen mogelijk zijn:

Als een projectgebaseerde prijsopgaveregel **Tijd** en de taak **T1** bevat, wordt de taak als toerekenbaar aan de prijsopgaveregel gekoppeld. Als er een tweede prijsopgaveregel is die **Onkosten** bevat, kunt u de **T1**-taak op de prijsopgaveregel als niet-toerekenbaar koppelen. Het resultaat is dat alle tijd die voor de taak is geregistreerd, toerekenbaar is en dat alle onkosten die voor de taak zijn geregistreerd niet-toerekenbaar zijn.

Het factureringstype van een taak kan worden geconfigureerd op het tabblad **Toerekenbare taken** van de projectgebaseerde prijsopgaveregel door het veld **Factureringstype** op het subraster **Taken van contractregel** bij te werken. U kunt ook het factureringstype voor een projecttaak bijwerken in het veld **Factureringstype** op het subraster Factureringsinstellingen van een project bijwerken dat de prijsopgaveregels toont die aan een taak zijn gekoppeld.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Een rol bijwerken als toerekenbaar of niet-toerekenbaar

Een rol kan toerekenbaar en niet-toerekenbaar zijn in de context van een specifieke projectgebaseerde prijsopgaveregel.

Het factureringstype van een rol kan worden geconfigureerd op het tabblad **Toerekenbare rollen** door het veld **Factureringstype** op het subraster **Toerekenbare rollen** bij te werken.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar

Een transactiecategorie kan toerekenbaar of niet-toerekenbaar zijn op een specifieke prijsopgaveregel.

Het factureringstype van een transactie kan worden geconfigureerd op het tabblad **Toerekenbare categorieën** door het veld **Factureringstype** op het subraster **Toerekenbare categorieën** bij te werken.

### <a name="resolve-chargeability"></a>Toerekenbaarheid oplossen
Een schatting of een werkelijke waarde die is gemaakt voor tijd, wordt alleen als toerekenbaar beschouwd als **Tijd** is opgenomen op de prijsopgaveregel, en als **Taak** en **Rol** zijn geconfigureerd als toerekenbaar op de prijsopgaveregel.

Een schatting of een werkelijke waarde die is gemaakt voor onkosten, wordt alleen als toerekenbaar beschouwd als **Onkosten** is opgenomen op de prijsopgaveregel, en als **Taak** en **Transactiecategorie** zijn geconfigureerd als toerekenbaar op de prijsopgaveregel.

| Bevat Tijd | Bevat Onkosten | Opgenomen taken | - Rol | Categorie | Opdracht | Facturering |
| --- | --- | --- | --- | --- | --- | --- |
| Ja | Ja | Geheel project | Toerekenbaar | Toerekenbaar | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Toerekenbaar </br>Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar |
| Ja | Ja | Alleen geselecteerde taken | Toerekenbaar | Toerekenbaar | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Toerekenbaar</br>Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar |
| Ja | Ja | Alleen geselecteerde taken | Niet-toerekenbaar | Toerekenbaar | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar</br>Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar |
| Ja | Ja | Alleen geselecteerde taken | Toerekenbaar | Toerekenbaar | Niet-toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar</br> Factureringstype voor een werkelijke waarde van Onkosten: Niet-toerekenbaar |
| Ja | Ja | Alleen geselecteerde taken | Niet-toerekenbaar | Toerekenbaar | Niet-toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar</br> Factureringstype voor een werkelijke waarde van Onkosten: Niet-toerekenbaar |
| Ja | Ja | Alleen geselecteerde taken | Niet-toerekenbaar | Niet-toerekenbaar | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar</br> Factureringstype voor een werkelijke waarde van Onkosten: Niet-toerekenbaar |
| Geen | Ja | Geheel project | Kan niet worden ingesteld | Toerekenbaar | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Niet beschikbaar </br>Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar |
| Geen | Ja | Geheel project | Kan niet worden ingesteld | Niet-toerekenbaar | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Niet beschikbaar </br>Factureringstype voor een werkelijke waarde van Onkosten: Niet-toerekenbaar |
| Ja | Geen | Geheel project | Toerekenbaar | Kan niet worden ingesteld | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Toerekenbaar</br>Factureringstype voor een werkelijke waarde van Onkosten: Niet beschikbaar |
| Ja | Geen | Geheel project | Niet-toerekenbaar | Kan niet worden ingesteld | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar </br>Factureringstype voor een werkelijke waarde van Onkosten: Niet beschikbaar |

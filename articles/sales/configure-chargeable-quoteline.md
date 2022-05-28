---
title: De toerekenbare componenten van een projectgebaseerde prijsopgaveregel configureren
description: Dit onderwerp bevat informatie over inbegrepen, toerekenbare en niet-toerekenbare componenten op projectgebaseerde prijsopgaveregels.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 025a04fa63bfdb53aaababcd964a5dcb92c0a3a1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601180"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>De toerekenbare componenten van een projectgebaseerde prijsopgaveregel configureren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Een projectgebaseerde prijsopgaveregel kan componenten en toerekenbare componenten bevatten.

Op de opgenomen componenten zijn de factureringsmethode, klantensplitsingen, niet-overschrijdingslimieten en factuurfrequentie-instellingen van toepassing die zijn gedefinieerd op de projectgebaseerde prijsopgaveregel.
Een subset van de meegeleverde componenten kan worden gemarkeerd als toerekenbaar door gebruik te maken van **Factureringstype**. U kunt een van de volgende opties selecteren in het veld **Factureringstype** in de context van een prijsopgaveregel:

   - Toerekenbaar
   - Niet-toerekenbaar

Toerekenbare onderdelen kunnen worden gedefinieerd voor rollen en transactiecategorieën.

Als rollen zijn gedefinieerd als factureerbaar voor een projectofferteregel, is dat alleen van toepassing op de transactieklasse **Tijd**. Als voor een projectprijsopgaveregel **Tijd opnemen** = **Nee** is ingesteld, is het tabblad **Toerekenbare rollen** niet beschikbaar.

Als transactiecategorieën zijn gedefinieerd als factureerbaar voor een projectofferteregel, is dat alleen van toepassing op de transactieklasse **Onkosten**. Als voor een projectprijsopgaveregel **Onkosten opnemen** = **Nee** is ingesteld, is het tabblad **Toerekenbare categorieën** niet beschikbaar.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Een rol bijwerken als toerekenbaar of niet-toerekenbaar
Een rol kan al dan niet toerekenbaar zijn op een projectgebaseerde prijsopgaveregel. Het factureringstype voor een rol kan worden geconfigureerd op het tabblad **Toerekenbare rollen** van een projectgebaseerde prijsopgaveregel. Werk hiervoor **Factureringstype** bij in het subraster **Toerekenbare rollen**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar
Een transactiecategorie kan al dan niet toerekenbaar zijn op een projectgebaseerde prijsopgaveregel. Het factureringstype voor een transactie kan worden geconfigureerd op het tabblad **Toerekenbare categorieën** van een projectgebaseerde prijsopgaveregel. Werk hiervoor het veld **Factureringstype** bij in het subraster **Toerekenbare categorieën**. 

## <a name="resolve-chargeability"></a>Toerekenbaarheid oplossen

Een schatting of werkelijke tijd die voor tijd is gemaakt, wordt alleen als toerekenbaar beschouwd als de tijd is opgenomen op de prijsopgaveregel en als de rol is geconfigureerd als toerekenbaar.
Een schatting of werkelijke tijd die voor onkosten is gemaakt, wordt alleen als toerekenbaar beschouwd als de onkosten zijn opgenomen op de prijsopgaveregel en als de transactiecategorie is geconfigureerd als toerekenbaar. De volgende tabel laat de standaardinstelling voor toerekenbaar zien voor elke werkelijke waarde. De standaardinstellingen zijn gebaseerd op de opgenomen componenten en het factureringstype dat is ingesteld op de prijsopgaveregel.

| Bevat tijd | Bevat onkosten | - Rol | Categorie | Opdracht |
| --- | --- | --- | --- | --- |
| Ja | Ja | Toerekenbaar | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Toerekenbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Toerekenbaar |
| Ja | Ja | Niet-toerekenbaar | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Toerekenbaar |
| Ja | Ja | Niet-toerekenbaar | Niet-toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Niet-toerekenbaar |
| Geen | Ja | Kan niet worden ingesteld | Toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet beschikbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Toerekenbaar |
| Geen | Ja | Kan niet worden ingesteld | Niet-toerekenbaar | Facturering voor een werkelijke waarde van tijd: Niet beschikbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Niet-toerekenbaar |
| Ja | Geen | Toerekenbaar | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Toerekenbaar </br>Factureringstype voor een werkelijke waarde van onkosten: Niet beschikbaar |
| Ja | Geen | Niet-toerekenbaar | Kan niet worden ingesteld | Facturering voor een werkelijke waarde van tijd: Niet-toerekenbaar </br> Factureringstype voor een werkelijke waarde van onkosten: Niet beschikbaar |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
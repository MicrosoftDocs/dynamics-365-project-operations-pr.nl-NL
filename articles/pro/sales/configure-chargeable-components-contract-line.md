---
title: Toerekenbare componenten van een projectgebaseerde contractregel configureren
description: Dit onderwerp bevat informatie over het toevoegen van niet-toerekenbare onderdelen aan contractregels in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858467"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Toerekenbare componenten van een projectgebaseerde contractregel configureren

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

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

Een schatting of werkelijke waarde gemaakt voor tijd wordt alleen als toerekenbaar beschouwd als:

   - **Tijd** is opgenomen op de contractregel.
   - **Rol** is geconfigureerd als toerekenbaar op de contractregel.
   - **Opgenomen taken** is ingesteld op **Geselecteerde taken** op de contractregel.
 
 Als deze drie dingen van toepassing zijn, is de taak geconfigureerd als toerekenbaar. 

Een schatting of werkelijke waarde gemaakt voor onkosten wordt alleen als toerekenbaar beschouwd als:

   - **Onkosten** is opgenomen op de contractregel.
   - **Transactiecategorie** is geconfigureerd als toerekenbaar op de contractregel.
   - **Opgenomen taken** is ingesteld op **Geselecteerde taak** op de contractregel.
  
 Als deze drie dingen van toepassing zijn, is de **taak** geconfigureerd als toerekenbaar. 

Een schatting of werkelijke waarde gemaakt voor materiaal wordt alleen als toerekenbaar beschouwd als:

   - **Materialen** is opgenomen op de contractregel.
   - **Opgenomen taken** is ingesteld op **Geselecteerde taken** op de contractregel

Als deze twee dingen van toepassing zijn, is de **taak** geconfigureerd als toerekenbaar. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Bevat Tijd</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Bevat Onkosten</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Bevat materialen</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Opgenomen taken</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>- Rol</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Categorie</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Opdracht</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impact op toerekenbaarheid</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Geheel project </p>
            </td>
            <td width="65" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="70" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde van onkosten: <strong>Toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor werkelijke materiaalwaarde: <strong>Toerekenbaar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="65" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="70" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="65" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde van onkosten: <strong>Toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor werkelijke materiaalwaarde: <strong>Toerekenbaar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="65" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar </p>
                <p>
Factureringstype op werkelijke materiaalwaarde: Toerekenbaar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="65" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="70" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype op werkelijke materiaalwaarde: Toerekenbaar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Geen</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Geheel project </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Toerekenbaar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Niet beschikbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar </p>
                <p>
Factureringstype op werkelijke materiaalwaarde: Toerekenbaar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Geen</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Geheel project </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Niet beschikbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype op werkelijke materiaalwaarde: Toerekenbaar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Geen</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Geheel project </p>
            </td>
            <td width="65" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="70" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: Toerekenbaar </p>
                <p>
Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet beschikbaar</strong>
                </p>
                <p>
Factureringstype op werkelijke materiaalwaarde: Toerekenbaar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Geen</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Geheel project </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet beschikbaar</strong>
                </p>
                <p>
Factureringstype op werkelijke materiaalwaarde: Toerekenbaar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Geen</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Geheel project </p>
            </td>
            <td width="65" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="70" valign="top">
                <p>
Toerekenbaar </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: Toerekenbaar </p>
                <p>
Factureringstype voor een werkelijke waarde van Onkosten: Toerekenbaar </p>
                <p>
Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet beschikbaar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Geen</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Geheel project </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Niet-toerekenbaar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan niet worden ingesteld </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor onkosten: <strong>Niet-toerekenbaar</strong>
                </p>
                <p>
Factureringstype voor een werkelijke waarde voor materiaal: <strong>Niet beschikbaar</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

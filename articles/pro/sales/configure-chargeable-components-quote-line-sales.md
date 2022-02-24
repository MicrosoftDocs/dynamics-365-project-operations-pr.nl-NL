---
title: De toerekenbare onderdelen van een prijsopgaveregel configureren
description: Dit onderwerp bevat informatie over het instellen van toerekenbare en niet-toerekenbare onderdelen op een projectgebaseerde prijsopgaveregel.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858287"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>De toerekenbare componenten van een prijsopgaveregel configureren 

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

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

Een projecttaak kan in de context van een projectgebaseerde prijsopgaveregel toerekenbaar of niet-toerekenbaar zijn, waardoor de volgende instellingen mogelijk zijn.

Als een projectgebaseerde prijsopgaveregel **Tijd** en de taak **T1** bevat, wordt de taak als toerekenbaar aan de prijsopgaveregel gekoppeld. Als er een tweede prijsopgaveregel is die **Onkosten** bevat, kunt u de **T1**-taak op de prijsopgaveregel als niet-toerekenbaar koppelen. Het resultaat is dat alle tijd die voor de taak is geregistreerd, toerekenbaar is en dat alle onkosten die voor de taak zijn geregistreerd niet-toerekenbaar zijn.

Het factureringstype van een taak kan worden geconfigureerd op het tabblad **Toerekenbare taken** van de projectgebaseerde prijsopgaveregel door het veld **Factureringstype** op het subraster **Taken van contractregel** bij te werken. U kunt ook het factureringstype voor een projecttaak bijwerken in het veld **Factureringstype** op het subraster Factureringsinstellingen van een project bijwerken dat de prijsopgaveregels toont die aan een taak zijn gekoppeld.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Een rol bijwerken als toerekenbaar of niet-toerekenbaar

Een rol kan toerekenbaar en niet-toerekenbaar zijn in de context van een specifieke projectgebaseerde prijsopgaveregel.

Het factureringstype van een rol kan worden geconfigureerd op het tabblad **Toerekenbare rollen** door het veld **Factureringstype** op het subraster **Toerekenbare rollen** bij te werken.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Een transactiecategorie bijwerken als toerekenbaar of niet-toerekenbaar

Een transactiecategorie kan toerekenbaar of niet-toerekenbaar zijn op een specifieke prijsopgaveregel.

Het factureringstype van een transactie kan worden geconfigureerd op het tabblad **Toerekenbare categorieën** door het veld **Factureringstype** op het subraster **Toerekenbare categorieën** bij te werken.

### <a name="resolve-chargeability"></a>Toerekenbaarheid oplossen
Een schatting of werkelijke waarde gemaakt voor de tijd wordt alleen als toerekenbaar beschouwd als:

   - **Tijd** is opgenomen op de prijsopgaveregel.
   - **Rol** is geconfigureerd als toerekenbaar op de prijsopgaveregel.
   - **Opgenomen taken** is ingesteld op **Geselecteerde taken** op de prijsopgaveregel. 

Als deze drie dingen van toepassing zijn, is de **taak** is ook geconfigureerd als toerekenbaar. 

Een schatting of werkelijke waarde gemaakt voor onkosten wordt alleen als toerekenbaar beschouwd als: 

   - **Onkosten** is opgenomen op de prijsopgaveregel.
   - **Transactiecategorie** is geconfigureerd als toerekenbaar op de prijsopgaveregel.
   - **Opgenomen taken** is ingesteld op **Geselecteerde taken** op de prijsopgaveregel.

Als deze drie dingen van toepassing zijn, is de **taak** is ook geconfigureerd als toerekenbaar. 

Een schatting of werkelijke waarde gemaakt voor materiaal wordt alleen als toerekenbaar beschouwd als:

   - **Materialen** is opgenomen op de prijsopgaveregel.
   - **Opgenomen taken** is ingesteld op **Geselecteerde taken** op de prijsopgaveregel.

Als deze twee dingen van toepassing zijn, moet de **taak** ook als toerekenbaar zijn geconfigureerd. 


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
Facturering voor een werkelijke waarde van tijd: Toerekenbaar </p>
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
Toerekenbaar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturering voor een werkelijke waarde van tijd: Toerekenbaar </p>
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

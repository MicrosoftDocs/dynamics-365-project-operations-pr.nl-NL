---
title: Subcontractregels voor tijd
description: In dit onderwerp wordt uitgelegd hoe u subcontractregels voor tijd registreert en hoe u de aankoop van tijd van leveranciers registreert.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c1adc1e88369e9f60548ed69b5950070d5f10c57
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595676"
---
# <a name="subcontract-lines-for-time"></a>Subcontractregels voor tijd

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een subcontract in Dynamics 365 Project Operations kan een subcontractregel voor tijd hebben. Subcontractregels voor tijd stellen een projectmanager in staat om de tijd van leverancierresources te kopen om projecttaken en resourcevereisten te bemannen.

Voer de volgende stappen uit om een subcontractregel voor tijd te maken in Project Operations.

1. Selecteer in het navigatievenster de optie **Subcontracten** en open een subcontract.
2. Selecteer op het tabblad **Subcontractregels** de optie **Nieuw** om een nieuwe subcontractregel te maken.
3. Op de pagina **Snelle invoer** selecteert u in het veld **Transactieklasse** de optie **Tijd**.
4. Geef de overige veldgegevens op en selecteert **Opslaan**.

  De volgende tabel bevat informatie over de velden op de pagina's **Subcontractregel** en **Snelle invoer**.

| **Veld** | **Beschrijving** | **Functionele impact** |
| --- | --- | --- |
| Meetcriterium | Naam van de subcontractregel om te helpen bij identificatie. | Dit wordt weergegeven als de eerste kolom in alle zoekopdrachten op basis van subcontractregels. |
| Beschrijving | Een korte beschrijving van services die worden gekocht op de subcontractregel. |Geen |
| Type lijn |   Dit veld heeft de standaardwaarde **Op hoeveelheid gebaseerd**.| Geen |
| Factureringsmethode | Dit is een optieset die de twee belangrijkste contractmodellen vertegenwoordigt die worden ondersteund door Project Operations: **Vaste prijs** en **Tijd- en materiaalverbruik**. | Op basis van de geselecteerd factureringsmethode wordt een op mijlpalen gebaseerd factuurschema beschikbaar gesteld voor subcontractregels met de factureringsmethode Vaste prijs. |
| Transactieklasse | De standaardwaarde is **Tijd**. | Dit geeft aan dat de subcontractregel wordt gebruikt om een aankoop van onderaannemerstijd vast te leggen. |
| - Rol | Selecteer de rol van de subcontractresources waarvan de tijd wordt ingekocht. | De rol die wordt uitgevoerd door de subcontractresources is bepalend voor de kosten van de aankoop. |
| Aangevraagd begin | Voer de datum in waarop de resources van de onderaannemer moeten beginnen met werken. | Dit wordt gebruikt om een projectprijslijst te kiezen uit de projectprijslijsten die bij het subcontract zijn gevoegd. De kosten van de rol op de subcontractregel zijn afkomstig uit die prijslijst. |
| Aangevraagd einde | Voer de datum in waarop de toewijzing van de resource van de onderaannemer eindigt. | Dit wordt gebruikt om waarschuwingen weer te geven wanneer een projectmanager gebruikmaakt van de capaciteit voor resourcevereisten die na deze datum plaatsvinden. |
| Bestelde hoeveelheid | Voer het aantal uren in van de rol die bij de leverancier wordt aangeschaft. | Dit wordt gebruikt om waarschuwingen weer te geven wanneer een projectmanager te veel gebruikmaakt van deze capaciteit voor resourcevereisten. |
| Eenhedengroep | De standaardwaarde is **Eenhedengroep Tijd**, die niet kan worden gewijzigd. | Geen|
| Eenheid | De standaard voor dit veld is de basiseenheid van uren van de **Eenhedengroep Tijd**. U kunt deze waarde wijzigen om elke eenheid van de **eenhedengroep Tijd** te kopen, zoals dag of week. | De combinatie van **Rol** en **Eenheid** wordt standaard gebruikt of berekend voor de eenheidsprijs voor de subcontractregel. |
| Prijs per eenheid | De standaardprijs per eenheid gebruikt de combinatie van **Rol** en **Eenheid** uit de categorieprijzen die zijn gerelateerd aan de projectprijslijst, die van toepassing is op de gevraagde datum voor **Aangevraagd begin** van de subcontractregel. | Wanneer voor de toepasselijke projectprijslijst de prijs op een andere eenheid is ingesteld dan de eenheid op de subcontractregel, gebruikt het systeem de eenheidsconversie om de prijs per eenheid te berekenen. |
| Subtotaal |    Dit is een alleen-lezen veld dat wordt berekend als Hoeveelheid x Eenheidsprijs, als zowel de waarde voor de hoeveelheid als de eenheidsprijs wordt ingevoerd. Als de velden voor hoeveelheid en/of eenheidsprijs leeg zijn, kunt u handmatig een waarde invoeren. | Geen|
| Omzetbelasting |   Voer het bedrag aan omzetbelasting in. |Geen |
| Totale bedrag | Het totale bedrag van de subcontractregel, inclusief belastingen. Dit veld wordt berekend als Subtotaal + Btw.|Geen |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

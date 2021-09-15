---
title: Subcontractregels voor tijd
description: In dit onderwerp wordt uitgelegd hoe u subcontractregels voor tijd registreert en hoe u de aankoop van tijd van leveranciers registreert.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323860"
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

| **Veld** | **Beschrijving** |
| --- | --- |
| Meetcriterium | De naam van de subcontractregel. |
| Beschrijving | Een korte beschrijving van services die worden gekocht op de subcontractregel. | 
| Type lijn | Dit veld is een standaardwaarde.  |
| Factureringsmethode | Selecteer de factureringsmethode. Op basis van de factureringsmethode van de subcontractregel waarnaar wordt verwezen, wordt een op mijlpalen gebaseerd factuurschema beschikbaar gemaakt voor de factureringsmethode met vaste prijs. |
| Transactieklasse | Dit veld is een standaardwaarde die aangeeft of de subcontractregel wordt gebruikt om een aankoop van onderaannemerstijd vast te leggen. |
| - Rol | De rol van de subcontractresources waarvan tijd wordt ingekocht. De rol die aan de subcontractresources is toegewezen, bepaalt de kosten van de inkoop. |
| Aangevraagd begin | De datum waarop de resources van de onderaannemer moeten beginnen met werken. Het aangevraagde begin wordt gebruikt om een projectprijslijst te kiezen uit de projectprijslijsten die bij het subcontract zijn gevoegd. De kosten van de rol op de subcontractregel zijn dan afkomstig uit die prijslijst. |
| Aangevraagd eind | De datum waarop de toewijzing van de resources van de onderaannemer eindigt. Deze datum wordt gebruikt om waarschuwingen weer te geven wanneer een projectmanager na deze datum gebruikmaakt van deze capaciteit voor resourcevereisten. |
| Bestelde hoeveelheid | Het aantal roluren dat wordt ingekocht bij de leverancier. Deze waarde wordt gebruikt om waarschuwingen weer te geven wanneer een projectmanager te veel van deze capaciteit gebruikt voor resourcevereisten. |
| Eenhedengroep | Deze veldwaarde is standaard ingesteld op de groep Tijdseenheid en kan niet worden gewijzigd.  |
| Eenheid | Dit veld is standaard ingesteld op de basiseenheid van uren uit de groep Tijdseenheid. U kunt deze waarde wijzigen om elke eenheid van de eenheidsgroep Tijd te kopen, zoals dag of week. De combinatie van rol en eenheid wordt gebruikt om de eenheidsprijs voor de subcontractregel te berekenen. |
| Prijs per eenheid | De eenheidsprijs wordt standaard ingesteld op basis van de combinatie van rol en eenheid uit de prijslijst die van toepassing is op de gevraagde begindatum van de subcontractregel. Wanneer voor de toepasselijke projectprijslijst de prijs op een andere eenheid is ingesteld dan de eenheid op de subcontractregel, gebruikt het systeem de eenheidsconversie om de prijs per eenheid te berekenen. |
| Subtotaal | Dit is een alleen-lezen veld dat automatisch wordt berekend als **Aantal x Eenheidsprijs** als zowel het aantal als de eenheidsprijs is ingevoerd. Als de velden voor hoeveelheid en/of eenheidsprijs leeg zijn, kunt u handmatig een waarde invoeren. |
| Omzetbelasting |  Voer het bedrag aan omzetbelasting in. |
| Totale bedrag | Het totale bedrag van de subcontractregel, inclusief belastingen. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

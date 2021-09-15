---
title: Subcontractregels voor onkostencategorieën
description: In dit onderwerp wordt uitgelegd hoe u subcontractregels voor onkosten registreert en de velden gebruikt om de inkoop van tijd van leveranciers vast te leggen.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323815"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Subcontractregels voor onkostencategorieën

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een subcontract in Dynamics 365 Project Operations kan een regel voor tijd onkostencategorieën. Subcontractregels voor onkostencategorieën stellen een projectmanager in staat om categorieën van diensten of producten te kopen van leveranciers die ze aan de projectkosten kunnen toevoegen.

Voer de volgende stappen uit om een subcontractregel voor onkostencategorieën te maken in Project Operations.

1. Selecteer in het navigatievenster de optie **Subcontracten** en open het subcontract waarmee u wilt werken.
2. Selecteer op het tabblad **Subcontractregels** de optie **Nieuw** om een nieuwe regel te maken.
3. Selecteer op de pagina **Snelle invoer** in het veld **Transactieklasse** de optie **Onkosten** en voer de overige vereiste veldinformatie in of selecteer deze.

De volgende tabel bevat informatie over de velden op de pagina's **Subcontractregel** en **Snelle invoer**.

| **Veld** |  **Beschrijving** |
| ----------| ---------------- |
| Meetcriterium | De naam van de subcontractregel. |
| Beschrijving | Een korte beschrijving van de service of onkostencategorieën die worden gekocht op de subcontractregel. |
| Type lijn | Dit veld heeft de standaardwaarde **Op hoeveelheid gebaseerd**.  |
| Factureringsmethode | De factureringsmethode van de subcontractregel. Op basis van de factureringsmethode van de regel wordt een op mijlpalen gebaseerd factuurschema beschikbaar gemaakt voor de factureringsmethode met vaste prijs.  |
| Transactieklasse | Dit veld heeft als standaardwaarde **Tijd**. Om subcontractregels voor het aankopen van producten te maken, stelt u het veld **Transactieklasse** in op **Onkosten**. Deze veldwaarde geeft aan dat de subcontractregel wordt gebruikt om een aankoop van een categorie producten of services voor projecten vast te leggen. |
| Transactiecategorie | Selecteer de transactiecategorie. |
| Aangevraagd begin | De datum waarop de inkoopcategorieën beschikbaar moeten zijn van de leverancier. Het aangevraagde begin wordt gebruikt om een projectprijslijst te kiezen uit de projectprijslijsten die bij het subcontract zijn gevoegd. De kosten van de categorie op de subcontractregel zijn afkomstig uit die prijslijst. |
| Aangevraagd eind | De datum waarop de aankoopcategorieën niet meer nodig zijn. Deze datum roept een waarschuwing op wanneer een projectmanager deze subcontractregel koppelt aan specifieke onkostenramingen voor de projecten die na deze datum zijn gedateerd. |
| Bestelde hoeveelheid | De hoeveelheid van de categorie die van de leverancier wordt gekocht. Als een projectmanager te veel van de gekochte hoeveelheid gebruikt, volgt er een waarschuwing.  |
| Eenhedengroep | Deze veldwaarde wordt standaard gebaseerd op de standaardeenheidsgroep die is ingesteld voor de geselecteerde categorie. |
| Eenheid | Deze veldwaarde wordt standaard gebaseerd op de standaardeenheid die is ingesteld voor de geselecteerde categorie. De combinatie van categorie en eenheid wordt gebruikt om de eenheidsprijs voor de subcontractregel te berekenen. |
| Prijs per eenheid | De eenheidsprijs wordt standaard ingesteld op basis van de combinatie van categorie en eenheid uit de categorieprijzen gerelateerd aan de projectprijslijst die van toepassing is op het gevraagde begin van de subcontractregel.  |
| Subtotaal | Dit alleen-lezen veld wordt automatisch berekend als de eenheidsprijs voor hoeveeheid als zowel het aantal als de eenheidsprijs is ingevoerd. Als een of beide velden leeg zijn, kunt u handmatig een waarde invoeren in dit veld.  |
| Omzetbelasting | Voer het bedrag aan omzetbelasting in.  |
| Totale bedrag | Het totale bedrag van de subcontractregel, inclusief belastingen. Dit veld wordt berekend als subtotaal + btw.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

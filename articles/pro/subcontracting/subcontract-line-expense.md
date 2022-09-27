---
title: Subcontractregels voor onkostencategorieën
description: In dit artikel wordt uitgelegd hoe u subcontractregels voor onkosten registreert en de velden gebruikt om de aankoop van tijd bij leveranciers vast te leggen.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ba1241ce40b7c5b488e278e8f1b8e9f352f45dc8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522601"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Subcontractregels voor onkostencategorieën

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Een subcontract in Dynamics 365 Project Operations kan een regel voor tijd onkostencategorieën. Subcontractregels voor onkostencategorieën stellen een projectmanager in staat om categorieën van diensten of producten te kopen van leveranciers die ze aan de projectkosten kunnen toevoegen.

Voer de volgende stappen uit om een subcontractregel voor onkostencategorieën te maken in Project Operations.

1. Selecteer in het navigatievenster de optie **Subcontracten** en open het subcontract waarmee u wilt werken.
2. Selecteer op het tabblad **Subcontractregels** de optie **Nieuw** om een nieuwe regel te maken.
3. Selecteer op de pagina **Snelle invoer** in het veld **Transactieklasse** de optie **Onkosten** en voer de overige vereiste veldinformatie in of selecteer deze.

De volgende tabel bevat informatie over de velden op de pagina's **Subcontractregel** en **Snelle invoer**.

| **Veld** | **Beschrijving** | **Functionele impact** |
| --- | --- | --- |
| Meetcriterium | Naam van de subcontractregel om te helpen bij identificatie. | Dit wordt weergegeven als de eerste kolom in alle zoekopdrachten op basis van subcontractregels. |
| Beschrijving | Een korte beschrijving van de onkostencategorieën die via de subcontractregel worden ingekocht. | Geen |
|Type lijn | Dit veld heeft **Op hoeveelheid gebaseerd** als standaardwaarde. |Geen |
| Factureringsmethode | Dit is een optieset die de twee belangrijkste contractmodellen vertegenwoordigt die worden ondersteund door Project Operations: **Vaste prijs** en **Tijd- en materiaalverbruik**. | Er wordt een op mijlpalen gebaseerd factuurschema beschikbaar gesteld voor subcontractregels als de factureringsmethode Vaste prijs is geselecteerd. |
| Transactieklasse | Dit veld heeft **Tijd** als standaardwaarde. Als u subcontractregels wilt maken voor het aankopen van producten, stelt u het veld **Transactieklasse** in op **Onkosten**.  | Dit geeft aan dat de subcontractregel wordt gebruikt om de inkoop vast te leggen van een onkostencategorie die voor projecten wordt gebruikt. |
| Transactiecategorie | Toont een lijst met actieve transactiecategorieën in het systeem. |Geen |
| Aangevraagd begin | Voer de datum in waarop de inkoopcategorieën beschikbaar moeten zijn bij de leverancier. | Aangevraagd begin wordt gebruikt om een projectprijslijst te kiezen uit de projectprijslijsten die bij het subcontract zijn gevoegd. De kosten van de categorie op de subcontractregel zijn afkomstig uit die prijslijst. |
| Aangevraagd einde | Voer de datum in waarop de aankoopcategorieën niet langer nodig zijn. | Dit wordt gebruikt om waarschuwingen weer te geven wanneer een projectmanager deze subcontractregel aan specifieke onkostenramingen voor het project koppelt die na deze datum vereist zijn. |
| Bestelde hoeveelheid | Hoeveelheid van de categorie die wordt aangeschaft bij de leverancier. | Dit wordt gebruikt om waarschuwingen weer te geven wanneer een projectmanager een te grote hoeveelheid aanschaft.|
| Eenhedengroep | De standaardwaarde is gebaseerd op de standaardeenhedengroep die is ingesteld voor de geselecteerde categorie. |Geen |
| Eenheid | De standaardwaarde is gebaseerd op de standaardeenheid die is ingesteld voor de geselecteerde categorie.  | De combinatie van **Categorie** en **Eenheid** wordt standaard gebruikt of berekend voor de eenheidsprijs voor de subcontractregel.  |
| Prijs per eenheid | De standaardwaarde gebruikt de combinatie van **Categorie** en **Eenheid** uit de categorieprijzen die zijn gerelateerd aan de projectprijslijst, die van toepassing is op de gevraagde begindatum van de subcontractregel. |Geen |
| Subtotaal | Dit is een alleen-lezen veld dat wordt berekend als hoeveelheid X Eenheidsprijs, als zowel de waarde voor de hoeveelheid als de eenheidsprijs wordt ingevoerd. Als een of beide velden leeg zijn, kunt u een waarde in dit veld invoeren. |Geen |
| Omzetbelasting | Voer het bedrag aan omzetbelasting in. |Geen |
| Totale bedrag | Het totale bedrag van de subcontractregel, inclusief belastingen. Dit veld wordt berekend als Subtotaal + Btw. |Geen |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

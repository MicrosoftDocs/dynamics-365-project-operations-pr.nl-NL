---
title: Een betalingsbewijs vastleggen via OCR
description: Dit onderwerp bevat informatie over de OCR-verwerking (optische tekenherkenning) voor betalingsbewijzen.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499845"
---
# <a name="capture-a-receipt-using-ocr"></a>Een betalingsbewijs vastleggen via OCR

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

De invoer van kosten is verbeterd door de introductie van OCR-verwerking (optische tekenherkenning) voor betalingsbewijzen. Deze functionaliteit is ontworpen om de gebruikerservaring te verbeteren bij het maken van onkostennota's.

## <a name="key-features"></a>Belangrijke functies

- Het systeem extraheert de naam van de winkel, de datum en het totale bedrag uit de betalingsbewijzen.
- Het systeem probeert om niet-gekoppelde betalingsbewijzen te matchen met niet-gekoppelde onkostentransacties.
- U kunt handmatig ingevoerde onkostentransacties maken op basis van betalingsbewijzen.

## <a name="attach-receipts-to-an-expense-report"></a>Betalingsbewijzen koppelen aan een onkostennota

Als u betalingsbewijzen die creditcardtransacties omvatten, automatisch wilt koppelen bij het maken van een onkostennota, neemt u de volgende stappen.

  1. Open de werkruimte **Onkostenbeheer**.
  2. Controleer op het tabblad **Ontvangsten** of de niet-gekoppelde betalingsbewijzen bestaan. U kunt ook betalingsbewijzen uploaden op het tabblad **Ontvangsten**.
  3. Controleer op het tabblad **Onkosten** of de niet-gekoppelde onkosten bestaan. Meestal importeert degene die verantwoordelijk is voor de onkostenadministratie, deze onkosten vanuit de creditcardprovider.
  4. Selecteer **Nieuwe onkostennota**. U ziet dat u bij het maken van een onkostennota nu niet alleen onkosten, maar ook betalingsbewijzen kunt opnemen. Als u zowel onkosten als betalingsbewijzen toevoegt, wordt het automatisch matchen van betalingsbewijzen met onkosten geactiveerd.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Betalingsbewijzen maken of matchen voor een onkostennota
Voer de volgende stappen uit om onkosten aan te maken of om onkosten te matchen op basis van een betalingsbewijs.

  1. Ga in een onkostennota naar het tabblad **Ontvangsten** en koppel een betalingsbewijs door **Ontvangsten toevoegen** te selecteren.
  2. Onder de geüploade afbeelding van het betalingsbewijs vindt u de opties **Maken** en **Matchen**.

      - Selecteer **Maken** om een handmatig ingevoerde onkostentransactie aan te maken en de waarden in te vullen die uit het betalingsbewijs kunnen worden geëxtraheerd.
      - Als u **Matchen** selecteert, probeert het systeem bestaande onkosten te matchen met het betalingsbewijs.

## <a name="installation"></a>Installatie

Als u deze geavanceerde mogelijkheden voor onkosten wilt gebruiken, installeert u de invoegtoepassing Expense Management Service voor Microsoft Dynamics 365 Finance en schakelt u de functies in in uw exemplaar. U kunt de invoegtoepassing openen vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS).

1. Meld u aan bij LCS en open de gewenste omgeving.
2. Ga naar **Volledige details**.
3. Selecteer **Onderhouden** of scrol omlaag naar het sneltabblad **Omgevingsinvoegtoepassingen**.
4. Selecteer **Een nieuwe invoegtoepassing installeren**.
5. Selecteer **Expense Management Service**.
6. Volg de installatiehandleiding en ga akkoord met de algemene voorwaarden.
7. Selecteer **Installeren**.

Schakel in de werkruimte **Functiebeheer** de volgende functies in:

- Opnieuw ontworpen onkostennota's
- Automatisch onkosten matchen en maken op basis van een betalingsbewijs

Wanneer u deze functies inschakelt, vinden de volgende acties plaats:

- De bestaande werkruimte **Onkostenbeheer** wordt vervangen door de nieuwe werkruimte.
- Er wordt een nieuw menu-item voor de zichtbaarheid van onkostenvelden toegevoegd.
- U kunt de voormalige pagina **Onkostennota's** nog steeds openen door naar **Onkostenbeheer > Mijn onkosten > Onkostennota's** te gaan.
- Via werkstromen en goedkeuringen komt u nog steeds uit bij de bestaande pagina met onkostennota's.
- Betalingsbewijzen worden verwerkt via Microsoft Azure Cognitive Services en metagegevens worden geëxtraheerd en toegevoegd.
- Er wordt een optie toegevoegd waarmee u een onkostennota kunt maken die gematchte niet-gekoppelde betalingsbewijzen bevat.
- Met een optie die aan onkostennota's wordt toegevoegd, kunt u een onkostenregel maken op basis van een betalingsbewijs of wordt geprobeerd een bestaand betalingsbewijs te matchen met een bestaande onkostenregel.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

**Gebruikt Microsoft mijn gegevens voor zijn modellen?**

Nee, Microsoft heeft een algemeen Machine Learning-model gebouwd voor zijn service voor de verwerking van betalingsbewijzen. Dit model is niet gebaseerd op de betalingsbewijzen die u uploadt.

**Waar is deze functie beschikbaar en waar vindt de gegevensverwerking plaats?**

Momenteel worden de Verenigde Staten ondersteund.

**Waar gaan mijn betalingsbewijzen naartoe?**

Finance neemt contact op met Cognitive Services om de veldgegevens te extraheren. Cognitive Services bewaart gedurende maximaal 24 uur een kopie van uw betalingsbewijs terwijl de verwerking plaatsvindt. Nadat de verwerking is voltooid, verwijdert Cognitive Services het betalingsbewijs. Betalingsbewijzen worden nog steeds opgeslagen in Finance.

Zie [Het begrijpen van betalingsbewijzen mogelijk maken met de nieuwe mogelijkheid van Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) voor meer informatie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

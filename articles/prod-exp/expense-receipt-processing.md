---
title: Verwerking van betalingsbewijzen
description: Dit onderwerp bevat informatie over de OCR-verwerking (optische tekenherkenning) voor betalingsbewijzen. Deze functie is bedoeld om de gebruikerservaring te verbeteren bij het maken van onkostennota's in Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 067432106742447d2b8fa215ec05bf05f4b41e70
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684314"
---
# <a name="expense-receipt-processing"></a>Verwerking van betalingsbewijzen

De invoer van kosten is verbeterd door de introductie van OCR-verwerking (optische tekenherkenning) voor betalingsbewijzen. Deze functie is ontworpen om de gebruikerservaring te verbeteren bij het maken van onkostendeclaraties.

## <a name="key-features"></a>Belangrijke functies

- De naam van de winkel, de datum en het totale bedrag worden uit de betalingsbewijzen gehaald.
- De functie probeert om niet-gekoppelde betalingsbewijzen te matchen met niet-gekoppelde onkostentransacties.
- Gebruikers kunnen handmatig ingevoerde onkostentransacties maken op basis van betalingsbewijzen.

## <a name="usage-examples"></a>Gebruiksvoorbeelden

Als u betalingsbewijzen die creditcardtransacties omvatten, automatisch wilt koppelen bij het maken van een onkostendeclaratie, doet u het volgende:

  1. Open de werkruimte **Onkostenbeheer**.
  2. Controleer op het tabblad **Ontvangsten** of de niet-gekoppelde betalingsbewijzen bestaan. U kunt ook betalingsbewijzen uploaden op het tabblad **Ontvangsten**.
  3. Controleer op het tabblad **Onkosten** of de niet-gekoppelde onkosten bestaan. Meestal importeert degene die verantwoordelijk is voor de onkostenadministratie, deze onkosten vanuit de creditcardprovider.
  4. Selecteer **Nieuwe onkostennota**. U ziet dat u bij het maken van een onkostennota nu niet alleen onkosten, maar ook betalingsbewijzen kunt opnemen. Als u zowel onkosten als betalingsbewijzen toevoegt, wordt het automatisch matchen van betalingsbewijzen met onkosten geactiveerd.

Voer de volgende stappen uit om onkosten te maken of om onkosten te matchen op basis van een betalingsbewijs:

  1. Ga in een onkostennota naar het tabblad **Ontvangsten** en koppel een betalingsbewijs door **Ontvangsten toevoegen** te selecteren.
  2. Onder de geüploade afbeelding van het betalingsbewijs vindt u de opties **Maken** en **Matchen**.

      - Selecteer **Maken** om een handmatig ingevoerde onkostentransactie aan te maken en de waarden in te vullen die uit het betalingsbewijs kunnen worden geëxtraheerd.
      - Als u **Matchen** selecteert, probeert het systeem bestaande onkosten te matchen met het betalingsbewijs.

## <a name="installation"></a>Installatie

Deze functie werkt in combinatie met de functie **Opnieuw ontworpen onkostendeclaraties** om het invoeren van onkosten te vereenvoudigen. Deze functie is alleen beschikbaar voor Tier 2+-omgevingen, namelijk Sandbox en Production.

Als u deze geavanceerde onkostenmogelijkheden wilt gebruiken, installeert u de invoegtoepassing Service voor onkostenbeheer voor Microsoft Dynamics 365 Finance en schakelt u de functies in uw exemplaar in. U kunt de invoegtoepassing openen vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS).

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

Zie [Opnieuw ontworpen onkostendeclaraties](ExpenseWorkspaceNew.md) voor meer informatie over de vernieuwde functie Onkostendeclaraties.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

**Gebruikt Microsoft mijn gegevens voor zijn modellen?**

Nee, Microsoft heeft een algemeen Machine Learning-model gebouwd voor zijn service voor de verwerking van betalingsbewijzen. Dit model is niet gebaseerd op de betalingsbewijzen die u uploadt.

**Waar is deze functie beschikbaar en waar vindt de gegevensverwerking plaats?**

Momenteel worden de Verenigde Staten ondersteund.

**Waar gaan mijn betalingsbewijzen naartoe?**

Finance neemt contact op met Cognitive Services om de veldgegevens te extraheren. Cognitive Services bewaart gedurende maximaal 24 uur een kopie van uw betalingsbewijs terwijl de verwerking plaatsvindt. Nadat de verwerking is voltooid, verwijdert Cognitive Services het betalingsbewijs. Betalingsbewijzen worden nog steeds opgeslagen in Finance.

Zie [Het begrijpen van betalingsbewijzen mogelijk maken met de nieuwe mogelijkheid van Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) voor meer informatie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
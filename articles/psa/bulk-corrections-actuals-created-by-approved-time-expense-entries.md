---
title: Bulkcorrecties van werkelijke waarden voor goedgekeurde tijds- en onkostenvermeldingen
description: In dit artikel wordt uitgelegd hoe een beheerder enkele of bulkcorrecties kan aanbrengen in eerder goedgekeurde tijd- of onkostenboekingen als de facturering niet is voltooid.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 82c9b38e4c79511fe3b6abfcb973fff8b56f1522
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916283"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Bulkcorrecties van werkelijke waarden voor goedgekeurde tijds- en onkostenvermeldingen

[!include [banner](../includes/psa-now-project-operations.md)]

Af en toe worden tijds- en onkostenvermeldingen onjuist ingevoerd. Een consultant kan bijvoorbeeld de verkeerde datum selecteren bij het invoeren van tijdgegevens of ze kunnen de cijfers transponeren bij het invoeren van onkosten. Als een consultant de ingediende items niet kan bijwerken, kan een beheerder de invoer voor een project rechtstreeks corrigeren.

Als u de procedures in dit artikel wilt voltooien, hebt u beheerdersmachtigingen nodig.

## <a name="correct-approved-time-entries"></a>Correcte goedgekeurde tijdsvermeldingen     

Voer de volgende stappen uit om enkele of meerdere tijdsvermeldingen voor een project te corrigeren.

1. Selecteer in het gebied **Verkoop** de optie **Transacties** en selecteer vervolgens **Goedgekeurde tijd**. 

2. Zoek en selecteer in de lijst **Goedgekeurde tijd** een of meer goedgekeurde tijdsvermeldingen om te corrigeren. U kunt het filter gebruiken om gerelateerde items te lokaliseren. U kunt bijvoorbeeld filteren op een project-id en alle goedgekeurde tijdsvermeldingen met die project-id selecteren.

3. Selecteer **Posten corrigeren**. Er wordt automatisch een nieuw correctiejournaal gemaakt met het toegewezen type **Correctie van tijd**. De geselecteerde items worden toegevoegd aan het journaal. 

4. Voer op de pagina **Nieuw journaal** een **Beschrijving** voor uw correctiejournaal in en selecteer vervolgens het tabblad **Correcties van tijdsvermeldingen**.  
5. Werk in de sectie **Nieuwe waarden voor tijdsvermeldingen** de velden indien nodig bij met de juiste informatie. U kunt bijvoorbeeld het toegewezen project of de boekbare resource wijzigen.

6. Selecteer **Voorbeeld**. Selecteer **OK** in het dialoogvenster. Op het tabblad **Journaalregels** kunt u een lijst bekijken van de originele werkelijke waarden die betrekking hebben op de geselecteerde tijdsvermeldingen die zijn teruggedraaid en de gecorrigeerde overeenkomstige regels die zijn gemaakt. Herhaal stap 5 en 6 als er aanvullende correcties nodig zijn. 

> [!NOTE]
> Alle gecorrigeerde werkelijke waarden hebben dezelfde waarden die u in de sectie **Nieuwe waarden voor tijdsvermeldingen** hebt geselecteerd.

7. Selecteer **Bevestigen** als de correcties verschijnen zoals verwacht. Selecteer **OK** in het dialoogvenster.

8. Ga terug naar het gebied **Verkoop**, selecteer **Projecten** en open vervolgens het project waarvoor u zojuist de tijdsvermeldingen hebt bijgewerkt. 

9. Bekijk op de pagina **Projecten**, op het tabblad **Werkelijke waarden** de wijzigingen die u hebt aangebracht. 

> [!NOTE]
> Als het tabblad **Werkelijke waarden** niet zichtbaar is, selecteert u **Gerelateerd** > **Werkelijke waarden**.  

10. In de lijst **Gekoppelde weergave van werkelijke waarden** kunt u zien dat de oorspronkelijke tijdsvermeldingen die zijn teruggedraaid, nog steeds worden vermeld evenals de corresponderende gecorrigeerde tijdsvermeldingen. 


## <a name="correct-approved-expense-entries"></a>Correcte goedgekeurde onkostenvermeldingen

Voer de volgende stappen uit om een of meer onkostenvermeldingen te corrigeren. 

1. Selecteer in het gebied **Verkoop** in het linkernavigatievenster onder **Transacties** de optie **Goedgekeurde onkosten**.

2. Selecteer in de lijst **Goedgekeurde onkosten** het project dat u wilt corrigeren en selecteer vervolgens **Correcte vermeldingen**. Er wordt automatisch een nieuw correctiejournaal gemaakt met het toegewezen type **Correctie van onkosten**. 

3. Voer op de pagina **Nieuw journaal** een **Beschrijving** voor de correctie in, en selecteer op het tabblad **Onkostencorrectie**, in de sectie **Nieuwe waarden voor onkosten** de gegevensvelden die u wilt corrigeren voor de geselecteerde onkostenregels. U kunt de uitgave bijvoorbeeld toewijzen aan een ander **Project** of de **Onkostencategorie**, **Onkostendatum** of **Boekbare resource** corrigeren.

4. Selecteer **Voorbeeld**. Selecteer **OK** in het dialoogvenster. 

5. Controleer de correcties op het tabblad **Journaalregels**. U kunt u een lijst bekijken van de originele werkelijke waarden die betrekking hebben op de geselecteerde onkostenvermeldingen die zijn teruggedraaid en de gecorrigeerde overeenkomstige regels die zijn gemaakt.

6. Selecteer **Bevestigen** als de gecorrigeerde waarden voldoen aan de verwachting. Selecteer **OK** in het dialoogvenster. Als de waarden niet worden weergegeven zoals verwacht, selecteert u **Annuleren** om terug te keren naar de lijst **Goedgekeurde onkosten**. Herhaal de stappen 2 tot en met 5. 

> [!NOTE]
> De gecorrigeerde werkelijke waarden hebben dezelfde waarden die u in de sectie **Nieuwe waarden voor onkosten** hebt geselecteerd.

7. Nadat u het correctiejournaal hebt bevestigd, navigeert u terug naar het project of de projecten die u hebt bijgewerkt om uw wijzigingen te bekijken.  

8. Controleer op het tabblad **Werkelijke waarden** op de projectpagina de **Gekoppelde weergave van werkelijke waarden**. De oorspronkelijke vermeldingen en de gecorrigeerde vermeldingen worden vermeld. In de volgende afbeelding ziet u de oorspronkelijke bedragen voor onkostenvermeldingen en de overeenkomstige gecorrigeerde bedragen voor onkostenvermeldingen. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

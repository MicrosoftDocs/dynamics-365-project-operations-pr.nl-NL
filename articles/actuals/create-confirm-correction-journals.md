---
title: Correctiejournalen maken en bevestigen
description: Dit onderwerp bevat informatie over het maken en bevestigen van een correctiejournaal.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582797"
---
# <a name="create-and-confirm-correction-journals"></a>Correctiejournalen maken en bevestigen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Af en toe kan een tijdsvermelding of onkostenpost verkeerd worden ingevoerd. Een consultant kan bijvoorbeeld de verkeerde datum selecteren wanneer hij een tijdsvermelding maakt, of hij kan het verkeerde project selecteren bij het invoeren van een onkostenpost. Als een consultant de ingediende vermeldingen niet kan bijwerken, kan een back-endbeheerder direct de werkelijke waarden voor een project corrigeren.

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

7. Nadat u het correctiedagboek hebt bevestigd, keert u terug naar het project of de projecten die u hebt bijgewerkt om uw wijzigingen te bekijken.

8. Bekijk op de projectpagina, op het tabblad **Werkelijke waarden**, de lijst **Gekoppelde weergave van werkelijke waarden**. De oorspronkelijke vermeldingen en de gecorrigeerde vermeldingen worden vermeld.


## <a name="correct-approved-material-usage-logs"></a>Goedgekeurde logboeken voor materiaalgebruik corrigeren

Voer de volgende stappen uit om een of meer logboekvermeldingen voor materiaalgebruik te corrigeren.

1. Selecteer in het gebied **Verkoop**, in het linkernavigatievenster, onder **Transacties** de optie **Werkelijke waarden**.

2. Maak in de lijst **Werkelijke waarden** gebruik van kolomfilters om de transactieklasse **Materiaal** te selecteren, zodat alleen de werkelijke waarden voor materialen worden weergegeven. Gebruik andere kolomfilters om de weergegeven werkelijke waarden verder te beperken. Nadat u de gewenste set werkelijke waarden hebt gevonden, selecteert u de werkelijke waarden en selecteert u vervolgens **Posten corrigeren**. Er wordt automatisch een nieuw correctiedagboek gemaakt en het type **Materiaalcorrectie** wordt toegewezen.

3. Voer op de pagina **Nieuw dagboek** in het veld **Beschrijving** een beschrijving voor de correctie in. Selecteer vervolgens, op het tabblad **Materiaalcorrectie**, in de sectie **Nieuwe waarden voor materialen**, de gegevensvelden die u wilt corrigeren voor de geselecteerde materiaalregels. U kunt het materiaal bijvoorbeeld aan een ander project toewijzen of het product, de materiaaldatum of het subcontract corrigeren.

4. Selecteer **Voorbeeld**. Vervolgens selecteert u in het dialoogvenster de optie **OK**.

5. Controleer de correcties op het tabblad **Dagboekregels**. U kunt een lijst bekijken van de oorspronkelijke werkelijke waarden die zijn gerelateerd aan de geselecteerde artikelposten die zijn teruggeboekt en de gecorrigeerde overeenkomstige regels die zijn gemaakt.

6. Selecteer **Bevestigen** als de gecorrigeerde waarden voldoen aan de verwachting. Vervolgens selecteert u in het dialoogvenster de optie **OK**. Als de waarden niet zijn zoals verwacht, selecteert u **Annuleren** om terug te keren naar de lijst **Werkelijke waarden**. Herhaal vervolgens stap 2 tot en met 5.

7. Nadat u het correctiedagboek hebt bevestigd, keert u terug naar het project of de projecten die u hebt bijgewerkt om uw wijzigingen te bekijken.

8. Bekijk op de projectpagina, op het tabblad **Werkelijke waarden**, de lijst **Gekoppelde weergave van werkelijke waarden**. De oorspronkelijke vermeldingen en de gecorrigeerde vermeldingen worden vermeld.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

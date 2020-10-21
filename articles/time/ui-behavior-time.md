---
title: Gedrag van UI voor tijdinvoer
description: Dit onderwerp bevat informatie over het gedrag van de UI voor tijdinvoer.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961697"
---
# <a name="time-entry-ui-behavior"></a>Gedrag van UI voor tijdinvoer

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


Het raster **Wekelijkse tijdinvoer** is een aangepast besturingselement met de hoofdsecties **Dimensies** en **Duur**.

## <a name="dimensions"></a>Dimensies
De sectie **Dimensies** bevat alle dimensies waarvoor tijd kan worden ingevoerd. De volgende dimensies worden standaard ondersteund:

  - Project
  - Projecttaak
  - - Rol
  - Type
  - Vermeldingsstatus

De sectie **Dimensies** staat geen inline bewerking toe. Deze sectie wordt ondersteund door een weergave waarmee aangepaste velden kunnen worden toegevoegd aan het wekelijkse tijdinvoerraster.

## <a name="duration"></a>Duur
In de sectie Duur worden de dagen van de week weergegeven als kolomkoppen. In deze sectie is ook inline bewerken mogelijk. Nadat een rij voor tijdinvoer is gemaakt met de juiste dimensies, kunnen gebruikers snel de hoeveelheid tijd invoeren die ze aan deze dimensies hebben besteed.

## <a name="create-a-new-time-entry"></a>Een nieuwe tijdsvermelding maken

1. Selecteer **Nieuw** in het tijdinvoerraster. 
2. Selecteer in het dialoogvenster **Snelle invoer van tijdsvermelding** de datum van de tijdsvermelding.
3. Voer gegevens in voor de dimensies **Project**, **Projecttaak**, **Rol** en **Duur**. Deze informatie moet in minuten, uren of dagen worden toegevoegd door **h**, **m** of **d** in te voeren samen met het aantal. 
4. Voer een beschrijving en opmerkingen in die extern kunnen worden gedeeld voor de tijdsvermelding. 

Wanneer u het item opslaat, verschijnen de ingevoerde waarden in de sectie **Dimensies**. De gegevens die in het veld **Duur** zijn ingevoerd, worden weergegeven op de datum waarop de tijdsvermelding is gemaakt.

Opzoekvelden worden ondersteund door systeemweergaven. Nadat een gebruiker bijvoorbeeld een project heeft ingevoerd, wordt het veld **Projecttaak** standaard ingesteld op de weergave **Kopiëren**. Als u tijdsvermeldingen wilt maken voor taken die niet aan een gebruiker zijn toegewezen, klikt u op **Weergave wijzigen** in het zoekvenster en selecteert u de weergave **Alle actieve projecttaken**.

## <a name="edit-a-time-entry"></a>Een tijdsvermelding bewerken 
Details van bepaalde velden op de pagina voor tijdinvoer, zoals **Beschrijving** en **Externe opmerkingen**, worden niet weergegeven in het wekelijkse tijdinvoerraster. In plaats daarvan wordt een kleine driehoekige indicator weergegeven in cellen voor **Duur** waarvoor aanvullende gegevens bestaan. 

1. Om een tijdvermelding te bewerken, selecteert u de cel die u wilt bijwerken in de tijdvermelding.
2. Selecteer **Details bewerken** om de gegevens in deelvenster **Hoofdformulier tijdinvoer** bij te werken. 

## <a name="copy-a-time-entry-row"></a>Een rij met tijdinvoer kopiëren
Nadat de rij is gemaakt, kunt u **Rij kopiëren** selecteren om de hele rij naar een nieuwe rij te kopiëren. Wanneer een rij op deze manier wordt gekopieerd, worden ook dimensies en duur gekopieerd. U kunt ook **Rij bewerken** selecteren om dimensiewaarden en duur bij te werken in de sectie **Duur**.

## <a name="open-a-time-entry-behavior"></a>Een tijdsvermelding openen
Om een optimale en snelle invoer in de belangrijkste velden te ondersteunen, wordt in het wekelijkse tijdinvoerraster een subset van de geselecteerde dimensies en tijdsduur weergegeven. Als u alle details van een enkele tijdsvermelding wilt weergeven , selecteert u onder **Vermelding bewerken** de optie **Openen**.

## <a name="submit-a-time-entry"></a>Een tijdsvermelding indienen
U kunt één tijdsvermelding of een groep tijdsvermeldingen indienen door een blok cellen of een hele rij met tijdsvermeldingen te selecteren en vervolgens **Indienen** te kiezen. Ingediende tijdsvermeldingen worden weergegeven als posten die wachten op goedkeuring op de pagina **Goedkeuring** van de fiatteurs. Nadat de tijdsvermeldingen zijn verzonden, kunnen ze niet meer worden bewerkt.

## <a name="recall-a-time-entry"></a>Een tijdsvermelding intrekken
U kunt tijdvermeldingen die u hebt ingediend, intrekken. U kunt één tijdsvermelding, een blok met tijdsvermeldingen of een hele rij met tijdsvermeldingen intrekken. Ingetrokken tijdgegevens kunnen worden bewerkt.

## <a name="time-entry-status"></a>Status van tijdsvermelding

- **Concept**: nieuwe tijdsvermeldingen krijgen automatisch de status **Concept** toegewezen. Alleen tijdsvermeldingen met de status **Concept** kunnen worden verwijderd.
- **Ingediend**: wanneer een tijdsvermelding wordt ingediend, wordt de status bijgewerkt naar **Ingediend**. 
- **Goedgekeurd**: wanneer een ingediende tijdsvermelding wordt goedgekeurd, wordt de status bijgewerkt naar **Goedgekeurd**. 
- **Geretourneerd**: als een tijdsvermelding wordt afgewezen, wordt de status bijgewerkt naar **Geretourneerd** en wordt de vermelding beschikbaar voor correctie en opnieuw indienen. 

## <a name="view-rejection-comments"></a>Opmerkingen bij afwijzing weergeven
Wanneer een tijdsvermelding wordt afgewezen door een fiatteur, kan de fiatteur opmerkingen toevoegen om de resource te helpen de reden voor de afwijzing te begrijpen. Als u de afwijzingsopmerkingen voor een tijdsvermelding wilt weergeven, selecteert u **Vermelding openen**. De opmerkingen voor afwijzing worden weergegeven in de tijdlijn. De gebruiker kan reageren op de afwijzingsopmerkingen voordat ze het item opnieuw indienen.

## <a name="copy-week"></a>Week kopiëren
Nadat een paar tijdsvermeldingen zijn gemaakt, kunnen gebruikers meerdere tijdsvermeldingen tegelijk maken.

1. Selecteer in het formulier **Tijdsvermeldingen** de optie **Week kopiëren** om bulksgewijs extra tijdsvermeldingen te maken. 
2. Gebruik in het dialoogvenster **Kopiëren** in de sectie **Van-periode** de velden **Begindatum** en **Einddatum** om het datumbereik te definiëren waaruit u tijdsvermeldingen wilt kopiëren. 
3. Geef in de sectie **Tot-periode** in het veld **Begindatum** de datum op waarop u tijdsvermeldingen wilt maken. 
4. Selecteer **Kopiëren**. Vervolgens wordt voor de opgegeven datum in de **Tot-periode** een kopie gemaakt van de tijdsvermeldingen van de overeenkomstige dag van de week in de **Van-periode**. De tijdsvermelding van maandag van vorige week wordt bijvoorbeeld gekopieerd naar maandag voor de week die is aangegeven in de **Tot-periode**.

## <a name="import"></a>Import
Hetzelfde basisproces wordt gebruikt om te importeren uit boekingen, toewijzingen en uitwisselingen. U kunt het datumbereik opgeven waaruit de boekingen zijn geïmporteerd en vervolgens expliciet de boekingen selecteren die moeten worden gekopieerd als concept-tijdsvermeldingen. 

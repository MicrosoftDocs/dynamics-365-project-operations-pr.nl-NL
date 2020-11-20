---
title: Tijdsvermeldingen maken
description: Dit onderwerp bevat informatie over het maken van tijdsvermeldingen.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8c87f0fd2cc021bb9088d0fac73ccd52980a905
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131260"
---
# <a name="create-time-entries"></a>Tijdsvermeldingen maken

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In eerdere versies van Dynamics 365 Project Service Automation werden tijdsvermeldingen per week ingevoerd. In versie 3 van Project Service Automation worden tijdsvermeldingen per dag ingevoerd. Nadat een paar keer vermeldingen zijn gemaakt, kunt u ze bulksgewijs maken of kopiëren.

## <a name="create-a-time-entry"></a>Een tijdsvermelding maken

Volg deze stappen om een tijdsvermelding te maken.

1. Selecteer **Nieuw** op de pagina **Tijdsvermeldingen**.
2. Voer in het dialoogvenster **Snelle invoer: tijdsvermelding** de duur van de tijdsvermelding in minuten, uren of dagen in. De duur moet als volgt worden ingevoerd:  *x* minuten, *x* uur of *x* dagen. De uren en dagen kunnen ook worden ingevoerd als decimale waarden, bijvoorbeeld *x,x* uur of *x,x* dagen.
3. Selecteer het type tijdsvermelding en het project waarvoor u de tijd invoert.
4. Zoek in **het veld** Projecttaak de taak voor deze tijdsvermelding.

    > [!NOTE]
    > Als u een tijdsvermelding maakt voor een taak die niet aan een gebruiker is toegewezen, selecteert u in het veld **Projecttaak** de knop **Zoeken**, en selecteert u vervolgens **Weergave wijzigen** en **Alle actieve projecttaken** om alle taken te vermelden.

5. Voer een omschrijving in als een omschrijving vereist is en selecteer vervolgens **Opslaan en sluiten**.

Nadat de tijdsvermelding is gemaakt en opgeslagen, kunt u deze bewerken in het tijdinvoerraster. Het tijdinvoerraster ondersteunt twee indelingen:

- U kunt tijdsvermeldingen invoeren in de notatie **uu:mm**. Deze indeling wordt vervolgens geconverteerd naar uren en breuken.
- U kunt uren en breuken rechtstreeks invoeren.

Houd er rekening mee dat de fracties van een uur geen minuten zijn. 1,5 uur staat voor 1 uur en 30 minuten. Dezelfde regel geldt voor fracties van een dag. Eén dag is 24 uur en 0,5 dagen vertegenwoordigt 12 uur.

## <a name="bulk-create-time-entries"></a>Tijdsvermeldingen in bulk maken

Nadat er enkele tijdsvermeldingen zijn gemaakt, kunt u ze kopiëren en bulksgewijs extra tijdsvermeldingen maken.

1. Selecteer **Nieuw** op de pagina **Week kopiëren**.
2. Definieer in de veldgroep **Van-periode** in de velden **Begindatum** en **Einddatum** het datumbereik waaruit u tijdsvermeldingen wilt kopiëren.
3. Geef in de veldgroep **Tot-periode** in het veld **Begindatum** de datum op waarop u tijdsvermeldingen wilt maken.
4. Selecteer **Kopiëren** om een kopie te maken van de tijdsvermeldingen die overeenkomen met de dag van de week die is opgegeven in de veldgroep **Tot-periode**. De tijdsvermelding van maandag van vorige week wordt bijvoorbeeld gekopieerd naar maandag voor de week die is aangegeven in de veldgroep **Tot-periode**.

## <a name="import-data-for-time-entries"></a>Gegevens voor tijdsvermeldingen importeren

U kunt gegevens importeren uit projectboekingen en -toewijzingen. Wanneer u gegevens importeert, kunt u het datumbereik opgeven van de boekingen die u wilt importeren en vervolgens expliciet de boekingen selecteren die moeten worden gemaakt als tijdsvermeldingen in **Concept**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Functies voor groeperen op, sorteren, zoeken en filteren

U tijdsvermeldingen groeperen en filteren op de dimensies die in de kolommen zijn opgegeven. Selecteer in het veld **Groeperen op** de dimensie die u wilt gebruiken om tijdsvermeldingen te filteren. U kunt de records met tijdsvermeldingen ook in oplopende of aflopende volgorde sorteren met behulp van de sorteerpijl op de kolomkoppen. Bovendien kunt u items weergeven of verbergen door de knop **Filteren** in de kolomkoppen te selecteren en vervolgens in het **zoekvak** de tekst in te voeren die moet worden gebruikt om tijdsvermeldingen te zoeken op projectnaam, projecttaak, tijdsvermelding of resource.

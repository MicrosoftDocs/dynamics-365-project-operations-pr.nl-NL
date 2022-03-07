---
title: Een schatting maken van de verkoop en kosten van projecten wanneer een boekbare resource meerdere rollen in een project vervult
description: In dit onderwerp vindt u informatie over hoe prijsdimensies kunnen worden gebruikt om prijs- en kostenschattingen te ondersteunen voor een resource die meerdere rollen in een project vervult.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28a67e79b03dfbc38e9786350c931838ef27891a3d26787fc0334e0572528228
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990130"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Een schatting maken van de verkoop en kosten van projecten wanneer een boekbare resource meerdere rollen in een project vervult 

_**Geldt voor:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van voorradige artikelen/productieorders_ 

In projectgebaseerde bedrijven moet één resource vaak meerdere rollen in een project vervullen. Met elke rol kunnen verschillende prijzen en kosten samenhangen. Dit betekent dat voor de tijd van dezelfde resource in een project een andere financiële schatting kan gelden, afhankelijk van de factuur- en kostentarieven voor elke rol. U kunt de waarden voor de teamlidrecord voor de genoemde resource instellen met verschillende overschrijvingen voor elk van de taken waaraan het teamlid is toegewezen.

In het volgende voorbeeld wordt uitgelegd hoe door het eenvoudig overschrijven van een waarde een resource meerdere rollen in een project kan hebben met verschillende kosten- en factureringstarieven.

## <a name="create-tasks"></a>Taken maken
Als u taken wilt maken, moet u taken en overzichtstaken toevoegen, waarna u de taak toewijst voordat u de taakduur toevoegt. 

### <a name="add-tasks-and-summary-tasks"></a>Taken en overzichtstaken toevoegen
Voer de volgende stappen uit om een taak toe te voegen:

1. Ga naar **Projecten** en open het project waaraan u taken wilt toevoegen.
2. Selecteer **Nieuwe taak toevoegen**. Geef de taak een naam en druk op **Enter**.
3. Voer een andere taaknaam in en druk op **Enter**. Herhaal dit totdat u een volledige lijst met taken hebt.
3. Als u taken wilt laten inspringen onder het **overzichtstaken**, selecteert u de drie verticale stippen bij de taaknaam en selecteert u vervolgens **Een subtaak maken**. 

  > [!TIP]
  > Als u meer dan één taak wilt selecteren, selecteert u een taak en houdt u **Ctrl** ingedrukt en selecteert u vervolgens nog een taak.
  >
  > U kunt ook **Subtaak promoten** kiezen om taken te verplaatsen vanuit de **overzichts** taken.

### <a name="assign-tasks"></a>Taken toewijzen

Voer de volgende stappen uit om taken toe te wijzen.

1. In de kolom **Toegewezen aan** voor een taak selecteert u het persoonspictogram.
2. Kies een teamlid uit de lijst of voer tekst in om een naam te zoeken.

### <a name="add-task-duration-and-columns"></a>Taakduur en kolommen toevoegen

Het is vaak het gemakkelijkst om met de duur van uw project te beginnen. Voer de volgende stappen uit om een duur aan een taak toe te voegen.

1. Voer in de kolom **Duur** voor een taak het aantal dagen in dat u denkt dat het duurt om de taak te voltooien. Als u een andere tijdseenheid wilt gebruiken, voert u een getal plus het woord **uren**, **weken** of **maanden**.
2. Als u wilt dat uw taak verschijnt als een diamantvormige mijlpaal in de weergave **Tijdlijn**, voert u in de kolom **Duur** **0 dagen** in.
3. Druk op **Enter** om naar het veld **Duur** van de volgende taak te gaan en ga door met het invoeren van de duur.

  > [!NOTE]
  > U kunt geen duur invoeren voor overzichtstaken.

U kunt kolommen aan uw project toevoegen om meer details te geven. Selecteer **Kolom toevoegen** om dit te doen. 

Zie [Een project maken](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749) voor meer informatie.

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>De rol en organisatie-eenheid instellen voor een algemeen projectteamlid
Voer de volgende stappen uit om een rol en organisatie-eenheid in te stellen voor een algemeen teamlid.

1. Selecteer op de pagina **Taken** de rij **Taak** voor **Taak A**. 
2. Selecteer bij **Toegewezen aan** **Generieke resource toevoegen**. Hiermee wordt de pagina **Snelle invoer voor teamleden** geopend.
3. Geef op de pagina **Snelle invoer voor teamleden** de kenmerken op van het algemene teamlid dat deze taak kan uitvoeren.
4. Selecteer de juiste rol en organisatie-eenheid en selecteer vervolgens **Opslaan en sluiten**. Er wordt een algemeen teamlid gemaakt en toegewezen aan deze taak. 
5. Herhaal stap 1-4 voor **Taak B**. Voor **Taak B** moeten echter een andere rol en organisatie-eenheid worden toegewezen aan het generieke teamlid dan voor **Taak A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>De rol en organisatie-eenheid instellen voor een projecttaak
Voer de volgende stappen uit om een rol en organisatie-eenheid in te stellen voor een taak.

1. Nadat u **Taak A** hebt gemaakt, selecteert u de taak en selecteer het pictogram **i** om het deelvenster **Taakdetails** te openen. 
2. Scrol in het deelvenster **Taakdetails** naar beneden en selecteer **Details bekijken** om de pagina **Taakdetails** te openen.
3. Op de pagina **Taakdetails** voegt u bij **Rol** en **Organisatie-eenheid** de waarden toe die nodig zijn om deze taak voor de resource uit te voeren. 

  > [!NOTE]
  > Als u dit scenario voltooit met de demogegevens van Project Operations, selecteert u **Adviserend leider** voor de rol en **Fabrikam US** als de organisatie-eenheid.

4. Selecteer **Taak B** en vervolgens de taak.
5. Selecteer het pictogram **i** om het deelvenster **Taakdetails** te openen. 
6. Scrol in het deelvenster **Taakdetails** naar beneden en selecteer **Details bekijken** om de pagina **Taakdetails** te openen.
7. Op de pagina **Taakdetails** voegt u bij **Rol** en **Organisatie-eenheid** de waarden toe die de resource nodig heeft om deze taak uit te voeren. De waarden in **Rol** en **Organisatie-eenheid** voor **Taak B** moet anders zijn dan die voor **Taak A**. 

  > [!NOTE]
  > Als u dit scenario voltooit met de demogegevens van Project Operations, selecteert u **Netwerktechnicus** voor de rol en **Fabrikam US** als de organisatie-eenheid.

8. Sla op en sluit de pagina **Taakdetails**. 

## <a name="team-member-and-estimates-behavior"></a>Teamlid en gedrag van schattingen 
Als u het gedrag van het raster **Teamlid** en de schattingen wilt begrijpen, voert u de volgende stappen uit.

1. Selecteer in het raster **Teamlid** de twee algemene teamleden en selecteer vervolgens **Vereisten genereren**. Vervolgens worden er resourcevereisten gegenereerd. 
2. Selecteer de teamlidrij voor **Adviserend leider** en selecteer vervolgens **Boeken**. Het planbord wordt geopend met een lijst met resources. Selecteer een resource en vervolgens **Boeken** om de resource voor die vereiste te boeken.
3. Selecteer de teamlidrij voor **Netwerktechnicus** en selecteer vervolgens **Boeken**. Het planbord wordt geopend met een lijst met resources. Selecteer dezelfde resource als hierboven en vervolgens **Boeken** om de resource voor die vereiste te boeken.

### <a name="team-member-grid"></a>Het raster Teamlid 

In het raster **Teamlid** worden de twee generieke teamlidrecords verwijderd en vervangen door slechts één resource. Er is één set waarden voor die resource met een standaardset waarden voor **Rol** en **Organisatie-eenheid**.

Wanneer u de rij voor dat teamlidrecord uitvouwt, kunt u voor beide taken verschillende toewijzingen in de teamlidrecord zien. Elke toewijzingsrij bevat taakspecifieke waarden voor **Rol** en **Organisatie-eenheid**. 

### <a name="estimates-grid"></a>Het raster Schattingen 

In het raster **Schattingen** zijn voor beide toewijzingen voor dezelfde resource verschillende prijzen opgenomen. De toewijzing voor de resource voor **Taak A** wordt geprijsd met de kenmerkwaarde **Adviserend leider** voor **Rol**. De toewijzing voor dezelfde resource voor **Taak B** wordt geprijsd met de kenmerkwaarde **Netwerktechnicus** voor **Rol**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
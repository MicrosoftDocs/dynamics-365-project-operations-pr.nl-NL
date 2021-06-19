---
title: Een schatting maken van de verkoop en kosten van projecten wanneer een boekbare resource meerdere rollen voor een project vervult
description: Dit onderwerp biedt informatie over hoe prijsdimensies kunnen worden gebruikt om prijzen en kosten te ondersteunen voor een resource die meerdere rollen in een project vervult.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013255"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Een schatting maken van de verkoop en kosten van projecten wanneer een boekbare resource meerdere rollen voor een project vervult 

[!include [banner](../includes/psa-now-project-operations.md)]

In bedrijven die op projectbasis werken, moet één resource vaak meerdere rollen in een project vervullen. Voor elk van deze rollen kunnen verschillende prijzen en kosten worden ingesteld, wat betekent dat de tijd van dezelfde resource aan het project een andere financiële schatting kan krijgen, afhankelijk van de rekening en kostentarieven voor elk van de rollen. In Project Service Automation kunnen de waarden in de teamlidrecord voor de genoemde resource worden ingesteld en kunnen verschillende overschrijvingen worden uitgevoerd voor elk van de taken waaraan het teamlid is toegewezen.

In het volgende voorbeeld wordt uitgelegd hoe door een eenvoudige overschrijving van deze waarde een resource meerdere rollen in een project kan hebben met verschillende kosten- en factureringstarieven.

## <a name="create-tasks"></a>Taken maken
Maak twee projecttaken van elk 40 uur: Taak A en Taak B. Selecteer Taak A als een voorgaande taak van Taak B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Rol en organisatie-eenheid instellen voor een algemeen projectteamlid

1. Selecteer op de pagina **Planning** de rij **Taak** voor Taak A. 
2. Selecteer in het veld **Resources** de optie **Maken** in de vervolgkeuzelijst.
3. Geef op de pagina **Snelle invoer voor teamleden** de kenmerken op van het algemene teamlid dat deze taak kan uitvoeren.
4. Selecteer de juiste rol en organisatie-eenheid en selecteer vervolgens **Opslaan en sluiten**. Er wordt een algemeen teamlid gemaakt en toegewezen aan deze taak. 

Herhaal deze stappen voor taak B en zorg ervoor dat de rol en organisatie-eenheid van het algemene teamlid dat voor taak B is gemaakt, afwijken van die voor taak A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Rol en organisatie-eenheid instellen voor een projecttaak

1. Nadat u taak A hebt gemaakt, selecteert u de taak en vervolgens selecteert u **Taak bewerken**.
2. Zoek op de pagina **Taakdetails** naar de velden **Rol** en **Organisatie-eenheid** en voeg de waarden toe die vereist zijn voor een resource die deze taak zou uitvoeren. 

  > [!NOTE]
  > Als u deze scenario's voltooit met demogegevens van Project Service Automation, selecteert u **Adviesleider** voor de rol en **Fabrikam US** als de organisatie-eenheid.

3. Selecteer Taak B en selecteer vervolgens **Taak bewerken**.
4. Zoek op de pagina **Taakdetails** naar de velden **Rol** en **Organisatie-eenheid** en voeg de waarden toe die vereist zijn voor een resource die deze taak zou uitvoeren. Zorg ervoor dat de waarden in de velden **Rol** en **Organisatie-eenheid** anders zijn voor taak B dan de waarden voor taak A. 

  > [!NOTE]
  > Als u deze scenario's voltooit met demogegevens van Project Service Automation, selecteert u **Netwerktechnicus** voor de rol en **Fabrikam US** als de organisatie-eenheid.

5. Sla op en sluit de pagina **Taakdetails**. 

## <a name="team-member-and-estimates-behavior"></a>Teamlid en gedrag van schattingen 

1. Selecteer op de pagina **Taakdetails** voor **Teamlid** de twee algemene teamleden en selecteer vervolgens **Vereisten genereren**. 
2. Selecteer de teamlidrij voor **Adviesleider** en selecteer vervolgens **Boeken**. Het planbord wordt geopend en er wordt een resource voor die vereiste geboekt.
3. Selecteer de teamlidrij voor **Netwerktechnicus** en selecteer vervolgens **Boeken**. Het planbord wordt geopend en dezelfde resource wordt voor die vereiste geboekt.

### <a name="team-member-grid"></a>Het raster Teamlid 
In het raster **Teamlid** zijn de twee generieke teamlidrecords verwijderd en vervangen door één resource. Er is één set waarden voor die resource met een standaardverzameling waarden voor **Rol** en **Organisatie-eenheid**.
Wanneer u de rij van die teamlidrecord uitvouwt, kunt u voor beide taken verschillende toewijzingen in de teamlidrecord zien. Elke toewijzingsrij bevat taakspecifieke waarden voor **Rol** en **Organisatie-eenheid**. 

### <a name="estimates-grid"></a>Het raster Schattingen 
Wanneer u naar het raster **Schattingen** navigeert, ziet u dat de toewijzingen voor dezelfde resource verschillend zijn geprijsd.
De toewijzing voor de resource voor Taak A wordt geprijsd met de kenmerkwaarde **Adviesleider** voor **Rol**. De toewijzing voor dezelfde resource voor Taak B wordt geprijsd met de kenmerkwaarde **Netwerktechnicus** voor **Rol**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
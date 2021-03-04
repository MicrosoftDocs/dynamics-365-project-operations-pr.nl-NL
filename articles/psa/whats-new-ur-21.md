---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 21, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 21, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b1194c1cf1997b68030fe88360c6ebb756c715fd
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147017"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, updaterelease 21, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 21. Deze versie heeft buildnummer V 3.10.32.50 en is algemeen beschikbaar via een zelfupdate in juni 2020.

## <a name="update-release-21"></a>Updaterelease 21

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost:

- Bij het hosten van het besturingselement **Tijdinvoerraster** in Dashboards gebruikt het raster niet de volledige breedte van de dashboardrastercontainer.
- Voor specifieke tijdzones geeft het rasterbesturingselement **Tijdinvoer** geen records weer.
- Tijdinvoer van na 21.00 uur verschijnt op de verkeerde dag.
- Gebruikers kunnen geen onkosten indienen als de onkostencategorie **Betalingsbewijs vereist** geen waarde bevat.

**Resourcebeheer**

De volgende problemen zijn opgelost:

- Inactieve boekingen worden weergegeven in de weergave **Afstemming**.
- Er ontbrak validatie aan algemene resource-vervulling om ervoor te zorgen dat er een geldige boekingsstatus bestaat.

**Projectbeheer**

De volgende problemen zijn opgelost:

- De **Project** formulierrasters ( **Resourcetoewijzing**, **Taak**, weergave **Afstemming**, **Onkostenschattingen**) blijven bewerkbaar, ook als een project niet actief is.
- Dubbele klanten kunnen niet worden samengevoegd met klanten die zijn gekoppeld aan bevestigde projectcontracten.
- Wanneer een resource zonder geldige kalender agenda wordt toegevoegd, geeft het systeem geen gebruiksvriendelijke foutmelding.
- De knop **Taak toevoegen** op het taakraster is ingeschakeld wanneer het project is gekoppeld aan **Microsoft project-invoegtoepassing**.
- Inspanning groeit oncontroleerbaar wanneer een taak met een categorie wordt toegewezen aan een resource met een rol waarvoor een kostprijs is gedefinieerd.

**Sales**

De volgende verbeteringen zijn aangebracht:

- **Factuurfrequentie** en **Begin facturering** zijn verplaatst naar het tabblad **Factuurschema**.

De volgende problemen zijn opgelost:

- **Totale verkoopprijs** is nul (0) voor **Categorie** ondanks dat **Rol** een totale verkoopprijs heeft die niet nul is.
- Klanten kunnen de waarde van het veld **Factuurstatus** niet wijzigen in **Gereed voor facturering** wanneer een ander aangepast proces een extra veld bijwerkt.
- De knop **Factuurregels vernieuwen** kan meerdere gedupliceerde regels maken als deze herhaaldelijk wordt geselecteerd.
- De knop **Prijzen bijwerken** werkt niet in het subraster **Rolprijzen** in het formulier **Snelle weergave**.
- De logica voor **Oplossing verkoopprijslijst** behandelt tijdzones onjuist, wat resulteert in de verkeerde selectie van prijslijsten.
- De **Totale werkelijke kosten** van een project kunnen een fractie afwijken nadat een enkele tijdpost is goedgekeurd.
- De logica voor **Prijsoplossing** geeft geen gebruiksvriendelijke foutmelding if **Opgehaalde rolprijs** geen waarden bevat in de velden **'Primaire eenheid'** en **'Prijs in primaire eenheid'**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
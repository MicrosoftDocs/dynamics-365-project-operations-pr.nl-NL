---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 24, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 24, v3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074516"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, updaterelease 24, v3

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 24. Deze versie heeft het buildnummer V 3.10.42.43 en is algemeen beschikbaar via een zelf-update vanaf oktober 2020.

## <a name="update-release-24"></a>Updaterelease 24

### <a name="bug-fixes"></a>Opgeloste fouten

**Sales**

De volgende problemen zijn opgelost:

- Probleem bij het instellen van de standaardprijslijst van producten.
- De prestaties van Prijsopgave winnen zijn traag vanwege de ingesloten prijslijst en het kopiëren van de rolprijsrecords.
- **Projectcontract/Verkoophub** > **Productregelartikel/Orderregelhoeveelheid** wordt automatisch afgerond op het dichtstbijzijnde gehele getal.
- Stel systeemprivileges in bij het lezen van prijslijsten.
- Kopieer de klantadresvelden **address1_freighttermscode** en **address1_shippingmethodcode** naar Prijsopgave/Order. 


**Tijd en onkosten**

De volgende problemen zijn opgelost:

- Het **tijdinvoerraster** biedt geen ondersteuning voor het gedrag van de tijd **Alleen datum**.
- **Tijdsvermelding** wordt niet automatisch vernieuwd. Handmatig vernieuwen is vereist.
- De tijdsvermeldingen van een toewijzing kunnen niet worden geïmporteerd als er een pauze (0 uur) is opgenomen in de toewijzingen van een resource.
- Stel bij het maken van een tijdsvermelding het begin op dezelfde waarde in als **msdyn_date**.
- Schakel bulkbewerking opnieuw in voor tijdsvermeldingen.

**Resourcebeheer**

De volgende problemen zijn opgelost:

- Als u de status van een interdagboeking zonder vereiste probeert bij te werken, wordt een null-ref-uitzondering gegenereerd.
- Fout bij het laden van de weergave **Vereffening**.


**Projectbeheer**

De volgende problemen zijn opgelost:

- Wanneer u in **Projectplanning** de waarde **Handmatig** in **Auto** wijzigt, wordt automatisch opslaan niet voltooid.
- Onkosten mogen niet worden meegerekend voor variantie in het raster **Projectschattingen**.
- Inconsistent gedrag voor kolommen op het tabblad **Schattingen** tijdens het laden en het wijzigen van het type **Tijdsfase**.
- De werkelijke kosten van een project komen mogelijk niet overeen met de totalen van **Werkelijke waarden**.
- **Geschatte einddatum** op het tabblad **Samenvatting** komt niet overeen met de **WBS-planning**.
- **Werkelijke uren bijwerken** werkt niet bij verkleinen van inspringing.
- Een projectmanager buiten de hoofdmap **BU** kan geen project maken.
- Wijzigingen in taak of categorie voor **Kostenramingen** worden niet bewaard.
- **Kopie van contract** kopieert de factuurplanningen en de uitvoeringsstatus.
- De knop **Werkelijke waarden vernieuwen** berekent overzichtstaken onjuist.
- Microsoft Project-invoegtoepassing: herstel de fout met de null-referentie als een teamlid een lege resource-eenheid heeft.


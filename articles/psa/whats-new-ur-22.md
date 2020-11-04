---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 22, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 22, v3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074512"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, updaterelease 22, v3

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 22. Deze versie heeft buildnummer V 3.10.33.48 en is algemeen beschikbaar via een zelfupdate in juni 2020.

## <a name="update-release-22"></a>Updaterelease 22

### <a name="bug-fixes"></a>Opgeloste fouten



**Tijd en onkosten**

De volgende problemen zijn opgelost:

- **Tijdsvermeldingen** worden na het importeren niet automatisch toegevoegd aan het tijdsvermeldingenschema.
- De datumkiezer van het raster **Tijdsvermelding** herkent de regionale instellingen van een gebruiker niet.

**Resourcebeheer**

De volgende problemen zijn opgelost:

- In handmatige modus worden wijzigingen in **Resourcetoewijzings** contouren niet herkend bij het genereren van **Resourcevereisten**.
- **Resourceaanvragen** ondersteunen geen aangepaste aanvraagstatussen.

**Projectbeheer**

De volgende problemen zijn opgelost:

- Als u dubbelklikt op EstimateGridControl, worden getallen in de Nederlandse indeling niet correct geparseerd.
- Toegewezen uren worden niet correct bijgewerkt wanneer toewijzingen worden gewijzigd met de Microsoft Project-desktopclient-invoegtoepassing.
- De rasters voor Projecten bijhouden en Schattingen geven een onjuiste valutacode voor verkoop weer wanneer de contractvaluta anders is dan de valuta van de klant en de organisatie is geconfigureerd om valutacodes weer te geven in plaats van valutasymbolen.
- De einddatum van een teamlid telt één dag op als het werkuurschema 24 uur per dag is.
- In de projectplanning leidt het toevoegen van een transactiecategorie aan een taak niet tot automatisch opslaan.
- De volgende fout wordt weergegeven bij het toevoegen van een teamlid aan de projectsjabloon: "Resourcevereisten kunnen niet worden gekoppeld aan projectsjablonen". 
- Lintregelscript "msdyn.Approval.CanApproveOrReject" geeft een time-outfout weer.

**Sales**

De volgende problemen zijn opgelost:

- Validatiefoutbericht wordt niet weergegeven wanneer een kostprijslijst is geselecteerd bij het opzoeken van prijslijsten op het formulier/de entiteit 'Projectprijslijst nieuwe prijsopgave'.
- Als u de prijsopgave als gewonnen sluit, navigeert u niet naar het gemaakte contract als een BPF die aan de prijsopgave is gekoppeld, zich in de laatste fase bevindt.
- Omkeren van **Niet-gefactureerde verkopen** is gekoppeld aan de oorspronkelijke kosten wanneer een tijdsvermelding wordt teruggeroepen.
- Nadat u de knop **Bevestigen** hebt geselecteerd, verandert de factuurstatus niet in **Bevestigd** tenzij de factuur wordt vernieuwd.
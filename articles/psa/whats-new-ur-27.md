---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 27, v3
description: In dit artikel worden de functies en oplossingen vermeld die beschikbaar zijn in Project Service Automation-updateversie 27, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912924"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 27, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 27, V3. Deze versie heeft het buildnummer V3.10.45.98 en is algemeen beschikbaar via een zelf-update vanaf januari 2021.

## <a name="update-release-27"></a>Updateversie 27

### <a name="bug-fixes"></a>Opgeloste fouten

**Algemeen**

De volgende problemen zijn opgelost:

- Logboeken die zijn gegenereerd door invoegtoepassingen in Project Service Automation, zijn niet ingesteld op automatisch verwijderen.
- Automatische upgrade mislukt omdat de Project Service Automation-oplossing een oud null NavBarArea- en titelelement bevat.

**Tijd en onkosten**

De volgende problemen zijn opgelost:

- Het raster voor **Tijdsvermelding** geeft onjuiste gegevens weer voor **Tijdzone-onafhankelijk** gegevensgedrag.
- Het raster voor **Tijdsvermelding** maakt een onjuiste tijd voor **Tijdzone-onafhankelijk** gegevensgedrag.
- Het opzoeken van taken is niet beperkt tot het geselecteerde project op de pagina **Tijdsvermelding bewerken**.
- Tijdgoedkeuringen voor niet-projectgebonden tijdsvermeldingen is geblokkeerd, omdat het systeem zoekt naar een projectfiatteur.
- Correcte invoer in Werkelijke waarden geeft een onjuist foutbericht weer.
- Wanneer een taak een null-waarde voor de werkelijke kosten bevat en de projecttotalen worden vernieuwd, treedt de volgende fout op: 'Gegeven sleutel niet aanwezig in woordenboek'.
- In specifieke gevallen geven filters voor **Groeperen op** op de pagina **Projectschatting** geen onkostenramingen weer.
- **Zomertijd**-interval is niet correct voor tijdsvermeldingen.

**Projectbeheer**

De volgende problemen zijn opgelost:

- Verbeteringen in het cachegeheugen, waardoor de prestaties bij het laden van de pagina **Project** verbeteren.
- Verouderde bedrijfsregel waardoor projecttaken niet kunnen worden voltooid.
- De contouren van de Microsoft Project-invoegtoepassing respecteren de agenda van de invoegtoepassing niet, wat resulteert in onjuiste resourcevereisten.
- Door projecten te maken op basis van sjablonen, worden toewijzingsdatums onjuist ingesteld en kunnen er geen resourcevereisten worden gegenereerd.
- Gebruiker heeft geen toegang tot de opties **Categorie**, **Omschrijving**, **Toestand** bij gebruik van het toetsenbord.
- Werkelijke verkoopwaarden van het project zijn exclusief kosten en materiaalverkoopwaarden.
- Aggregatie van werkelijke verkopen en werkelijke kosten verloopt niet goed bij verschillende wisselkoersen.
- De beschrijving in de **Standaard werkurensjabloon** is misleidend.
- Door inspringen van een taak wordt **Categorie** pas verwijderd in de gebruikersinterface wanneer deze wordt vernieuwd.
- Ontbrekende validatie om ervoor te zorgen dat het verplaatsen van een project na de einddatum niet toegestaan is.

**Sales**

De volgende problemen zijn opgelost:

- Een null-referentie-uitzondering wordt gegenereerd op een projectprijsopgaveregel omdat **Importeren vanuit projectschatting** zichtbaar is wanneer er geen project is geselecteerd.
- De volgende fout 'Objectverwijzing niet ingesteld op een exemplaar van een object' treedt op bij het afsluiten van een prijsopgave als **Binnengehaald**.
- De correctiestatus is niet ingesteld tijdens terugboeken van werkelijke waarden bij het loskoppelen van een project van een contractregel.
- Wanneer Dynamics 365 Field Service en Project Service Automation beide zijn geïnstalleerd, worden de opties **Prijzen vergrendelen** en **Huidige prijzen gebruiken** niet tegelijkertijd weergegeven op de pagina **Factuur**.
- Voor de Japanse taal is er een inconsistente vertaling met andere agendagebaseerde pagina's.
- **Activeren** en **Deactiveren** zijn verwijderd uit **Prijslijstkoppeling** entiteiten in Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 26, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 26, v3.
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
ms.openlocfilehash: cebfcd6425f11b74ce6331a093d8d3db3da356a0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577276"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, updaterelease 26, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 26, V3. Deze versie heeft buildnummer V3.10.44.59 en is algemeen beschikbaar via een zelfupdate in december 2020.

## <a name="update-release-26"></a>Updaterelease 26

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost:

- Gebruikers kunnen de taak wijzigen voor een tijdsvermelding die is goedgekeurd/ingediend.
- "Objectreferentie niet ingesteld"-fout bij het opslaan van tijdsvermelding.
- Bij het importeren van tijdsvermeldingen uit resourcetoewijzingen worden tijdsvermeldingen gemaakt met de onjuiste DateTime-waarden.
- Wanneer Project Service Automation en de Field Service-app beide zijn geïnstalleerd, wordt de knop **Nieuw** twee keer weergegeven op de opdrachtbalk voor tijdsvermeldingen in de Field Service-app.
- Celupdates voor **Eenheid toestaan** en **Eenhedengroep** werken nu in het raster **Onkostenschattingen**.
- Formulier **Update tijdsvermelding bewerken** omvat **Tijdlijn**.
- Tijdgoedkeuringen voor niet-projectgebonden tijdsvermeldingen blokkeren het systeem bij het zoeken naar een projectgoedkeurdersrol.

**Resourcebeheer**

De volgende problemen zijn opgelost:

- Validatie toegevoegd in de invoegtoepassing **PostprojectCreate** om te controleren op een primaire vereiste voordat u deze maakt.
- Formulier voor snelle invoer van **projectteamlid** genereert een null-verwijzingsuitzondering als velden uit het formulier worden verwijderd.
- Het genereren van vereisten voor 12 uur gedurende 1 jaar zal mislukken.
- Verbeterde foutmelding voor null-verwijzingsuitzondering tijdens het maken van resourcevereisten.

**Projectbeheer**

De volgende problemen zijn opgelost:

- Verbeterde validatie om een null-verwijzingsuitzondering op te lossen die is gegenereerd in de invoegtoepassing **PreprojectUpdate**.
- Projecten die zijn gepubliceerd door de Microsoft Project-desktopinvoegtoepassing, verwijderen niet-toegewezen toewijzingen.
- Nieuwe validatie toegevoegd wanneer de projectverwijzing van een taak ongeldig is vanwege een null-verwijzingsuitzondering in de invoegtoepassing **PreValidateprojectTaskUpdate**.
- Het raster Teamlid toont geen afzonderlijke toewijzingen in de teamlidrecord.
- Nieuwe validatie- en foutmeldingen toegevoegd vanwege een null-verwijzingsuitzondering in de invoegtoepassing **PreprojectTaskDelete**.

**Sales**

De volgende problemen zijn opgelost:

- Bij het selecteren van een projectgebaseerde regel in een prijsopgave of contract, mag de knop **Suggestie** alleen zichtbaar zijn bij het selecteren van een productgebaseerde regel die is gekoppeld aan een bestaand product.
- Splits bevoegdheid **Create_Product** van bevoegdheid **Create_ProjectContract**.
- Het verwijderen van een factuurregel veroorzaakt een null-verwijzingsfout op **MarkReadyToInvoiceForproductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

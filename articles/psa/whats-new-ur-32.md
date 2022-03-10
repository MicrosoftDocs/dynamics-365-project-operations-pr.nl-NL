---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 32, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 32, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994855"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 32, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 32. Deze versie heeft het buildnummer V3.10.53.108 en is algemeen beschikbaar via een zelfupdate in juni 2021.

## <a name="update-release-32"></a>Updaterelease 32

### <a name="bug-fixes"></a>Opgeloste fouten

#### <a name="general"></a>Algemeen

- Wanneer een grote upgrade mislukt, moeten alleen de belangrijkste toegangspunten van de toepassing worden geblokkeerd om ervoor te zorgen dat gedeelde entiteiten nog steeds toegankelijk zijn.

#### <a name="time-and-expense"></a>Tijd en onkosten

De volgende problemen zijn opgelost:

- Met **TimeEntriesImportFromResourceAssignment** worden de begin- en eindtijden van het toewijzingscontoursegment van de resource niet behouden.
- Wanneer u **Vermelding openen** in het raster **Tijdsvermelding** selecteert, is het mogelijk dat u geen andere formulieren kunt selecteren.
- Terwijl u toewijzingen importeert naar tijdsvermeldingen, kan de clientcodequery een lange URL genereren die mislukt voor de query.
- In het raster **Tijdsvermelding** blijft de focus, nadat een waarde uit een cel is verwijderd, niet in het raster.
- De knop **Afwijzen** is verwijderd uit de weergave **Goedkeuringen verwerken** voor moderne goedkeuringen.
- De stabiliteit en prestaties van bulkgoedkeuring voor tijdsvermeldingen worden beïnvloed door impasses en het niet adequaat afhandelen van aanpassingen die verband houden met de entiteit **Tijdsvermelding**.

#### <a name="project-planning"></a>Projectplanning

- Er wordt een null-referentie-uitzondering gegenereerd wanneer u een project bijwerkt dat een null-waarde heeft in het veld **Contracterende eenheid**.
- Met **Projecttotalen vernieuwen** worden de resterende kosten en resterende verkopen van een project onjuist berekend.
- Overbodige prijsberekeningen zijn van invloed op de prestaties die verband houden met updates van de resourcetoewijzingscontouren.

#### <a name="resource-management"></a>Resourcebeheer

Het volgende probleem is opgelost:

- Wanneer de agendacapaciteit van een boekbare resource meer dan 1 is, herkent Project Service Automation de capaciteit ten onrechte als 0 (nul). Daarom treedt er een oneindige lus op in de planningsweergave.

#### <a name="sales"></a>Verkoop

De volgende problemen zijn opgelost:

- Wanneer een journaalregel wordt gemaakt met een aangepast transactietype, treedt de volgende null-referentie-uitzondering op: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Rollen en categorieën die zijn gedeactiveerd voordat een offerte wordt gekopieerd, mogen niet worden toegevoegd aan factureerbare rollen en categorieën van de nieuw gekopieerde offerte.
- De documentdatum en boekhouddatum komen niet overeen met de begindatum die is opgegeven op een factuurregeldetail dat rechtstreeks op een conceptfactuur wordt aangemaakt.
- Null-referentie-uitzonderingen worden gegenereerd in scenario's die verband houden met het deactiveren van rollen en categorieën voordat een offerte wordt gekopieerd.
- Met de actie **Prijzen bijwerken** op de pagina **Projecten** worden geen kostenschattingen en materiaalschattingen bijgewerkt.

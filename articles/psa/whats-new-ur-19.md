---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 19, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 19, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ad61589125e42e8dceb462290f65ddc05e171bd828d26d34ebd548ca285e9aa4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993640"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, updaterelease 19, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor PSA v3, updaterelease 19. Deze versie heeft een buildnummer van V3.10.30.41 en is algemeen beschikbaar via een zelfupdate in mei 2020.

## <a name="update-release-19"></a>Updaterelease 19

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost: 

- Fouten die zijn afgeleid van geïmporteerde tijdsvermeldingen, worden niet correct weergegeven.
- Tijdsvermeldingsraster ondersteunt niet velden van het type **Alleen datum**.
- Projectresources kunnen geen kosten maken met een project.

**Projectbeheer**

De volgende problemen zijn opgelost: 

-  Dieper onderliggende taak veroorzaakt een onjuiste inspanningsschatting tijdens de voltooiingsberekening (EAC).

**Sales**

De volgende problemen zijn opgelost: 

- De actie **Herberekenen** werkt niet met onkostencontractregeldetails of prijsopgaveregeldetails.
- **Prijzen bijwerken** ontbreekt voor kostenramingen.
-  Klanten kunnen geen redenen voor aangepaste contractstatus selecteren op de pagina **Projectcontract**.
- Klanten ervaren verminderde prestaties bij het maken van een aangepaste prijslijst op basis van een prijsopgave.
- Klanten ervaren inconsistenties met standaardwaarden voor **eenheid** op de pagina's **Prijsopgaveregeldetails** en **Contractregeldetails**.
- Als niet-toerekenbare transactiecategorie-items worden toegevoegd aan een toerekenbare contractregel, wordt geen rekening gehouden met het factureringstype **Niet-toerekenbaar** van de transactiecategorie.
- Klanten kunnen de nieuw toegevoegde rollen en categorie niet gebruiken in eerder gemaakte contracten.
- Klanten ervaren verminderde prestaties door onnodig ophalen in PreValidateprojectTeamMemberUpdate.cs
- Rollen die zijn ingesteld als niet-toerekenbaar in de lijst **Resourcecategorieën**, moeten aan het tabblad **Toerekenbare rollen** worden toegevoegd als **Niet-toerekenbaar** op de contractregel voor een project.
- Klanten kunnen verminderde prestaties ervaren bij het maken van een project omdat met **GetBookableResourceIdFromUser** alle kolommen met boekbare resources worden opgehaald in plaats van alleen de primaire id.
- In de entiteit **TransactionType** ontbreekt de update-invoegtoepassing voor prevalidatie die voorkomt dat gebruikers **Eenheden** en **UnitGroups** invoeren die niet geldig zijn voor transactietypen.
- De stap **Verwijderen** werkt niet voor het importeren van tijdsvermeldingen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
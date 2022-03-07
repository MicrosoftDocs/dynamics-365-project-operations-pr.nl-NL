---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 20, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 20, v3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 9939e2f354b69dcbc304f4f6e2ac41a00f251fed69f37978059f4053335ee651
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993595"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, updaterelease 20, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 20. Deze versie heeft buildnummer V 3.10.31.37 en is algemeen beschikbaar via een zelfupdate in juni 2020.

## <a name="update-release-20"></a>Updaterelease 20

### <a name="bug-fixes"></a>Opgeloste fouten

**Projectbeheer**

De volgende problemen zijn opgelost:

- Het importeren van projectteamleden met een toewijzingsmethode waarvoor uren nodig zijn, resulteert in een onduidelijk foutbericht wanneer de opgegeven uren nul zijn.
- Gebruikers ontvangen een onjuiste fout wanneer het maximale aantal tekens is ingevoerd in het veld **Omschrijving** voor een projecttaak.
- De pagina **Invoegtoepassing Microsoft Dynamics 365 Project Service Automation downloaden** verwijst door naar de Engelse downloadpagina wanneer de taalinstellingen van de gebruiker zijn ingesteld op Japans.
- Als er een serverfout optreedt, blijft het synchronisatielabel op het tabblad **Schema** van het formulier **Projecten** soms bestaan.
- Bij het wijzigen van een taak worden redundante taakupdates naar de server gestuurd.

**Sales**

De volgende problemen zijn opgelost:

- Als op het formulier **Contract** wordt gedubbelklikt op **Factuur maken**, worden twee facturen gemaakt voor één record met werkelijke waarden.
- In Internet Explorer11 kunnen gebruikers geen onkostenboekingen maken.
- Terugboeking van kosten en terugboeking van niet-gefactureerde werkelijke verkoopwaarden zijn niet gekoppeld.
- Met de knop **Werkelijke waarden vernieuwen** op het formulier **Project** worden niet de **Werkelijke taakuren** vernieuwd.
- De invoegtoepassing **PreValidateprojectTeamMemberCreate** kan dubbele generieke boekbare resources creëren wanneer het kenmerk **msdyn_isgenericresourceprojectscoped** op **Onwaar** is ingesteld.
- Met **Herberekenen** wist u de toerekenbare kosten van productgebaseerde prijsopgaveregeldetails en contractregeldetails.
- In specifieke scenario's geeft de invoegtoepassing **PostEstimateLineUpdate** een uitzonderingsfout met een null-referentie weer.
- De duur van de tijdsfase in de grafiek **Winstgevendheidsanalyse** komt niet overeen met de duur van de kosten in de prijsopgaveregeldetails voor de vaste prijs.
- Eenheids- en eenheidsgroepwaarden worden niet correct standaard ingesteld voor onkostencategorieën in de formulieren **Contractregeldetails** en **Prijsopgaveregeldetails**.
- De lijsten met **Kostprijs organisatie-eenheid** staan overlappingen in de geldigheidsdatums toe.
- Het is gebruikers niet toegestaan **OrgUnit** te wijzigen wanneer het ordertype niet op werk is gebaseerd omdat dit zal leiden tot een uitzonderingsfout met een null-referentie.
- Wanneer u uit het formulier **Prijsopgaveregeldetails** probeert terug te gaan naar het tabblad **Prijsopgave**, wordt het formulier vernieuwd en verschijnt het tabblad **Overzicht**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
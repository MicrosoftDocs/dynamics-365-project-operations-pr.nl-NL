---
title: Nieuw in september 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations van september 2021 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06f23630ef0205394f376e5bb93a29ae8a9eab15
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582888"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuw in september 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

*Van toepassing op: Project Operations voor scenario's op basis van resources/niet-voorradige artikelen*

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

   - Project Operations in Microsoft Dataverse-omgeving versie 4.14.0.99.
   - Projectbeheer en financiële administratie in Dynamics 365 Finance-omgeving versie 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release. Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Bepaalde functies en mogelijkheden werken mogelijk niet correct als niet de meest recente versie van de toewijzing is geactiveerd. U kunt de actieve versie van de toewijzing zien op de pagina **Twee keer wegschrijven** in de kolom **Versie**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de kaart, volgt u de instructies in de [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Tijd en onkosten | 1811407 | De beveiligingsrol Projectgoedkeurder is aangepast voor goedkeuringen van onkostenposten. |
| Tijd en onkosten | 1811438 | De beveiligingsrol Projectgoedkeurder is aangepast voor annulering van goedkeuringen van tijdsvermeldingen. |
| Tijd en onkosten | 2370126 | De pictogrammen **Projecttaak** en **Rol** zijn bijgewerkt in de entiteit **Tijdsvermelding**. |
| Tijd en onkosten | 2379879 | De functie **Week kopiëren** is gecorrigeerd in tijdsinvoer bij gebruik van Dynamics 365 voor telefoons. |
| Facturering en prijzen | 2371906 | Het totale bedrag van de pro-formafactuur mag niet worden aangepast in Project Operations voor implementaties op basis van resources. |
| Facturering en prijzen | 2385802 | De fout die optreedt bij negatieve werkelijke uren wanneer projecttotalen worden vernieuwd is opgelost. |
| Facturering en prijzen | 2389675 | Bevestigingsgedrag voor pro-formafacturen is verbeterd. De entiteit voor langlopende taken moet rekening houden met de activiteit die nodig is om bevestigingsresultaten voor de boekhouding weg te schrijven. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Reizen en onkosten | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | De bedragen voor leveranciers- en btw-transacties die zijn geboekt op basis van een onkostenpost die is gemaakt op basis van een creditcardtransactie zijn onjuist. |
| Reizen en onkosten | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Er worden onjuiste vereffeningsregels gemaakt bij het genereren van het betalingsdagboek. |
| Reizen en onkosten | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | De bedragen voor btw-transacties die zijn geboekt op basis van een onkostenpost die is gemaakt op basis van een creditcardtransactie zijn onjuist. |
| Reizen en onkosten | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Het verwijderen van een onkostenregel kan lang duren. |
| Projectboekhouding | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Nadat u KB 4619395 hebt toegepast, wordt het wijzigen van de nummerreeks in **Doorlopend** niet ondersteund en wanneer u een schatting plaatst, treedt de fout "Systeem biedt geen ondersteuning voor instelling 'doorlopend' van nummerreeks Proj_X" op. |
| Projectboekhouding | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Het boeken van een leveranciersfactuur kan mislukken met het volgende foutbericht: "De transacties op het boekstuk zijn niet in evenwicht per 17-05-2021. (valuta voor boekhouding: 0,00 - rapporteringsvaluta: 0,01)." |

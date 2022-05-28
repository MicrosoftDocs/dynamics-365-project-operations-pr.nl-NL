---
title: Nieuwe functies van augustus 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit onderwerp bevat informatie over de kwaliteitsupdates die beschikbaar zijn in de release van augustus 2021 van Project Operations voor scenario´s op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 144a8c0d5ac47ad6fee54850c149a349f1698049
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594158"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van augustus 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

*Van toepassing op: Project Operations voor scenario's op basis van resources/niet-voorradige artikelen*

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

   - Project Operations in Microsoft Dataverse-omgeving versie 4.13.0.152.
   - Projectbeheer en financiële administratie in Dynamics 365 Finance-omgeving versie 10.0.20.

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- **Goedkeuringssets**: in goedkeuringssets worden goedkeuringsverzoeken voor tijd, onkosten of materiaalgebruik gegroepeerd in kleinere subsets van bewerkingen. Dankzij deze groepering kunnen goedkeuringen per project worden verwerkt, in een specifieke volgorde, en kunnen deze opnieuw worden geprobeerd en op volgorde worden gezet. Door de verzoeken te groeperen, worden de betrouwbaarheid en traceerbaarheid van goedkeuringsverwerking voor grote hoeveelheden goedkeuringen verbeterd. Zie [Goedkeuringssets](../approvals/approval-sets.md) voor meer informatie.

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release.

Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Bepaalde functies en mogelijkheden werken mogelijk niet correct als niet de meest recente versie van de toewijzing is geactiveerd. U kunt de actieve versie van de toewijzing zien op de pagina **Twee keer wegschrijven** in de kolom **Versie**. Activeer een nieuwe versie van de toewijzing door **Versies van tabeltoewijzing** te selecteren, de nieuwste versie te selecteren en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in het gedeelte [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) in de handleiding voor het oplossen van problemen met twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Facturering en prijzen | 2295625 | De naam van de mijlpaal moet worden gekopieerd van het factuurschema naar het factuurregeldetail. |
| Facturering en prijzen | 2316323 | De korting mag niet bewerkbaar zijn in een pro-formafactuur in Project Operations voor op resources gebaseerde scenario's. |
| Verkoopkansenbeheer | 2338619 | De bedrijfsregels **Verkoopkans** en **Prijsopgave** mogen alleen op pagina's worden aangeroepen. |
| Resourcebeheer | 2316523 | Er moet geen fout worden weergegeven als **Verzoek verzenden** wordt gebruikt vanuit een resourcevereiste waaraan een rol is gekoppeld. |
| Resourcebeheer | 2326885 | Er moet geen fout worden weergegeven als een resourcevereiste via een project wordt gemaakt. |
| Tijd en onkosten | 2335584 | Afgekeurde taakstromen in de tijdsinvoer. |
| Tijd en onkosten | 2336884 | De knop **Week kopiëren** voor tijdinvoer moet voor meer dan alleen de huidige gebruiker werken. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Reizen en onkosten | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Er worden onjuiste bedragen voor leverancierstransacties en btw-transacties geboekt wanneer onkosten worden gemaakt op basis van een creditcardtransactie. |
| Reizen en onkosten | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | De verkeerde vereffening zijn regels die zijn gemaakt wanneer het betalingsjournaal wordt gegenereerd. |
| Reizen en onkosten | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Er worden onjuiste bedragen voor btw-transacties worden geboekt wanneer onkosten worden gemaakt op basis van een creditcardtransactie. |
| Reizen en onkosten | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Het verwijderen van een onkostenregel kan lang duren. |
| Projectboekhouding | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Het systeem ondersteunt de instelling van continue nummerreeksen niet wanneer u een schatting plaatst na toepassing van KB 4619395. |
| Projectboekhouding | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Het boeken van leveranciersfacturen kan mislukken met het foutbericht 'De transacties op het boekstuk zijn niet in evenwicht per 17-05-2021. (boekhoudvaluta: 0,00 - rapporteringsvaluta: 0,01)' |

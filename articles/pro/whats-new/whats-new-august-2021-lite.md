---
title: Nieuwe functies augustus 2021 - Project Operations Lite-implementatie
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations Lite-implementatie van augustus 2021.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 84318a26d97355fe56794e1d1532576cde4af661
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922032"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Nieuwe functies augustus 2021 - Project Operations Lite-implementatie

_Van toepassing op: Lite-implementatie - van deal tot pro-formafacturering_

Dit artikel is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

  - Project Operations in Dataverse-omgeving, versie 4.13.0.152

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- **Goedkeuringssets**: in goedkeuringssets worden goedkeuringsverzoeken voor tijd, onkosten of materiaalgebruik gegroepeerd in kleinere subsets van bewerkingen. Dankzij deze groepering kunnen goedkeuringen per project worden verwerkt, in een specifieke volgorde, en kunnen deze opnieuw worden geprobeerd en op volgorde worden gezet. Door de verzoeken te groeperen, worden de betrouwbaarheid en traceerbaarheid van goedkeuringsverwerking voor grote hoeveelheden goedkeuringen verbeterd. Zie [Goedkeuringssets](../../approvals/approval-sets.md) voor meer informatie.

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

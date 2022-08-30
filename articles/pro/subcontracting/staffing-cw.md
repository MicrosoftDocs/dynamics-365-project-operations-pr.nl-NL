---
title: Een project bemannen met contractwerknemers en toeleveringscapaciteit
description: In dit artikel wordt uitgelegd hoe projectvereisten kunnen worden bemand met behulp van contractwerknemers of toeleveringscapaciteit in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8edb053467ef200ca3e051e2fd78106734318389
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261248"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Een project bemannen met contractwerknemers en toeleveringscapaciteit

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Ook voor het bemannen van algemene projectteamleden kunnen medewerkers of contractwerknemers worden gebruikt. Bij het bemannen van een project met contractwerknemers, kunt u uw personeelsopties beperken tot specifieke contractwerknemers die zijn toegewezen aan een toeleveringscontractregel. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Zoeken naar personeelsvereisten voor bemannen met contractwerknemers die tot een specifieke toeleveringscontractregel behoren

Om te zoeken naar personeelsvereisten en deze te bemann met contractwerknemers die tot een specifieke toeleveringscontractregel behoren, volgt u deze stappen:

1. Maak een algemeen projectteamlid dat verwijst naar een toeleveringscontract en toeleveringscontractregel.
2. Genereer een resourcevereiste voor dit algemene projectteamlid met behulp van de knop **Vereisten genereren** op het subraster van projectteamleden.
3. Selecteer de rij met teamleden en selecteer vervolgens de knop **Boeken** op het subraster. 
4. Dit opent het planbord met de context van de vereiste. Naast andere kenmerken, zoals datums, rollen en velden voor organisatie-eenheden, worden de planbordfilters ook automatisch gevuld met de velden leverancier, toeleveringscontract en toeleveringscontractregel uit de resourcevereiste.
5. Het systeem zoekt naar resources die voldoen aan de filtercriteria en geeft deze weer. 
6. Selecteer een van de gefilterde resources en boek de resource voor de vereiste. 
7. Er wordt een algemeen projectteamlid gemaakt en bijgewerkt met verwijzingen naar toeleveringscontract en toeleveringscontractregel. Ga naar **Projectschattingen** en selecteer **Prijzen bijwerken** om de bijgewerkte kosten van de resourcetoewijzing te zien. 

> [!NOTE]
> Het bijwerken van het projectteamlid met een toeleveringscontract- en toeleveringscontractregelregelverwijzing is misschien niet altijd mogelijk tijdens de boeking als de resource is toegewezen aan meerdere toeleveringscontractregels. Als het systeem het projectteamlid niet kan bijwerken met een toeleveringscontract en toeleveringscontractregel, opent u de record voor het projectteamlid en werkt u handmatig de toeleveringscontract- en toeleveringscontractregelvelden bij, zodat de schatting van de financiële kosten de kosten van de contractwerknemer nauwkeurig weergeeft.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Zoeken naar personeelsvereisten en deze bemannen met een contractwerknemer

Ga als volgt te werk om te zoeken naar personeelsvereisten en deze bemannen met een contractwerknemer:

1. Maak een algemeen teamlid.
2. Genereer een resourcevereiste voor dit algemene projectteamlid met behulp van de knop **Vereisten genereren** op het subraster van projectteamleden.
3. Selecteer de rij met teamleden en selecteer vervolgens de knop **Boeken** op het subraster. 
4. Dit opent het planbord met de context van de vereiste. Naast andere kenmerken, zoals datums, rollen en velden voor organisatie-eenheden, worden de planbordfilters ook automatisch gevuld met de velden leverancier, toeleveringscontract en toeleveringscontractregel uit de resourcevereiste. Omdat voor de vereiste geen toeleveringscontract- en toeleveringscontractregelregelwaarden zijn ingevuld, zijn deze kenmerken leeg in het filtervenster.
5. Het systeem zoekt naar resources die voldoen aan de filtercriteria en geeft deze weer.
6. Werk het veld **Type werknemer** in het filtervenster bij naar **Contractwerknemer** om het zoeken te beperken tot contractwerknemers. Werk **Leverancier** bij in het filtervenster om een leverancier te selecteren zodat u de zoekopdracht kunt beperken tot alleen contractwerknemers die bij een specifiek leveranciersbedrijf horen.
7. Selecteer een contractwerknemer uit de lijst en boek de resource voor de vereiste.
8. Er is een algemeen teamlid gemaakt. Het projectteamlid wordt echter niet bijgewerkt met een toeleveringscontract en toeleveringscontractregel en daarom worden de resourcetoewijzingskosten niet bepaald met behulp van de toeleveringsprijzen. Werk het projectteamlid handmatig bij met een toeleveringscontractregel en ga naar **Projectschattingen** en selecteer **Prijzen bijwerken** om de bijgewerkte kosten van de resourcetoewijzing te zien.

> [!NOTE]
> Projectteamleden bij wie **Contractwerknemer** als **Werknemertype** staat, maar geen toeleveringscontractreferentie hebben, worden gemarkeerd als **Ongeldig** op het raster **Projectteamleden**. Als er projectteamleden met deze status zijn, opent u de record voor het projectteamlid en werkt u handmatig de toeleverings- en toeleveringscontractregelvelden bij, zodat de schatting van de financiële kosten de kosten van de contractwerknemer op het tabblad **Schattingen** nauwkeurig weergeeft. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

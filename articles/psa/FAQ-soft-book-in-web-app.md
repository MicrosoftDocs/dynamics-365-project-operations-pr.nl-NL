---
title: Hoe kan ik resources 'zacht boeken' in appversie 2.x?
description: In dit artikel wordt beschreven hoe u leden van een projectteam zacht boekt met Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 472529c146fbb5e7a4540676c880cabd4ab1a32b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585188"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Hoe kan ik resources 'zacht boeken' in de webapp (Project Service-app v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

U kunt een resource voorlopig plannen of 'zacht boeken' voor een projectteam om te laten zien dat u van plan bent om de resource aan een project toe te wijzen. Zachte boekingen verbruiken de beschikbare capaciteit van een resource niet. Zacht geboekte teamleden kunnen niet aan projecttaken worden toegewezen. Alleen resources met de status Hard geboekt en het toewijzingstype Vastgelegd kunnen aan taken worden toegewezen (ervan uitgaand dat ze voldoende hard te boeken uren hebben voor de betreffende toewijzing).

Zacht geboekte projectteamleden worden in het raster Teamlid weergegeven met hun zacht geboekte uren in de kolom Zacht boeken. Ze worden ook weergegeven op het planbord. Zoals aangegeven verbruiken zachte boekingen geen capaciteit.

U kunt een teamlid op drie manieren zacht boeken voor een project met Project Service-versie 2.x. U kunt zacht boeken via het planbord, de functie Boekingen bijhouden gebruiken of een algemene resource maken. Deze methoden worden hieronder beschreven.

## <a name="soft-book-with-the-schedule-board"></a>Zacht boeken via het planbord

Ga als volgt te werk om zacht te boeken via het planbord: 
1. Open het planbord.
2. Selecteer het tabblad Project in het onderste deelvenster Boekingsvereisten van het planbord.
3. Zoek het project waarvoor u een resource zacht wilt boeken. Als u veel projecten hebt, klikt u op de kolomkop Project en gebruikt u vervolgens het filter om het project te zoeken.
4. Klik op het project en sleep het naar het tijdraster van de resource.
5. Het deelvenster Resourceboeking maken wordt rechts geopend. Pas de begin- en einddatum aan, selecteer de boekingsstatus Zacht en stel de uren in. 
6. Klik op Boeken.
7. In het project wordt de resource nu als teamlid met de zacht geboekte uren weergegeven in de kolom Zacht boeken.

U kunt deze resources niet toewijzen aan taken in de structuur voor werkspecificatie omdat alleen hard geboekte resources in het team kunnen worden toegewezen.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Zacht boeken via de functie Boekingen bijhouden

Ga als volgt te werk om zacht te boeken via Boekingen bijhouden:
1. Klik op Nieuw in het raster voor teamleden.
2. Selecteer de te boeken resource, functie en datums.
3. Selecteer een andere toewijzingsmethode dan Geen:
- Volledige capaciteit
- Percentagecapaciteit
- Uren gelijkmatig verdelen
- Uren vooraf laden
4. Klik op Opslaan. De resource in het teamraster en de uren worden weergegeven als hard geboekt.
5. Houd de boekingen van de resource bij door te klikken op Boekingen bijhouden.
6. Wanneer het planbord wordt geopend, vouwt u de resource uit om de boekingen weer te geven. De boeking wordt aangeduid als hard geboekt.
7. Klik met de rechtermuisknop op de boeking en selecteer onder Status wijzigen de optie Zacht boeken en vervolgens Zacht. De boekingsstatus is nu Zacht.
8. Wanneer u het planbord sluit, ziet u dat de uren voor de resource van Hard in Zacht zijn gewijzigd in het raster van het teamlid.
Als u een resource hard boekt voor het team, vervolgens taken aan deze resource toewijst in de structuur van de werkspecificatie en ten slotte Boekingen onderhouden gebruikt om de status van Hard in Zacht te wijzigen, worden de toewijzingen voor die resource verwijderd, aangezien alleen hard geboekte resources aan taken kunnen worden toegewezen.

## <a name="soft-book-by-creating-a-generic-resource"></a>Zacht boeken door een algemene resource te maken

U kunt een zachte boeking maken door een algemeen resourceteamlid te maken, te voldoen aan een planbord- of resourceaanvraag en het type te wijzigen tijdens het boeken.
Ga hiervoor als volgt te werk:

1. Wijs in de structuur voor werkspecificatie rollen toe aan de taken waarvoor u algemene teamleden wilt genereren.
2. Klik op Projectteam genereren.
3. Selecteer de algemene resource in het raster van het projectteamlid en klik op Boeken.
4. Selecteer de resource die u wilt boeken op het planbord.
5. Wijzig de boekingsstatus in Zacht in het deelvenster Resourceboeking maken van het planbord.
6. Klik op Boeken of Boeken en Afsluiten.

Nadat u het planbord hebt gesloten, wordt de geselecteerde resource aan het team toegevoegd met zacht geboekte uren en toegewezen uren. Daarnaast blijft de algemene resource deel uitmaken van het team als indicatie dat de taken zijn toegewezen aan een zacht geboekt teamlid.

Ga als volgt te werk wanneer u een zacht geboekte teamlidresource in een hard geboekt teamlid wilt wijzigen zodat u taken aan hem of haar kunt toewijzen:

1. Selecteer de resource en klik op Boekingen bijhouden.
2. Wanneer het planbord wordt geopend, vouwt u de resource uit om de boekingen weer te geven. De boeking wordt gemarkeerd als Zacht.
3. Klik met de rechtermuisknop op de boeking en selecteer onder Status wijzigen de optie Hard boeken en vervolgens Hard. De boekingsstatus is nu Hard.
4. Wanneer u het planbord sluit, ziet u dat de uren voor de resource van Zacht in Hard zijn gewijzigd in het raster van het teamlid. U kunt de resource nu aan taken toewijzen (als de hard geboekte uren en de inspanningsuren van de taak voor toewijzing overeenkomen). Als u de stappen in procedure 3 hierboven hebt uitgevoerd en de status van de zacht geboekte boekbare resource in hard wijzigt, wordt het algemene teamlid verwijderd uit het team.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Een resource zacht boeken
description: Dit onderwerp bevat informatie over het voorlopig plannen of zacht boeken van projectteamleden.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: cf67769fef39f95785320ae38055f0a3359b3a82d996b740bdb5d51e864f3d56
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005340"
---
# <a name="soft-book-a-resource"></a>Een resource zacht boeken

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U kunt een resource voorlopig plannen of 'zacht boeken' voor een projectteam om te laten zien dat u van plan bent om de resource aan het project toe te wijzen. Zachte boekingen verbruiken geen beschikbare capaciteit van een resource en u kunt zacht geboekte teamleden aan projecttaken toewijzen. Omdat zachte boekingen de capaciteit van een resource niet verbruiken, kunt u de resource nog steeds 'hard boeken' voor andere taken in hetzelfde tijdsbestek. Algemene resources kunnen niet zacht worden geboekt en een algemene resourceaanvraag kan niet worden vervuld met een zachte boeking.

Zacht geboekte projectteamleden worden op het tabblad **Team** van de pagina **Project** weergegeven met de zacht geboekte uren in de kolom **Zacht geboekte uren** in de weergave **Benoemde teamleden**. Zacht geboekte teamleden worden ook weergegeven op het planbord. Omdat ze zacht geboekt zijn, wordt op het planbord geen verbruik van capaciteit voor deze resources weergegeven. Zacht geboekte tijd wordt niet weergegeven op het tabblad **Vereffening** of in het veld **Boekingen uitbreiden** op het tabblad **Vereffening** van het planbord. 

U kunt een teamlid op twee manieren zacht boeken voor een project: rechtstreeks via het planbord of door het teamlid toe te voegen op het tabblad **Team**. 

## <a name="soft-book-from-the-schedule-board"></a>Zacht boeken via het planbord
Voer de volgende stappen uit om een resource zacht te boeken via het planbord. 

1. Open het planbord en selecteer het tabblad **Project** in het deelvenster **Boekingsvereisten**.
2. Zoek het project waarvoor u een resource zacht wilt boeken. Als de lijst een groot aantal projecten bevat, selecteert u de kolomkop **Project** en gebruikt u vervolgens het filter om te zoeken naar een of meer projecten.
3. Selecteer het project en sleep het naar het tijdraster van de resource.
5. Pas in het deelvenster **Resourceboeking maken** de begin- en einddatum aan, stel **Boekingsstatus** in op **Zacht** en stel vervolgens de uren in. 
6. Klik op **Boeken**. De resource wordt nu als resource voor het project weergegeven op het tabblad **Team**. In de weergave **Benoemde teamleden** worden de zacht geboekte uren weergegeven in de kolom **Zacht geboekte uren**.

> [!NOTE]
> U kunt de zacht geboekte uren nu toewijzen aan taken op het tabblad **Planning**. Op het tabblad **Vereffening** wordt voor de resource een boekingstekort ten opzichte van de taaktoewijzing weergegeven aangezien op het tabblad **Vereffening** alleen harde boekingen tellen. U kunt de functie **Boekingen uitbreiden** gebruiken om de resource hard te boeken en het tekort van harde boekingen ten opzichte van de resourcetoewijzingen ongedaan te maken. U moet in dat geval de zachte boekingen handmatig annuleren voor de resource via **Boekingen bijhouden**.

## <a name="soft-book-on-the-team-tab"></a>Zacht boeken op het tabblad Team

U kunt teamleden rechtstreeks op het tabblad **Team** toevoegen en hun boekingsstatus vervolgens wijzigen van **Hard** in **Zacht** via **Boekingen bijhouden**. Als u een teamlid op deze manier toevoegt, resulteert dit altijd in een harde boeking tenzij u de toewijzingsmethode **Geen** gebruikt.

Ga als volgt te werk om deze methode te gebruiken.

1. Klik op de pagina **Project** op het tabblad **Team** op **Nieuw**.
2. Selecteer de te boeken resource, de rol en de begin- en einddatum.
3. Selecteer een andere toewijzingsmethode dan **Geen**.
4. Selecteer **Opslaan**. De resource wordt in het raster en de uren worden in de kolom **Hard geboekte uren** weergegeven.
5. Houd de boekingen van de resource bij door **Boekingen bijhouden** te selecteren.
6. Wanneer het planbord wordt geopend, vouwt u de resource uit om de boekingen weer te geven. De boeking wordt weergegeven als **Hard**.
7. Klik met de rechtermuisknop op de boeking en selecteer onder **Status wijzigen** de optie **Zacht boeken** \> **Zacht**. De boekingsstatus is nu **Zacht**.
8. Als u het planbord sluit, ziet u in de weergave **Benoemde teamleden** dat de uren voor de resource van de kolom **Hard geboekte uren** naar de kolom **Zacht geboekte uren** in het raster op het tabblad **Team** zijn verplaatst.

> [!NOTE]
> Als u **Boekingen onderhouden** gebruikt om de status van **Hard** in **Zacht** te wijzigen, vervolgens een resource hard boekt voor het team en taken aan de resource toewijst, worden de taaktoewijzingen voor de resource bewaard. Op het tabblad **Vereffening** heeft de resource echter een boekingstekort omdat alleen naar harde boekingen wordt gekeken bij het afstemmen van boekingen en toewijzingen. U kunt de functie **Boekingen uitbreiden** op het tabblad **Vereffening** gebruiken om de resource hard te boeken en het tekort van harde boekingen ten opzichte van de resourcetoewijzingen ongedaan te maken. U moet in dat geval de zachte boekingen voor de resource annuleren via **Boekingen bijhouden**.

Ga als volgt te werk wanneer u een zacht geboekte teamlidresource in een hard geboekt teamlid wilt wijzigen:

1. Vouw op het planbord de resource uit om de boekingen weer te geven. De boeking wordt weergegeven als **Zacht**.
2. Klik met de rechtermuisknop op de boeking en selecteer onder **Status wijzigen** de optie **Hard boeken** \> **Hard**. De boekingsstatus is nu **Hard**.
3. Als u het planbord sluit en terugkeert naar het project en het tabblad **Team** opent, ziet u in de weergave **Benoemde teamleden** dat de uren voor de resource van de kolom **Zacht geboekte uren** naar de kolom **Hard geboekte uren** op het tabblad **Team** zijn verplaatst. Als de resource was toegewezen aan taken, wordt op het tabblad **Vereffening** geen boekingstekort meer weergegeven omdat de boekingen nu hard zijn.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Projecten en taken toewijzen aan een projectgebaseerde contractregel - lite
description: Dit onderwerp bevat informatie over het toevoegen en verwijderen van projecten en taken aan een contractregel.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ce99e6f770c5eb39e5f2740a861721cf3d210ac9743bbd9d2a1e1a7236f368c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989725"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Projecten en taken toewijzen aan een projectgebaseerde contractregel 

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Op projectgebaseerde contractregels kunt u specifieke taken in een project toewijzen aan de contractregel.

Wanneer u specifieke taken toewijst aan een contractregel, zijn de factureringsmethode, de opties voor toerekening, de niet-overschrijdingslimieten en de klanten die op de contractregel zijn gedefinieerd, alleen van toepassing op die specifieke taken.

Als u een scenario hebt waarbij één fase van een project, bijvoorbeeld de prototypefase, een vaste prijs heeft en alle andere fasen voor tijd en materiaal zijn, kunt u de prototypefase en alle bijbehorende onderliggende taken aan de contractregel koppelen voor die fase met een factureringsmethode tegen een vaste prijs.

Alle andere fasen in de structuur voor werkspecificatie van uw project kunnen worden gekoppeld aan de contractregel op basis van tijd en materiaal.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Taken koppelen aan projectgebaseerde contractregels

Taken kunnen worden gekoppeld aan contractregels van het tabblad **Toerekenbare taken** op de pagina **Contractregel** of van het tabblad **Taakfacturering** op de pagina **Project**.

### <a name="from-the-contract-line-page"></a>Vanaf de pagina Contractregel

Voer de volgende stappen uit om projecttaken te koppelen aan de contractregel van het tabblad **Toerekenbare taken** van de pagina **Contractregel**.

1. Op het tabblad **Algemeen** van een projectgebaseerde contractregel, controleert u of het veld **Project** is ingevuld.
2. Selecteer in het veld **Opgenomen taken** de optie **Alleen geselecteerde taken**.
3. Sla uw wijzigingen op. Het formulier wordt vernieuwd en het tabblad **Toerekenbare taken** wordt zichtbaar.
4. Selecteer het tabblad **Toerekenbare taken** en selecteer in het subraster **Een contractregeltaak toevoegen**.
5. Selecteer op de pagina **Contractregeltaken** de taak in de vervolgkeuzelijst **Taken**. 
6. Voer informatie in het veld **Factureringstype** in en selecteer **Opslaan en sluiten**. De geselecteerde taak wordt gekoppeld aan de contractregel.

> [!NOTE]
> Dit is niet de optimale methode om projecttaken aan contractregels te koppelen. Met deze methode moet elk project handmatig worden gekoppeld. De beste manier is via het tabblad **Taakfacturering** op de pagina **Project**.

### <a name="from-the-project-page"></a>Vanaf de pagina Project

Dit is de optimale methode om taken aan contractregels te koppelen. U kunt meerdere taken selecteren en alle taken en hun onderliggende taken aan de geselecteerde contractregel koppelen. Voer de volgende stappen uit om taken te koppelen aan de contractregel vanaf de pagina **Project**.

1. Op het tabblad **Algemeen** van een projectgebaseerde contractregel, controleert u of het veld **Project** is ingevuld.
2. Selecteer in het veld **Opgenomen taken** de optie **Alleen geselecteerde taken**.
3. Sla de projectgebaseerde contractregel op. Het formulier wordt vernieuwd en het tabblad **Toerekenbare taken** wordt zichtbaar. Dit is uitsluitend bedoeld voor verificatiedoeleinden.
4. Op het tabblad **Algemeen** van de projectgebaseerde contractregel, selecteert u de projectkoppeling in het veld **Project**.
5. Op de pagina **Project** selecteer u het tabblad **Factureringsinstellingen van taak**.
6. Dit bevat twee rasters. Het ene raster is bedoeld voor contractregels die van toepassing zijn op het hele project. Het tweede raster is van toepassing op taakspecifieke factureringsinstellingen. Selecteer in het tweede raster een of meer taken en selecteer vervolgens **Contractregels koppelen**.
7. Selecteer in het dialoogvenster dat wordt geopend een contractregel in de vervolgkeuzelijst.
8. Gebruik de vervolgkeuzelijst **Factureringstype** om de taken te markeren als toerekenbaar of niet-toerekenbaar.
9. Schakel het selectievakje in om aan te geven of de koppeling ook onderliggende taken van de geselecteerde taken moet omvatten. Als u het vakje aanvinkt, worden ook de onderliggende taken van de geselecteerde taken aan de contractregel gekoppeld.
10. Kies **OK** om het dialoogvenster te sluiten.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Taken loskoppelen van projectgebaseerde contractregels

### <a name="from-the-contract-line-page"></a>Vanaf de pagina Contractregel

Voer de volgende stappen uit om projecttaken los te koppelen van de contractregel op het tabblad **Toerekenbare taken** van de pagina **Contractregel**.

1. Selecteer op het tabblad **Toerekenbare taken** de optie **Contractregeltaak verwijderen**.
2. Een waarschuwingsbericht geeft aan dat het verwijderen van deze koppeling kan resulteren in de omkering van de werkelijke waarden die eerder voor de taak zijn geregistreerd. Selecteer **OK** in het dialoogvenster om de koppeling tussen de taak en de projectgebaseerde contractregel te verwijderen. 

> [!NOTE]
> Hiermee verwijdert u de taak niet uit het project. In plaats daarvan wordt de taakkoppeling verwijderd uit de projectgebaseerde contractregel.

### <a name="from-the-project-page"></a>Vanaf de pagina Project

Dit is de betere methode om projecttaken los te koppelen van contractregels. U kunt meerdere taken selecteren en alle taken en hun onderliggende taken loskoppelen van de geselecteerde contractregel. Voer de volgende stappen uit om taken los te koppelen van de contractregel.

1. Vanaf het tabblad **Algemeen** van de projectgebaseerde contractregel, klikt u op de projectkoppeling in het veld **Project**.
2. Op de pagina **Project** selecteer u het tabblad **Factureringsinstellingen van taak**.
3. Er zijn twee rasters op de pagina. Het ene raster is voor contractregels die van toepassing zijn op het hele project en het tweede is van toepassing op taakspecifieke factureringsinstellingen. Selecteer in het tweede raster een of meer taken en selecteer vervolgens **Contractregels loskoppelen**.
4. Selecteer in het dialoogvenster dat wordt geopend een contractregel in de vervolgkeuzelijst.
5. Schakel het selectievakje in om aan te geven of de koppeling ook moet worden verwijderd voor onderliggende taken van de geselecteerde taken. Als u het vakje aanvinkt, worden ook de onderliggende taken van de geselecteerde taken losgekoppeld van de contractregel.
6. Selecteer **OK**. Een waarschuwingsbericht geeft aan dat het verwijderen van deze koppeling kan resulteren in de omkering van de werkelijke waarden die eerder voor de taak zijn geregistreerd. Selecteer **OK** in het waarschuwingsvenster om de koppeling tussen de taak en de projectgebaseerde contractregel te verwijderen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

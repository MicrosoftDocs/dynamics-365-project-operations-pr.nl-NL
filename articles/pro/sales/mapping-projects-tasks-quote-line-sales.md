---
title: Projecten en taken toewijzen aan een projectgebaseerde prijsopgaveregel
description: Dit onderwerp bevat informatie over het toewijzen van projecten en taken aan een projectgebaseerde taakregel.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074456"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Projecten en taken toewijzen aan een projectgebaseerde prijsopgaveregel

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Op projectgebaseerde prijsopgaveregels kunt u de specifieke taken toewijzen van een project dat al aan een prijsopgaveregel is gekoppeld.

Wanneer u taken toewijst aan een prijsopgaveregel, zijn de volgende items die u op de prijsopgaveregel hebt gedefinieerd alleen van toepassing op die taken:

- Factureringsmethode
- Opties voor toerekenbaarheid
- Niet-overschrijdingslimieten
- Klanten

U kunt bijvoorbeeld een project hebben waarbij de ene fase een vaste prijs heeft en voor alle andere fasen tijd en materiaal geldt. In dit geval kunt u de eerste fase en alle onderliggende taken aan de prijsopgaveregel voor die fase koppelen met een factureringsmethode tegen een vaste prijs. U kunt dan alle andere fasen aan de op tijd en materiaal gebaseerde prijsopgaveregel koppelen.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Taken koppelen aan projectgebaseerde prijsopgaveregels

U kunt taken koppelen aan prijsopgaveregels van de volgende locaties:

- Pagina **Project** > tabblad **Taakfacturering** (optimaal)
- Pagina **Prijsopgaveregel** > tabblad **Toerekenbare taken** 

### <a name="from-the-project-page"></a>Vanaf de pagina Project

De pagina **Project** biedt de optimale voorzieningen voor het koppelen van taken aan offerteregels. Gebruik deze pagina om meerdere taken te selecteren en ze allemaal, plus hun onderliggende taken, aan de geselecteerde prijsopgaveregel te koppelen.

1. Op het tabblad **Algemeen** van een projectgebaseerde prijsopgaveregel, controleert u of het veld **Project** is ingevuld.
2. Selecteer in het veld **Opgenomen taken** **Alleen geselecteerde taken**.
3. Sla de projectgebaseerde prijsopgaveregel op. Wanneer het formulier wordt vernieuwd, wordt het tabblad **Toerekenbare taken** weergegeven.
4. Selecteer op het tabblad **Algemeen** de koppeling voor het project in het veld **Project**.
5. Selecteer op de pagina **Project** het tabblad **Taakfacturering**.
6. Selecteer in het tweede raster, dat van toepassing is op taakspecifieke factureringsinstellingen, een of meer taken en selecteer vervolgens **Prijsopgaveregels koppelen**.
7. Selecteer in het dialoogvenster dat verschijnt een prijsopgaveregel die projectgebaseerde prijsopgaveregels in de prijsopgave weergeeft.
8. Geef in het veld **Factureringstype** aan of deze taken wel of niet toerekenbaar zijn.
9. Schakel het selectievakje in om aan te geven of de koppeling onderliggende taken van de geselecteerde taken moet bevatten. Als u het vakje selecteert, worden de onderliggende taken van de geselecteerde taken aan de prijsopgaveregel gekoppeld.
10. Kies **OK** om het dialoogvenster te sluiten.

### <a name="from-the-quote-line-page"></a>Vanaf de pagina Prijsopgave

U kunt projecttaken koppelen aan prijsopgaveregels uit het tabblad **Toerekenbare taken** op de pagina **Prijsopgaveregel**.

>[!NOTE]
>De optimale plaats om projecttaken aan prijsopgaveregels te koppelen is op het tabblad **Taakfacturering** op de pagina **Project**. Als u taken uit het tabblad **Toerekenbare taken** op de pagina **Prijsopgaveregel** koppelt, moet u elk project handmatig koppelen.

1. Op het tabblad **Algemeen** van een projectgebaseerde prijsopgaveregel, controleert u of een project is geselecteerd in het veld **Project**.
2. Selecteer in het veld **Opgenomen taken** **Alleen geselecteerde taken**.
3. Sla de projectgebaseerde prijsopgaveregel op. Wanneer het formulier wordt vernieuwd, wordt het tabblad **Toerekenbare taken** weergegeven.
4. Op het tabblad **Toerekenbare taken** selecteert u **Een taak voor een prijsopgaveregel toevoegen**.
5. Selecteer de taak op de pagina **Taak voor prijsopgaveregel** in het veld **Taken** en selecteer **Opslaan** in het veld **Factureringstype**. 
6. Sluit de pagina. De geselecteerde taak wordt nu gekoppeld aan de prijsopgaveregel.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Taken loskoppelen van projectgebaseerde prijsopgaveregels

### <a name="from-the-project-page"></a>Vanaf de pagina Project

Deze methode biedt de optimale voorzieningen voor het loskoppelen van taken van offerteregels. Gebruik deze pagina om meerdere taken te selecteren en ze allemaal, plus hun onderliggende taken, los te koppelen van de geselecteerde prijsopgaveregel.

1. Op het tabblad **Algemeen** van een projectgebaseerde prijsopgaveregel, selecteert u de projectkoppeling in het veld **Project**.
2. Selecteer op de pagina **Project** het tabblad **Taakfacturering**.
3. Selecteer in het tweede raster, dat van toepassing is op taakspecifieke factureringsinstellingen, een of meer taken en selecteer vervolgens **Prijsopgaveregels loskoppelen**.
4. Selecteer een prijsopgaveregel in het dialoogvenster dat verschijnt.
5. Schakel het selectievakje in om aan te geven of de koppeling ook moet worden verwijderd uit onderliggende taken van de geselecteerde taken. Als u het vakje selecteert, worden ook de onderliggende taken van de geselecteerde taken losgekoppeld van de prijsopgaveregel.
6. Selecteer **OK**. Een waarschuwingsbericht informeert u dat als u deze koppeling verwijdert, eventuele werkelijke waarden die eerder voor de taak zijn geregistreerd, kunnen worden teruggedraaid. 
7. Selecteer **OK** om door te gaan en de koppeling tussen de taak en de projectgebaseerde prijsopgaveregel te verwijderen.

### <a name="from-the-quote-line-page"></a>Vanaf de pagina Prijsopgave

U kunt projecttaken ook loskoppelen van prijsopgaveregels via het tabblad **Toerekenbare taken** op de pagina **Prijsopgaveregel**.

1. Op het tabblad **Toerekenbare taken** selecteert u **Een taak voor een prijsopgaveregel verwijderen**.
2. Selecteer **OK**. Een waarschuwingsbericht informeert u dat als u deze koppeling verwijdert, eventuele werkelijke waarden die eerder voor de taak zijn geregistreerd, kunnen worden teruggedraaid. 
3. Selecteer **OK** om door te gaan en de koppeling tussen de taak en de projectgebaseerde prijsopgaveregel te verwijderen.

>[!NOTE]
> Met deze procedure verwijdert u de taak niet uit het project. U verwijdert alleen de taakkoppeling van de projectgebaseerde prijsopgaveregel.

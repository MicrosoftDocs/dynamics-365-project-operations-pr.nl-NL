---
title: Mobiele toepassing voor projecturenstaten
description: Dit onderwerp biedt informatie over de mobiele toepassing Microsoft Dynamics 365 Project Timesheet. Met de mobiele app Project Timesheet kunnen gebruikers urenstaten voor projecten op hun mobiele apparaat indienen en goedkeuren.
author: abruer
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: df6d286b6d5716fb0ea908ed71c2257b4db21ecfd35148fea65dfd96e058ac9a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997195"
---
# <a name="project-timesheet-mobile-application"></a>Mobiele toepassing voor projecturenstaten

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Samenzicht

Met de mobiele app Microsoft Dynamics 365 Project Timesheet kunnen gebruikers urenstaten voor projecten op hun mobiele apparaat (iPhone of Android) indienen en goedkeuren. Deze mobiele app toont de urenstaatfunctionaliteit in het gebied van Projectmanagement en financiële administratie van Dynamics 365 Finance, waardoor de productiviteit en efficiëntie van de gebruiker wordt verbeterd en tijdige invoer en goedkeuring van projecturenstaten mogelijk wordt gemaakt.

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren

Download en installeer de mobiele app Microsoft Dynamics 365 Project Timesheet voor Android of iPhone vanuit de mobiele store voor uw apparaat.

## <a name="enable-the-app"></a>De app inschakelen 

In Finance moet de mobiele app Project Timesheet zijn ingeschakeld. U kunt functionaliteit inschakelen door naar **Parameters voor Projectmanagement en financiële administratie \> Urenstaat** te gaan en de parameter **Microsoft Dynamics 365 Project Timesheet inschakelen** te selecteren.

## <a name="sign-in-to-the-app"></a>Aanmelden bij de app

1.  Start de app op uw mobiele apparaat.

2.  Voer uw URL voor Finance in.

3.  Wanneer u zich voor het eerst aanmeldt, wordt u om uw gebruikersnaam en wachtwoord gevraagd. Voer uw referenties in.

4.  U wordt aangemeld bij uw standaardbedrijf.

## <a name="submit-a-project-timesheet"></a>Een projecturenstaat indienen

U kunt in de app een projecturenstaat maken en indienen. U kunt een nieuwe urenstaat baseren op informatie uit een eerdere urenstaat, opgeslagen regels of projectopdrachten. Als u als gemachtigde bent aangewezen, kunt u ook een urenstaat voor een andere werknemer invoeren. Als u een urenstaat wilt maken als gemachtigde, selecteert u de knop **Menu** en selecteert u vervolgens een resourcenaam.

Op de urenstaatpagina wordt een nieuwe urenstaat gemaakt voor de urenstaatperiode, op basis van de huidige datum. De werkweek wordt weergegeven. Als de urenstaatperiode meerdere weken beslaat, kunt u een andere werkweek selecteren op de tabbladen voor werkweken.
Als er een urenstaat bestaat voor de huidige datum, wordt deze weergegeven. Als u een nieuwe urenstaat moet maken in een andere urenstaatperiode, selecteert u de knop **Menu** en selecteert u vervolgens **Nieuwe urenstaat**.

U kunt projectinformatie invoeren door op de actie **Tijd toevoegen** of de actie **Tijd kopiëren van** te klikken. De actie **Tijd kopiëren van** kopieert projectregelinformatie, maar niet de uren. Het menu **Tijd kopiëren van** bevat de volgende opties:

- **Kopiëren van bestaande urenstaat** - Kopieer urenstaatregels van een bestaande urenstaat.

- **Kopiëren van favoriet** - Maak nieuwe urenstaatregels door de urenstaatinstellingen te gebruiken die u als favorieten hebt geselecteerd.

- **Kopiëren van opdracht** - Maak nieuwe urenstaatregels van toegewezen projecten.

De projectinformatie die wordt weergegeven, is afhankelijk van de mobiele parameters die u hebt gedefinieerd op de pagina **Parameters voor Projectmanagement en financiële administratie**.

Selecteer in het veld **Rechtspersoon** de rechtspersoon waarvoor u projectwerk hebt uitgevoerd. Het veld **Rechtspersoon** is alleen beschikbaar als ondersteuning voor intercompany-urenstaten is ingeschakeld voor uw rechtspersoon.

Selecteer de klant die aan het project is gekoppeld voor de urenstaat. Voor de eerste release op Android wordt invoer door de klant niet ondersteund, aangezien u eerst het project moet selecteren. Als u het project eerst hebt geselecteerd, wordt het veld **Klant** automatisch ingevuld.

Selecteer in het veld **Project** het project waarvoor u tijd invoert. Het veld **Klant** wordt automatisch ingevuld.

De zoekopdrachten voor klanten en projecten maken zoeken in zowel klanten als projecten mogelijk.

Selecteer informatie in de velden **Categorie**, **Activiteit**, **Regeleigenschap**, **Omzetbelastinggroep** en **Btw-groep artikel** zoals vereist. Deze velden kunnen worden overschreven.

Het veld **Regeleigenschap** wordt ingesteld op een standaardwaarde, gebaseerd op parameters voor projectmanagement en financiële administratie. Wanneer de project/categorie en categorie/resourceparameters zijn ingeschakeld, wordt de waarde voor **Regeleigenschap** ingesteld op de standaardwaarde die u voor deze validatie hebt gedefinieerd. Als de project/categorie en categorie/resourceparameters niet zijn ingeschakeld, wordt de waarde voor **Regeleigenschap** standaard ingesteld volgens het veld **Standaardregeleigenschap inschakelen** op de pagina **Parameters voor projectmanagement en financiële administratie**. De waarde voor **Regeleigenschap** kan worden overschreven.

Selecteer een dag om tijd toe te voegen. Voer het aantal uren in dat u elke dag hebt gewerkt.

U kunt opmerkingen toevoegen over de uren die u invoert door op **Commentaar toevoegen** te klikken en vervolgens opmerkingen in te voeren voor een interne publiek, klantpubliek of beide.
Interne opmerkingen kunnen worden bekeken door projectmanagers. Klantopmerkingen wordt op facturen vermeld.

Als u de lijn als favoriet wilt opslaan, schakelt u het selectievakje in en klikt u vervolgens op **Opslaan als favoriet**.

Ondersteuning voor financiële dimensies en bijlagen is niet beschikbaar in de mobiele toepassing.

Ga door met het toevoegen van projectregels om uw urenstaat compleet te maken.

Klik op **Indienen** om de urenstaat naar de goedkeuringsworkflow te verzenden.

## <a name="review-timesheets"></a>Urenstaten controleren

Een lijst met de urenstaten die moeten worden gecontroleerd, is beschikbaar in het menu. Deze optie is alleen beschikbaar als u bent aangewezen als werkstroomgoedkeurder. Zowel koptekst- als regelgoedkeuring worden ondersteund. Goedkeuring op regelniveau biedt de mogelijkheid om een of meer regels voor goedkeuring te markeren. Klik na het controleren van de urenstaatinformatie op **Goedkeuren**, **Delegeren** of **Terugkeren** om de werkstroom voort te zetten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
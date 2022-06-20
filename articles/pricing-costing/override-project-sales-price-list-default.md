---
title: Verkoopprijslijsten voor project overschrijven
description: Dit artikel biedt informatie over het maken van aangepaste verkoopprijslijsten.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8d0a769f415679b08f3228fcb14fbbbd37533ebc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911912"
---
# <a name="override-project-sales-price-lists"></a>Verkoopprijslijsten voor project overschrijven

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

## <a name="customer-specific-project-price-lists"></a>Klantspecifieke projectprijslijsten

Klantspecifieke prijsafspraken kunnen worden ingesteld als projectprijslijsten op een accountrecord in Dynamics 365 Project Operations.

Als u een klantspecifieke projectprijslijst wilt instellen, gaat u in het gebied **Verkoop** naar de accountrecord.

1. Open de lijstpagina **Accounts**.
2. Zoek en dubbelklik op een klantrecord om de detailpagina **Account** te openen.
3. Selecteer op het tabblad **Projectprijslijsten** **+ Nieuwe projectprijslijst**.
4. Op de pagina **Nieuwe projectprijslijst** selecteert u een prijslijst in de vervolgkeuzelijst. Alleen prijslijsten waarvoor de context is ingesteld op **Verkoop** en waarvan de valuta overeenkomt met de accountvaluta zijn inbegrepen.
5. Geef de koppeling een naam en selecteer **Opslaan**. Er wordt een klantspecifieke projectprijslijst gemaakt. Deze prijslijst wordt gebruikt om de standaardprojectprijzen te gebruiken voor projectoffertes of contracten die voor deze klant zijn gemaakt, waarbij de aanmaakdatum van de offerte of het projectcontract binnen de geldigheidsperiode van de prijslijst valt.

## <a name="custom-pricing-on-project-quotes"></a>Aangepaste prijzen voor projectoffertes

Voor projectoffertes kunt u projectprijzen gebruiken die beginnen met een standaardprijslijst van de klant of de projectparameters.

Als u aangepaste prijzen nodig hebt voor projectgerelateerd werk aan een bepaalde offerte, kunt u deze vinden in de projectprijslijsten van de bijbehorende entiteit.

Voer de volgende stappen uit om offertespecifieke projectprijzen in te stellen.

1. Open de projectofferte en selecteer het tabblad **Projectprijslijsten**.
2. Selecteer **Aangepaste prijzen maken** in het subraster.

Alle projectprijslijsten die bij de offerte zijn gevoegd, worden gekopieerd naar nieuwe prijslijsten. De namen van de nieuwe prijslijsten weerspiegelen de naam van de offerte met een datum-tijdstempel voor wanneer deze prijslijsten zijn gemaakt.

U kunt elk van deze prijslijsten gebruiken en de prijzen voor arbeid (rolprijs) en onkosten (categorieprijs) bijwerken. Deze gewijzigde prijzen zijn alleen van toepassing op deze projectofferte.

## <a name="price-lists-on-a-project-contract"></a>Prijslijsten voor een projectcontract

Bij een projectcontract wordt de projectprijs altijd standaard ingesteld als een aangepaste prijslijst met de naam van het contract en de aangemaakte datum-tijdstempel toegevoegd aan de naam. Dit geldt ongeacht of het contract is gemaakt toen de offerte werd gewonnen of dat het contract helemaal opnieuw is gemaakt. Indien nodig kunt u deze koppeling met de aangepaste prijslijst verwijderen en in plaats daarvan een standaardprijslijst aan het projectcontract koppelen.

Wanneer u een standaardprijslijst koppelt aan de projectprijslijsten in de offerte of het contract, hebben eventuele wijzigingen in de prijzen in de prijslijst invloed op alle offertes en contracten die de prijslijst gebruiken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
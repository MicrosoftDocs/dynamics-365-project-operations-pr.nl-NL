---
title: Projectprijslijsten in projectprijsopgaven beheren - lite
description: Dit onderwerp biedt informatie over het werken met projectprijslijsten in prijsopgaven. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ff830c63f7acf4cc23ac75d44afa9c3553b8724
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175975"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Projectprijslijsten in projectprijsopgaven beheren - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Projectprijsopgaven zijn ontworpen om verkoopprijslijsten met meerdere ingangsdatums te ondersteunen. Met Dynamics 365 Project Operations wordt een nieuwe bijbehorende entiteit met de naam **Prijslijsten voor projecten** toegevoegd. Deze entiteit heeft een 1-op-veel-relatie met een projectprijsopgave.

Projectprijslijsten worden gebruikt om prijzen op te geven voor tijd- en onkostentransacties voor een project. Als een offerte een of meer projectprijslijsten heeft, worden deze prijslijsten gebruikt om tijd- en onkostenramingen en werkelijke waarden te bepalen voor projecten die aan de prijsopgave zijn gekoppeld via de prijsopgaveregel.

Als er geen projectprijslijsten op een projectprijsopgave staan, ontvangt u een waarschuwing. Hierin staat dat omdat er geen projectprijslijsten zijn, uw geschatte en werkelijke projectwerkzaamheden en uitgaven niet worden beprijsd. In plaats daarvan hebben ze een prijs van nul (0) voor verkoopwaarden.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Een projectprijslijst aan een projectprijsopgave koppelen of loskoppelen

Voer de volgende stappen uit om een specifieke prijslijst te maken of te selecteren voor het schatten van projectgebaseerd werk en onkosten.

1. Selecteer op de prijsopgave het tabblad **Projectprijs** en selecteer in het subraster **+Nieuwe projectprijslijst toevoegen**.
2. Selecteer een prijslijst op de pagina Snel maken. De vervolgkeuzelijst toont alle prijslijsten waarvoor de context is ingesteld op **Verkoop** en de valuta komt overeen met de valuta op de prijsopgave.
4. Voer een beschrijving in voor de projectprijslijstkoppeling en selecteer **Opslaan en sluiten**.

Er wordt een koppeling met de projectprijslijst gemaakt.

U kunt dit proces herhalen als u meer dan één projectprijslijst aan de projectprijsopgave moet koppelen. Maak alleen meerdere projectprijslijsten aan als u verschillende ingangsdatums hebt voor elk van de bijbehorende projectprijslijsten.

> [!NOTE]
> Overlappende ingangsdatums op projectprijslijsten worden niet ondersteund in Project Operations. Als er meerdere projectprijslijsten zijn voor een transactie met een opgegeven datum, wordt de prijs voor die transactie standaard op nul (0) gezet.
Als u een koppeling met een projectprijslijst wilt verwijderen, selecteert u de projectprijslijst en vervolgens **Projectprijslijst voor prijsopgave verwijderen**. De prijslijst wordt verwijderd uit de projectprijslijsten van de prijsopgave, maar de prijslijst zelf wordt niet verwijderd. Alleen de koppeling met de prijsopgave wordt verwijderd.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Standaard projectprijslijsten instellen voor een prijsopgave

Projectprijslijsten kunnen als standaard worden ingesteld voor een projectofferte. Deze instelling zorgt ervoor dat alle prijsopgaven in uw organisatie altijd beginnen met een standaard prijslijst voor die prijsperiode.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Standaardwaarde voor organisatie instellen voor projectprijslijsten

1. Ga naar **Instellingen** > **Algemeen** > **Parameters**.
2. Zoek de record op de lijstpagina **Actieve parameters** en dubbelklik om deze te openen. 
3. Selecteer op de lijstpagina **Parameters** het tabblad **Prijslijst**. U kunt zien dat de lijst met standaardprijslijsten wordt weergegeven. Dit is een lijst met standaard kosten- en verkoopprijslijsten. Als u hier een verkoopprijslijst hebt gekoppeld voor elke valuta waarin u verkoopt, zorgt u ervoor dat deze verkoopprijslijst standaard wordt gebruikt voor elke prijsopgave die u maakt voor klanten die transacties in deze valuta uitvoeren.

### <a name="set-up-customer-specific-project-price-lists"></a>Klantspecifieke projectprijslijsten instellen

Klantspecifieke prijslijsten voor projecten kunnen ook worden opgesteld wanneer u een hoofdprijsovereenkomst met uw klanten hebt gesloten.

Als u een klantspecifieke projectprijslijst wilt instellen, voert u de volgende stappen uit.

1. Selecteer **Klanten** in het gebied **Verkoop**.
2. Selecteer en open in de lijst met uw actieve accounts de klantrecord waarvoor u een speciale prijslijst hebt.
3. Op het tabblad **Projectprijslijsten** kunt u een nieuwe prijslijstkoppeling maken voor de projectprijslijst die specifiek is voor deze klant.

## <a name="create-custom-pricing-on-a-project-quote"></a>Aangepaste prijzen opgeven in een projectprijsopgave

Nadat u organisatorische en klantspecifieke standaard projectprijslijsten hebt gemaakt, worden uw projectprijsopgaven automatisch gemaakt met deze koppelingen voor projectprijslijsten. In bepaalde gevallen moet u echter mogelijk aangepaste prijzen maken voor een specifieke projectprijsopgave. 

1. Controleer in de **Projectprijsopgave** op het tabblad **Projectprijslijst** of in het subraster geen specifieke prijslijstrecord is geselecteerd.
2. Selecteer **Aangepaste prijzen maken**. Hiermee worden kopieën gemaakt van alle standaardprijslijsten die momenteel aan de prijsopgave zijn gekoppeld en worden deze kopieën aan de prijsopgave gekoppeld. De bestaande koppelingen met standaardprijslijsten worden verwijderd. De verkoper kan vervolgens beginnen met het bewerken van prijzen op deze exemplaren. Deze gewijzigde prijzen zijn alleen van toepassing op deze projectprijsopgave.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
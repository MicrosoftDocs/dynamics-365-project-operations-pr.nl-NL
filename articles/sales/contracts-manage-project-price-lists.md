---
title: Projectprijslijsten in projectcontracten beheren
description: Dit artikel biedt informatie over het beheren van projectprijslijsten bij projectcontracten.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 23b9e6f9bc3e4bc3fb03de62064644dd58da34c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926172"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Projectprijslijsten in projectcontracten beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Projectcontracten in Dynamics 365 Project Operations zijn ontworpen om verkoopprijslijsten met meerdere ingangsdatums te ondersteunen voor een contract. Project Operations bevat een nieuwe gekoppelde entiteit genaamd **Projectprijslijsten**. Deze entiteit heeft een een-op-veel-relatie met een projectcontract.

Projectprijslijsten worden gebruikt om de prijs te bepalen voor tijd-, materiaal- en onkostentransacties voor een project. Als een contract een of meer projectprijslijsten bevat, worden deze prijslijsten gebruikt om de prijs van tijd, materiaal, onkostenschattingen en werkelijke waarden te bepalen voor projecten die via de contractregel aan het contract zijn gekoppeld.

Als er geen projectprijslijsten in een projectcontract zijn opgenomen, ziet u een waarschuwingsbericht dat er geen projectprijslijsten zijn en worden uw geregistreerde schattingen, werkelijke projectwerk, materiaal en uitgaven niet geprijsd. Er is geen prijs voor verkoopwaarden.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Een projectprijslijst aan een projectcontract koppelen of ontkoppelen

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Een specifieke prijslijst voor het schatten van projectgebaseerd werk, materiaal en onkosten maken of koppelen

1. Selecteer in het projectcontract het tabblad **Projectprijslijsten**.
2. Selecteer in het subraster **+ Nieuwe projectprijslijst toevoegen**.
3. Selecteer een prijslijst op de schuifregelaar **Snelle invoer**. 

  De vervolgkeuzelijst toont alle prijslijsten waarvoor de context is ingesteld op **Verkoop**, waarbij de valuta op de prijslijst overeenkomt met de valuta op het contract.
  
4. Voer een beschrijving in voor de projectprijslijstkoppeling, selecteer **Opslaan** en sluit vervolgens de schuifregelaar **Snelle invoer**.

   Er wordt een koppeling met de projectprijslijst gemaakt.
   
5. Herhaal stap 1-4 om meer dan één projectprijslijst aan het projectcontract te koppelen. Maak alleen meerdere projectprijslijsten aan als u verschillende ingangsdatums hebt voor elk van de bijbehorende projectprijslijsten.

> [!NOTE]
> Project Operations ondersteunt geen overlapping van de ingangsdatums van de projectprijslijsten. Als er meerdere projectprijslijsten zijn voor een transactie met een bepaalde datum, wordt de prijs voor die transactie standaard op nul gezet.

### <a name="remove-a-project-price-list-association"></a>Koppeling met een projectprijslijst verwijderen

- Selecteer de prijslijst van het project en selecteer vervolgens **Projectprijslijst voor contract verwijderen** in het subraster. 

  De prijslijst wordt verwijderd uit de projectprijslijsten in het contract. De prijslijst zelf wordt niet verwijderd. Alleen de koppeling met het contract wordt verwijderd.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Projectprijslijsten automatisch als standaardinstelling voor een contract opgeven

Een projectprijslijst kan worden ingesteld als de standaardprojectprijslijst. Deze opzet zorgt ervoor dat alle contracten in uw organisatie altijd beginnen met een standaardprojectprijslijst voor die prijsperiode.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Standaardwaarde voor de organisatie instellen voor projectprijslijsten

1. Ga naar **Instellingen** > **Algemeen** en selecteer **Parameters**.
2. Selecteer in de lijstpagina **Actieve parameters** het record en dubbelklik om het te openen. Zorg ervoor dat u tijdens het dubbelklikken niet op een veldwaarde klikt die een hyperlink is. 
3. Selecteer op de pagina **Actieve parameters** het tabblad **Prijslijst**. Een subraster toont een lijst met standaardprijslijsten. Dit is een lijst met standaardkosten en verkoopprijzen. Als er een **verkoopprijslijst** is gekoppeld voor elke valuta waarin u verkoopt, is de verkoopprijslijst standaard voor elk contract dat u maakt voor klanten die transacties in deze valuta uitvoeren.

### <a name="set-up-a-customer-specific-project-price-list"></a>Een klantspecifieke projectprijslijst instellen

U kunt ook klantspecifieke projectprijslijsten opstellen wanneer u met uw klanten een hoofdprijsovereenkomst hebt gesloten.

1. Ga naar **Verkoop** > **Klanten**.
2. Selecteer in de lijst met actieve accounts de klant voor wie u een speciale prijslijst hebt.
3. Selecteer de klantrecord om deze te openen en selecteer vervolgens het tabblad **Projectprijslijsten**. Een subraster toont een lijst met projectprijslijsten die specifiek zijn voor deze klant. 
4. Maak hier een nieuwe prijslijstkoppeling om een specifieke projectprijslijst voor deze klant te hebben.

## <a name="custom-pricing-on-a-project-contract"></a>Aangepaste prijzen op een projectcontract

Als u organisatorische en klantspecifieke standaardprijslijsten hebt, worden uw projectcontracten automatisch gemaakt met deze projectprijslijstkoppelingen. Projectprijslijsten in een projectcontract worden echter altijd gekopieerd met de datum en de contractnaam eraan toegevoegd. De account- en projectmanagers kunnen vervolgens beginnen met het bewerken van prijzen op deze exemplaren. Deze gewijzigde prijzen zijn alleen van toepassing op dit projectcontract.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Kenmerken van invoegtoepassingen bijwerken met nieuwe prijsdimensies
description: Dit onderwerp bevat informatie over het bijwerken van kenmerken van invoegtoepassingen voor prijsdimensies.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d57ec617d2c7b10a01a75e7eaa9ca2d646af3f6ee1d06d4e6fb228fc0533da27
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988330"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Kenmerken van invoegtoepassingen bijwerken met nieuwe prijsdimensies

Dit onderwerp bevat informatie over het bijwerken van kenmerken van invoegtoepassingen voor prijsdimensies.

> [!NOTE]
> Dit onderwerp is alleen van toepassing op de offerte- en contractfuncties in Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Vereisten
Voordat u de stappen in dit onderwerp voltooit, moet u de procedures in de volgende onderwerpen hebben voltooid:

  - [Aangepaste velden en entiteiten maken](create-custom-fields-entities-pricing-dimensions.md) 
  - [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten ](add-custom-fields-price-setup-transactional-entities.md)
  - [Aangepaste velden instellen als prijsdimensies](set-up-custom-fields-pricing-dimensions.md). 
  
Als u deze procedures niet hebt voltooid, voltooit u ze en keert u terug naar dit onderwerp.

## <a name="register-a-plug-in"></a>Een invoegtoepassing registreren
Wanneer een detail van een prijsopgaveregel wordt gemaakt op de pagina **Prijsopgaveregel** voor een projectprijsopgaveregel, creëert het systeem twee schattingsregels. De ene regel is voor de kostenzijde van de schatting en de andere regel is voor de verkoopzijde. Dit is hetzelfde voor projectcontractregels.

Wanneer u een wijziging aanbrengt in de hoeveelheid of een veld aan de kostenzijde, wordt die wijziging ook gemaakt aan de verkoopzijde. Dit is mogelijk doordat de PreOperation-invoegtoepassingen voor de entiteiten prijsopgaveregeldetail en contractregeldetail specifieke kenmerken aan de kostenzijde koppelen met de verkoopzijde van de transactie. Als u wijzigingen in de prijsdimensiewaarden aan de verkoopzijde ook aan de kostenzijde wilt doorvoeren, moeten de volgende invoegtoepassingen opnieuw worden geregistreerd nadat u wijzigingen in een prijsdimensie hebt aangebracht.

Deze invoegtoepassingen moeten worden bijgewerkt en opnieuw geregistreerd:

- PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**

Voer de volgende stappen uit om de invoegtoepassingen bij te werken en opnieuw te registreren.

1. Open **PluginRegistrationTool** en maak verbinding met uw Project Operations Dataverse-omgeving.
2. Selecteer **Zoeken** en typ de eerste paar letters van de invoegtoepassing die moet worden bijgewerkt.
3. Nadat de invoegtoepassing is gevonden, selecteert u deze en selecteer u **Selecteren op hoofdformulier**.
4. Selecteer de stap **Update msdyn_orderlinetransaction**, klik met de rechtermuisknop en selecteer **Bijwerken**.
5. Selecteer op de pagina **Bijwerken** het beletselteken (**...**) in de filterkenmerken.
6. Het venster met filterkenmerken wordt geopend en biedt een lijst met alle kenmerken in de entiteit en de prijsdimensies. Schakel de selectievakjes in voor de prijsdimensiekenmerken.
7. Selecteer **OK** om de pagina te sluiten en selecteer vervolgens **Stap bijwerken**.
8. Herhaal stap 2 tot 7 voor de tweede invoegtoepassing, **PreOperationQuoteLineDetail**. Werk voor deze invoegtoepassing de stap **Update msdyn_quotelinetransaction** bij.
9. Sluit **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
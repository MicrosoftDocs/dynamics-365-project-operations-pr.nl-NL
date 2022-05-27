---
title: Kenmerken van invoegtoepassingen bijwerken met nieuwe prijsdimensies
description: Dit onderwerp bevat informatie over het bijwerken van kenmerken van invoegtoepassingen voor prijsdimensies.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3b441b9ea0418e10db80a86613b2c41ea2c4673
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575022"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Kenmerken van invoegtoepassingen bijwerken met nieuwe prijsdimensies

Dit onderwerp bevat informatie over het bijwerken van kenmerken van invoegtoepassingen voor prijsdimensies.

> [!NOTE]
> Dit onderwerp is alleen van toepassing op de offerte- en contractfuncties in Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Vereisten
Voordat u de stappen In dit onderwerp voltooit, moet u de procedures in de volgende onderwerpen hebben voltooid:

  - [Aangepaste velden en entiteiten maken](create-custom-fields-entities-pricing-dimensions.md) 
  - [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten ](add-custom-fields-price-setup-transactional-entities.md)
  - [Aangepaste velden instellen als prijsdimensies](set-up-custom-fields-pricing-dimensions.md). 
  
Als u deze procedures niet hebt voltooid, voltooit u ze en keert u terug naar Dit onderwerp.

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
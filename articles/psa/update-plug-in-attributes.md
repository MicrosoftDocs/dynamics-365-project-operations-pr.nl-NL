---
title: Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen
description: Dit onderwerp bevat informatie over het bijwerken van kenmerken van invoegtoepassingen voor prijsdimensies.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c42e5fda79d51430f4dedf46037e11c86a38c474
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121842"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen

> [!NOTE]
> Als u de functies voor prijsopgaven en contracten van de Project Service Automation (PSA) niet gebruikt, kunt u dit onderwerp overslaan.

Er wordt in dit onderwerp vanuit gegaan dat u de procedures hebt voltooid in de onderwerpen [Aangepaste velden en entiteiten maken](create-custom-fields-entities.md), [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](field-references.md) en [Aangepaste velden instellen als prijsdimensies](set-up-pricing-dimensions.md). Als u deze procedures niet hebt voltooid, gaat u terug, voltooit u deze en keert u terug naar dit onderwerp.

Wanneer details voor een prijsopgaveregel zijn gemaakt op de pagina **Prijsopgaveregel** voor een project, maakt het systeem twee schattingsregels op de achtergrond, één regel voor de kostenzijde van de schatting en één voor verkoopzijde. Dit is hetzelfde voor projectcontractregels.

Wanneer u een wijziging aanbrengt in de hoeveelheid of een veld aan de kostenzijde, wordt die wijziging doorgegeven aan de verkoopzijde. Dit is mogelijk vanwege de volgende invoegtoepassingen die opnieuw moeten worden geregistreerd na een wijziging in de prijsdimensies.

- PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.

In de volgende stappen wordt het proces van het registreren van de invoegtoepassingen uitgelegd.

1. Open **PluginRegistrationTool** en maak verbinding met uw online-exemplaar.
2. Klik op **Zoeken** en zoek de invoegtoepassing om bij te werken.

 ![Schermopname van de zoekstructuur](media/PRT-1.png)

3. Nadat de invoegtoepassing is gevonden, selecteert u deze en klikt u op **Selecteren op hoofdformulier**.

4. Selecteer de stap van de invoegtoepassing, klik met de rechtermuisknop en selecteer **Bijwerken**.

 ![Schermopname van de invoegtoepassing dit moet worden bijgewerkt](media/PRT-2.png)
 
5. Klik in het venster Bijwerken op het beletselteken (**...**) in de filterkenmerken.

 ![Schermopname van de configuratiegegevens voor Bestaande stap bijwerken](media/PRT-3.png)
 
6. Selecteer de selectievakjes met prijskenmerken.

 ![Schermopname met het ingeschakelde selectievakje voor prijskenmerken](media/PRT-4.png)

7. Klik op **OK** om de pagina te sluiten en selecteer vervolgens **Stap bijwerken**.

 ![Schermopname met de knop "Stap bijwerken"](media/PRT-5.png)
 
8. Herhaal dit proces voor de tweede invoegtoepassing **PreOperationQuoteLineDetail - update van msdyn_quotelinetransaction**.

9. Sluit het registratiehulpprogramma.


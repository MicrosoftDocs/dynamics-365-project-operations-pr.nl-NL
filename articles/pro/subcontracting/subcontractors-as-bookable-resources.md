---
title: Onderaannemers instellen als boekbare resources
description: In dit onderwerp wordt uitgelegd hoe u resources voor onderaannemers instelt en onderhoudt die zijn gemaakt op basis van gebruikers en contactpersonen in het systeem, zodat ze aan subcontracten kunnen worden gekoppeld in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994180"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Onderaannemers instellen als boekbare resources

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Volg deze stappen om onderaannemers in te stellen als boekbare resources in Microsoft Dynamics 365 Project Operations.

1. Ga naar **Project** \> **Resources** en selecteer **Nieuw**.
2. Selecteer op de pagina **Nieuwe boekbare resource**, in het veld **Resourcetype**, een van de volgende opties:

    - **Gebruiker**: selecteer dit resourcetype als de onderaannemer toegang moet hebben tot Project Operations om tijd of onkosten in te voeren. Als u **Gebruiker** selecteert, heeft de onderaannemer een geldige licentie nodig om toegang te krijgen tot het systeem.
    - **Contactpersoon** of **Account**: selecteer een van deze resourcetypen als de onderaannemer geen toegang tot Project Operations nodig heeft, maar beschikbaar moet zijn voor taaktoewijzingen of boekingen voor projecten. Geen van deze resourcetypen biedt toegang tot het systeem. Selecteer **Account** om het bedrijf van de verkoper te vertegenwoordigen als boekbare resource. Selecteer **Contactpersoon** om de individuele werknemers van de verkoper te vertegenwoordigen.

3. Afhankelijk van het resourcetype dat u hebt geselecteerd, wordt u gevraagd de bijbehorende gebruikers-, account- of contactpersoonrecord te selecteren.
4. Selecteer in het veld **Type werknemer** de "Contractmedewerker" om de onderaannemer in te stellen als een boekbare resource.

    > [!NOTE]
    > Als u het veld **Type werknemer** leeg laat, wordt de boekbare resource als een werknemer beschouwd.

5. Als u **Contractwerker** hebt geselecteerd als het type werknemer, selecteert u de leverancier voor wie de resource werkt.
6. Selecteer de tijdzone van de resource en selecteer vervolgens **Opslaan**. Als u een werkuursjabloon wilt toewijzen aan de boekbare resource, kunt u **Kalender instellen** selecteren op de lijstpagina **Boekbare resource**.

Als u een boekbare resource aan een subcontractregelresource wilt koppelen, moet aan deze voorwaarden worden voldaan:

- De boekbare resource moet een contractwerker zijn.
- Een boekbare resource van het resourcetype **Contactpersoon** moet als contactpersoon aan het leveranciersaccount zijn gekoppeld. Een boekbare resource van het resourcetype **Gebruiker** hoeft niet als contactpersoon aan het leveranciersaccount te zijn gekoppeld.
- De waarde van het veld **Leverancier** voor de boekbare resource moet overeenkomen met de waarde van het veld **Leverancier** voor het subcontract.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Het type werknemer- en leverancierstoewijzing voor boekbare resources bijwerken

Het veld **Type werknemer** voor een boekbare resource bepaalt of de boekbare resource een contractwerker of een werknemer is. Het veld **Leverancier** definieert het leveranciersaccount waaraan de boekbare resource is gekoppeld. Door een boekbare resource als contactpersoon aan een leverancier te koppelen, geeft u aan dat de contactpersoon een werknemer van het leveranciersbedrijf is.

Als de velden **Type werknemer** en **Leverancier** voor een boekbare resource worden gewijzigd, zijn de wijzigingen van invloed op toekomstige validaties van nieuwe records die de boekbare resource maakt, zoals tijdsvermeldingen. De wijzigingen maken bestaande records echter niet ongeldig.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: De Project Operations Dataverse-app met ondersteuning voor twee keer wegschrijven handmatig implementeren
description: In dit artikel wordt uitgelegd hoe u de Project Operations Dataverse-app handmatig kunt implementeren zodat twee keer wegschrijven wordt ondersteund.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: be80ea3956fbf0264c2eeb7a5e30dd50b77e3c78
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912004"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>De Project Operations Dataverse-app met ondersteuning voor twee keer wegschrijven handmatig implementeren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

In dit artikel wordt uitgelegd hoe u Microsoft Dynamics 365 Project Operations handmatig kunt implementeren in Microsoft Dataverse zodat twee keer wegschrijven wordt ondersteund. In Project Operations wordt de configuratie van de omgeving gedetecteerd en wordt extra ondersteuning toegevoegd voor twee keer wegschrijven als aan de vereisten wordt voldaan.

Tijdens implementatie via Microsoft Dynamics Lifecycle Services (LCS), kunt u, als u de instructies in dit artikel hebt gevolgd, de implementatie van de Microsoft Power Platform-integratie (voorheen bekend als de Common Data Service-omgeving) overslaan.

Het implementatieproces van Project Operations in Dataverse zodat twee keer wegschrijven wordt ondersteund, heeft vier hoofdstappen:

1. [Een nieuwe omgeving in Dataverse maken waarin twee keer wegschrijven wordt ondersteund](#create).
2. [Vereisten voor twee keer wegschrijven toevoegen aan de omgeving](#prerequisites).
3. [De Project Operations Dataverse-app toevoegen](#dataverse).
4. [Uw omgevingen koppelen](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Een nieuwe omgeving in Dataverse maken waarin twee keer wegschrijven wordt ondersteund

Om deze procedure te voltooien, moet u zich aanmelden als beheerder.

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.com) en meld u aan als beheerder.
2. Maak een nieuwe omgeving en geef deze een naam.
3. Selecteer het omgevingstype. Als u zich hebt aangemeld voor de proefaanbieding, selecteert u **Proefversie (op abonnement gebaseerd)**.
4. Bevestig de implementatieregio.
5. Schakel de optie **Een database voor deze omgeving maken** in. 
6. Bevestig de taal en bevestig vervolgens dat de valuta overeenkomt met de valuta voor uw apps voor financiën en bedrijfsactiviteiten.
7. Schakel de optie **Dynamics 365-apps** in en bevestig dat het veld **Deze apps automatisch implementeren** is ingesteld op **Geen**.
8. Voeg een beveiligingsgroep toe als er een beveiligingsgroep is vereist.
9. Selecteer **Opslaan** om de omgeving te maken.
10. Wacht tot de implementatie is voltooid en de omgeving de status **Gereed** heeft.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Vereisten voor twee keer wegschrijven toevoegen aan de omgeving

Ondersteuning voor twee keer wegschrijven omvat extra velden die worden toegevoegd aan belangrijke entiteiten, zoals de entiteit **Bedrijf**. Als u ondersteuning voor twee keer wegschrijven toevoegt aan een bestaande omgeving, moet u mogelijk de gegevens bijwerken om de ondersteuning in te schakelen. Zie [Bootstrap van bedrijfsgegevens](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data) voor informatie over bootstrap voor de gegevens. Zie [Systeemvereisten voor twee keer wegschrijven](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req) voor meer informatie over twee keer wegschrijven.

Voltooi deze procedure om de vereisten voor twee keer wegschrijven aan uw omgeving toe te voegen.

1. Open de omgeving die u zojuist hebt gemaakt en ga naar **Resource** \> **Dynamics 365-apps**.
2. Selecteer **Kernoplossing voor twee keer wegschrijven** in de app-lijst en installeer deze.
3. Wacht tot de installatie is voltooid. Selecteer vervolgens **Indelingsoplossing voor twee keer wegschrijven** in de app-lijst en installeer deze.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>De Project Operations Dataverse-app toevoegen

U kunt deze procedure alleen voltooien als u de vorige procedures hebt voltooid voordat u Project Operations installeerde. Tijdens de installatie wordt de omgevingsconfiguratie geanalyseerd en wordt indien nodig ondersteuning voor twee keer wegschrijven toegevoegd.

1. Open de omgeving die u eerder hebt gemaakt en ga naar **Resource** \> **Dynamics 365-apps**.
2. Selecteer **Microsoft Dynamics 365 Project Operations** in de app-lijst en installeer deze.

## <a name="link-your-environments"></a><a name="link"></a>Uw omgevingen koppelen

Nadat de Dataverse-omgeving is geïmplementeerd, kunt u de koppeling instellen in uw apps voor financiën en bedrijfsactiviteiten. Voer de stappen uit in [De wizard voor twee keer wegschrijven gebruiken om uw omgevingen te koppelen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).

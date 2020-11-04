---
title: Microsoft Project Client-integratie
description: Het plannen en bijhouden van een projectplanning kan complex zijn, dus projectmanagers moeten tools gebruiken die hen helpen bij het beheren van deze taak. Integratie met Microsoft Project Client biedt ondersteuning voor het openen en beheren van een projectstructuur voor werkspecificatie.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074625"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client-integratie

[!include [banner](../includes/banner.md)]

Het plannen en bijhouden van een projectplanning kan complex zijn, dus projectmanagers moeten tools gebruiken die hen helpen bij het beheren van deze taak. Integratie met Microsoft Project Client biedt ondersteuning voor het openen en beheren van een projectstructuur voor werkspecificatie. De projectmanager kan eventuele wijzigingen terug publiceren naar de Dynamics 365 Finance-projectstructuur voor werkspecificatie.

> [!NOTE]
> Als u de update van juli (versie 10.0.4) gebruikt, moet u KB 4054797 en 4055884 installeren.

## <a name="configure-the-microsoft-project-client-add-in"></a>De invoegtoepassing Microsoft project Client configureren
Om de integratie met Microsoft Project Client mogelijk te maken, moet een Microsoft Dynamics 365-invoegtoepassing worden geïnstalleerd in de Microsoft Project-clienttoepassing van de gebruiker. Dit doet u door de **Werkruimte voor projectmanagement** te openen.

•   Klik op **Project Client-invoegtoepassing configureren** vanuit de sectie **Koppelingen** > **Instelling** van de werkruimte.

•   Klik op **Openen** en vervolgens op **Uitvoeren** als daarom gevraagd wordt.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Een bestaande conceptstructuur voor werkspecificatie openen en bewerken in Microsoft Project Client
Als een project in Dynamics 365 Finance al een structuur voor werkspecificatie heeft gemaakt, kan de structuur voor werkspecificatie worden geopend in de toepassing Microsoft Project Client als de structuur voor werkspecificatie zich in een conceptstatus bevindt. U kunt openen vanaf de pagina **Project** door op de koppeling **Openen in Microsoft Project** te klikken op het tabblad **Plannen**. Deze pagina kan ook worden geopend vanuit de Microsoft Project Client-toepassing door op **Openen** te klikken op het tabblad **Microsoft Dynamics 365**. Selecteer de **rechtspersoon** en het **project** in de lijst.

> [!NOTE]
> Als u Internet Explorer als uw browser gebruikt, moet u op **Opslaan** klikken om handmatig te openen vanaf de locatie waarnaar het bestand is gedownload. Of klik op **Opslaan en openen** om het bestand te openen in Microsoft Project Client. Wijzig de bestandsnaam niet tijdens het opslaan.

Voordat u het bestand bewerkt met Microsoft Project Client, moet u het eerst controleren. Klik op **Uitchecken** op het tabblad **Microsoft Dynamics 365**. Dit voorkomt dat andere gebruikers de structuur voor werkspecificatie tegelijkertijd kunnen bewerken binnen Finance. Als u de structuur voor werkspecificatie wilt publiceren nadat eventuele bewerkingen zijn voltooid, klikt u op **Inhecken** op het tabblad **Microsoft Dynamics 365**.

Als er al een projectteam is toegevoegd aan het project in Finance, wordt de resourcelijst gevuld met de teamleden. Als er nog geen projectteam aan het project is toegevoegd, kunt u resources selecteren en het team samenstellen binnen Microsoft Project Client door op de knop **Resources** te klikken op het tabblad **Microsoft Dynamics 365**. 

De volgende gegevens worden teruggesynchroniseerd naar Finance als onderdeel van het incheckproces:

•   Taaknaam

•   Begindatum

•   Einddatum

•   Voorgaande elementen

•   Resourcenamen

•   Categorie

•   Resourcecategorie

•   Werkuren

•   Notities

•   Prioriteit

> [!NOTE]
> Als u andere kolommen aan uw Microsoft Project Client-bestand toevoegt, worden deze niet in het bestand opgeslagen en worden ze niet weergegeven wanneer het bestand opnieuw wordt geopend.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>De structuur voor werkspecificatie maken voor een bestaand project met Microsoft Project Client
Als u een nieuwe structuur voor werkspecificatie wilt maken Microsoft Project Client, voert u deze stappen uit:


1.  Open Microsoft Project Client.

2.  Klik op het tabblad **Microsoft Dynamics 365** op **Openen**.

3.  Selecteer de **rechtspersoon** voor het project.

4.  Selecteer het **project**.

5.  Klik op **Uitchecken** op het tabblad **Microsoft Dynamics 365**.

6.  Als u gereed bent om naar Finance te publiceren, klikt u op **Inchecken** op het tabblad **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>De bestaande structuur voor werkspecificatie vervangen voor een bestaand project met Microsoft Project Client
Volg deze stappen om een nieuwe structuur voor werkspecificatie te maken met Microsoft Project Client en een bestaande structuur voor werkspecificatie te vervangen voor een bestaand project:

1.  Open de Microsoft Project Client.

2.  Maak de planning in Microsoft Project Client.

3.  Klik op het tabblad **Microsoft Dynamics 365** op **Wijzigingen opslaan** > **Bestaand project vervangen**.

4.  Selecteer de **rechtspersoon** voor het project.

5.  Selecteer het **project**.

6.  Klik op **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Een nieuw project makien vanuit Microsoft Project Client


1.  Open de Microsoft Project Client.

2.  Maak de planning in Microsoft Project Client.

3.  Klik op het tabblad **Microsoft Dynamics 365** op **Wijzigingen opslaan** > **Opslaan naar nieuw project**.

4.  Selecteer de **rechtspersoon** voor het project.

5.  Voer de **project-id** in, indien nodig.

6.  Voer de **projectnaam** in.

7.  Selecteer het **projecttype** , de **projectgroep** en de **projectcontract-id**. U kunt ook een nieuw projectcontract maken door op **Nieuw** te klikken.

8.  Selecteer de **agenda** die moet worden gebruikt voor het toewijzen van resources.

11. Klik op **OK**.

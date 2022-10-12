---
title: Functiewijzigingen van Project Service Automation naar Project Operations
description: Dit artikel biedt een overzicht van de functiewijzigingen van Microsoft Dynamics 365 Project Service Automation naar Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621216"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Functiewijzigingen van Project Service Automation naar Project Operations

Nadat een upgrade van een project is uitgevoerd van Microsoft Dynamics 365 Project Service Automation 3.X naar Dynamics 365 Project Operations Lite, is het bewerken van projecttaken in de structuur voor werkspecificatie (WBS) van het taakraster niet mogelijk. Klanten kunnen de WBS'en bekijken in het traceringsraster waar nieuwe velden zijn toegevoegd om alle details te verstrekken die verband houden met de taak. Voor projecten waarvoor bewerkingen in de WBS zijn vereist, kunt u in aanmerking komende projecten selectief converteren naar de nieuwe webplanningservaring van Project for the web.

## <a name="project-conversion-process"></a>Proces van projectconversie

Voer deze stappen uit om een project te converteren.

1. Open de hoofdpagina van het project en selecteer **Converteren** in het actievenster.
1. Selecteer **OK** in het venster voor bevestigingsberichten om de projectconversie te starten. De volgende acties vinden plaats:

    1. In een berichtenbalk op de hoofdpagina van het project verschijnt het bericht: "De projectplanning wordt geconverteerd. U kunt geen wijzigingen in het project aanbrengen totdat de conversie is voltooid."
    1. U wordt doorgestuurd naar de projectenlijst.

    Nadat de projectconversie is voltooid, vinden de volgende acties plaats:

    1. De toegewezen projectmanager ontvangt een melding aan de rechterkant van de toepassing.
    1. De berichtenbalk die aangeeft dat de conversie bezig is, wordt verwijderd.
    1. Het tabblad **Planning** toont de nieuwe planningservaring met Project for the web. Elke gebruiker met de juiste licenties en beveiligingsrollen kan de WBS bewerken.
    1. Het veld **Planningsengine** wordt bijgewerkt naar **Project for the web**.
    1. De knop **Converteren** wordt verwijderd uit het actievenster.

> [!IMPORTANT]
> Bulkconversie van projecten is niet toegestaan. Elke poging om een groot aantal projecten tegelijkertijd bij te werken, wordt beperkt. Deze beperking zorgt voor hoge prestaties voor alle klanten.

## <a name="manual-tasks-vs-automatic-tasks"></a>Handmatige taken versus automatische taken

Wanneer een upgrade van een omgeving wordt uitgevoerd van Project Service Automation naar Project Operations, worden alle taken in de WBS als automatisch gepland beschouwd. Het concept van handmatig geplande taken is niet beschikbaar in Project for the web. U kunt echter het geprefereerde planningsgedrag voor uw projecten definiëren met behulp van de instelling voor de [planningsmodus](/project-management/scheduling-modes.md) wanneer u nieuwe projecten maakt.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Beperkte bewerkingen voor pre-conversieprojecten

In dit gedeelte worden de functionele verschillen beschreven die u kunt verwachten als projecten niet zijn geconverteerd.

### <a name="copy-project"></a>Project kopiëren

De bewerking **Kopiëren** wordt alleen ondersteund voor geconverteerde projecten. Projecten waarvoor een upgrade is uitgevoerd kunnen niet worden gekopieerd vóór de conversie.

### <a name="move-project"></a>Project verplaatsen

Een wijziging in de begindatum van een project zal de start van de taken niet proportioneel verplaatsen, tenzij het project is geconverteerd.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Wat zijn de verschillen tussen geconverteerde projecten en nieuwe projecten die worden gemaakt nadat de upgrade is voltooid?

Voor projecten die worden geconverteerd nadat een upgrade van de omgeving is uitgevoerd, wordt een vlag ingesteld die de planning instrueert om alleen de projectagenda te respecteren. Dit gedrag komt overeen met het gedrag in Project Service Automation. De vlag wordt echter niet ingesteld voor nieuwe projecten die na de upgrade worden gemaakt. Daarom respecteert de planning de werkuren van resources wanneer ze aan een taak worden toegewezen.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Wat moet ik doen als mijn project niet kan worden geconverteerd?

Als uw project niet kan worden geconverteerd, is de eerste stap het bekijken van de foutenlogboeken om algemene problemen te identificeren die verband houden met uw WBS. Als de logboeken geen specifieke fout aangeven waarop u actie kunt ondernemen, neemt u contact op met de klantenondersteuning zodat uw zaak verder kan worden beoordeeld.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Hoe worden bedrijfssluitingen afgehandeld in Project for the web?

Project for the web houdt geen rekening met bedrijfssluitingen die de onderneming op organisatieniveau definieert. Het respecteert echter wel andere type vrije dagen die zijn gedefinieerd in een bepaalde werkuursjabloon.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Wat zijn de beperkingen van Project for the web?

Zie [Een structuur voor werkspecificatie maken: projectbeperkingen](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Kan ik wijzigingen verwachten in mijn kosten- en verkoopramingen?

In zeldzame gevallen waarin de contouren van resourcetoewijzingen opnieuw worden berekend of waarin ze op een andere datumgrens vallen dan het bronproject, ziet u mogelijk verschillen in verkoop- en kostenramingen. Als onderdeel van het upgradeproces wordt van klanten verwacht dat ze een representatieve voorbeeldset van projecten testen, zodat ze eventuele planningswijzigingen kunnen begrijpen.

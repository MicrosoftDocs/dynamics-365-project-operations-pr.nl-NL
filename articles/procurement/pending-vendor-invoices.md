---
title: Niet-voorradige materialen aanschaffen via een in behandeling zijnde leveranciersfactuur
description: In dit onderwerp wordt uitgelegd hoe u in behandeling zijnde leveranciersfacturen registreert.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547283"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Niet-voorradige materialen aanschaffen via een in behandeling zijnde leveranciersfactuur

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Als een bedrijf niet-voorradig materiaal voor een project aanschaft, kunnen de kosten direct op het project worden geboekt. 

Contoso Robotics US voert bijvoorbeeld een vernieuwingsproject voor apparatuur uit en heeft softwarelicenties nodig. Deze licenties worden aangeschaft bij een externe leverancier.  Met behulp van Dynamics 365 Finance registreert de crediteurenadministrateur een in behandeling zijnde leveranciersfactuur en rekent de licentiekosten rechtstreeks toe aan het vernieuwingsproject voor apparatuur. 

> [!IMPORTANT]
> Voordat u de functionaliteit gebruikt die in dit onderwerp wordt beschreven, moet u de vereiste configuraties bekijken en toepassen. Zie [Niet-voorradige materialen en in behandeling zijnde leveranciersfacturen inschakelen](configure-materials-nonstocked.md) voor meer informatie. 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Een projectgerelateerde in behandeling zijnde leveranciersfactuur boeken 

In behandeling zijnde leveranciersfacturen kunnen worden geregistreerd op de pagina **In behandeling zijnde leveranciersfacturen** (**Leveranciers** > **Facturen** > **In behandeling zijnde leveranciersfacturen**). Voer de volgende stappen uit om een projectgerelateerde in behandeling zijnde leveranciersfactuur te boeken:

1. Ga naar **Leveranciers** > **Facturen** en selecteer **Nieuw**. 
2. Selecteer in het veld **Factuurrekening** een leverancier en voer in het veld **Nummer** de identificatie van de leveranciersfactuur in.
3. Voeg een regel toe aan de leveranciersfactuur en selecteer in het veld **Artikelnummer** het niet-voorradige artikel dat bij de leverancier is gekocht. 

    > [!NOTE]
    > Leveranciersfactuurregels die zijn gebaseerd op een inkoopcategorie kunnen niet voor het project worden geregistreerd. 
    
5. Voeg de aangeschafte hoeveelheid toe. Het systeem vult de eenheidsprijs in op basis van de configuratie van de prijs voor het artikel dat niet op voorraad is. 
6. Controleer het totale bedrag en andere vereiste details op de regel.
7. Selecteer in de regeldetails, op het tabblad **Project**, de id van het project waarvoor dit artikel wordt vastgelegd.
8. Selecteer optioneel het activiteitnummer en werk de projectcategorie en regeleigenschap bij.
9. Boek de in behandeling zijnde leveranciersfactuur. Wanneer de factuur is geboekt, registreert het systeem:
    
    - Het saldo van de leverancier.
    - Het bedrag aan omzetbelasting.
    - De kosten voor het project worden geboekt op het inkoopintegratieaccount.
    - De werkelijke kostentransactie van het project in Dataverse.  Deze transactie wordt verder verwerkt met behulp van het [Project Operations Integration-journaal](../project-accounting/project-operations-integration-journal.md). Als dit journaal wordt geboekt, wordt het bedrag van het inkoopintegratieaccount verplaatst naar het projectkostenaccount. 
    - Aankopen die worden gefactureerd aan de projectklant met behulp van de factureringsmethode voor tijd en materialen. Daarnaast worden nog niet-gefactureerde verkooptransacties voor de aankopen gemaakt in Dataverse. De productprijslijst in Dataverse wordt gebruikt voor de verkoopprijzen en bedragen voor niet-gefactureerde verkooptransacties.

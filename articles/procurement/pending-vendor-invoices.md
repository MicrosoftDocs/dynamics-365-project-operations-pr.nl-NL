---
title: Niet-voorradige materialen aanschaffen via een in behandeling zijnde leveranciersfactuur
description: In dit onderwerp wordt uitgelegd hoe u in behandeling zijnde leveranciersfacturen registreert.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009030"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Niet-voorradige materialen aanschaffen via een in behandeling zijnde leveranciersfactuur

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Als een bedrijf niet-voorradig materiaal voor een project aanschaft, kunnen de kosten direct op het project worden geboekt. 

Stel bijvoorbeeld dat Contoso Robotics US een vernieuwingsproject voor apparatuur uitvoert en softwarelicenties nodig heeft. Deze licenties worden aangeschaft bij een externe leverancier.  Met behulp van Dynamics 365 Finance registreert de crediteurenadministrateur een in behandeling zijnde leveranciersfactuur en rekent de licentiekosten rechtstreeks toe aan het vernieuwingsproject voor apparatuur. 

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
    - De daadwerkelijke transactie van het project in Dataverse. Deze transactie wordt verder verwerkt met behulp van het [Project Operations Integration-journaal](../project-accounting/project-operations-integration-journal.md). Als dit journaal wordt geboekt, wordt het bedrag van het inkoopintegratieaccount verplaatst naar het projectkostenaccount.

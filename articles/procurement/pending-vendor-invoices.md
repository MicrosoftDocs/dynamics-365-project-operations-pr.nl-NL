---
title: Niet-voorradige materialen of inkoopcategorieën aanschaffen via een in behandeling zijnde leveranciersfactuur
description: In dit artikel wordt uitgelegd hoe u in behandeling zijnde leveranciersfacturen registreert.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921986"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Niet-voorradige materialen of inkoopcategorieën aanschaffen via een in behandeling zijnde leveranciersfactuur

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Als een bedrijf niet-voorradige materialen of inkoopcategorieën voor een project aanschaft, kunnen de kosten onmiddellijk worden geboekt voor het project. 

Contoso Robotics US voert bijvoorbeeld een vernieuwingsproject voor apparatuur uit en heeft softwarelicenties nodig. Deze licenties worden aangeschaft bij een externe leverancier.  Met Dynamics 365 Finance registreert de crediteurenadministratie een openstaand leveranciersfactuurdocument en schrijft de licentiekosten rechtstreeks toe aan het project voor apparatuurvernieuwing. 

> [!IMPORTANT]
> Voordat u de functionaliteit gebruikt die in dit artikel wordt beschreven, moet u de vereiste configuraties doornemen en toepassen. Zie [Niet-voorradige materialen en openstaande leveranciersfacturen inschakelen](configure-materials-nonstocked.md) en [Inkoopcategorieën gebruiken met projectinkooporders en openstaande leveranciersfacturen](configure-procurement-categories.md) voor meer informatie

## <a name="post-a-project-related-pending-vendor-invoice"></a>Een projectgerelateerde in behandeling zijnde leveranciersfactuur boeken 

In behandeling zijnde leveranciersfacturen kunnen worden geregistreerd op de pagina **In behandeling zijnde leveranciersfacturen** (**Leveranciers** > **Facturen** > **In behandeling zijnde leveranciersfacturen**). Voer de volgende stappen uit om een projectgerelateerde in behandeling zijnde leveranciersfactuur te boeken:

1. Ga naar **Leveranciers** > **Facturen** en selecteer **Nieuw**. 
1. Selecteer in het veld **Factuuraccount** een leverancier en voer vervolgens, in het veld **Nummer** de identificatie van de leveranciersfactuur in.
1. Voeg een regel toe aan de leveranciersfactuur en selecteer vervolgens in het veld **Artikelnummer** het niet-voorradige artikel dat bij de leverancier is gekocht. Als alternatief selecteert u in het veld **Inkoopcategorie** de inkoopcategorie die bij de leverancier is gekocht.   
1. Voeg de hoeveelheid toe die is gekocht. Het systeem vult de eenheidsprijs in op basis van de configuratie van de prijs voor niet-voorradige artikelen. 
1. Controleer het totale bedrag en andere vereiste details op de regel.
1. Selecteer in de regeldetails, op het tabblad **Project**, de id van het project waarvoor dit artikel wordt vastgelegd.
1. Optioneel: selecteer het activiteitsnummer en werk de projectcategorie en regeleigenschap bij.
1. Boek vervolgens de in behandeling zijnde leveranciersfactuur. Wanneer de factuur is geboekt, registreert het systeem de volgende informatie:
    
    - Het saldo van de leverancier.
    - Het bedrag aan omzetbelasting.
    - De kosten voor het project worden geboekt op het inkoopintegratieaccount.
    - De werkelijke kostentransactie van het project in Dataverse.  Deze transactie wordt verder verwerkt met behulp van het [Project Operations Integration-journaal](../project-accounting/project-operations-integration-journal.md). Als dit journaal wordt geboekt, wordt het bedrag van het inkoopintegratieaccount verplaatst naar het projectkostenaccount. 
    - Aankopen die worden gefactureerd aan de projectklant met behulp van de factureringsmethode voor tijd en materialen. Daarnaast worden nog niet-gefactureerde verkooptransacties voor de aankopen gemaakt in Dataverse. De productprijslijst in Dataverse wordt gebruikt voor de verkoopprijzen en bedragen voor niet-gefactureerde verkooptransacties.

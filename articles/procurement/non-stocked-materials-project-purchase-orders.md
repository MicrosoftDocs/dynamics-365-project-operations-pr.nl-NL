---
title: Niet-voorradige materialen bestellen voor een project met behulp van projectinkooporders
description: In dit onderwerp wordt uitgelegd hoe u niet-voorradige materialen kunt bestellen voor een project met behulp van projectinkooporders.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563016"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Niet-voorradige materialen bestellen voor een project met behulp van projectinkooporders

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

De inkoopafdeling in uw organisatie kan gebruikmaken van [inkooporders](/dynamics365/supply-chain/procurement/purchase-order-overview) om orders van goederen en diensten bij te houden. Inkooporders voor niet-voorradige materialen kunnen worden toegewezen aan een project. Door deze inkooporders te factureren, worden de kosten vastgelegd voor het project.

## <a name="prerequisites"></a>Vereisten
Voer de volgende stappen uit om de functionaliteit voor projectinkooporders in te schakelen.

1. Ga in Dynamics 365 Finance naar de werkruimte **Functiebeheer**.
2. Zoek en selecteer in de functielijst de functie **Projectinkooporders inschakelen in Project Operations voor op resources gebaseerde/niet-voorraadscenario's**.
3. Selecteer **Inschakelen**.
4. Configureer niet-voorradige materialen en openstaande leveranciersfacturen zoals beschreven in [Niet-voorradige materialen en openstaande leveranciersfacturen configureren](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Een projectinkooporder maken vanuit de projectinkooporderlijst

1. Ga in Finance naar **Projectbeheer en boekhouding** > **Projecten** > **Alle projecten** en selecteer een project.
2. Selecteer in het actievenster op het tabblad **Beheren** in de groep **Nieuw** de optie **Artikeltaak** > **Inkooporder**.
3. Selecteer op de pagina **Inkooporder maken** de leverancier bij wie u de inkooporder wilt plaatsen, voer eventueel andere informatie in en selecteer vervolgens **OK**.
4. Selecteer op de pagina **Inkooporder** in het raster **Inkooporderregels** de optie **Regel toevoegen**.
5. Voer indien nodig een artikelnummer, hoeveelheid, eenheid, prijs per eenheid en andere informatie in.

    > [!NOTE]
    > Alleen niet-voorradige artikelen en services kunnen worden gebruikt met projectinkooporders. Voorraadartikelen en aanschaffingscategorieën worden niet ondersteund.

6. Ga zo nodig door met het toevoegen van artikelen en bevestig de inkooporder.

    Ontvangsten van goederen en diensten kunnen worden vastgelegd door een productontvangst te maken en te boeken.

    > [!NOTE]
    > Productontvangsten worden niet vastgelegd in de werkelijke projectwaarden in Microsoft Dataverse en hebben geen invloed op het subgrootboek van het project.

    Nadat een leverancier de factuur voor artikelen en services in de inkooporder heeft verzonden, kan de inkoopafdeling een factuur voor de inkooporder genereren door naar **Factuur** > **Genereren** > **Factuur** in het actievenster te gaan. Zie [Niet-voorradige materialen kopen via een openstaande leveranciersfactuur](pending-vendor-invoices.md) voor meer informatie over openstaande leveranciersfacturen.

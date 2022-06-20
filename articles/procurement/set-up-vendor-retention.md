---
title: Leveranciersinhoudingen instellen
description: In dit artikel wordt uitgelegd u leveranciersinhoudingen instelt.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f30e8829d8d5d99c81fce730cb93cd7ce31913fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929760"
---
# <a name="set-up-vendor-retention"></a>Leveranciersinhoudingen instellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel biedt informatie over het instellen van leveranciersinhoudingen.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Een leveranciersinhoudingsrekening instellen in het grootboek

1. Ga in Dynamics 365 Finance naar **Grootboek** > **Boekingsinstellingen** > **Rekeningen voor automatische transacties**.
2. Voeg een nieuwe regel toe.
3. Selecteer **Leveranciersinhouding** in het veld **Boekingstype**.
4. Selecteer de hoofdrekening voor de boeking voor leveranciersinhoudingen.

## <a name="create-vendor-retention-terms"></a>Inhoudingstermijnen voor leveranciers maken

Gebruik de pagina **Voorwaarden voor leveranciersinhoudingen** om inhoudingsvoorwaarden leveranciersbetalingen in te stellen en te onderhouden. Voer het percentage van de leveranciersbetaling die moet worden ingehouden in en het percentage van de eerder ingehouden bedragen dat u wilt vrijgeven. Bedragen worden automatisch ingehouden op leveranciersfacturen totdat het contract de opgegeven status van voltooiing bereikt. Nadat er inhoudingsvoorwaarden zijn ingesteld voor een leverancier, kunt u deze toepassen op elk project waaraan de leverancier werkt.

1. Ga in Finance naar **Projectbeheer en financiële administratie** > **Instellingen** > **Inhouding** > **Inhoudingsvoorwaarden voor leveranciersbetalingen**.
2. Selecteer **Nieuw** om een nieuwe inhoudingstermijn voor leveranciers toe te voegen. De waarde in het veld **Regel-id** voor de nieuwe voorwaarde wordt automatisch ingevoerd. 
3. Voer in het veld **Beschrijving** een beschrijvende naam voor de nieuwe voorwaarde in.
4. Selecteer op het tabblad **Voorwaarden** de optie **Regel toevoegen** om een voorwaarde voor leveranciersinhoudingen in te voeren.
5. Voer in het veld **Percentage geleverde eenheden** een voltooiingspercentage voor de regel in. Bedragen worden automatisch op leveranciersfacturen ingehouden totdat de voltooiingsfase van het project gelijk is aan het percentage dat u invoert. Als u bijvoorbeeld 50,00 invoert, worden bedragen ingehouden totdat het project voor 50 procent is voltooid.
6. Voer in het veld **In te houden percentage** het percentage in van een bedrag op de leveranciersfactuur dat moet worden ingehouden. Als u in dit veld bijvoorbeeld 10,00 invoert in dit veld, wordt 10 procent van het bedrag op leveranciersfacturen ingehouden totdat het project het voltooiingspercentage bereikt dat u selecteert in het veld **Percentage geleverde eenheden**.
7. Voer in het veld **Vrij te geven percentage** het percentage in van eventuele eerder ingehouden bedragen die moeten worden vrijgegeven bij het aangewezen voltooiingsniveau van het project.

> [!NOTE]
> Als er meer dan één mijlpaal is ingesteld voor verschillende voltooiingsniveaus van een project, voert u een afzonderlijke regel met een voorwaarde voor leveranciersinhoudingen in voor elke inhoudingsregel. Elke regel kan een ander in te houden percentage betekenen en een ander vrij te geven percentage voor elk aangewezen voltooiingsniveau van een project.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Een leveranciersovereenkomst instellen voor het project

De voorwaarden voor leveranciersinhoudingen instellen die van toepassing zijn op het project. De inhoudingstermijnen voor leveranciers worden ook weergegeven op inkooporders die u voor de leverancier maakt.

1. Ga in Finance naar **Projectbeheer en financiële administratie** > **Projecten** > **Alle projecten**. 
2. Selecteer een project en selecteer in het actievenster de optie **Projectgroep** > **Leveranciersovereenkomsten**.
3. Voeg op de pagina **Leveranciersovereenkomsten** een nieuwe regel toe.
4. Selecteer in het veld **Rekeningcode** een van de volgende opties:
   - **Tabel**: de inhoudingstermijnen voor leveranciers zijn van toepassing op één leverancier.
   - **Groep**: de inhoudingstermijnen voor leveranciers zijn van toepassing op alle leveranciers in een leveranciersgroep.
   - **Alle**: de inhoudingstermijnen voor leveranciers zijn van toepassing op alle leveranciers.
5. Selecteer in het veld **Leverancier/Leveranciersgroep** de leverancier of leveranciersgroep waarop de inhoudingstermijnen voor leveranciers van toepassing zijn. Als u **Alle** hebt gekozen in de vorige stap, is dit veld niet beschikbaar.
6. Selecteer in het veld **Voorwaarden voor leveranciersinhoudingen** de regel-id voor de inhoudingsvoorwaarden die van toepassing zijn op deze leverancier.


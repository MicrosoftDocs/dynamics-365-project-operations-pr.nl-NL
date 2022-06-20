---
title: Onder contract nemen van projectteamleden
description: In dit artikel wordt uitgelegd hoe u projectteamleden onder contract neemt in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 649687cb9ac66e684069434a353b63155103aefb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916880"
---
# <a name="subcontracting-project-team-members"></a>Onder contract nemen van projectteamleden

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In Microsoft Dynamics 365 Project Operations kunt u ervoor kiezen om teamleden voor onbemande of bemande projecten onder contract te nemen.

- Teamleden van onbemande projecten hebben een algemene resource toegewezen gekregen.
- Teamleden van bemande projecten hebben een benoemde resource toegewezen gekregen.

Wanneer u een projectteamlid aan een toeleveringscontractregel koppelt, worden de kosten van eventuele toewijzingen aan taken die het teamlid heeft opnieuw berekend op basis van de inkoopprijslijst die aan het toeleveringscontract is gekoppeld.  Op het tabblad **Schattingen** op de pagina **Projectgegevens** selecteert u de knop **Prijzen bijwerken** om bijgewerkte prijzen en/of kostprijsberekeningen te zien die voortvloeien uit de beslissing om uit te besteden. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Een teamlid voor een onbemand project onder contract nemen
Op de pagina **Gegevens teamlid** staan toeleveringscontract- en toeleveringscontractregelvelden waarmee een projectmanager kan aangeven hoe de benodigde capaciteit uit een toeleveringscontract gehaald moet worden. Volg deze stappen om een projectteamlid onder contract te nemen als algemene resource:

1.  Kies een toeleveringscontract op de pagina **Details teamlid**.

2.  U kunt alleen toeleveringscontracten selecteren met **Concept** of **Bevestigd** als status. Toeleveringscontracten met **Gesloten** of **Geannuleerd** als status kunnen niet worden geselecteerd. 

3.  Het veld **Toeleveringscontractregel** wordt zichtbaar nadat u een toeleveringscontract hebt geselecteerd.

4.  In het veld **Toeleveringscontractregel** kunt u alleen toeleveringscontractregels selecteren die voor tijd zijn. U kunt geen toeleveringscontractregels voor onkosten of materiaal selecteren.

5.  De rol voor de record van het projectteamlid moet overeenkomen met de rol op de toeleveringscontractregel. Dit zorgt ervoor dat de tijd voor de rol die voor het project wordt geschat, dezelfde is als de rol die is ingekocht op de toeleveringscontractregel. 

Wanneer een algemeen teamlid is gekoppeld aan een toeleveringscontract en toeleveringscontractregel, wordt het veld **Werknemertype** op de algemene-teamlidrij bijgewerkt naar **Contractwerknemer** en **Geldigheid toeleveringscontract** zal worden ingesteld op **Geldig**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Een teamlid voor een bemand project onder contract nemen
Net als bij leden van algemene of onbemande teams, kan de voor een project benodigde capaciteit van bemande-teamleden ook worden gekoppeld aan een toeleveringscontract. Volg deze stappen om een benoemd projectteamlid onder contract te nemen:

1.  Zorg ervoor dat de benoemde resource is ingesteld als een boekbare resource van het type contractwerknemer. Zorg er ook voor dat het veld **Leverancier** op de boekbare resource overeenkomt met de leverancier op het toeleveringscontract dat u selecteert. 

2.  U kunt alleen toeleveringscontracten selecteren met **Concept** of **Bevestigd** als status. Toeleveringscontracten met **Gesloten** of **Geannuleerd** als status kunnen niet worden geselecteerd. 

3.  Het veld **Toeleveringscontractregel** wordt zichtbaar nadat u een toeleveringscontract hebt geselecteerd.

4.  In het veld **Toeleveringscontractregel** kunt u alleen toeleveringscontractregels selecteren die voor tijd zijn. U kunt geen toeleveringscontractregels voor onkosten of materiaal selecteren.

5.  De rol voor de record van het projectteamlid moet overeenkomen met de rol op de toeleveringscontractregel. Dit zorgt ervoor dat de tijd voor de rol die voor het project wordt geschat, dezelfde is als de rol die is ingekocht op de toeleveringscontractregel. 

Benoemde projectteamleden die zijn ingesteld als contractwerknemerstype van **Boekbare resource** wordt weergegeven met een geldigheidsstatus van het toeleveringscontract van **Niet geldig** als ze niet gekoppeld zijn aan een toeleveringscontract. Wanneer een benoemd projectteamlid is gekoppeld aan een toeleveringscontract en toeleveringscontractregel, wordt het veld **Werknemertype** op de algemene-teamlidrij bijgewerkt naar **Contractwerknemer** en **Geldigheid toeleveringscontract** zal worden ingesteld op **Geldig**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

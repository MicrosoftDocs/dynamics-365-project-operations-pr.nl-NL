---
title: Beveiliging en goedkeuringen
description: Dit artikel bevat informatie over de beveiligingsconfiguratie voor het werken met goedkeuringen in Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841917"
---
# <a name="security-and-approvals"></a>Beveiliging en goedkeuringen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Microsoft Dynamics 365 Project Operations gebruikt twee beveiligingsrollen voor de goedkeuring van tijds-, onkosten- en materiaalposten:

- Projectfiatteur
- Beheerder van projectfiatteur

## <a name="project-approver"></a>Projectfiatteur

U moet over de beveiligingsrol **Projectgoedkeurder** beschikken om de projecttijd-, onkosten- en materiaalposten goed te keuren. U moet ook toegang hebben tot de relevante gerelateerde entiteiten, zoals **Project**. Die toegang kan worden toegewezen door iemand met de rol **Projectmanager**. Bovendien moet u een teamlid van het project zijn en als fiatteur zijn gemarkeerd.

Om niet-projectboekingen goed te keuren, moet u de manager van de indiener zijn.

## <a name="project-approver-admin"></a>Beheerder van projectfiatteur

> [!NOTE]
> De functie [Goedkeuringssets](approval-sets.md) moet zijn ingeschakeld voordat u de functionaliteit Beheerder van projectfiatteur kunt gebruiken.

Met de beveiligingsrol **Beheerder van projectfiatteur** kunnen gebruikers beleid omzeilen en boekingen voor alle projecten goedkeuren. Toewijzing van deze rol omzeilt de validatielogica waarbij het teamlidmaatschap en de markering als fiatteur vereist is. U moet toegang hebben tot de relevante gerelateerde tabellen, zoals **Project**, via beveiligingsrollen die aan u zijn toegewezen.

De gebruikerscontext SYSTEM omzeilt validaties op dezelfde manier als de beveiligingsrol Beheerder van projectfiatteur.

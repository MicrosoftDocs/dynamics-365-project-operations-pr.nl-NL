---
title: Planningsmodi
description: Dit onderwerp biedt informatie over planningsmodi.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981429"
---
# <a name="scheduling-modes"></a>Planningsmodi

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


Dynamics 365 Project Operations biedt organisaties de mogelijkheid om te definiëren hoe zij wijzigingen in sleutelvariabelen in taken binnen de structuur voor werkspecificatie beheren. Op basis van de specifieke behoeften van de organisatie kunnen projectmanagers wijzigingen aanbrengen in de planningsmodus wanneer een project wordt gemaakt.

Er zijn drie planningsmodi beschikbaar in Project Operations:

  - Vaste duur (dit is de standaardmodus)
  - Vast werk
  - Vaste eenheden

De waarden die worden beïnvloed door de definitie van een specifieke planningsmodus, worden bepaald door de volgende formule:

  Inspanning (*Werk*) = Duur x Eenheden

Wanneer u de planningsmodus van een project definieert, stelt u een van deze waarden in, die dan niet kunnen worden gewijzigd. Als u deze waarde als een constante aanhoudt, krijgt die waarde een prioriteit, waardoor het systeem wordt geïnformeerd dat deze niet moet worden gewijzigd wanneer de andere twee waarden veranderen. De volgende tabel bevat informatie over de gevolgen van het selecteren van een specifieke modus.

| **In deze taak**             | **Als u eenheden herziet**   | **Als u duur herziet** | **Als u inspanning herziet**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Taak met vaste eenheden     | Duur wordt opnieuw berekend. | Inspanning wordt opnieuw berekend.    | Duur wordt opnieuw berekend. |
| Taak met vaste inspanning    | Duur wordt opnieuw berekend. | Eenheden worden opnieuw berekend.    | Duur wordt opnieuw berekend. |
| Taak met vaste duur  | Inspanning wordt opnieuw berekend.   | Inspanning wordt opnieuw berekend.    | Eenheden worden opnieuw berekend.   |

Zie [Het taaktype wijzigen voor een nauwkeurigere planning](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72) voor meer informatie over de implicaties van een bepaalde modus. In het onderwerp wordt de term **Werk** gebruikt in plaats van **Inspanning**.

## <a name="change-the-organizations-scheduling-mode"></a>De planningsmodus van de organisatie wijzigen

Voer de volgende stappen uit om de planningsmodus van een organisatie te definiëren.

1. Ga naar **Instellingen** \> **Algemeen** \> **Parameters** en selecteer vervolgens de projectparameter. 
2. Selecteer op de pagina **Projectparameters** de standaardplanningsmodus voor de organisatie en definieer vervolgens de mogelijkheid voor de projectmanager om de instelling te overschrijven bij het maken van een nieuw project.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>De instelling voor de planningsmodus wijzigen in een project

Als een organisatie de projectmanager toestaat om de standaardplanningsmodus te overschrijven, kan de projectmanager die wijziging doorvoeren bij het maken van een nieuw project. Nadat het project is opgeslagen, kan de planningsmodus echter niet meer worden gewijzigd.

## <a name="copied-projects"></a>Gekopieerde projecten

Omdat een project wordt gemaakt wanneer de actie voor het kopiëren van een project wordt uitgevoerd, kan de projectmanager de planningsmodus niet instellen. Het bestemmingsproject zal altijd standaard de modus gebruiken die op organisatieniveau is gedefinieerd.

## <a name="copied-tasks"></a>Gekopieerde taken

Wanneer een taak van het ene project naar het andere wordt gekopieerd, neemt de taak de planningsmodus van het bestemmingsproject over.

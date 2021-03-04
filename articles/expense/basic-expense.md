---
title: Onkostenpost (Lite)
description: Dit onderwerp biedt informatie over het werken met onkosteninvoer in een Lite-implementatie.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590940"
---
# <a name="expense-entry-lite"></a>Onkostenpost (Lite)

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Eenvoudig, of Lite, onkostenbeheer is de mogelijkheid om eenvoudige onkosten vast te leggen. U kunt onkosten voor een project boeken waarna de projectfiatteur deze beoordeelt en goedkeurt.

Meer informatie over onkostenfuncties in Dynamics 365 Project Operations vindt u in [Onkostenoverzicht](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Eenvoudige onkosten vastleggen

U kunt uw onkosten vastleggen, zodat u ze kunt indienen bij de fiatteur.

1. Ga naar **Onkosten** en selecteer **Nieuw**.
2. Voer op de pagina **Nieuwe onkosten** de vereiste onkostengegevens in en selecteer vervolgens **Opslaan**.

## <a name="submit-a-basic-expense"></a>Eenvoudige onkosten indienen

Nadat u al uw onkosten hebt vastgelegd en klaar bent om deze te laten goedkeuren, moet u ze indienen.

1. Ga naar **Onkosten** en selecteer een item. Of selecteer alle onkosten met behulp van het selectievakje in de koptekst.
2. Selecteer **Indienen**. De geselecteerde items worden verwerkt en vervolgens worden er aanvragen voor onkostengoedkeuring gemaakt.

## <a name="add-an-attachment"></a>Een bijlage toevoegen

Mogelijk moet u de fiatteur aanvullende documentatie over uw onkosten verstrekken. U kunt een ontvangstbewijs bijvoegen in de tijdlijn van de onkosteninvoer. Selecteer **Bewerken** in de sectie **Tijdlijn** en selecteer vervolgens het paperclippictogram om uw ontvangstbewijs bij te voegen.

## <a name="recall-a-basic-expense"></a>Eenvoudige onkosten intrekken

Als u onkosten per ongeluk indient, kunt u deze intrekken. Binnen hoeveel tijd u onkosten moet intrekken, is afhankelijk van de goedkeuringsfase.  Als de fiatteur de onkosten nog niet heeft goedgekeurd, kan de intrekking onmiddellijk plaatsvinden. Is de boeking echter al goedgekeurd, dan wordt de fiatteur gevraagd om de intrekking goed te keuren en de transacties terug te draaien.

1. Ga naar **Onkosten** en selecteer vervolgens in de lijst met onkosten de onkosten die u wilt intrekken.
2. Selecteer **Intrekken**. Als de onkostenvermelding nog niet is goedgekeurd, wordt deze direct ingetrokken. Als de onkostenvermelding al is goedgekeurd, wordt een intrekkingsverzoek gemaakt om de fiatteur te laten weten dat u de onkosten wilt storneren. De fiatteur bevestigt dan dat de terugboeking kan worden uitgevoerd.

## <a name="delete-a-basic-expense"></a>Eenvoudige onkosten verwijderen

Onkosten die nog niet zijn ingediend, kunnen worden verwijderd. Om onkosten te verwijderen die al zijn ingediend, moet u deze eerst intrekken.

## <a name="see-also"></a>Zie ook

- [Overzicht van goedkeuringen](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
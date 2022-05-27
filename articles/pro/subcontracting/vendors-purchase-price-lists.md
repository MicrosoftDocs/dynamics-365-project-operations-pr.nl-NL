---
title: Beheer van leveranciers- en inkoopprijslijsten in Project Operations
description: Dit onderwerp biedt informatie die u helpt bij het maken en onderhouden van leveranciersgegevens en inkoopprijslijsten voor onderaanneming.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576724"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Beheer van leveranciers- en inkoopprijslijsten in Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

## <a name="vendors-in-project-operations"></a>Leveranciers in Project Operations

In Microsoft Dynamics 365 Project Operations hebben leveranciersaccounts het relatietype **Verkoper** of **Leverancier**. U kunt alleen een accountrecord met een van deze relatietypen selecteren als leverancier op een subcontract.

U kunt een of meer inkoopprijslijsten koppelen aan een verkopersrecord. Elke inkoopprijslijst die aan een verkopersrecord is gekoppeld, moet echter een duidelijke datumeffectiviteit hebben. Project Operations ondersteunt geen overlappende datumeffectiviteit voor inkoopprijslijsten.

Standaard worden de volgende velden en concepten in een leveranciersrecord gebruikt voor elk subcontract dat voor de verkoper wordt gemaakt:

- Betalingsvoorwaarden
- Contactpersoon voor factuur
- Primaire contactpersoon

    > [!NOTE]
    > Standaard wordt de primaire contactpersoon van de verkoper gebruikt als de leveranciersaccountmanager van het subcontract.

- Valuta
- Huidige inkoopprijslijsten

## <a name="purchase-price-lists-in-project-operations"></a>Inkoopprijslijsten in Project Operations

Een prijslijst waarbij het veld **Context** is ingesteld op **Aankoop** wordt als een inkoopprijslijst beschouwd. Inkoopprijslijsten kunnen worden gedefinieerd om een catalogus van inkooptarieven voor tijd, onkosten en materialen weer te geven. Inkoopprijslijsten lijken op kostprijs- en verkoopprijslijsten in Project Operations. De volgende concepten gelden voor inkoopprijslijsten op dezelfde manier als voor kostprijs- en verkoopprijslijsten:

- **Datumeffectiviteit**: inkoopprijslijsten hebben datumeffectiviteit. Datumeffectiviteit wordt weergegeven via velden voor begindatum en einddatum in elke prijslijst. De tijd tussen de begindatum en de einddatum is de datumeffectiviteitsperiode.
- **Valuta**: de valuta in de koptekst van de prijslijst wordt gebruikt als de valuta waarin inkoopprijzen worden uitgedrukt voor arbeid, onkostencategorieën en producten in de catalogus.
- **Standaardtijdseenheid**: de standaardtijdseenheid drukt de arbeidsprijzen voor aankopen uit. Het tijdseenheidsveld in een prijslijst wordt alleen gebruikt om een standaardwaarde op te geven. Die waarde kan worden gewijzigd in prijsrijen voor afzonderlijke rollen.

Inkoopprijslijsten kunnen aan leveranciersrecords worden toegevoegd als koppelingen die projectprijslijsten worden genoemd. Deze prijslijsten worden gebruikt om standaardprijzen op subcontractregels in te voeren. Als er meerdere inkoopprijslijsten aan een leveranciersrecord zijn gekoppeld, wordt standaard de meest actuele prijslijst gebruikt voor subcontracten die voor de leverancier zijn gemaakt. Alleen prijslijsten waarbij het veld **Context** is ingesteld op **Aankoop** kunnen aan leveranciersrecords worden gekoppeld.

### <a name="subcontract-specific-purchase-price-lists"></a>Subcontractspecifieke inkoopprijslijsten

Inkoopprijslijsten kunnen tevens aan subcontracten worden toegevoegd als koppelingen die projectprijslijsten worden genoemd. Deze prijslijsten worden gebruikt om standaardprijzen op subcontractregels in te voeren. Als er meerdere inkoopprijslijsten aan een subcontract zijn gekoppeld, moet elk standaard een afzonderlijke datumeffectiviteit hebben. Project Operations ondersteunt geen inkoopprijslijsten met overlappende datumeffectiviteit. Alleen prijslijsten waarbij het veld **Context** is ingesteld op **Aankoop** kunnen aan subcontracten worden gekoppeld.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Creditcardtransacties importeren en onderhouden
description: In dit onderwerp wordt uitgelegd hoe u onkostengerelateerde creditcardtransacties importeert en onderhoudt. Deze transacties kunnen zo worden ingesteld dat ze automatisch worden geïmporteerd volgens een periodiek schema, of ze kunnen handmatig worden geïmporteerd als ze nodig zijn.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951068"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Creditcardtransacties importeren en onderhouden

Onkostengerelateerde creditcardtransacties kunnen zo worden ingesteld dat ze automatisch volgens een terugkerende planning worden geïmporteerd. U kunt de transacties ook handmatig importeren als u ze nodig hebt. De creditcardtransacties worden geïmporteerd via de gegevensentiteit Creditcardtransacties.

Zie [Gegevensentiteiten](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities) voor meer informatie over gegevensentiteiten.

## <a name="import-credit-card-transactions"></a>Creditcardtransacties importeren

1. Selecteer op de pagina **Creditcardtransacties** de optie **Transacties importeren**. Als u gegevensbeheer voor het eerst opent, moet het systeem de lijst met gegevensentiteiten bijwerken voordat u verder kunt gaan.
2. Geef een unieke naam voor de importtaak op in het veld **Naam**.
3. Selecteer in het veld **Brongegevensindeling** de indeling van het bestand met de creditcardtransacties die u wilt importeren.
4. Selecteer **Uploaden** en selecteer het bestand dat u wilt importeren.
5. Nadat het bestand is geüpload, controleert u de toewijzing van het creditcardtransactiebestand en de kolommen van de gegevensentiteit Creditcardtransacties door de koppeling **Toewijzing weergeven** op de tegel te selecteren. Als er toewijzingsfouten zijn, of als u de toewijzing moet wijzigen, brengt u de wijzigingen in de toewijzing aan op het tabblad **Visualisering van toewijzing** of het tabblad **Toewijzingsdetails**.
6. Selecteer **Terugkerende gegevenstaak maken** om de creditcardtransacties te automatiseren. U kunt vervolgens het terugkeerpatroon instellen dat bepaalt hoe vaak creditcardtransacties moeten worden geïmporteerd. Als u klaar bent, selecteert u **OK**.
7. Selecteer **Importeren** om het geselecteerde bestand nu te importeren.
8. Als er fouten optreden tijdens het importeren, kunt u het uitvoeringslogboek of de faseringsgegevens bekijken om de fouten weer te geven die u moet herstellen om het bestand te kunnen importeren.

> [!NOTE]
> Als u meer dan een bestandsindeling moet importeren, moet u voor elk indelingstype een afzonderlijke importtaak maken.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>De creditcardtransacties opnieuw toewijzen aan werknemers van wie het dienstverband is beëindigd

Nadat een werknemersrecord is verwijderd, wordt het Active Directory Domain Services-account (AD DS) van de werknemer uitgeschakeld. Er kunnen echter actieve creditcardtransacties zijn die alsnog moeten worden afgeschreven en terugbetaald. Op de pagina **Creditcardtransacties** kunt u de werknemer opnieuw toewijzen voor elke creditcardtransactie waaruit de gekoppelde werknemer is verwijderd.

Selecteer een of meer creditcardtransacties en selecteer vervolgens **Transacties opnieuw toewijzen**. U kunt vervolgens een andere werknemer selecteren aan wie u de creditcardtransacties wilt toewijzen. Nadat de creditcardtransacties opnieuw zijn toegewezen, kunnen ze worden geselecteerd voor een onkostennota en worden betaald via het gebruikelijke proces voor terugbetaling van onkostennota's.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
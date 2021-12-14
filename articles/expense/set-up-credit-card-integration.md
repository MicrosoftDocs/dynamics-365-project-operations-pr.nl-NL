---
title: Creditcardintegratie instellen
description: In dit onderwerp wordt uitgelegd hoe u kunt werken met onkostengerelateerde creditcardtransacties.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 49c8f2369a8be41fbc04c74bdb6b565b4f4b7b79
ms.sourcegitcommit: 9f26cf8bb640af1eb9f7f0872805965d7ffcb9d3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/19/2021
ms.locfileid: "7826250"
---
# <a name="set-up-credit-card-integration"></a>Creditcardintegratie instellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Onkostengerelateerde creditcardtransacties kunnen zo worden ingesteld dat ze automatisch volgens een terugkerende planning worden geïmporteerd. U kunt de transacties ook handmatig importeren als u ze nodig hebt. De creditcardtransacties worden geïmporteerd via de gegevensentiteit voor creditcardtransacties.

## <a name="import-credit-card-transactions"></a>Creditcardtransacties importeren

Volg deze stappen om creditcardtransacties te importeren:

1. Selecteer op de pagina **Creditcardtransacties** de optie **Transacties importeren**. Als u gegevensbeheer voor het eerst opent, moet het systeem de lijst met gegevensentiteiten bijwerken voordat u verder kunt gaan.
2. Voer in het veld **Naam** een unieke beschrijving in voor de importtaak.
3. Selecteer in het veld **Brongegevensindeling** de indeling van het bestand met de creditcardtransacties die u wilt importeren.
4. Selecteer **Uploaden** en selecteer het bestand dat u wilt importeren.
5. Nadat het bestand is geüpload, controleert u de toewijzing van het creditcardtransactiebestand en de kolommen van de gegevensentiteit voor creditcardtransacties door de koppeling **Toewijzing weergeven** op de tegel te selecteren. Als er toewijzingsfouten zijn, of als u de toewijzing moet wijzigen, brengt u de wijzigingen in de toewijzing aan op het tabblad **Visualisering van toewijzing** of het tabblad **Toewijzingsdetails**.
6. Selecteer **Terugkerende gegevenstaak maken** om de creditcardtransacties te automatiseren. U kunt vervolgens het terugkeerpatroon instellen dat bepaalt hoe vaak creditcardtransacties moeten worden geïmporteerd. Als u klaar bent, selecteert u **OK**.
7. Selecteer **Importeren** om het geselecteerde bestand nu te importeren.
8. Als er fouten optreden tijdens het importeren, kunt u het uitvoeringslogboek of de faseringsgegevens bekijken om te zien welke fouten u moet oplossen om een succesvolle import te garanderen.

> [!NOTE]
> Als u meer dan één bestandsindeling moet importeren, moet u voor elk indelingstype afzonderlijke importtaken maken.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>De creditcardtransacties opnieuw toewijzen aan werknemers van wie het dienstverband is beëindigd

Nadat een werknemersrecord is verwijderd, wordt het Active Directory Domain Services-account (AD DS) van de werknemer uitgeschakeld. Er kunnen echter actieve creditcardtransacties zijn die alsnog moeten worden afgeschreven en terugbetaald. Op de pagina **Creditcardtransacties** kunt u de werknemer opnieuw toewijzen voor elke creditcardtransactie waarbij de gekoppelde werknemer is ontslagen.

Selecteer een of meer creditcardtransacties en selecteer vervolgens **Transacties opnieuw toewijzen**. U kunt vervolgens een andere werknemer selecteren aan wie u de creditcardtransacties wilt toewijzen. Nadat de creditcardtransacties opnieuw zijn toegewezen, kunnen ze worden geselecteerd voor een onkostennota en worden betaald via het gebruikelijke proces voor terugbetaling van onkostennota's.

## <a name="delete-credit-card-transactions"></a>Creditcardtransacties verwijderen 

Na het importeren van creditcardtransacties moeten bepaalde transacties mogelijk worden verwijderd. Dit kan zijn omdat de transacties dubbelingen zijn of omdat de gegevens niet nauwkeurig zijn. Beheerders kunnen de functie **Creditcardtransacties verwijderen** gebruiken om creditcardtransacties te selecteren en verwijderen die **niet zijn gekoppeld** aan een onkostennota. 

1. Ga naar **Periodieke taken** > **Creditcardtransacties verwijderen**.
2. Selecteer **Filter** en geef informatie op om de op te nemen records te identificeren.
3. Als u de records wilt verwijderen, selecteert u **OK**. 

## <a name="storing-credit-card-numbers"></a>Creditcardnummers opslaan

Er zijn drie opties beschikbaar voor het opslaan van creditcardnummers. Creditcardnummers worden opgeslagen op de pagina **Parameters onkostenbeheer**.

- **Invoer van kaartnummer voorkomen** – Creditcardnummers worden niet opgeslagen.
- **Hash-kaartnummers (laatste vier cijfers opslaan)** – De laatste vier cijfers van creditcardnummers worden versleuteld opgeslagen.
- **Kaartnummers opslaan** – Creditcardnummers worden niet-versleuteld opgeslagen. Deze optie voldoet niet aan de PCI DSS (beveiligingsstandaard voor gegevens). Om ervoor te zorgen dat de organisatie blijft voldoen aan de PCI DSS-regelgeving, moeten organisatiebeheerders ervoor kiezen ofwel geen creditcardnummers op te slaan of hash-kaartnummers op te slaan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

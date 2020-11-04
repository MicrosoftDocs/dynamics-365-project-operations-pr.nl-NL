---
title: Prestaties van projectresourceplanning
description: Dit onderwerp bevat informatie over hoe de prestaties van resourceplanning bij een groot aantal projecten kunnen worden verbeterd.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074547"
---
# <a name="project-resource-scheduling-performance"></a>Prestaties van projectresourceplanning

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Prestatieproblemen met betrekking tot resourceplanning kunnen optreden wanneer het om duizenden projecten gaat. Om de prestaties van de resourceplanning te verbeteren, is er een functie beschikbaar waarmee gebruikers het resourcebeschikbaarheidsformulier sneller kunnen starten. Met name wordt hiermee het synchronisatieproces van de resourcecapaciteit overgeslagen en wordt de tabel **ResprojectResource** gebruikt om het zoeken naar resources te versnellen. Houd er rekening mee dat de tabel **ResRollup** wordt niet meer gebruikt.

> [!IMPORTANT]
> Als er een afhankelijkheidsrelatie is met het synchronisatieproces van de resourcecapaciteit of de tabel **ResprojectResource** , gebruik deze functie dan niet.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Prestatieverbeteringen van resourceplanning inschakelen
Voer de volgende stappen uit om prestatieverbeteringen voor resourceplanning in te schakelen.

1. Ga naar **Functiebeheer** > **Alles** en zoek in de lijst met functies naar **Functie voor prestatieverbeteringen van projectresources inschakelen**.
2. Selecteer **Nu inschakelen**.

> [!NOTE]
> Als u de functie niet in de lijst kunt vinden, selecteert u **Controleren op updates** om de lijst te vernieuwen.

3. Vernieuw uw browser en ga naar **Projectmanagement en financiële administratie** > **Periodiek** > **Projectresources** > **Capaciteit van resourcekalenders voor alle bedrijven synchroniseren**.
4. Stel **Bestaande capaciteitsrecords verwijderen** in op **Ja** om eerdere gegevens te verwijderen. Als u incrementele gegevens wilt genereren, stelt u dit in op **Nee**.
5. Selecteer in het veld **Periodecode** de periode waarin gegevens moeten worden gegenereerd. Als u een periodecode selecteert, hoeft u geen begin- en einddatum te definiëren.
6. Als u het veld **Periodecode** leeglaat, selecteert u specifieke start- en einddatums om gegevens te genereren.
7. Selecteer **OK**.

 > [!NOTE]
 > Hiermee worden algemene gegevens gegenereerd voor de tabel **ResCalendarCapacity** voor alle bedrijven in uw omgeving, dus de batchtaak hoeft maar in één rechtspersoon te worden uitgevoerd. De gegevens in deze batchtaak zijn nodig om de resourcecapaciteit te berekenen via de bijbehorende kalender.

8. Ga naar **Projectmanagement en financiële administratie** > **Periodiek** > **Projectresources** > **Projectresources invullen voor alle bedrijven** en selecteer vervolgens **OK**. Dit is het gegevensupgradescript voor algemene gegevens in de tabellen **ResProjectResource** , **ResCalendarDateTimeRange** en **ResEffectiveDateTimeRange**. Waarden voor het veld **PSAPRojSchedRole.RootActivity** worden ook bijgewerkt. Als dit niet wordt uitgevoerd, ontvangt u een waarschuwing wanneer u bewerkingen voor resourceplanning probeert uit te voeren.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Prestatieverbeteringen van resourceplanning uitschakelen

1. Ga naar **Functiebeheer** > **Alles** en zoek naar **Functie voor prestatieverbeteringen van projectresources inschakelen**.
2. Selecteer de functie en vervolgens de knop **Uitschakelen**.
3. Vernieuw de browser.
4. Ga naar **Projectmanagement en boekhouding** > **Periodiek** > **Capaciteitssynchronisatie** > **Samenvoegen van resourcecapaciteit synchroniseren**.
5. Stel op de pagina **Synchronisatie van capaciteitsopbouw** de optie **Bestaande capaciteitsrecords verwijderen** in op **Ja** om eerdere gegevens te verwijderen. Als u incrementele gegevens wilt genereren, stelt u dit in op **Nee**.
6. Selecteer in het veld **Periodecode** de periode waarin gegevens moeten worden gegenereerd. Als u een periodecode selecteert, hoeft u geen begin- en einddatum te definiëren.
7. Als u het veld **Periodecode** leeglaat, selecteert u specifieke start- en einddatums om gegevens te genereren.
8. Selecteer **OK**.

> [!NOTE]
> Hiermee worden algemene gegevens gegenereerd voor de tabel **ResRollup** voor alle bedrijven in uw omgeving, dus de batchtaak hoeft maar in één rechtspersoon te worden uitgevoerd. Deze batchtaak is vereist voor alle weergaven voor **Beschikbaarheid van resources**. Als deze batchtaak niet wordt uitgevoerd, worden de gegevens voor **ResRollup** tijdens de uitvoering gegenereerd, wat even kan duren.

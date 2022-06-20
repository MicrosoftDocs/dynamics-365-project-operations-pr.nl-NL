---
title: Projectresources opzetten
description: Dit artikel bevat informatie over het instellen of aanvragen van projectresources.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a4e6fe829d6b39aed9eb6aaea42f245fc997593
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933762"
---
# <a name="set-up-project-resources"></a>Projectresources opzetten

[!include [banner](../includes/banner.md)]

U moet een agenda opstellen en deze aan een medewerker of werknemer koppelen. De agenda wordt gebruikt om het project en de werktijd van de resources die voor het project zijn gereserveerd in te plannen. Tijdens het instellen van de agenda kunnen projectmanagers resourcenivellering uitvoeren als onderdeel van resource-optimalisatie. Op basis van het agendaschema kunnen beperkingen worden opgelegd aan resources. U kunt een agenda opzetten op de pagina **Agenda's**.

Wanneer u een werknemer instelt als projectresource, kunt u kiezen uit werknemers die werken in het bedrijf waarvoor u resources instelt. U kunt ook werknemers van andere bedrijven in uw organisatie selecteren. Deze werknemers worden intercompany-resources genoemd.

In de volgende procedures wordt uitgelegd hoe u een werknemer instelt als projectresource in uw bedrijf en hoe u een intercompany-projectresource instelt.

## <a name="set-up-a-worker-as-a-project-resource"></a>Een werknemer instellen als projectresource

1. Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de werknemer die u toevoegt als een projectresource. Open vervolgens de werknemerrecord.
2. Selecteer in het actievenster de optie **Project** &gt; **Instelling** &gt; **Project instellen**.
3. Selecteer een agenda en sluit vervolgens de pagina.

U kunt ook standaardprojecten voor een resource specificeren als een soort toewijzing vooraf. Toewijzingen vooraf kunnen worden gebruikt wanneer de resourcemanager of projectmanager van tevoren weet aan welke projecten de resource zal werken. Toewijzingen vooraf kunnen ook plaatsvinden op verzoek van een projectsponsor of klant. Als u een project vooraf wilt toewijzen, gaat u naar de pagina **Projecten toewijzen**, tabblad **Projecten** en selecteert u het juiste project in de lijst **Resterende projecten**.

## <a name="set-up-an-intercompany-resource"></a>Een intercompany-resource instellen

Wanneer u een werknemer instelt als intercompany-resource, moet u de instellingen zowel in het uitlenende bedrijf als in het lenende bedrijf uitvoeren.

### <a name="in-the-lending-company"></a>In het uitlenende bedrijf

1. Controleer in Finance of het uitlenende bedrijf is geselecteerd en voltooi vervolgens de procedure in de vorige sectie, "Een werknemer instellen als projectresource".
2. Selecteer **Nieuw** op de pagina **Intercompany-boekhouding**.
3. Selecteer het uitlenende bedrijf in het veld **Id van rechtspersoon**. Vul de resterende velden in en selecteer vervolgens **Opslaan**.
4. Selecteer **Nieuw** op de pagina **Verrekenprijs**.
5. Selecteer het juiste bedrijf in het veld **Lenende rechtspersoon**.
6. Als u aan het lenende bedrijf alleen de resource wilt uitlenen die u aan het begin van deze sectie in het veld **Resource** hebt gemaakt, selecteert u e naam van de resource die u hebt gemaakt. Als u alle resources in het uitlenende bedrijf ter beschikking wilt stellen aan het lenende bedrijf, laat u het veld **Resource** leeg.
7. Stel op de pagina **Parameters voor Projectmanagement en financiële administratie**, op het tabblad **Intercompany**, de optie **Intercompany-resourceplanning en urenstaten inschakelen** in op **Ja**.

### <a name="in-the-borrowing-company"></a>In het lenende bedrijf

- Voer op de pagina **Lijst met resources**, in het zoekfilter de naam in van de resource die u voor het uitlenende bedrijf hebt gemaakt, om te controleren of de naam is opgenomen in de resourcelijst voor het lenende bedrijf.

## <a name="request-project-resources"></a>Aanvragen van projectresources
Met de functionaliteit voor het plannen van projectresources kunnen resourcemanagers alleen bemande resources verdelen over opdrachten of projecten. Als u deze functionaliteit wilt inschakelen, voert u de volgende taken uit of controleert u of deze zijn voltooid:

- Nummerreeksen instellen.
- Werkstromen voor Projectbeheer en financiële administratie instellen.
- Werkstromen voor resourceaanvragen inschakelen.

Nadat de voorgaande taken zijn voltooid, kunt u naar behoefte de volgende taken uitvoeren:

- Een resourceaanvraag op basis van een voorlopig geboekte bemande resource.
- Resourceaanvragen bewaken.
- Resourceaanvragen afhandelen.
- Een bemande resource aanvragen vanuit een WBS.
- Resources voor een project zonder dat u een bemande resource hoeft aan te vragen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
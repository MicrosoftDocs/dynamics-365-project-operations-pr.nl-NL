---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 38, v3
description: Dit artikel biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Microsoft Dynamics 365 Project Service Automation-updateversie 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915179"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 38, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 38, V3. Deze versie heeft buildnummer V3.10.59.117 en is algemeen beschikbaar via een zelfupdate in december 2021.

## <a name="update-release-38"></a>Updateversie 38

### <a name="bug-fixes"></a>Opgeloste fouten

De volgende problemen zijn opgelost.

**Tijd en onkosten**

- Er treedt een uitzondering op wanneer de logboeken van goedkeuringssets meer dan 100.000 records bedragen.
- Gebruikers hebben geen toegang tot het raster **Tijdsvermelding** van de hoofdpagina **Tijdsvermelding**.
- Het dialoogvenster **Tijdsvermeldingsimport** toont geen tekst als er geen items in aanmerking komen voor import.
- Gebruikers kunnen goedkeuringssets maken waarbij het veld **Doelstatus** is ingesteld op **Onbekend**.

**Projectbeheer**

- Contouren worden niet correct weergegeven in resourcetoewijzingen voor UTC (+09:30) en UTC (+10:00) wanneer de zomertijd begint.
- Het veld **Extra kolom** voor werkspecificatiestructuren is bij sommige landinstellingen verborgen.
- De datumkiezer voor het kalenderbesturingselement in het raster **Projecttaak** is niet correct gelokaliseerd voor Chinees.

**Verkoop**

- De waarden van **Contractprestaties** en **Werkelijke projectkosten** komen niet overeen wanneer boekbare resources met verschillende contracteenheden en valuta's tijdsvermeldingen indienen.
- Een aangepaste workflow om facturen automatisch te bevestigen mislukt wanneer de facturen worden geïmporteerd als een beheerde oplossing. Het volgende bericht wordt weergegeven: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException-bericht: ongeldige factuurstatus."
- Wanneer **Hoofdniveau** is geselecteerd als de samenvattingsoptie en het project bevat schattingen van een combinatie van transactieklassen (bijvoorbeeld een combinatie van schattingen voor tijd, onkosten en materiaal), vat het systeem alle transactieklassen samen als één enkele tariefregel.
- In scenario's waarin een onkostenregel wordt toegevoegd voordat een contractregel aan een project is gekoppeld, wordt de juiste prijsstelling niet als standaardwaarde ingevoerd in het veld **Prijs bijwerken**.
- Negatieve verkoopbedragen zijn niet toegestaan op de entiteiten **Project** en **Taak**.

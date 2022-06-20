---
title: Rollen instellen voor sjablonen voor structuur voor werkspecificatie
description: Dit artikel bevat informatie over het instellen van rolgegevens in structuursjablonen voor werkspecificaties.
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
ms.openlocfilehash: 8721c5e5798c2b80c6f3eb65cef118d1ade5e680
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920790"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Rollen instellen voor sjablonen voor structuur voor werkspecificatie

[!include [banner](../includes/banner.md)]

Projectmanagers kunnen WBS-sjablonen (structuur voor werkspecificatie) instellen die zij kunnen toepassen wanneer zij een WBS voor nieuwe projecten maken. Projectmanagers kunnen rollen toevoegen wanneer zij een sjabloon maken. Gebruik de volgende procedure om een rol toe te wijzen aan een WBS-sjabloon.

1. Selecteer **Projectmanagement en financiële administratie** > **Instelling** > **Projecten** > **WBS-sjablonen**.
2. Selecteer **Details** voor een geselecteerde WBS-sjabloon.
3. Selecteer een taak in de lijst en selecteer vervolgens in het veld **Rol** een rol om aan de taak toe te wijzen.

## <a name="work-with-a-wbs"></a>Werken met een WBS

U kunt een nieuwe WBS maken of u kunt een WBS van een bestaande WBS-sjabloon kopiëren. Een projectmanager kan de resources eenvoudig beheren door rollen toe te wijzen aan nieuwe taken in de WBS. Rollen kunnen worden vervangen nadat een resource is verworven of nadat een bevestigde resource is geïdentificeerd om aan de taak te werken. Dankzij deze flexibiliteit kunnen projectmanagers de volgende taken uitvoeren:

- Het aantal resources identificeren dat vereist is voor WBS-werkpakketten.
- Projectkosten ramen.
- Een voorlopig budget vaststellen.
- De duur van activiteiten inschatten op basis van rollen en resources.
- Een aantal projectmanagementplannen ontwikkelen op basis van de beschikbare projectinformatie.

Er zijn extra opties toegevoegd in de WBS om de functionaliteit voor het toewijzen van resources beter te benutten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Optie</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resourcetoewijzingen</td>
<td>Bekijk de toegewezen resources, datums, aantal uren en boekingstype voor taken in de WBS.</td>
</tr>
<tr class="even">
<td>Automatisch team genereren</td>
<td>Voeg automatisch geplande resources toe door rollen te gebruiken die aan een taak zijn gekoppeld. Finance stelt automatisch geplande resources voor door middel van beslissingsanalyse op basis van meerdere criteria die is gebaseerd op rollen. Nadat de rollen en inspanning (uren) zijn ingesteld voor de taken in een WBS, en nadat de structuur is vrijgegeven, selecteert u <strong>Automatisch team genereren</strong>. Het vereiste aantal geplande resources wordt toegevoegd aan de WBS en het tabblad <strong>Project- en teamplanning</strong>.</td>
</tr>
<tr class="odd">
<td>Resource (vervolgkeuzelijst)</td>
<td>Op de pagin a <strong>Resourcetoewijzing starten</strong> kunt u resources selecteren om hard of zacht te boeken, op basis van de opgegeven duur. U kunt de weergave-instellingen aanpassen om de duur van resourceactiviteiten te bekijken en in te stellen. U kunt resources op werkpakketniveau selecteren en toewijzen met behulp van de volgende opties:
<ul>
<li><strong>Accepteren</strong> – Bevestig wijzigingen aan de resource die aan een taak is toegewezen.</li>
<li><strong>Annuleren</strong> – Annuleren wijzigingen aan de resource die aan een taak is toegewezen.</li>
<li><strong>Automatisch toewijzen</strong> – Een beschikbare bemande resource met een bijpassende rol wordt automatisch geselecteerd en toegewezen aan de geselecteerde taak.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Selecteer op de pagina **Alle projecten** het project **XYZ-upgrade fase 2**.
2. Selecteer **Plannen** > **Activiteiten** > **Structuur voor werkspecificatie**.
3. Selecteer **Nieuw** om de volgende activiteiten van niveau één toe te voegen aan de WBS:

    - Initiëren
    - Plannen
    - Uitvoeren
    - Bewaking en controle
    - Sluiten

4. Stel de datums en inspanning (uren) in, zoals weergegeven in de volgende afbeelding.

    [![De datums en inspanning instellen.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selecteer de taakregel **Initiëren** en selecteer vervolgens in het veld **Rol** de optie **Senior projectmanager**.
6. Selecteer **Publiceren**.
7. Selecteer op dezelfde regel, in veld **Resource** de naam **Daniel Goldschmidt** en selecteer vervolgens **Accepteren**.
8. Selecteer de taakregel **Plannen** en selecteer vervolgens in het veld **Rol** de optie **Bedrijfsanalist**.
9. Selecteer **Publiceren** en selecteer vervolgens **Automatisch team genereren**.
10. Selecteer in het berichtenvak dat wordt weergegeven de optie **Ja**.
11. Controleer in het veld **Resource** of de waarde **Bedrijfsanalist 1** is.
12. Open de zoekopdracht voor de resource **Bedrijfsanalist 1** en selecteer vervolgens **Resourcetoewijzingen starten**. Selecteer vervolgens een werknemer voor de taak.
13. Selecteer **Voorlopig toewijzen** &gt; **Volledige capaciteit**.

    > [!NOTE] 
    > U ontvangt geen waarschuwing dat de opgegeven resource nu 2 is, omdat het aantal resources 1 blijft.

14. Valideer op de pagina **Structuur voor werkspecificatie** de resourcetoewijzing in de WBS en selecteer vervolgens **Opslaan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
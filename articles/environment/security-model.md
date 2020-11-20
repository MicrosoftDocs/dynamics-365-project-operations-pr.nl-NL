---
title: Beveiligingsmodel.
description: Dit onderwerp bevat informatie over het beveiligingsmodel in Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 3fc4101d0ea4b8e2a4ba8f1d43540d57239cf402
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124362"
---
# <a name="security-model"></a>Beveiligingsmodel

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Microsoft Dynamics 365 Project Operations bevat een uniek beveiligingsmodel dat een op rollen gebaseerd bedrijfsbeveiligingsmodel mogelijk maakt dat samenwerkt met Microsoft Office Groepen. 


## <a name="security-roles"></a>Beveiligingsrollen
De front-endfuncties van Project Operations omvatten de volgende rollen:

| - Rol                          | Beschrijving                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Praktijkbeheerder              | Ondersteunt projectoverschrijdende rapportage.                                                                                                            | Bedrijfsonderdeel              |
| Projectfiatteur              | Geeft goedkeuring voor tijd en onkosten voor een project.                                                                                                                              | Bedrijfsonderdeel |
| Factureringsbeheerder voor project | Maakt het factuurvoorstel.                                                                                                                                                 | Bedrijfsonderdeel |
| Projectmanager               | Maakt het projectplan en vraagt middelen aan.                                                                                                                              | Bedrijfsonderdeel |
| Projectresource              | Teamleden die kunnen worden geboekt en tijd kunnen melden.                                                                                                          | Bedrijfsonderdeel|
| Resourcebeheerder              | Alle resourcebeheerfuncties, zoals het afhandelen van resourceaanvragen en boekingen, naast een configuratie met hybride projectmanager + resourcemanager en een enkele en gecentraliseerde resourcemanagerrol. | Bedrijfsonderdeel |


Microsoft Project for the Web bevat de volgende rollen:

| - Rol           | Beschrijving                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Projectgebruiker   | Samenwerkende Project-gebruiker die eigen projecten kan maken en projecten kan bekijken die met hen zijn gedeeld. | Gebruiker   |
| Projectsysteem | Rol gebruikt voor toepassingscontext. Klanten mogen deze systeemrol niet gebruiken.                                    | Globaal |

## <a name="security-enforcement"></a>Veiligheidshandhaving
Acties die op projectniveau worden uitgevoerd in de context van de ingelogde gebruiker. Dit betekent dat de gebruiker toegang moet hebben in CDS om een project te maken, te openen of te verwijderen. Toegang tot CDS kan worden verleend via de beschikbare mechanismen die in het platform zijn opgenomen. Een gebruiker met een groter bereik heeft bijvoorbeeld toegang tot het project of als een expliciete actie voor het delen van projecten is uitgevoerd die de gebruiker toegang verleent.

Het is belangrijk om hiermee rekening te houden bij het maken van projecten in Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderne groepssamenwerking met Project Operations
Project for the Web en Project Operations ondersteunen moderne groepen voor samenwerking. Gebruikers die via een groep aan het project zijn toegevoegd, kunnen het projectplan bewerken.

Project for the Web voegt automatisch gebruikers toe aan de groep na toewijzing.

Groepen staan de projectmachtigingen toe en ondersteunen samenwerkingsonderdelen om gezamenlijk aan te werken. Het volgende diagram geeft de gebeurtenissen en statusveranderingen weer die plaatsvinden tijdens het groepstoewijzingsproces.

Project Operations creëert geen groep door middel van impliciete actie en doet dit alleen door de expliciete actie van groepen.

Groepslid zoeken in het dialoogvenster **Groepsbeheer** is beperkt tot degenen die zijn ingesteld als onderdeel van de beveiligingsgroep van de omgeving. Zie voor meer informatie [Gebruikerstoegang tot omgevingen controleren: beveiligingsgroepen en licenties](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Groepsmodus](./media/groupsmode.png)

1. Het project wordt gemaakt door eis n eigendom van de creërende gebruiker.
2. De projecteigenaar wordt bijgewerkt in het team.
3. Het team dat eigenaar is, wordt toegewezen aan de opgegeven of gemaakte Office-groep.
4. De oorspronkelijke eigenaar van het project wordt toegevoegd aan de Office-groep.

## <a name="deployment-recommendation"></a>Aanbevelingen voor gebruik
Naarmate het Office-groepssamenwerkingsmodel evolueert, wordt functionaliteit toegevoegd voor meer gedetailleerde tijdscontrole. Klanten die Project Operations nu implementeren, kunnen het beste een traditioneel Microsoft Dynamics 365-beveiligingsmodel toepassen.

Voor meer informatie raadpleegt u [Beveiliging in Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Beveiliging in Project Operations en Microsoft Dynamics 365 Finance
Project Operations bevat de volgende rollen:

- Projectmanager
- Projectboekhouder

Zie [Rolgebaseerde beveiliging](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security) voor meer informatie over beveiliging in Finance.



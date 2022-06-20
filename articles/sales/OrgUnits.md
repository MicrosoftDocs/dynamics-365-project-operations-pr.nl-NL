---
title: Organisatie-eenheden
description: In dit artikel wordt het concept van organisatie-eenheden beschreven en uitgelegd hoe organisatie-eenheden in Microsoft Dynamics 365 Project Operations kunnen worden gemaakt en onderhouden.
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921618"
---
# <a name="organizational-units-overview"></a>Overzicht van organisatie-eenheden

In Microsoft Dynamics 365 Project Operations is een *organisatie-eenheid* een afzonderlijke groep of divisie bij een professionele dienstverlener die factureerbare resources met kostentarieven in dienst heeft.

Voor professionele dienstverleners die technische resources gebruiken voor verschillende operationele gebieden of bedrijfslijnen, kunnen de kosten voor het vervullen van een rol variëren, afhankelijk van het operationeel gebied of de bedrijfslijn waar de rol wordt vervuld. In dit scenario biedt het concept van organisatie-eenheden hulp door een manier te verstrekken om een verzameling factureerbare rollen te groeperen in een divisie van een bedrijf dat een afzonderlijke kostenstructuur heeft voor die rollen.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Het concept van organisatie-eenheden in Project Operations

In Project Operations heeft een organisatie-eenheid een specifieke valuta en specifieke kostprijslijsten.

De valuta van een organisatie-eenheid is de primaire valuta die wordt gebruikt om kosten bij te houden.

Aan elke organisatie-eenheid kunnen een of meer kostprijslijsten worden gekoppeld. Project Operations stelt de volgende beperkingen aan de prijslijsten die aan een organisatie-eenheid kunnen worden gekoppeld:

- De prijslijsten moeten dezelfde valuta als de organisatie-eenheid hebben.
- De prijslijsten moeten kostprijslijsten zijn.

Bovendien bevat de entiteit Resource een kenmerk voor de organisatie-eenheid. Elke resource kan aan één organisatie-eenheid worden toegewezen.

### <a name="roles-of-organizational-units"></a>Rollen van organisatie-eenheden

De organisatie-eenheid speelt twee rollen in Project Operations:

- **Contracterende eenheid**: de organisatie-eenheid die de bedrijfsgroep of divisie vertegenwoordigt die primair verantwoordelijk is voor het sluiten van de verkoop en het beheren van de levering van arbeid en diensten aan de klant. De contracterende eenheid wordt geïdentificeerd door het veld **Contracterende eenheid** in het koptekstgedeelte van de pagina's **Verkoopkans**, **Prijsopgave**, **Projectcontract** en **Project**.
- **Resource-eenheid**: de organisatie-eenheid waar een resource hoort of waaraan deze is toegewezen. Deze organisatie-eenheid kan de resources voor bepaalde rollen leveren in werkomschrijvingen en projecten die eigendom zijn van de contracterende eenheid.

![Contracterende en resource-eenheden.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Veelgestelde vragen over organisatie-eenheden

Hier vindt u antwoorden op een aantal van de meest gestelde vragen over organisatie-eenheden.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hoe verhoudt de entiteit Organisatie-eenheid in Project Operations zich tot de organisatie-entiteit die al bestaat in Dynamics 365?

De entiteit Organisatie in Dynamics 365 vertegenwoordigt de naam van een algemeen Dynamics 365-exemplaar. Deze naam is meestal de naam van de globale onderneming.

De entiteit Organisatie-eenheid vertegenwoordigt een groep of divisie in de globale onderneming. Deze groep of divisie heeft een verzameling rollen en een kostprijslijst voor deze rollen. Deze rollen en prijslijst verschillen van de rollen en prijslijst van andere groepen of divisies in de onderneming.

Wanneer Project Operations is geïnstalleerd, wordt een standaardorganisatie-eenheid gemaakt op basis van de organisatie. Alle bestaande resources worden toegewezen aan de standaardorganisatie-eenheid. Als nieuwe Active Directory-gebruikers of -resources worden geïmporteerd in Dynamics 365, worden deze tijdens het importproces toegewezen aan de standaardorganisatie-eenheid in Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Hoe verschilt de entiteit Organisatie-eenheid van de entiteit Business unit?

In Dynamics 365 is de eenheid Business Unit een beveiligingsconstructie. De koppeling van een gebruiker aan een Business Unit bepaalt de entiteiten en entiteitsrecords waartoe de gebruiker toegang heeft. Het bepaalt ook de machtigingen (maken, lezen, schrijven, verwijderen, toevoegen, toevoegen aan, toewijzen of delen) van de gebruiker voor deze entiteitsrecords.

De entiteit Organisatie-eenheid vertegenwoordigt een bedrijfsgroep of divisie met specifieke kostentarieven voor werknemers die hieraan zijn toegewezen. De projectkosten van een resource zijn afhankelijk van de organisatie-eenheid waaraan de resource is gekoppeld.

Wanneer u Dynamics 365 implementeert, optimaliseert u de beveiligingsautorisatie voor de hiërarchie van Business Units en de toewijzing van gebruikers aan Business Units. Wijs alle gebruikers toe die doorgaans toegang moeten hebben tot dezelfde set records voor dezelfde Business Unit. De organisatie-eenheid heeft geen invloed op de beveiligingsmachtiging of toegang.

**Voorbeeld dat één potentieel verschil laat zien in de modellering van organisatie-eenheden en business units**

Contoso, Ltd. heeft een bloeiende onderneming in Microsoft-technologieën. Stijn en Esmee zijn allebei C\#-ontwikkelaars, maar Esmee woont in de Verenigde Staten en Stijn in India. Voor de meeste projectopdrachten zijn resources van zowel Contoso India als Contoso US vereist. Stijn en Esmee hebben hetzelfde beveiligingsniveau voor toegang tot projecten in dit praktijkgebied nodig. De kosten van ontwikkelaars van Contoso India wijken echter aanzienlijk af van de kosten van ontwikkelaars van Contoso US.

Hier volgt een optimale manier om te ontwerpen voor dit scenario met Dynamics 365 en Project Operations.

1. Maak de Microsoft-technologiepraktijk als een Business Unit en koppel Stijn en Esmee hieraan. Op deze manier zorgt u ervoor dat beide werknemers het beveiligingsniveau hebben voor toegang tot de projecten in dat praktijkgebied. Ze kunnen beide de voortgang controleren en tijd, onkosten, materiaalgebruik en taakupdates rapporteren.
2. Maak twee organisatie-eenheden om ervoor te helpen zorgen dat de kosten voor het project correct worden weerspiegeld.
3. Koppel Esmee aan Contoso US en Stijn aan Contoso India.
4. Wijs de juiste kostprijslijsten toe aan beide organisatie-eenheden. Op deze manier zorgt u ervoor dat in de kosten die zijn vastgelegd in het project voor Stijn en Esmee nauwkeurig het verschil in kosten tussen Contoso US en Contoso India tot uitdrukking komt.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Zijn organisatie-eenheden gerelateerd aan verkooprayons in Dynamics 365?

Er is geen koppeling of relatie tussen verkooprayons en organisatie-eenheden. Een verkooprayon is meestal een geografisch gebied waar de verkoop plaatsvindt. Er kan een verkoopprijslijst aan elk verkooprayon worden gekoppeld.

Een organisatie-eenheid is een interne groep of divisie in het bedrijf die kosten bijhoudt voor een set rollen die wordt verkocht aan andere divisies of aan externe klanten.

**Voorbeeld dat één potentieel verschil laat zien in de modellering van organisatie-eenheden en verkooprayons**

Contoso, Ltd. heeft twee ontwikkelingscentra: Contoso US en Contoso India. De kosten van resources verschillen sterk tussen deze twee ontwikkelingscentra. Contoso verkoopt zijn IT-services (informatietechnologie) in veel internationale markten, zoals Latijns-Amerika, Noord-Amerika, Azië en Stille Oceaan, West-Europa en het Midden-Oosten. Factuurtarieven voor dezelfde projectrollen kunnen sterk variëren in deze markten. Contoso US en Contoso India moeten worden ingesteld als organisatie-eenheden en elke organisatie-eenheid moet een eigen kostprijslijst hebben. Azië en Stille Oceaan, Latijns-Amerika, Noord-Amerika, West-Europa en het Midden-Oosten moeten worden ingesteld als verkooprayons en elk verkooprayon moet een eigen verkoopprijslijst hebben.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Waarom geldt er een beperking ten aanzien van de koppeling van prijslijsten met organisatie-eenheden?

De verkoopprijs is meestal uniek voor de geografische gebieden of markten waar diensten worden verkocht. Interne divisies van een bedrijf hebben doorgaans niet hun eigen verkoopprijzen voor hetzelfde type diensten. Interne divisies hanteren echter verschillende kosten van verkochte goederen, afhankelijk van de vaardigheden van de mensen die zij in dienst hebben en de arbeidsomstandigheden van de regio waar ze actief zijn. Omdat organisatie-eenheden zijn gemodelleerd als interne divisies van een bedrijf, kunnen ze alleen kostprijslijsten hebben.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Waarom kunnen we verkoopprijslijsten niet aan organisatie-eenheden koppelen?

In Project Operations kunnen verkoopprijslijsten aan klanten en verkooprayons worden gekoppeld. Transactie-entiteiten, zoals Verkoopkans, Prijsopgave, Projectcontract en Project, gebruiken verkoopprijslijsten die zijn gekoppeld aan de klantaccount of het verkooprayon om factuurtarieven en potentiële omzet voor de projectopdracht te bepalen.

Kostprijslijsten worden gekoppeld aan organisatie-eenheden. Transactie-entiteiten zoals Verkoopkans, Prijsopgave, Projectcontract en Project gebruiken kostprijslijsten die zijn gekoppeld aan de contracterende eenheid om kosten van een projectcontract te berekenen.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Zijn organisatie-eenheden hiërarchisch in Project Operations?

Nee In de huidige versie van Project Operations zijn organisatie-eenheden niet hiërarchisch. Daarom kunt u de volgende taken niet uitvoeren:

- Een patroon configureren voor het invoeren van standaardkostprijzen die in een hiërarchie in oplopende volgorde worden toegepast.
- Getotaliseerde omzet of kosten van verschillende niveaus van de hiërarchie van de organisatie-eenheid rapporteren.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>We zijn een grote multinationale onderneming met een complexe, uit meerdere niveaus bestaande hiërarchie van kostencentra, divisies en factureringskantoren. Hoe kunnen we het concept van organisatie-eenheden het beste gebruiken in de huidige versie van Project Operations?

Wanneer u een complexe hiërarchie met kostencentra, divisies, factureringskantoren enzovoort hebt, stelt u de bladbladknooppunten van die hiërarchie in als afzonderlijke organisatie-eenheden.

In het volgende voorbeeld ziet u een typische hiërarchie.

**Contoso India**

- SAP

    - Technische consultants
    - Functionele consultants

- Microsoft-technologie

    - Technische consultants
    - Functionele consultants

**Contoso US**

- SAP

    - Technische consultants
    - Functionele consultants

- Microsoft-technologie

    - Technische consultants
    - Functionele consultants

Als uw hiërarchie op dit voorbeeld lijkt, moet u deze instellen als een platte lijst, zoals hier wordt weergegeven:

- Contoso India - SAP - Technische consultants
- Contoso India - SAP - Functionele consultants
- Contoso India - Microsoft-technologie - Functionele consultants
- Contoso India - Microsoft-technologie - Functionele consultants
- Contoso US - SAP - Technische consultants
- Contoso US - SAP - Functionele consultants
- Contoso US - Microsoft-technologie - Technische consultants
- Contoso US - Microsoft-technologie - Functionele consultants

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>We zijn een kleine professionele dienstverlener die als één divisie werkt. Hoe kunnen we het concept van organisatie-eenheden het beste gebruiken in de huidige versie van Project Operations?

Als uw bedrijf fungeert als één eenheid met één kostprijslijst, hoeft u geen organisatie-eenheden in te stellen. Tijdens de installatie van Project Operations maakt Dynamics 365 één standaardorganisatie-eenheid die dezelfde naam heeft als de organisatie. Standaard worden alle gebruikers toegewezen aan deze organisatie-eenheid. Wanneer het systeem vereist dat een organisatie-eenheid wordt geselecteerd, wordt standaard deze organisatie-eenheid geselecteerd.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Wanneer een project wordt gemaakt op basis van een prijsopgave of projectcontractregel, komt de standaard contracterende eenheid uit de prijsopgave of het projectcontract. Wat is de standaard contracterende eenheid als er een project wordt gemaakt vóór verkoopentiteiten, zoals Prijsopgave of Projectcontract?

Wanneer een zelfstandig project wordt gemaakt, wordt de standaard contracterende eenheid van het project gebaseerd op de gebruiker die het project maakt. Die gebruiker is ook de standaardprojectmanager. Als het project wordt toegewezen aan een verkoopentiteit, zoals een prijsopgave of projectcontract, wordt de contracterende eenheid van het project in plaats daarvan gebaseerd op de verkoopentiteit. In dit geval kunnen projectschattingen opnieuw worden berekend omdat de kostprijslijst wordt gebruikt om de wijzigingen in de kostenschatting te berekenen als de contracterende eenheid wordt gewijzigd. De verkoopprijslijst wordt gebruikt om de verkoopschattingen te berekenen die worden gewijzigd, zodat deze zijn gesynchroniseerd met de projectprijslijst van de prijsopgave.

De velden **Contracterende eenheid** en **Valuta** van het project zijn vergrendeld voor bewerking, omdat ze moeten zijn gesynchroniseerd met de waarden van de verkoopentiteit (prijsopgave of projectcontract) waaraan het project is toegewezen.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Organisatie-eenheden maken en onderhouden in Project Operations

Volg deze stappen om een organisatie-eenheid te maken in Project Operations.

1. Ga naar **Instellingen \> Organisatie-eenheden**.
2. Selecteer **Nieuw**.
3. Typ in het gebied **Algemeen** een naam voor de organisatie-eenheid in het veld **Naam**. Stel vervolgens naar behoefte de andere velden in.
4. Selecteer **Opslaan** om de record te maken, zodat u deze verder kunt bewerken.
5. Selecteer onder **Kostprijslijsten** het plusteken (**+**) om een prijslijst toe te voegen. U kunt hier alleen prijslijsten toevoegen die de context **Kosten** hebben.
6. Selecteer in het veld **Naam** de knop **Zoeken** en selecteer de prijslijst die u in de organisatie-eenheid beschikbaar wilt maken. Ga verder naar behoefte verder met het toevoegen van prijslijsten.
7. Als u gereed bent met het toevoegen van prijslijsten, selecteert u **Opslaan** in de rechterbenedenhoek van de pagina.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Organisatie-eenheden
description: Dit onderwerp bevat informatie over organisatie-eenheden in Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 89ff652e186601ccdf75d99dc08a4f082e576cb0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291658"
---
# <a name="organizational-units"></a>Organisatie-eenheden 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Dynamics 365 Project Service Automation is een organisatie-eenheid een afzonderlijke groep of divisie in een professionele dienstverlener die factureerbare resources met kostentarieven in dienst heeft.

Voor professionele dienstverleners die technische resources gebruiken voor verschillende operationele gebieden of bedrijfslijnen, kunnen de kosten voor het vervullen van een rol per operationeel gebied of bedrijfslijn verschillen. Het concept van organisatie-eenheden helpt in dit scenario door een manier te bieden om een verzameling factureerbare rollen te groeperen in een divisie van een bedrijf dat een afzonderlijke kostenstructuur heeft voor deze rollen.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Belangrijke kenmerken en koppelingen van organisatie-eenheden

In PSA heeft een organisatie-eenheid een specifieke valuta en specifieke kostprijslijsten.

De valuta van een organisatie-eenheid is de primaire valuta die wordt gebruikt om kosten bij te houden.

Aan elke organisatie-eenheid kunnen een of meer kostprijslijsten worden gekoppeld. PSA stelt de volgende beperkingen aan de prijslijsten die aan een organisatie-eenheid kunnen worden gekoppeld:

- Prijslijsten moeten dezelfde valuta als de organisatie-eenheid hebben
- Prijslijsten moeten kostprijslijsten zijn

Bovendien bestaat er een kenmerk voor de organisatie-eenheid in de entiteit Resource. Elke resource kan aan één organisatie-eenheid worden toegewezen.

## <a name="roles-of-organizational-units"></a>Rollen van organisatie-eenheden

De organisatie-eenheid speelt twee rollen in PSA:

- **Contracterende eenheid**: de organisatie-eenheid die de bedrijfsgroep of divisie vertegenwoordigt die primair verantwoordelijk is voor het sluiten van de verkoop en het beheren van de levering van arbeid en diensten aan de klant. De contracterende eenheid wordt geïdentificeerd door het veld **Contracterende eenheid** in het koptekstgedeelte van de pagina's **Verkoopkans**, **Prijsopgave**, **Projectcontract** en **Project**.
- **Resource-eenheid**: de organisatie-eenheid waar een resource hoort of waaraan deze is toegewezen. Deze organisatie-eenheid kan de resources voor bepaalde rollen leveren in werkomschrijvingen en projecten die eigendom zijn van de contracterende eenheid.

> ![Contracterende en resource-eenheden](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Veelgestelde vragen over organisatie-eenheden

Hier vindt u antwoorden op een aantal van de meest gestelde vragen over organisatie-eenheden.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hoe verhoudt de entiteit Organisatie-eenheid in PSA zich tot de organisatie-entiteit die al bestaat in Dynamics 365?

De entiteit Organisatie in Microsoft Dynamics 365 vertegenwoordigt de naam van een globaal Dynamics 365-exemplaar. Deze naam is meestal de naam van de globale onderneming.

De entiteit Organisatie-eenheid vertegenwoordigt een groep of divisie in de globale onderneming. Deze groep of divisie heeft een verzameling rollen en een kostprijslijst voor deze rollen. Deze rollen en prijslijst verschillen van de rollen en prijslijst van andere groepen of divisies in de onderneming.

Wanneer PSA is geïnstalleerd, wordt een standaardorganisatie-eenheid gemaakt op basis van de organisatie. Alle bestaande resources worden toegewezen aan de standaardorganisatie-eenheid. Als nieuwe Active Directory-gebruikers of -resources worden geïmporteerd in Dynamics 365, worden deze tijdens het importproces toegewezen aan de standaardorganisatie-eenheid in PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Hoe verschilt de entiteit Organisatie-eenheid van de entiteit Business Unit?

In Dynamics 365 is de eenheid Business Unit een beveiligingsconstructie. De koppeling van een gebruiker aan een Business Unit bepaalt de entiteiten en entiteitsrecords waartoe de gebruiker toegang heeft. Het bepaalt ook de machtigingen (maken, lezen, schrijven, verwijderen, toevoegen, toevoegen aan, toewijzen of delen) van de gebruiker voor deze entiteitsrecords.

De entiteit Organisatie-eenheid vertegenwoordigt een bedrijfsgroep of divisie met specifieke kostentarieven voor werknemers die hieraan zijn toegewezen. De projectkosten van een resource zijn afhankelijk van de organisatie-eenheid waaraan de resource is gekoppeld.

Wanneer u Dynamics 365 implementeert, optimaliseert u de beveiligingsautorisatie voor de hiërarchie van Business Units en de toewijzing van gebruikers aan Business Units. Wijs alle gebruikers toe die doorgaans toegang moeten hebben tot dezelfde set records voor dezelfde Business Unit. De organisatie-eenheid heeft geen invloed op de beveiligingsmachtiging of toegang.

#### <a name="example-of-organizational-units-and-business-units"></a>Voorbeeld van organisatie-eenheden en Business Units

Contoso, Ltd. heeft een bloeiende onderneming in Microsoft-technologieën. Stijn en Esmee zijn allebei C\#-ontwikkelaars, maar Esmee woont in de Verenigde Staten en Stijn in India. Voor de meeste projectopdrachten zijn resources van Contoso India en Contoso US vereist. Stijn en Esmee hebben hetzelfde beveiligingsniveau voor toegang tot projecten in dit praktijkgebied nodig. De kosten van ontwikkelaars van Contoso India wijken echter aanzienlijk af van de kosten van ontwikkelaars van Contoso US.

Hier volgt een optimale manier om te ontwerpen voor dit scenario met Dynamics 365 en PSA.

1. Maak de Microsoft-technologiepraktijk als een Business Unit en koppel Stijn en Esmee hieraan. Op deze manier zorgt u ervoor dat beide werknemers het beveiligingsniveau hebben voor toegang tot de projecten in dat praktijkgebied. Ze kunnen beide de voortgang controleren en tijd, onkosten en taakupdates rapporteren. 
2. Maak twee organisatie-eenheden om ervoor te zorgen dat de kosten voor het project correct worden weerspiegeld. 
3. Koppel Esmee aan Contoso US en Stijn aan Contoso India.
4. Wijs de juiste kostprijslijsten toe aan beide organisatie-eenheden. Op deze manier zorgt u ervoor dat in de kosten die zijn vastgelegd in het project voor Stijn en Esmee nauwkeurig het verschil in kosten tussen Contoso US en Contoso India tot uitdrukking komt.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Zijn organisatie-eenheden gerelateerd aan verkooprayons in Dynamics 365?

Er is geen koppeling of relatie tussen verkooprayons en organisatie-eenheden. Een verkooprayon is meestal een geografisch gebied waar de verkoop plaatsvindt. Er kan een verkoopprijslijst aan elk verkooprayon worden gekoppeld.

Een organisatie-eenheid is een interne groep of divisie in het bedrijf die kosten bijhoudt voor een set rollen die wordt verkocht aan andere divisies of aan externe klanten.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Voorbeeld van organisatie-eenheden en verkooprayons

Contoso, Ltd. heeft twee ontwikkelingscentra: Contoso US en Contoso India. De kosten van resources verschillen sterk tussen deze twee ontwikkelingscentra.

Contoso verkoopt zijn IT-Services in veel internationale markten, zoals Latijns-Amerika, Noord-Amerika, Azië en Stille Oceaan, West-Europa en het Midden-Oosten. Factuurtarieven voor dezelfde projectrollen kunnen sterk variëren in deze markten.

Contoso US en Contoso India moeten worden ingesteld als organisatie-eenheden en elke organisatie-eenheid moet een eigen kostprijslijst hebben. Azië en Stille Oceaan, Latijns-Amerika, Noord-Amerika, West-Europa en het Midden-Oosten moeten worden ingesteld als verkooprayons en elk verkooprayon moet een eigen verkoopprijslijst hebben.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Waarom geldt er een beperking ten aanzien van de koppeling van prijslijsten met organisatie-eenheden? 

De verkoopprijs is meestal uniek voor de geografische gebieden of markten waar diensten worden verkocht. Interne divisies van een bedrijf hebben doorgaans niet hun eigen verkoopprijzen voor hetzelfde type diensten. Interne divisies hanteren echter verschillende kosten van verkochte goederen, afhankelijk van de vaardigheden van de mensen die zij in dienst hebben en de arbeidsomstandigheden van de regio waar ze actief zijn. Omdat organisatie-eenheden zijn gemodelleerd als interne divisies van een bedrijf, kunnen ze alleen kostprijslijsten hebben.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Waarom kunnen we verkoopprijslijsten niet aan organisatie-eenheden koppelen?

In PSA kunnen verkoopprijslijsten worden gekoppeld aan klanten en verkooprayons. Transactie-entiteiten, zoals Verkoopkans, Prijsopgave, Projectcontract en Project, gebruiken verkoopprijslijsten die zijn gekoppeld aan de klantaccount of het verkooprayon om factuurtarieven en potentiële omzet voor de projectopdracht te bepalen.

Kostprijslijsten worden gekoppeld aan organisatie-eenheden. Transactie-entiteiten zoals Verkoopkans, Prijsopgave, Projectcontract en Project gebruiken kostprijslijsten die zijn gekoppeld aan de contracterende eenheid om kosten van een projectcontract te berekenen.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Zijn organisatie-eenheden hiërarchisch in PSA?

Nr. In de huidige versie van PSA zijn organisatie-eenheden niet hiërarchisch. Dit betekent dat u het volgende niet kunt doen:

- Een patroon configureren voor standaardinstellingen voor kostprijzen die in een hiërarchie in oplopende volgorde worden toegepast. 
- Getotaliseerde omzet of kosten van verschillende niveaus van de hiërarchie van de organisatie-eenheid rapporteren.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>We zijn een grote multinationale onderneming met een complexe, uit meerdere niveaus bestaande hiërarchie van kostencentra, divisies en factureringskantoren. Hoe kunnen we optimaal gebruikmaken van het concept van de organisatie-eenheid in deze versie van de Project Service-app?

Wanneer u een complexe hiërarchie met kostencentra, divisies, factureringskantoren en dergelijke enzovoort hebt, stelt u de bladbladknooppunten van die hiërarchie in als afzonderlijke organisatie-eenheden.
In het volgende voorbeeld ziet u een typische hiërarchie:

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
 
Als uw hiërarchie vergelijkbaar is, moet u deze instellen als een platte lijst, zoals hier wordt weergegeven:
- Contoso India - SAP - Technische consultants 
- Contoso India - SAP - Functionele consultants       
- Contoso India - Microsoft-technologie - Functionele consultants 
- Contoso India - Microsoft-technologie - Functionele consultants 
- Contoso US - SAP - Technische consultants  
- Contoso US - SAP - Functionele consultants  
- Contoso US - Microsoft-technologie - Technische consultants 
- Contoso US - Microsoft-technologie - Functionele consultants

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>We zijn een kleine professionele dienstverlener die als één divisie werkt. Hoe kunnen we het concept van de organisatie-eenheid het beste gebruiken in de huidige versie van PSA?

Als uw bedrijf fungeert als één eenheid met één kostprijslijst, hoeft u geen organisatie-eenheden in te stellen. Tijdens de PSA-installatie maakt Dynamics 365 één standaardorganisatie-eenheid die dezelfde naam heeft als de organisatie. Standaard worden alle gebruikers toegewezen aan deze organisatie-eenheid. Wanneer het systeem vereist dat een organisatie-eenheid wordt geselecteerd, wordt standaard deze organisatie-eenheid geselecteerd.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Wanneer een project wordt gemaakt op basis van een prijsopgave of projectcontractregel, komt de standaard contracterende eenheid uit de prijsopgave of het projectcontract. Wat is de standaard contracterende eenheid als er een project wordt gemaakt vóór verkoopentiteiten, zoals een prijsopgave of projectcontract?

Wanneer een zelfstandig project wordt gemaakt, wordt de standaard contracterende eenheid van het project gebaseerd op de gebruiker die het project maakt. Die gebruiker is ook de standaardprojectmanager. Als het project wordt toegewezen aan een verkoopentiteit, zoals een prijsopgave of projectcontract, wordt de contracterende eenheid voor het project in plaats daarvan gebaseerd op de verkoopentiteit. In dit geval kunnen projectschattingen opnieuw worden berekend omdat de kostprijslijst wordt gebruikt om de wijzigingen in de kostenschatting te berekenen als de contracterende eenheid wordt gewijzigd. De verkoopprijslijst wordt gebruikt om de verkoopschattingen te berekenen die worden gewijzigd, zodat deze zijn gesynchroniseerd met de projectprijslijst van de prijsopgave.

De velden **Contracterende eenheid** en **Valuta** voor het project zijn vergrendeld voor bewerking, omdat ze moeten zijn gesynchroniseerd met de waarden in de verkoopentiteit (prijsopgave of projectcontract) waaraan het project is toegewezen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
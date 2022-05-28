---
title: Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten
description: Dit onderwerp bevat informatie over het toevoegen van aangepaste velden aan prijsinstellingen en transactie-entiteiten.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cb4a99b10e5d0c79e80bcd46d2f60ccdab4487aa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596918"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten 

[!include [banner](../includes/psa-now-project-operations.md)]

In dit onderwerp wordt ervan uitgegaan dat u de procedures in het onderwerp [Aangepaste velden en entiteiten maken](create-custom-fields-entities.md) hebt voltooid. Als u deze procedures niet hebt voltooid, gaat u terug, voltooit u deze en keert u terug naar Dit onderwerp. 

In dit onderwerp wordt beschreven hoe u de vereiste aangepaste veldverwijzingen toevoegt aan entiteiten en aan de elementen van de gebruikersinterface (UI), zoals formulieren en weergaven.

## <a name="add-custom-pricing-dimension-fields"></a>Velden voor aangepaste prijsdimensies toevoegen 
Nadat er aangepaste velden en entiteiten zijn gemaakt, moet u in de volgende stap de prijsinstellingen en transactie-entiteiten 'laten weten' dat er aangepaste entiteiten of optiesets zijn door verwijzingsvelden te maken. Afhankelijk van het antwoord op de vraag of de lijst met prijsdimensies optiesetdimensies of entiteitsdimensies of beide bevat, volgt u alleen de stappen bij **Aangepaste prijsdimensies op basis van optieset** of **Aangepaste prijsdimensies op basis van entiteit** of de stappen bij beide.

### <a name="option-set-based-custom-pricing-dimensions"></a>Aangepaste prijsdimensies op basis van optieset
Wanneer een aangepaste prijsdimensie is gebaseerd op een optieset, voegt u deze aan belangrijke Project Service-entiteiten toe. In de volgende procedure worden **Werklocatie van resource** en **Werkuren van resource** gebruikt als de op een optieset gebaseerde prijsdimensies. Deze moeten eerst als velden worden toegevoegd aan de prijsentiteiten **Rolprijs** en **Opslag voor rolprijs**.

1. Klik in PSA (Project Service Automation) op **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**. 
2. Selecteer in Solution Explorer in het linkernavigatiedeelvenster **Entiteiten > Rolprijs**.
3. Vouw de entiteit **Rolprijs** uit en selecteer **Velden**.
4. Klik op **Nieuw** om een nieuw veld te maken met de naam **Werklocatie van resource** en selecteer **Optieset** als het veldtype. 
5. Selecteer **Een bestaande optieset gebruiken**, selecteer de optieset **Werklocatie van resource** en klik vervolgens op **Opslaan**.
6. Herhaal de stappen 1-5 om dit veld toe te voegen aan de entiteit **Opslag voor rolprijs**. 
7. Herhaal de stappen 1-5 voor de optieset **Werkuren van resource**.

> [!IMPORTANT]
> Wanneer u een veld aan meer dan één entiteit toevoegt, gebruikt u dezelfde veldnaam voor alle entiteiten. 

> ![Werklocatie van resource toevoegen aan Rolprijs.](media/RWL-Field.png)

In de verkoop- en schattingsfasen voor een project worden schattingen van de werkinspanning die is vereist om werk **Lokaal** en **Op locatie** te voltooien, in **Reguliere uren** en **Overuren** gebruikt om de waarde van de prijsopgave of het project te schatten. De velden **Werklocatie van resource** en **Werkuren van resource** worden toegevoegd aan de schattingsentiteiten **Details van prijsopgaveregel**, **Details van contractregel**, **Projecttaak**, **Projectteamlid** en **Schattingsregel**.

1. Selecteer in PSA de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**. 
2. Selecteer in Solution Explorer in het linkernavigatiedeelvenster **Entiteiten > Details van prijsopgaveregel**.
3. Vouw de entiteit **Details van prijsopgaveregel** uit en selecteer **Velden**.
4. Klik op **Nieuw** om een nieuw veld te maken met de naam **Werklocatie van resource** en selecteer **Optieset** als het veldtype. 
5. Selecteer **Een bestaande optieset gebruiken** en **Werklocatie van resource** en klik vervolgens op **Opslaan**.
6. Herhaal stap 1-5 om dit veld toe te voegen aan de entiteiten **Details van projectcontractregels**, **Projecttaak**, **Projectteamlid** en **Schattingsregel**.
7. Herhaal de stappen 1-6 voor de optieset **Werkuren van resource**. 

> ![Werklocatie van resource toevoegen aan Schattingsregel.](media/RWL-Default-Value.png)


Voor de levering en facturering moet voltooid werk nauwkeurig worden geprijsd en daarom moeten gebruikers kunnen selecteren of het werk **Lokaal** of **Op locatie** is uitgevoerd en of het is voltooid tijdens **Reguliere uren** of **Overuren** om de werkelijke waarden van het project te verkrijgen. De velden **Werklocatie van resource** en **Werkuren van resource** moeten worden toegevoegd aan de entiteiten **Tijdsvermelding**, **Werkelijk**, **Factuurregeldetail** en **Journaalregel**.

1. Selecteer in PSA de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.
2. Selecteer in Solution Explorer in het linkernavigatiedeelvenster **Entiteiten > Tijdsvermelding**.
3. Vouw **Details van prijsopgaveregel** uit en selecteer **Velden**.
4. Klik op **Nieuw** om een nieuw veld te maken met de naam **Werklocatie van resource** en selecteer **Optieset** als het veldtype. 
5. Selecteer **Een bestaande optieset gebruiken**, selecteer de optieset **Werklocatie van resource** en klik vervolgens op **Opslaan**.
6. Herhaal de stappen 1-5 om dit veld toe te voegen aan de entiteiten **Werkelijk**, **Factuurregeldetail** en **Journaalregel**.
7. Herhaal de stappen 1-6 voor de optieset **Werkuren van resource**. 

> ![Werklocatie van resource toevoegen aan Tijdsvermelding.](media/RWL-time-entry.png)

Hiermee zijn de schemawijzigingen voltooid die zijn vereist voor aangepaste dimensies op basis van een optieset.

## <a name="entity-based-custom-pricing-dimensions"></a>Aangepaste prijsdimensies op basis van entiteit

Wanneer de aangepaste prijsdimensie een entiteit is, voegt u 1:N-relaties toe tussen de dimensie-entiteit en de belangrijkste Project Service-entiteiten. Als het bovenstaande Standaardtitel-voorbeeld wordt gebruikt, is het redelijk om te verwachten dat aan elke werknemer een standaardtitel is toegewezen. Daarom hebt u een 1:N-relatie van de standaardtitel naar de boekbare resource nodig of een N:1-relatie als deze is gemaakt op basis van boekbare resource naar standaardtitel.

1. Selecteer in PSA de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**. 
2. Selecteer in Solution Explorer in het linkernavigatiedeelvenster **Entiteiten > Standaardtitel**.
3. Vouw de entiteit **Standaardtitel** uit en selecteer **1:N-relaties**.
4. Klik **op** nieuw om een nieuwe 1: N-relatie **te maken met de naam** Standaardtitel naar boekbare resource. Geef de vereiste informatie op en klik vervolgens op **Opslaan**.

> ![Standaardtitel toevoegen als een verwijzingsveld aan Boekbare resource.](media/ST-BR.png)

De standaardtitel moet ook worden toegevoegd aan de Project Service-prijsentiteiten **Rolprijs** en **Opslag voor rolprijs**. Dit wordt ook uitgevoerd met 1:N-relaties tussen de entiteiten **Standaardtitel** en **Rolprijs** en **Standaardtitel** en **Opslag voor rolprijs**.

1. Selecteer in Solution Explorer in het linkernavigatiedeelvenster **Entiteiten > Standaardtitel**.
2. Vouw de entiteit **Standaardtitel** uit en selecteer **1:N-relaties**.
3. Klik op **Nieuw** om een nieuwe 1:N-relatie te maken met de naam **Standaardtitel naar rolprijs**. Geef de vereiste informatie op en klik vervolgens op **Opslaan**.
4. Herhaal de stappen 1-4 om 1:N-relaties te maken tussen de entiteiten **Standaardtitel** en **Opslag voor rolprijs**.

In de verkoop- en schattingsfasen voor het project zijn schattingen van de werkinspanning vereist voor elke standaardtitel om de prijs van de prijsopgave of het project te bepalen. Dit betekent dat er 1:N-relaties van Standaardtitel naar elk van deze schattingsentiteiten in Project Service nodig zijn: 

- **Details van prijsopgaveregel**
- **Detail van projectcontractregels**
- **Projecttaak**
- **Projectteamlid**
- **Schattingsregel**

5. Herhaal stap 1-5 om 1:N-relaties te maken van **Standaardtitel** naar **Details van prijsopgaveregel**, **Details van projectcontractregels**, **Projecttaak**, **Projectteamlid** en **Schattingsregel**.

> ![Standaardtitel toevoegen als een verwijzingsveld aan Schattingsregel.](media/ST-Estimate-Line.png)

In de leverings- en factureringsfasen moet het werk dat door elke standaardtitel is voltooid, nauwkeurig worden geprijsd om de werkelijke waarden van het project te verkrijgen. Dit betekent dat er 1:N-relaties moeten zijn van **Standaardtitel** naar de entiteiten **Tijdsvermelding**, **Werkelijk**, **Factuurregeldetail** en **Journaalregel**.

6. Herhaal de stappen 1-6 om 1:N-relaties te maken van **Standaardtitel** naar de entiteiten **Tijdsvermelding**, **Werkelijk**, **Factuurregeldetail** en **Journaalregel**.

> ![Standaardtitel toevoegen als een verwijzingsveld aan Tijdsvermelding.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Standaarddimensiewaarden instellen met de toewijzingsfuncties van het platform
Voor de tijdsvermelding is het handig als het systeem standaard voor Tijdsvermelding de standaardtitel gebruikt van de boekbare resource die de tijdsvermelding vastlegt. Neem de volgende stappen om veldtoewijzingen toe te voegen aan de 1:N-relatie van **Boekbare resource** naar **Tijdsvermelding**.

1. Selecteer in Solution Explorer in het linkernavigatiedeelvenster **Entiteiten > Standaardtitel**.
2. Vouw de entiteit **Standaardtitel** uit en selecteer **1:N-relaties**.
3. Dubbelklik op **Boekbare resource naar Tijdsvermelding**. Klik op de pagina **Relatie** op **Veldtoewijzingen gebruiken**. 
4. Klik op **Nieuw** om een nieuwe veldtoewijzing te maken tussen het veld **Standaardtitel** van de entiteit **Boekbare resource** naar het verwijzingsveld **Standaardtitel** van de entiteit **Tijdsvermelding**. 

> ![Veldtoewijzingen instellen om te zorgen dat standaard de Standaardtitel van Boekbare resource wordt gebruikt voor Tijdsvermelding.](media/ST-Mapping2.png)


Hiermee zijn de schemawijzigingen voltooid die zijn vereist voor aangepaste dimensies op basis van entiteit.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Aangepaste velden toevoegen aan formulieren, weergaven en bedrijfsregels

Nadat u alle vereiste schemawijzigingen hebt aangebracht, moet u de velden zichtbaar maken in de gebruikersinterface door de velden toe te voegen aan de formulieren en weergaven.

1. Open het formulier of de weergave. Selecteer het veld in het rechternavigatiedeelvenster en sleep het veld naar het formuliercanvas. 
2. Als u een weergave bewerkt, gebruikt u het rechternavigatiedeelvenster, klikt u op **Velden toevoegen**, selecteert u in het dialoogvenster **Lijst met velden** de velden die u nodig hebt en klikt u op **OK**.

De volgende tabel bevat een uitgebreide lijst met gebruiksklare formulieren en weergaven per entiteit die moeten worden bijgewerkt met de nieuwe velden. Als u extra weergaven of formulieren in uw aanpassingen van deze entiteiten hebt, voegt u de nieuwe velden ook daar aan toe.

| Project Service-entiteit        | Formulieren die het nieuwe veld nodig hebben   |Weergaven die het nieuwe veld nodig hebben      |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolprijs|• Informatie |• Actieve resourcecategorieprijzen<br> • Gekoppelde weergave van resourcecategorieprijzen|
|  Opslag voor rolprijs|• Informatie|• Actieve opslag voor rolprijs<br>• Gekoppelde weergave van opslag voor rolprijs|
|  Details van prijsopgaveregel|• Projectgegevens<br>• Snelle invoer van project|• Details van actieve prijsopgaveregel<br>• Gecombineerde details van prijsopgaveregels<br>• Gekoppelde weergave van details van prijsopgaveregels|
|  Details van projectcontractregel|• Projectgegevens<br>• Snelle invoer van project|• Gecombineerde contractregeldetails<br>• Actieve contractregeldetails<br>• Gekoppelde weergave van contractregeldetails|
|  Projecttaak|• Informatie<br>• Nieuw formulier||
|  Projectteamlid|• Informatie<br>• Nieuw formulier|• Actieve projectteamleden<br>• Projectteamleden<br>• Gekoppelde weergave van projectteamleden|
|  Tijdsvermelding|• Informatie<br>• Tijdsvermelding maken|• Mijn tijdsvermeldingen op datum<br>• Mijn tijdsvermeldingen voor deze week<br>• Tijdsvermeldingen voor goedkeuring|
|  Journaalregel|• Informatie<br>• Snelle invoer|• Actieve journaalregels<br>• Gekoppelde weergave van journaalregel|
|  Factuurregeldetail|• Informatie<br>• Snelle invoer|• Actieve factuurregeldetails<br>• Factureerbare factuurtransacties<br>• Gratis factuurtransacties<br>• Gekoppelde weergave van factuurregeldetails<br>• Niet-factureerbare factuurtransacties|
|  Werkelijk|• Informatie<br>• Actieve werkelijke waarden|• Gekoppelde weergave van werkelijke waarden|

Aangepaste velden moeten mogelijk ook worden toegevoegd aan bedrijfsregels, afhankelijk van wat u hebt gedefinieerd. Eén gebruiksklaar voorbeeld is bedoeld voor de bedrijfsregel **Bewerkbaarheid van tijdsvermelding gebaseerd op status**. Deze regel bepaalt welke velden moeten worden vergrendeld wanneer de tijdsvermelding een niet-bewerkbare status heeft, zoals **Goedgekeurd.** Voeg velden aan deze bedrijfsregel toe zodat de velden zijn vergrendeld voor bewerking wanneer de tijdsvermelding een andere status heeft dan **Concept** of **Geretourneerd.**


[!INCLUDE[footer-include](../includes/footer-banner.md)]

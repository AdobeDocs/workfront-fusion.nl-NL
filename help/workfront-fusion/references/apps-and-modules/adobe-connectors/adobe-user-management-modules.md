---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe-gebruikersbeheermodules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die gebruikers in uw rekening van Adobe beheren.
author: Becky
feature: Workfront Fusion
exl-id: e8fe8ec4-4b00-4c9a-81a5-acb2039b153b
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '2374'
ht-degree: 0%

---

# Adobe-gebruikersbeheermodules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die gebruikers in uw Adobe-account beheren.

Als u instructies bij het creëren van een scenario nodig hebt, zie de artikelen onder [ een scenario creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor een oudere licentie: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en -integratie], [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het abonnement [!UICONTROL Select] of [!UICONTROL Prime] [!DNL Adobe Workfront] hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] is opgenomen in het abonnement [!UICONTROL Ultimate] [!DNL Workfront] .</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Verbinding maken met Adobe-gebruikersbeheer

Verbinding maken voor uw [!DNL Adobe User Management] -modules:

1. In om het even welke module, voegt de klik **[!UICONTROL toe]** naast het vakje van de Verbinding.

1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Voer een naam in voor deze verbinding.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL -omgeving]</td>
        <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL -type]</td>
        <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!UICONTROL Adobe] [!UICONTROL Client ID] in. Dit vindt u in het detailgedeelte [!UICONTROL Credentials] van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in het detailgedeelte [!UICONTROL Credentials] van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organisatie-ID]</td>
        <td>Voer uw [!DNL Adobe] IMS-referenties in. De unieke id voor een organisatie. Dit is een tekenreeks in de vorm A495E53@AdobeOrg, waarbij het voorvoegsel voor de @ een hexadecimaal getal is. U kunt deze waarde vinden als onderdeel van het URL-pad voor de organisatie in de Admin Console of in de adobe.io-console voor de integratie van uw gebruikersbeheer.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Aanvullend bereik]</td>
        <td>Voor elk extra werkingsgebied wilt u toevoegen, <b> toevoegen punt </b> en ingaan het werkingsgebied.</td>
        </tr>
      </tbody>
    </table>

1. Klik **[!UICONTROL verdergaan]** om de verbinding te bewaren en aan de module terug te keren.



## Adobe-gebruikersbeheermodules en de bijbehorende velden

Wanneer u Adobe-gebruikersbeheermodules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen er extra Adobe-gebruikersbeheervelden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Zoekopdrachten](#searches)
* [Handelingen van gebruikers](#user-actions)
* [Handelingen in gebruikersgroepen](#user-group-actions)
* [Overige](#other)

### Zoekopdrachten

* [Gebruikersgroepen en productprofielen ophalen](#get-user-groups-and-product-profiles)
* [Gebruikersgegevens ophalen](#get-user-information)
* [Gebruikers in een gebruikersgroep of productprofiel ophalen](#get-users-in-a-user-group-or-product-profile)
* [Gebruikers in een organisatie ophalen](#get-users-in-an-organization)

#### Gebruikersgroepen en productprofielen ophalen

Deze zoekmodule haalt een lijst op met alle gebruikersgroepen en productprofielen in uw organisatie, samen met informatie over de groepen en profielen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum aantal geretourneerde resultaten</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tr> 
 </tbody> 
</table>

#### Gebruikersgegevens ophalen

Deze zoekmodule haalt details op voor één gebruiker in de organisatie, geïdentificeerd door hun e-mailadres.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-mailadres</td> 
   <td>Voer het e-mailadres in of wijs het e-mailadres toe van de gebruiker waarvoor u gegevens wilt retourneren. Voor gebruikers met Adobe-id, Enterprise en e-mailfederatie moet dit het volledige e-mailadres zijn, inclusief het domein. In alle gevallen is de parameter niet hoofdlettergevoelig.</td> 
  </tr> 
 </tbody> 
</table>

#### Gebruikers in een gebruikersgroep of productprofiel ophalen

Deze zoekmodule haalt een lijst op met alle gebruikers in de opgegeven gebruikersgroep of het opgegeven productprofiel, samen met informatie over de gebruikers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepsnaam</td> 
   <td>De gebruikersgroep, de naam van het productprofiel of een beheergroep. Voor een beheerdersgroep kan de naam een van de vaste groepen <code>_org_admin</code>, <code>_deployment_admin</code> of <code>_support_admin</code> zijn, of een groepspecifieke beheergroep. Deze worden geïdentificeerd met een voorvoegsel op de groepsnaam, zoals <code>_admin_groupName</code> , <code>_product_admin_productName</code> of <code>_developer_groupName</code> . Als de groep bestaat, maar de beheergroep niet, wordt een lege lijst geretourneerd.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Alleen direct</td> 
   <td>Geef op of het veld Groepen in de geretourneerde gebruikersstructuur alleen de productprofielen bevat waarvan de gebruiker een direct lid is. Indien onwaar, keert alle groepen (gebruikersgroepen, productprofielen, en admingroepen) terug die de gebruiker bevatten, ongeacht of een recht voor een bepaald productprofiel direct (via gebruikerstoewijzing) of onrechtstreeks (via een gebruikersgroep die de gebruiker bevat die aan het productprofiel wordt toegewezen) is. Indien waar (true), worden alle gebruikersgroepen en beheergroepen geretourneerd die de gebruiker bevatten, maar alleen de productprofielen waaraan de gebruiker expliciet een machtiging heeft toegewezen. Een gebruiker kan zowel een direct als een indirect lid van een productprofiel zijn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepen uitsluiten</td> 
   <td>Geef op of de reactie de array van groepen uitsluit van het retourneren voor elke individuele gebruiker.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Status</td> 
   <td>Deze optie is alleen van toepassing op productprofielen. Selecteer actief om gebruikers weer te geven die zijn ingericht voor het product en een actieve licentie hebben. Selecteer Inactief om gebruikers weer te geven die aan het productprofiel zijn toegevoegd maar geen actieve licentie hebben. Als leeg gelaten, keert de module alle lidgebruikers ongeacht hun machtigingsstatus terug.
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum aantal geretourneerde resultaten</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tr> 
 </tbody> 
</table>

#### Gebruikers in een organisatie ophalen

Deze onderzoeksmodule keert alle gebruikers van de organisatie verbonden aan de verbinding terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum aantal geretourneerde resultaten</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tr> 
 </tbody> 
</table>

### Handelingen van gebruikers

* [Een gebruiker toevoegen als lid van een groep](#add-a-user-as-a-member-of-a-group)
* [Een gebruiker maken](#create-a-user)
* [Een gebruiker uit groepen verwijderen](#remove-a-user-from-groups)
* [Een gebruiker bijwerken](#update-a-user)

#### Een gebruiker toevoegen als lid van een groep

Deze actiemodule voegt een gebruiker toe als lid van de opgegeven groep of groepen. Deze module kan de gebruiker aan maximaal vier groepen toevoegen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebruiker</td> 
   <td>Ga of kaart de gebruiker in die u aan de groepen wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domein</td> 
   <td>Voor gefederaliseerde id's die geen e-mailadressen zijn, voert u het domein in waartoe de gebruiker behoort.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepen</td> 
   <td>Voor elke groep die u de gebruiker aan wilt toevoegen, <b> toevoegen punt </b> klikken en de groep ingaan of in kaart brengen. U kunt maximaal vier groepen invoeren en moet ten minste één groep invoeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe ID gebruiken</td> 
   <td>Selecteer waar om ervoor te zorgen dat de gebruiker - identiteitskaart wordt geïnterpreteerd om naar een bestaande Adobe ID te verwijzen zelfs als een Onderneming of Federated ID met de zelfde naam bestaat.</td> 
  </tr> 
 </tbody> 
</table>

#### Een gebruiker maken

Deze actiemodule leidt tot een nieuwe gebruiker in de organisatie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID-type</td> 
   <td>Selecteer of u een gebruiker wilt maken met een Adobe ID, een Enterprise ID of een Federated ID. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aanmelden</td> 
   <td>Als u een gebruiker met een Federated ID maakt, selecteert u het aanmeldingstype.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-mail</td> 
   <td>Voer het e-mailadres voor de nieuwe gebruiker in of wijs het toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domein</td> 
   <td>Als u een gebruiker maakt met een Federated ID met een domeingebaseerde aanmelding, voert u het domein in of wijst u dit toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebruiker</td> 
   <td>Als u een gebruiker met een Federated ID met een op domein-gebaseerde login creeert, ga of kaart de gebruiker in die deze nieuwe gebruiker zal vertegenwoordigen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Voornaam</td> 
   <td>Voer de voornaam van de gebruiker in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Achternaam</td> 
   <td>Voer de achternaam van de gebruiker in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Land</td> 
   <td>Voer de ISO-landcode van twee tekens in of wijs deze toe. Dit kan niet worden gewijzigd nadat de gebruiker is gemaakt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Optie</td> 
   <td>Selecteer de actie die u wilt uitvoeren als de gebruiker al in de organisatie bestaat. Als geen optie wordt geselecteerd, en de gebruiker reeds bestaat, keert de module een fout terug.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe ID gebruiken</td> 
   <td>Indien waar (true), wordt de gebruikersnaam geïnterpreteerd als een verwijzing naar een bestaande Adobe ID, zelfs als een Enterprise of Federated ID met dezelfde naam bestaat.</td> 
  </tr> 
 </tbody> 
</table>

#### Een gebruiker uit groepen verwijderen

Deze actiemodule verwijdert het lidmaatschap van een gebruiker uit de opgegeven groepen. U kunt een gebruiker uit maximaal vier groepen tegelijk verwijderen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebruiker</td> 
   <td>Voer de gebruiker in of wijs de gebruiker toe die u uit de groepen wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domein</td> 
   <td>Voor gefederaliseerde id's die geen e-mailadressen zijn, voert u het domein in waartoe de gebruiker behoort.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepen</td> 
   <td>Voor elke groep die u de gebruiker uit wilt verwijderen, <b> toevoegen punt </b> en ingaan of in kaart brengen de groep. U kunt maximaal vier groepen invoeren en moet ten minste één groep invoeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe ID gebruiken</td> 
   <td>Selecteer waar om ervoor te zorgen dat de gebruiker - identiteitskaart wordt geïnterpreteerd om naar een bestaande Adobe ID te verwijzen zelfs als een Onderneming of Federated ID met de zelfde naam bestaat.</td> 
  </tr> 
 </tbody> 
</table>



#### Een gebruiker bijwerken

Deze actiemodule werkt een bestaande gebruiker bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebruiker</td> 
   <td>Voer de id in of wijs deze toe aan de gebruiker die u wilt bijwerken. Dit is het e-mailadres van de gebruiker, zoals <code>user@example.com</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domein</td> 
   <td>Als u een gebruiker bijwerkt met een Federated ID die geen e-mailadres is, voert u het domein in of wijst u het toe waartoe de gebruiker behoort om de gebruiker te identificeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-mail</td> 
   <td>Voer het nieuwe e-mailadres voor de gebruiker in of wijs dit toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Voornaam</td> 
   <td>Voer de voornaam van de gebruiker in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Achternaam</td> 
   <td>Voer de achternaam van de gebruiker in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

### Handelingen in gebruikersgroepen

* [Lidmaatschappen toevoegen voor een gebruikersgroep](#add-memberships-for-a-user-group)
* [Een gebruikersgroep maken](#create-a-user-group)
* [Een gebruikersgroep verwijderen](#delete-a-user-group)
* [Lidmaatschappen voor een gebruikersgroep verwijderen](#remove-memberships-for-a-user-group)
* [Een gebruikersgroep bijwerken](#update-a-user-group)

#### Lidmaatschappen toevoegen voor een gebruikersgroep

Met deze actiemodule voegt u gebruikers en productprofielen toe aan een gebruikersgroep. Gebruikers die aan de gebruikersgroep zijn toegevoegd, krijgen recht op alle productprofielen in de gebruikersgroep. Als u een productprofiel toevoegt, krijgt u recht op dat profiel voor gebruikers in de gebruikersgroep.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepsnaam</td> 
   <td>Voer de naam in of wijs de naam toe van de groep waarvan u de gebruikers of profielen wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebruikers</td> 
   <td>Voor elke gebruiker die u wilt toevoegen, <b> klikken voegt gebruiker </b> toe en gaat het e-mailadres van de gebruiker in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profielen</td> 
   <td>Voor elk profiel dat u aan de groep wilt toevoegen, klik <b> gebruiker </b> toevoegen en de profielnaam ingaan</td> 
  </tr> 
 </tbody> 
</table>

#### Een gebruikersgroep maken

Deze actiemodule maakt een nieuwe gebruikersgroep. Als er al een groep met de opgegeven naam bestaat, kan de module de bestaande groep bijwerken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepsnaam</td> 
   <td>Voer een naam in of wijs een naam toe aan de nieuwe gebruikersgroep.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschrijving</td> 
   <td>Voer een beschrijving voor de nieuwe gebruikersgroep in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Optie</td> 
   <td>Selecteer de actie die u wilt uitvoeren als de gebruikersgroep al bestaat in de organisatie. Als er geen optie is geselecteerd en de gebruikersgroep al bestaat, retourneert de module een fout.</td> 
  </tr> 
 </tbody> 
</table>

#### Een gebruikersgroep verwijderen

Deze actiemodule verwijdert een bestaande gebruikersgroep.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepsnaam</td> 
   <td>Voer de naam in of wijs de naam toe van de groep die u wilt verwijderen.</td> 
  </tr> 
 </tbody> 
</table>

#### Lidmaatschappen voor een gebruikersgroep verwijderen

Deze actiemodule verwijdert gebruikers of profielen uit een gebruikersgroep.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepsnaam</td> 
   <td>Voer de naam in of wijs de naam toe van de groep waarvan u de gebruikers of profielen wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebruikers</td> 
   <td>Voor elke gebruiker die u wilt verwijderen, <b> klikken voegt gebruiker </b> toe en gaat het e-mailadres van de gebruiker in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profielen</td> 
   <td>Voor elk profiel dat u uit de groep wilt verwijderen, klik <b> gebruiker </b> toevoegen en de profielnaam ingaan</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe ID gebruiken</td> 
   <td>Indien waar (true), wordt de gebruikersnaam geïnterpreteerd als een verwijzing naar een bestaande Adobe ID, zelfs als een Enterprise of Federated ID met dezelfde naam bestaat.</td> 
  </tr> 
 </tbody> 
</table>

#### Een gebruikersgroep bijwerken

Deze actiemodule werkt een bestaande gebruikersgroep bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Oorspronkelijke groepsnaam</td> 
   <td>Voer de huidige naam in of wijs de naam toe van de groep die u wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nieuwe groepsnaam</td> 
   <td>Typ of wijs de nieuwe naam toe die u voor de groep wilt gebruiken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Oorspronkelijke groepsnaam</td> 
   <td>Voer de bijgewerkte beschrijving van de groep in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
 </table>

### Overige


#### Een aangepaste API-aanroep maken

Deze actiemodule maakt een aangepaste aanroep naar de Adobe-API voor gebruikersbeheer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan het Beheer van de Gebruiker van Adobe, zie <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" > een verbinding aan het Beheer van de Gebruiker van Adobe </a> in dit artikel tot stand brengen.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Een pad invoeren ten opzichte van <code>https://usermanagement.adobe.io/v2/usermanagement/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Methode</p>
      </td>
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Kopteksten</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Hiermee worden automatisch machtigingsheaders en x-api-sleutelkoppen toegevoegd.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Tekenreeks query  </td>
      <td>
        <p>Voer de queryreeks voor de aanvraag in.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Lichaam</td>
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

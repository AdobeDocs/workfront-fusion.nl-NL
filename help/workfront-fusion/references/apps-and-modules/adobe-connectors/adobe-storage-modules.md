---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe Storage-modules
description: In een Adobe Workfront Fusion-scenario kunt u projecten maken en beheren in de Adobe Admin Console.
author: Becky
feature: Workfront Fusion
exl-id: 78ee905f-4713-44a4-bffb-c64cdb3665c2
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1368'
ht-degree: 0%

---

# Adobe Storage-modules

In een Adobe Workfront Fusion-scenario kunt u projecten maken en beheren in de Adobe Admin Console.

Als u instructies bij het creëren van een scenario nodig hebt, zie de artikelen onder [&#x200B; een scenario creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie</td> 
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten</p>
   <p>of</p>
   <p>Verouderd: Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Select- of Prime Workfront-pakket: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultimate Workfront-pakket: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Verbinding maken met Adobe Storage

Voor het tot stand brengen van een verbinding met Adobe Storage hebt u een configuratie nodig in de Adobe Developer Console en in Fusion.

### Het project configureren in de Adobe Developer Console

U moet de API toevoegen aan uw project in de Adobe Developer Console.

1. Open uw project in de Adobe Developer Console.
1. Klik **toevoegen aan project**, en selecteren **API**.
1. Van de lijst van beschikbare APIs, uitgezochte **Platform van de Wolk van Adobe en Collaboration API**.
1. Voor het Uitgezochte scherm van het authentificatietype, selecteer **OAuth server-aan-Server** en klik **daarna**.
1. Voeg een naam voor de referentie toe.
1. Klik **daarna**, dan klik **sparen gevormde API**.
1. Noteer de opgegeven referenties die u gebruikt bij het configureren van de verbinding in Workfront Fusion.
1. Ga verder [&#x200B; van uw technische rekening een beheerder in Adobe Admin Console &#x200B;](#make-your-technical-account-an-admin-in-the-adobe-admin-console) maken.

### Een technisch account als beheerder instellen in de Adobe Admin Console

Selecteer op de Adobe Admin Console-pagina het tabblad Producten in de bovenste navigatiebalk en selecteer vervolgens Workfront Fusion

1. Zoek en kopieer het e-mailadres van de gebruiker van de technische account in uw organisatie.
1. Als een lijst wordt weergegeven, selecteert u de koppeling bovenaan.
1. Dit is uw instantie van de Productie waar uw gebruikers werken.
1. Klik in de lijst die wordt weergegeven en het tabblad Productprofielen is geselecteerd op de naam van de koppeling Workfront-productprofiel.

   Deze lijst bevat alle gebruikers die al zijn toegewezen aan uw productie-instantie van Workfront.

1. Selecteer het **Admins** lusje boven de lijst van gebruikers.
1. Selecteer **Admin** toevoegen.
1. In het Add vakje van de Beheerders van het productprofiel, ga de e-mailadressen van de technische rekening in, dan uitgezocht **sparen**.

   De technische rekening wordt een beheerder gemaakt.

1. Ga aan [&#x200B; verder creeer de verbinding in de Fusie van Workfront &#x200B;](#create-the-connection-in-workfront-fusion).

### Verbinding maken in Workfront Fusion

Verbinding maken voor uw [!DNL Adobe Storage] -modules:

1. Klik in een willekeurige module op **[!UICONTROL Add]** naast het vak Verbinding.

1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>Selecteer <code>Server to server</code> .</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Voer een naam in voor deze verbinding.</p>
        </td>
        </tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!UICONTROL Adobe] [!UICONTROL Client ID] in. Dit vindt u in de [!UICONTROL Credential details] -sectie van het project in de [!DNL Adobe Developer Console] .</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in de [!UICONTROL Credential details] -sectie van het project in de [!DNL Adobe Developer Console] .</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organization ID]</td>
        <td>Voer uw Adobe IMS-organisatie-id in of wijs deze toe. Dit is een tekenreeks met de notatie <code> 123abc@AdobeOrg</code> , waarbij de sectie voor de @ een hexadecimaal getal is. U kunt deze waarde vinden als onderdeel van het URL-pad voor uw organisatie in de Adobe Admin Console of in de Adobe.IO-console voor de integratie van uw gebruikersbeheer.</td>
        </tr>
      </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## Adobe Storage-modules en hun velden

Wanneer u Adobe-gebruikersbeheermodules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen er extra Adobe-gebruikersbeheervelden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [ESM-opslag](#esm-stores)
* [Uitnodigingen](#invitations)
* [Overige](#other)

### ESM-opslag

* [Een ESM-winkel maken](#create-an-esm-store)
* [Een ESM-winkel verwijderen](#delete-an-esm-store)
* [Een ESM-winkel negeren](#discard-an-esm-store)
* [Een ESM-winkel herstellen](#restore-an-esm-store)

#### Een ESM-winkel maken

Deze actiemodule stelt een nieuwe opslag van het Beheer van de Opslag van de Onderneming (ESM) op om zaken-kritieke activa te organiseren en te beheren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan de Opslag van Adobe, zie <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" > een verbinding aan de Opslag van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Projectnaam</td> 
   <td>Ga of kaart een naam voor het nieuwe project in.</td> 
  </tr> 
 </tbody> 
</table>

#### Een ESM-winkel verwijderen

Deze actiemodule verwijdert permanent een bestaande opslag ESM en al zijn bijbehorende gegevens. Deze handeling kan niet ongedaan worden gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan de Opslag van Adobe, zie <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" > een verbinding aan de Opslag van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">WinkelID</td> 
   <td>Voer de id in van de winkel die u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Een ESM-winkel negeren

Deze actiemodule markeert een EMS-winkel die kan worden verwijderd en die een respijtperiode toestaat voordat deze definitief wordt verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan de Opslag van Adobe, zie <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" > een verbinding aan de Opslag van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">WinkelID</td> 
   <td>Ga of kaart identiteitskaart van de opslag in u wilt verwerpen.</td> 
  </tr> 
 </tbody> 
</table>

#### Een ESM-winkel herstellen

Deze actiemodule herstelt een eerder geschrapte opslag ESM en herstelt toegang tot zijn gegevens en configuraties.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan de Opslag van Adobe, zie <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" > een verbinding aan de Opslag van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">WinkelID</td> 
   <td>Voer de id in van de opslagruimte die u wilt herstellen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

### Uitnodigingen

#### Gebruiker uitnodigen

Deze actiemodule verzendt een uitnodiging verleent een nieuwe gebruiker toegang tot een specifieke opslag ESM, toelatend samenwerking en dossierbeheer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td>Voor instructies bij het creëren van een verbinding aan de Opslag van Adobe, zie <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" > een verbinding aan de Opslag van Adobe </a> in dit artikel tot stand brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-mailadres</td> 
   <td>Voer het e-mailadres in of wijs het e-mailadres toe van de gebruiker die u wilt uitnodigen naar de winkel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element-id</td> 
   <td>Voer de id in van het element waarnaar u de gebruiker wilt uitnodigen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Rol</td> 
   <td>Selecteer de rol die de nieuwe uitgenodigde gebruiker voor de activa moet hebben.<ul><li>Eigenaar</li><li>Editor</li><li>Viewer</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kan opmerkingen maken</td> 
   <td>Schakel deze optie in als u wilt dat de gebruiker opmerkingen kan maken over het element.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kan delen</td> 
   <td>Schakel deze optie in als u wilt dat de gebruiker het element kan delen met andere gebruikers.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Acceptatie vereist</td> 
   <td>Schakel deze optie in om ervoor te zorgen dat de gebruiker de uitnodiging accepteert voordat hij of zij aan het element kan samenwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bevestigingen gebruiken</td> 
   <td>Schakel deze optie in als een koppelpunt naar de bron moet worden gemaakt voor de genodigde. U moet de optie Acceptatie inschakelen om deze optie in te schakelen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Meldingstype</td> 
   <td>Typ of wijs het Adobe-berichttype toe waarmee u de gebruiker op de hoogte wilt stellen van de uitnodiging. Als dit leeg blijft, is het berichttype gebaseerd op het mimetype van het element.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sjabloonnaam</td> 
   <td>Voer de Adobe Post Office-id in of wijs deze toe aan de sjabloon die u voor de e-mail met de uitnodiging wilt gebruiken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Landinstelling</td> 
   <td>Voer de landinstelling van de gebruiker in in de vorm van een taalcode en landcode. <p>Voorbeeld: <code>en-us</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Extern</td> 
   <td>Stel deze optie in op true als u meldingen wilt verzenden met een systeem dat geen deel uitmaakt van de Adobe Uitnodigingsservice. Externe meldingen worden alleen ondersteund wanneer acceptatie niet is vereist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type element</td> 
   <td>Voer het type element in of wijs het toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bericht</td> 
   <td>Voer een bericht in of wijs een bericht toe dat u in de e-mail met de uitnodiging wilt opnemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Doel-URL</td> 
   <td>Voer de URL in of wijs deze toe die de genodigde kan gebruiken om het element weer te geven.</td> 
  </tr> 
 </tbody> 
</table>

### Overige

#### Een aangepaste API-aanroep maken

Deze actiemodule doet een aangepaste HTTP-aanvraag voor de Adobe Storage API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
   <td>Voor instructies bij het creëren van een verbinding aan de Opslag van Adobe, zie <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" > een verbinding aan de Opslag van Adobe </a> in dit artikel tot stand brengen.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Een pad invoeren ten opzichte van <code>https://ccprojects.adobe.io/api/v3/.</code></p>
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
        <p>Workfront Fusion voegt automatisch machtigingsheaders en x-api-sleutelkopballen toe.</p>
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

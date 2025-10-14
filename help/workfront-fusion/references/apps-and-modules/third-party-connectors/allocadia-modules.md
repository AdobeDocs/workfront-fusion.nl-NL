---
title: Allocadia
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Allocadia gebruiken en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
exl-id: 9a6fccd6-6eee-42dc-a678-c1f34280d139
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1368'
ht-degree: 0%

---

# [!DNL Allocadia] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Allocadia] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-abonnement*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidige vergunningsvereiste: geen Workfront Fusion-vergunningsvereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] Adobe Workfront-abonnement hebt, moet uw organisatie zowel Adobe Workfront Fusion als Adobe Workfront aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. Workfront Fusion is opgenomen in het Workfront-plan van [!UICONTROL Ultimate] .</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet Adobe Workfront Fusion en Adobe Workfront aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met uw Workfront-beheerder om te weten te komen welk plan, licentietype of toegang u hebt.

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

Als u [!DNL Allocadia] -modules wilt gebruiken, hebt u een [!DNL Allocadia] -account nodig.

## [!DNL Allocadia] API-informatie

De Allocadia-aansluiting gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.7.6</td> 
  </tr>
 </tbody> 
</table>

## Verbinden [!DNL Allocadia] met Workfront Fusion

U kunt rechtstreeks vanuit een [!DNL Allocadia] -module verbinding maken met uw [!DNL Allocadia] -account.

1. Klik in een willekeurige [!DNL Allocadia] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Selecteer of u de server van Noord-Amerika of de server van Europa wilt gebruiken.
1. Voer uw gebruikersnaam en wachtwoord in.
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL Allocadia] modules en hun velden

Wanneer u [!DNL Allocadia] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Allocadia] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

#### [!UICONTROL Watch Record]

Deze triggermodule voert een scenario uit wanneer objecten van een specifiek type worden toegevoegd, bijgewerkt of beide. De module retourneert alle standaardvelden die zijn gekoppeld aan de record of records, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> <table style="table-layout:auto"> <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect Allocadia] to Workfront Fusion </a> in dit artikel voor instructies over het aansluiten van uw Allocadia-account op Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>Selecteer of u het scenario op Nieuwe slechts Verslagen, [!UICONTROL Updated Records Only], of Nieuwe en Bijgewerkte Verslagen wilt letten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type entiteit</td> 
   <td>Selecteer het allocadia-recordtype waarop u de module wilt letten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Uitvoer</td> 
   <td> <p>Selecteer de velden die u in de uitvoer van de module wilt opnemen. Beschikbare velden zijn afhankelijk van het type entiteit dat u hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limiet</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt letten.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [Aangepaste API-aanroep](#custom-api-call)
* [Record lezen](#read-record)
* [Record maken](#create-record)
* [Record verwijderen](#delete-record)
* [Record bijwerken](#update-record)

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Allocadia] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Allocadia] -modules kan worden uitgevoerd.

De handeling is gebaseerd op het door u opgegeven eenheidstype (allocadia-objecttype).

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Allocadia] rekening aan Workfront Fusion, zie <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Allocadia] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in dat is gebaseerd op <code>https://api-na.allocadia.com/{version}</code> of <code>https://api-eu.allocadia.com/{version}</code> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read Record]

Deze actiemodule leest gegevens uit één record in [!DNL Allocadia] .

U geeft de id van de record op.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Allocadia] rekening aan Workfront Fusion, zie <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Allocadia] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Selecteer het type [!DNL Allocadia] record dat u wilt lezen in de module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u in de uitvoer van de module wilt opnemen. Welke velden beschikbaar zijn, is afhankelijk van de geselecteerde [!UICONTROL Entity Type] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de unieke [!DNL Allocadia] -id in of wijs deze toe aan de record die u wilt lezen in de module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Record]

Deze actiemodule maakt een record.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Allocadia] rekening aan Workfront Fusion, zie <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Allocadia] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Selecteer of u een nieuwe record wilt maken op basis van de regel- of kolomkeuze.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Selecteer het budget waar u een record wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Column choices]</td> 
   <td>Selecteer de kolom die u wilt gebruiken om een nieuwe record te maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Label]</td> 
   <td>Een label voor de nieuwe record invoeren of toewijzen</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Record]

Deze actiemodule verwijdert een bepaalde record.

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Allocadia] rekening aan Workfront Fusion, zie <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Allocadia] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td> <p>Selecteer het type entiteit dat u wilt verwijderen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Line item]</strong> </p> <p>Geef de id van het lijstitem op</p> </li> 
     <li> <p><strong>[!UICONTROL Column Choice]</strong> </p> <p>Selecteer het budget waaruit u een record wilt verwijderen en voer vervolgens de kolom-id en de keuze-id in.</p> </li> 
     <li> <p><strong>[!UICONTROL Forecast Tags]</strong> </p> <p>Selecteer het budget waaruit u een record wilt verwijderen en voer vervolgens de tag-id in.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update Record]

Deze actiemodule werkt een record bij, zoals een regelitem, een gebruiker of een kolomkeuze.

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!UICONTROL Allocadia] rekening aan Workfront Fusion, zie <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Allocadia] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Selecteer het type [!DNL Allocadia] record dat u wilt bijwerken in de module. Andere velden worden weergegeven op basis van het eenheidstype dat u selecteert.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Selecteer het budget waar u een record wilt bijwerken. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

#### [!UICONTROL Search Record]

Deze zoekmodule zoekt naar records in een object in [!DNL Allocadia] dat overeenkomt met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

U geeft het gewenste type records op.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Allocadia] rekening aan Workfront Fusion, zie <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Allocadia] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Selecteer het type [!DNL Allocadia] record waarnaar u wilt zoeken in de module. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Selecteer het budget dat u wilt zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Selecteer of u de module Alle Overeenkomende Verslagen, of het Eerste Overeenkomende slechts Verslag wilt terugkeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Selecteer het veld waarnaar u wilt zoeken, selecteer de bewerking en voer de waarde in die u wilt zoeken. U kunt regels [!DNL AND] of [!DNL OR] toevoegen om uw zoekopdracht verder te filteren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u in de uitvoer van de module wilt opnemen. Beschikbare velden zijn afhankelijk van het type entiteit dat u hebt geselecteerd.</p> </td> 
  </tr> 
 </tbody> 
</table>

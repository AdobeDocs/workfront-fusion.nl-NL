---
title: ServiceNow-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die  [!DNL ServiceNow] gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 0%

---

# [!DNL ServiceNow] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL ServiceNow] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Als u [!DNL ServiceNow] -modules wilt gebruiken, moet u een [!DNL ServiceNow] -account hebben.

## ServiceNow API-informatie

De schakelaar ServiceNow gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://{connection.instance}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL ServiceNow] met [!DNL Workfront Fusion]

Verbinding maken voor uw [!DNL ServiceNow] -modules:

1. Klik op **[!UICONTROL Add]** naast het vak [!UICONTROL Connection] wanneer u de eerste module van [!DNL ServiceNow] gaat configureren.
1. Voer het volgende in:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Geef een naam op voor de nieuwe [!DNL ServiceNow] -verbinding</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Username]</p> </td> 
      <td>Voer uw [!DNL ServiceNow] gebruikersnaam in.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Voer uw wachtwoord voor ServiceNow in.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Instance]</p> </td> 
      <td> <p>Voer het adres in van uw [!DNL ServiceNow] -account zonder <code>https://</code> (gewoonlijk <code>&lt;company>.service-now.com</code> ).</p> </td> 
     </tr> 
    </tbody> 
   </table>

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow] modules en hun velden

Wanneer u [!DNL ServiceNow] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL ServiceNow] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Als een douaneverslag op een &quot;[!UICONTROL Record type]&quot;gebied wordt geselecteerd, kan het wat tijd vergen om de douanevelden te laden.
>
>* Als er geen aangepaste records zijn, is het vervolgkeuzemenu voor het veld Type record leeg.

### Triggers

#### [!UICONTROL Watch records]

Deze triggermodule activeert een scenario wanneer een record wordt gemaakt of bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecteer of de tabel die u wilt bekijken, een aangepaste tabel of een standaardtabel is.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecteer het type record dat u wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selecteer het type waarden dat u wilt weergeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de velden die u wilt uitvoeren in de module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Selecteer of u nieuwe records of bijgewerkte records wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Deactivate a User]](#deactivate-a-user)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)
* [[!UICONTROL Update a record]](#update-a-record)

#### [!UICONTROL Create a record]

Deze actiemodule maakt een nieuwe [!DNL ServiceNow] -record.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecteer of u een record wilt maken in een aangepaste tabel of een standaardtabel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecteer het type [!DNL ServiceNow] record dat u met de module wilt maken. Vervolgens kunt u de beschikbare velden voor dit recordtype invullen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL ServiceNow] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL ServiceNow] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> Voer een pad in dat relatief is ten opzichte van <code>https://&ltinstance_url&gt/api/</code> . </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> </td> 
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

#### [!UICONTROL Deactivate a User]

Met deze actiemodule wordt een gebruiker in [!DNL ServiceNow] gedeactiveerd met de systeem-id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User System ID]</td> 
   <td> Voer de unieke [!DNL ServiceNow] -id in of wijs deze toe aan de gebruiker die de module moet deactiveren.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a record]

Deze actiemodule verwijdert een incident of een gebruiker.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecteer of u een incident of een gebruiker wilt schrappen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>Voer de unieke [!DNL ServiceNow] -id in of wijs deze toe aan de record die u wilt verwijderen door de module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

Deze actiemodule downloadt een bijlage in een [!DNL ServiceNow] -record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment System ID]</td> 
   <td> Voer de unieke [!DNL ServiceNow] -id in of wijs deze toe aan de bijlage die u wilt downloaden.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Deze actiemodule leest een [!DNL ServiceNow] -record met de systeem-id.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Voer de unieke [!DNL ServiceNow] -id in of wijs deze toe aan de record die u wilt lezen in de module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecteer of de record die u wilt lezen zich in een aangepaste tabel of in een standaardtabel bevindt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecteer het type [!DNL ServiceNow] record dat u wilt lezen in de module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selecteer het type waarden dat u wilt weergeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de velden die u wilt uitvoeren in de module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Deze actiemodule maakt een nieuwe [!DNL ServiceNow] -record.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Voer de unieke [!DNL ServiceNow] -id in of wijs deze toe aan de record die u wilt bijwerken in de module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecteer of de record die u wilt bijwerken zich in een aangepaste tabel of een standaardtabel bevindt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecteer het type [!DNL ServiceNow] record dat u wilt bijwerken in de module. Vervolgens kunt u de beschikbare velden voor dit recordtype invullen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an attachment]

Deze actiemodule uploadt een bijlage naar een [!DNL ServiceNow] -record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table name]</td> 
   <td>Typ of wijs de naam van de tabel toe waar u de bijlage wilt uploaden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>Voer de unieke [!DNL ServiceNow] -id in of wijs deze toe aan het item waar u de bijlage wilt uploaden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

#### [!UICONTROL Search for records]

Deze module zoekt naar records aan de hand van criteria die u selecteert.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL ServiceNow] met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw ServiceNow-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Selecteer of de tabel die u wilt doorzoeken, een aangepaste tabel of een standaardtabel is.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecteer het type record waarnaar u wilt zoeken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Selecteer of u wilt dat de module alle records retourneert die aan de criteria voldoen, of alleen de eerste record die aan deze criteria voldoet. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search type]</td> 
   <td> <p>Selecteer welk type zoekopdracht u wilt uitvoeren door de module</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Advanced query]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Query]</p> <p>Voer de aangepaste zoekquery in. Voor informatie over [!DNL ServiceNow] vragen van het douaneonderzoek, zie de <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html"> ServiceNow vraagdocumentatie </a>.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Criteria]</p> <p>Voer de criteria in waarmee u de module wilt zoeken. </li> 
       <li> <p>[!UICONTROL Sort by]</p> <p>Geef aan op welk veld de module de resultaten moet sorteren en of ze oplopend of aflopend moeten worden gesorteerd.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selecteer het type waarden dat u wilt weergeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de velden die u wilt uitvoeren in de module.</td> 
  </tr> 
 </tbody> 
</table>

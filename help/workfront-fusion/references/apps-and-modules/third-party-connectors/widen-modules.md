---
title: Breedte-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!UICONTROL Widen] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 11376e58-a44b-4766-85dc-e2421b0112de
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1442'
ht-degree: 0%

---

# [!DNL Widen] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!UICONTROL Widen] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Elk Adobe Workfront Workflow-pakket en elk Adobe Workfront Automation and Integration-pakket</p><p>Workfront Ultimate</p><p>Workfront Prime en Select packages, met extra aanschaf van Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licenties</td> 
   <td> <p>Standard</p><p>Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie</td> 
   <td>
   <p>Exploitatie gebaseerd: geen Workfront Fusion-licentievereisten</p>
   <p>Connectorgebaseerde (verouderde): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Als u [!UICONTROL Widen] -modules wilt gebruiken, moet u een [!UICONTROL Widen] -account hebben.

## API-informatie verruimen

De breedste connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.10.11</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Widen] met Workfront Fusion  {#connect-widen-to-workfront-fusion}

U kunt rechtstreeks vanuit een [!DNL Widen] -module verbinding maken met uw [!DNL Widen] -account.

1. Klik in een willekeurige [!DNL Widen] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Selecteer de omgeving en het type account waarmee u verbinding maakt. Dit is alleen ter informatie en wordt weergegeven in het gebied Verbindingen van Fusion.
1. Selecteer het [!DNL Widen] -domein waarmee u verbinding wilt maken.
1. Voer het token voor uw [!DNL Widen] -account in. Voor instructies bij de plaats bepalen van dit teken, zie [[!DNL Widen]  API FAQs ](https://community.widen.com/collective/s/article/API-FAQs).
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL Widen] modules en hun velden

Wanneer u [!DNL Widen] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Widen] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggermodules](#trigger-modules)
* [Modules voor handelingen](#action-modules)
* [Zoekmodules](#search-modules)

### Triggermodules

#### [!UICONTROL Watch assets]

Deze triggermodule start een scenario wanneer een element wordt gemaakt of bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p>Selecteer of u nieuwe elementen of bijgewerkte elementen wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Selecteer de eigenschappen die u in de moduleuitvoer naast de activagebieden wilt omvatten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de velden die u wilt opnemen in de uitvoer van de module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal activa in u de module wilt werken met tijdens elke cyclus van de scenariouitvoering.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Modules voor handelingen

* [[!UICONTROL Add assets to collections]](#add-assets-to-collections)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download File]](#download-file)
* [[!UICONTROL Read asset info]](#read-asset-info)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Upload a file]](#upload-a-file)

#### [!UICONTROL Add assets to collections]

Deze actiemodule voegt een of meer elementen toe aan verzamelingen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td>Voor elke inzameling die u de activa aan wilt toevoegen, <strong> [identiteitskaart van Inzamelingen] </strong> klikken en [!UICONTROL Collection ID] ingaan of in kaart brengen.</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> Voor elk element dat u aan een verzameling wilt toevoegen, klikt u op <strong>[!UICONTROL Assets ID]</strong> en voert u de id van het element in of wijst u deze toe.</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal activa in u de module wilt werken met tijdens elke cyclus van de scenariouitvoering.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Widen] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Widen] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Selecteer of u de nieuwste versie van de API van [!DNL Widen] of versie 1.0 wilt gebruiken</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Ga of kaart URL voor uw API vraag in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] Hiermee voegt u de machtigingsheaders voor u toe.</p> </td> 
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

#### [!UICONTROL Download File]

Deze actiemodule downloadt een middel van uw [!DNL Widen] account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Voer de id in van het element dat u wilt downloaden of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read asset info]

Deze actiemodule wint een individueel middel door zijn unieke identiteitskaart terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Voer de id in van het element waarvoor u informatie wilt lezen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Selecteer de eigenschappen die u in de moduleuitvoer naast de activagebieden wilt omvatten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de velden die u wilt opnemen in de uitvoer van de module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection]

Deze actiemodule verwijdert een of meer elementen uit verzamelingen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td>Voor elke inzameling die u activa van wilt verwijderen, <strong> [identiteitskaart van Inzamelingen] </strong> klikken en [!UICONTROL Collection ID] ingaan of in kaart brengen.</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> Voor elk element dat u uit een verzameling wilt verwijderen, klikt u op <strong>[!UICONTROL Assets ID]</strong> en voert u de id van het element in of wijst u deze toe.</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal activa in u de module wilt werken met tijdens elke cyclus van de scenariouitvoering.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

In deze actiemodule worden de metagegevensvelden van een element bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Voer de id van het element in of wijs deze toe aan de locatie waar u de metagegevens wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata type]</td> 
   <td> <p>Selecteer het type metagegevens voor de metagegevens die u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Selecteer de metagegevensvelden die u wilt bijwerken. Voer voor elk veld de nieuwe waarde voor het veld in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal activa in u de module wilt werken met tijdens elke cyclus van de scenariouitvoering.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

Deze actiemodule uploadt een bestand naar uw [!DNL Widen] -account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Profile]</td> 
   <td> <p>Selecteer het uploadprofiel dat de module moet gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Method]</td> 
   <td> <p>Selecteer hoe u het bestand wilt uploaden.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL From File]</strong> </p> <p>Selecteer of wijs het brondossier van een vorige module in kaart.</p> </li> 
     <li> <p><strong>[!UICONTROL By URL]</strong> </p> <p>Voer de URL in van het bestand dat u wilt uploaden of wijs deze toe.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Voer een naam in voor het geüploade bestand of wijs een naam toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata Type]</td> 
   <td>Selecteer het type metagegevens voor het bestand dat u wilt uploaden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Selecteer de metagegevensvelden die u wilt opnemen in de bestandsupload. Voer voor elk veld de waarde [!UICONTROL value] voor het veld in.</td> 
  </tr> 
 </tbody> 
</table>

### Zoekmodules

* [[!UICONTROL Read collection assets]](#read-collection-assets)
* [[!UICONTROL Search assets]](#search-assets)

#### [!UICONTROL Read collection assets]

Deze actiemodule wint een lijst van activa binnen een inzameling terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Voer de id in van de verzameling die de elementen bevat die u wilt lezen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>Voer het nummer in of wijs het nummer toe van het eerste item dat u wilt aanbieden. Dit is een manier om de records te pagineren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>Selecteer de eigenschap waarmee u de elementen wilt sorteren. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Selecteer of u elementen in oplopende of aflopende volgorde wilt sorteren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de velden die u wilt opnemen in de uitvoer van de module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search assets]

Deze zoekmodule haalt een lijst op met elementen die voldoen aan de specifieke zoekcriteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie [!DNL Widen] Verbinding maken <a href="#connect-widen-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Widen] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search query]</td> 
   <td> <p>Voer de criteria in waarmee u elementen wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>Selecteer hoe u de elementen wilt sorteren. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Selecteer of u elementen in oplopende of aflopende volgorde wilt sorteren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include deleted]</td> 
   <td>Schakel deze optie in om verwijderde elementen op te nemen in de zoekopdracht.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Include archived]</p> </td> 
   <td> <p>Schakel deze optie in om gearchiveerde elementen op te nemen in de zoekopdracht.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search document text]</td> 
   <td>Schakel deze optie in om documenttekst in uw zoekopdracht op te nemen of ingesteld op false om alleen elementen op te nemen waarvoor de titel overeenkomt met de zoekcriteria.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Offset]</td> 
   <td>Ga of kaart het aantal van het eerste punt in u details voor wilt terugwinnen. Dit is een manier om de records te pagineren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scroll]</td> 
   <td>Schakel deze optie in als u schuiven wilt toestaan.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Selecteer de eigenschappen die u in de moduleuitvoer naast de activagebieden wilt omvatten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de velden die u wilt opnemen in de uitvoer van de module.</td> 
  </tr> 
 </tbody> 
</table>

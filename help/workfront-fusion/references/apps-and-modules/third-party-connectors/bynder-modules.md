---
title: Byndermodules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die  [!DNL Bynder] gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1534'
ht-degree: 0%

---

# [!DNL Bynder] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Bynder] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Als u [!DNL Bynder] -modules wilt gebruiken, moet u een [!DNL Bynder] -account hebben.

## Bynder-API-informatie

De verbindingslijn Bynder gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.25.21</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Bynder] met Workfront Fusion  {#connect-bynder-to-workfront-fusion}

>[!NOTE]
>
>Bynder gebruikt de code van de Toekenning van de Vergunning / vernieuw symbolische subsidietype. Dit is het enige subsidietype dat de schakelaar van de Bynder van de Fusie gebruikt.

* [Creeer een verbinding aan  [!DNL Bynder]  van  [!DNL Workfront Fusion]](#create-a-connection-to-bynder-from-workfront-fusion)
* [Een [!UICONTROL Client ID] en [!UICONTROL Client Secret] in  [!DNL Bynder]  genereren (optioneel)](#generate-a-client-id-and-client-secret-in-bynder-optional)

### Verbinding maken met [!DNL Bynder] van [!DNL Workfront Fusion]

U kunt rechtstreeks vanuit een [!DNL Bynder] -module een verbinding maken vanuit [!DNL Workfront Fusion] naar uw [!DNL Bynder] -account.

1. Klik in een willekeurige [!DNL Bynder] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Selecteer het [!DNL Bynder] -domein waarmee u verbinding wilt maken.
1. (Optioneel) Klik op **[!UICONTROL Advanced settings]** en voer vervolgens de [!UICONTROL Client ID] en [!UICONTROL Client Secret] in.

   Voor instructies bij het produceren van identiteitskaart van de Cliënt en Geheime cliënt, zie [ een identiteitskaart van de Cliënt en Geheime cliënt binnen  [!DNL Bynder]  (Facultatief) ](#generate-a-client-id-and-client-secret-in-bynder-optional) in dit artikel produceren.

1. Voer in het venster [!UICONTROL login] uw gebruikersnaam (e-mailadres) en wachtwoord in.
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

### Een lus [!UICONTROL Client ID] en [!UICONTROL Client Secret] in [!DNL Bynder] genereren (optioneel)

Als u een verbinding wilt maken met de client-id en het clientgeheim, kunt u deze genereren via uw [!DNL Bynder] -account. De client-id en het clientgeheim worden gegenereerd wanneer u een app maakt in [!DNL Bynder] .

Voor instructies voor het creëren van een app in [!DNL Bynder], zie [ Oauth 2.0 Apps ](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/) in de [!DNL Bynder] documentatie.

>[!NOTE]
>
>* Wanneer u de app maakt in [!DNL Bynder] , voert u het volgende in als de `redirect uri` :
>
>   * US-cluster: `https://app.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * EU-cluster: `https://app-eu.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Azure-cluster: `https://app-az.workfrontfusion.com/oauth/cb/workfront-bynder`
>* Bynder gebruikt de code van de Toekenning van de Vergunning / vernieuw symbolische subsidietype. Dit is het enige subsidietype dat de schakelaar van de Bynder van de Fusie gebruikt.

## [!DNL Bynder] modules en hun velden

Wanneer u [!DNL Bynder] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Bynder] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Handelingen](#actions)
* [Zoekopdrachten](#searches)
* [Triggers](#triggers)

### Handelingen

* [[!UICONTROL Add a tag to assets]](#add-a-tag-to-assets)
* [[!UICONTROL Add assets to a collection]](#add-assets-to-a-collection)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download asset]](#download-asset)
* [[!UICONTROL Read asset metadata]](#read-asset-metadata)
* [[!UICONTROL Remove a tag] van elementen](#remove-a-tag-from-assets)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Upload asset]](#upload-asset)

#### [!UICONTROL Add a tag to assets]

Deze actiemodule voegt een tag toe aan een of meer elementen

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>Voer de id in van de tag die u aan de elementen wilt toevoegen of wijs deze toe.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Voor elk element dat u wilt labelen, klikt u op <strong>[!UICONTROL Add item]</strong> en voert u de element-id in of wijst u deze toe.</p> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL Add assets to a collection]

Deze actiemodule voegt een of meer elementen toe aan een verzameling.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Ga of kaart identiteitskaart van de inzameling in waar u activa wilt toevoegen.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Voor elk element dat u aan de verzameling wilt toevoegen, klikt u op <strong>[!UICONTROL Add item]</strong> en voert u de element-id in of wijst u deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Bynder] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Bynder] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

De module keert een statuscode, samen met de kopballen en het lichaam van de API vraag terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://{your-bynder-domain}/api/{api-version}/</code> .</td> 
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

#### [!UICONTROL Download asset]

Deze actiemodule downloadt één element.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Voer de id in van het element dat u wilt downloaden of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset version]</td> 
   <td> <p>Voer de versie in van het element dat u wilt downloaden of wijs deze versie toe. Laat het veld leeg als u de meest recente versie van het element wilt downloaden.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read asset metadata]

In deze actiemodule worden de metagegevens van een element gelezen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Voer de id in van het element waarvoor u metagegevens wilt ophalen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a tag from assets]

Deze actiemodule verwijdert een tag uit een of meer elementen

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>Voer de id in van de tag die u uit de elementen wilt verwijderen of wijs deze toe.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Voor elk element waarvan u een tag wilt verwijderen, klikt u op <strong>[!UICONTROL Add item]</strong> en voert u de element-id in of wijst u deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection]

Deze actiemodule verwijdert een of meer elementen uit een verzameling.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Voer de id van de verzameling in of wijs deze toe op de plaats waar u elementen wilt verwijderen.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Voor elk element dat u uit de verzameling wilt verwijderen, klikt u op <strong>[!UICONTROL Add item]</strong> en voert u de element-id in of wijst u deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

In deze actiemodule worden de metagegevens van een bestaand element bijgewerkt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Voer de id in van het element waarvoor u metagegevens wilt bijwerken of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Selecteer de velden waarvoor u informatie wilt invoeren, en voer vervolgens de gegevens in of wijs de gegevens toe waarmee u de metagegevens wilt bijwerken naar die velden. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metaproperties]</p> </td> 
   <td>Selecteer de opties die u wilt bijwerken en voer de informatie in of wijs deze toe aan die eigenschappen. Metaeigenschappen zijn informatie over het element die geen specifieke velden in het element vertegenwoordigen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload asset]

Deze actiemodule uploadt één element.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save as]</td> 
   <td> <p>Selecteer hoe u het bestand dat u uploadt, wilt opslaan.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL New asset]</strong> </p> <p>Selecteer de velden en metaeigenschappen waarvoor u informatie wilt invoeren en voer de informatie in die velden in.</p> <p>Voer de id in van het merk dat u voor het geüploade element wilt gebruiken of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL New asset version]</strong> </p> <p>Voer de id in van het element waarvoor u een nieuwe versie uploadt.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asynchronous file upload]</td> 
   <td>Schakel deze optie in wanneer u grote bestanden uploadt. Zo voorkomt u dat grote bestanden de uitvoering van scenario's blokkeren.</td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

* [[!UICONTROL List record]](#list-record)
* [[!UICONTROL Search Assets]](#search-assets)

#### [!UICONTROL List record]

Deze zoekmodule haalt alle items van een bepaald type op.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt weergeven.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Read all collections]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read information about all tags]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read all assets of a collection]</strong> </p> <p>Voer de id in van de verzameling waarvan u de elementen wilt weergeven of wijs deze toe.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u in de uitvoer van de module wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal activa in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Assets]

Deze zoekmodule zoekt naar elementen op basis van criteria die u opgeeft.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td> <p>Voer de zoekcriteria in. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>Selecteer het veld dat u in de zoekopdracht wilt gebruiken</p> </li> 
     <li> <p><strong>[!UICONTROL Logical Operator]</strong> </p> <p>Selecteer de operator die u in de zoekopdracht wilt gebruiken.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Voer de waarde in die u in het geselecteerde veld wilt zoeken of wijs deze toe. Het waardetype moet hetzelfde zijn als het gegevenstype van het geselecteerde veld. </p> <p>Voor meer informatie over gegevenstypes, zie {de gegevenstypes van 0} Punt </a>.<a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref"></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Selecteer of u het eerste overeenkomende element of alle overeenkomende elementen wilt retourneren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Selecteer het veld waarop u wilt sorteren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort Direction]</td> 
   <td> <p>Selecteer of u oplopend of aflopend wilt sorteren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u in de uitvoer van de module wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal activa in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Triggers

#### [!UICONTROL Watch assets]

Deze triggermodule start een scenario wanneer een element wordt gemaakt of bijgewerkt.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Bynder] met [!DNL Workfront Fusion] </a> in dit artikel voor instructies over het verbinden van uw [!DNL Bynder] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Het type Event</td>
    <td>Selecteer of u het scenario wilt beginnen wanneer een nieuw element wordt gecreeerd of wanneer een bestaand element wordt bijgewerkt.</td>
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL Collections]</td>
   <td> <p>Selecteer de verzameling die u wilt controleren voor nieuwe elementen. Als u alle verzamelingen wilt bekijken, laat u dit veld leeg.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Uitvoer</td>
    <td>Selecteer de velden die u in de uitvoer wilt opnemen.</td>
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Limit]</td>

<td> <p>Ga het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

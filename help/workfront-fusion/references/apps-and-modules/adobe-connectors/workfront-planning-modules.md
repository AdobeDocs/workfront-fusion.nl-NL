---
title: Adobe Workfront-planningsmodules
description: Met de  [!DNL Adobe Workfront Planning]  modules, kunt u een  [!DNL Adobe Workfront Fusion]  scenario beginnen dat op gebeurtenissen in uw  [!DNL Adobe]  wordt gebaseerd de Plannende rekening van Workfront, overeenkomsten en andere verslagen tot stand brengen, lezen of bijwerken, onderzoek naar verslagen gebruikend criteria u plaatst, en documenten uploadt.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: cf2a4515ecd5e239e3370a6a0a3ffe70ecce3770
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# [!DNL Adobe Workfront Planning] modules

Met de [!DNL Adobe Workfront Planning] -modules kunt u een scenario activeren wanneer gebeurtenissen plaatsvinden in Workfront Planning. U kunt ook records maken, lezen, bijwerken en verwijderen of een aangepaste API-aanroep naar uw [!DNL Adobe Workfront Planning] -account uitvoeren.

## Toegangsvereisten

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
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
   </td>  
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] [!DNL Adobe Workfront] -abonnement hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Informatie over Adobe Workfront Planning API

De schakelaar van de Planning van Adobe Workfront gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://{connection.host}/maestro/api/{{common.maestroApiVersion}}/</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken met [!DNL Adobe Workfront Planning]

U kunt rechtstreeks vanuit een [!DNL Workfront Fusion] -module verbinding maken met uw [!DNL Workfront Planning] -account.

1. Klik in een willekeurige [!DNL Adobe Workfront Planning] -module op **[!UICONTROL Add]** naast het vak Verbinding.

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
          <td role="rowheader">[!UICONTROL Environment]</td>
          <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Type]</td>
          <td>Geef op of u verbinding wilt maken met een serviceaccount of een persoonlijke account.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(Optioneel)</p></td>
          <td>Voer uw [!DNL Adobe] [!UICONTROL Client ID] in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Optioneel)</p></td>
          <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(Optioneel)</p></td>
          <td>Voer de URL in die uw instantie van Workfront gebruikt om deze verbinding te verifiëren. <p>De standaardwaarde is <code>https://oauth.my.workfront.com/integrations/oauth2</code> .</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>Voer het hostvoorvoegsel in.<p>De standaardwaarde is <code>origin-</code> .</p>
        </tr>
      </tbody>
    </table>
1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## [!DNL Adobe Workfront Planning] modules en hun velden

### Triggers

#### Gebeurtenissen bekijken

Deze triggermodule start een scenario wanneer een record, recordtype of werkruimte wordt gemaakt, bijgewerkt of verwijderd in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Selecteer de webhaak die u wilt gebruiken of klik op Toevoegen om een nieuwe te maken.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>Selecteer of u records, recordtypen of werkruimten wilt bekijken.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Selecteer of u naar het oude of het nieuwe frame wilt kijken.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Trigger een scenario wanneer het verslag <b> in </b> een bepaalde waarde verandert.</p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Trigger een scenario wanneer het verslag <b> van </b> een bepaalde waarde verandert.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Als u records bekijkt, selecteert u de Workspace die u wilt controleren voor records.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Als u records wilt bekijken, selecteert u het type record waarop u wilt letten.</td>
    </tr>
    </tr>
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>U kunt filters instellen om alleen te controleren op records die voldoen aan de criteria die u selecteert.</p> <p>Voer voor elk filter het veld in dat door het filter moet worden geëvalueerd, de operator en de waarde die door het filter moet worden toegestaan. U kunt meer dan één filter gebruiken door EN regels toe te voegen.</p> <p>Opmerking: u kunt filters in bestaande [!DNL Workfront] -webhaken niet bewerken. Als u verschillende filters wilt instellen voor [!DNL Workfront] -gebeurtenisabonnementen, verwijdert u de huidige webhaak en maakt u een nieuwe.</p> <p>Voor meer informatie over gebeurtenisfilters, zie <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref"> de abonnementfilters van de Gebeurtenis in [!DNL Workfront] &gt; [!UICONTROL Watch Events] modules </a> in het de modulesartikel van Workfront.</p> </td> 
     </tr> 
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>Selecteer of u op nieuw wilt letten. bijgewerkte, nieuwe en bijgewerkte of verwijderde records.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Exclude updates made by this connection]</p>
      </td>
      <td>Schakel deze optie in om te voorkomen dat het scenario wordt geactiveerd wanneer een wijziging wordt aangebracht door de verbinding die door deze module wordt gebruikt. Hierdoor wordt voorkomen dat een andere instantie van het scenario wordt geactiveerd wanneer dit scenario een activerende actie uitvoert.</td> 
      </tr>
  </tbody>
</table>

### Handelingen

* [Een recordtype verwijderen](#delete-a-record-type)
* [Een aangepaste AI-aanroep maken](#make-a-custom-api-call)

#### Een recordtype verwijderen

Deze actiemodule schrapt één enkel verslagtype in de Planning van Workfront door zijn identiteitskaart

>[!WARNING]
>
>Als u een recordtype verwijdert in de Workfront-planning, worden ook alle records in de tabel met recordtypen verwijderd.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Voer de id in van het veld dat u wilt verwijderen of wijs deze toe.</td> 
      </tr>
  </tbody>
</table>

#### Een aangepaste API-aanroep maken

Deze module maakt een aangepaste API-aanroep naar de [!DNL Adobe Workfront Planning] API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Een pad invoeren ten opzichte van <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP-aanvraagmethoden in [!DNL Adobe Workfront Fusion]</a> voor meer informatie.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Voor elk sleutel/waardepaar dat u aan het vraagkoord wilt toevoegen, <b> toevoegen punt </b> klikt en de sleutel en de waarde ingaan.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

<!--
### Searches

#### Search records

This action module retrieves a list of records based on criteria you specify.

-->

### Niet gecategoriseerd


#### Een record maken

Met deze actie maakt u één record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Voer het type record in dat u wilt maken of wijs dit toe. Beschikbare recordtypen zijn gebaseerd op uw Workfront-planningsaccount.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Overige velden</p>
      </td>
      <td>Deze velden zijn gebaseerd op het geselecteerde recordtype.</td> 
      </tr>
     <tr>
  </tbody>
</table>

### Een record verwijderen

Deze actiemodule schrapt het gespecificeerde verslag in de Planning van Workfront.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Voer de id in van de record die u wilt verwijderen of wijs deze toe.</td> 
      </tr>
  </tbody>
</table>

<!--

### Get all records

This action module retrieves all records from an [!DNL Adobe Workfront Planning] account.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

-->

### Een record ophalen

Deze actiemodule haalt één record op uit [!DNL Adobe Workfront Planning] , opgegeven door de id.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record ID]</td>
      <td>Voer de id in of wijs deze toe aan de record die u wilt ophalen.</td>
    </tr>
  </tbody>
</table>

### Records ophalen op recordtype

Deze actiemodule wint alle verslagen van het gespecificeerde type terug.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Selecteer of wijs de werkruimte toe die de verslagen bevat u wilt terugwinnen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Selecteer het type record dat u wilt ophalen.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tbody>
</table>

### Recordtypen ophalen

Deze actiemodule haalt een lijst met recordtypen op in een [!DNL Adobe Workfront Planning] -account.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
  </tbody>
</table>

### Record bijwerken

Deze actie werkt één enkel verslag in de Planning van Workfront bij.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" > Verbinding maken met [!DNL Adobe Workfront Planning]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning] .</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Typ of wijs het type record toe dat u wilt bijwerken. Beschikbare recordtypen zijn gebaseerd op uw Workfront-planningsaccount.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Overige velden</p>
      </td>
      <td>Deze velden zijn gebaseerd op het geselecteerde recordtype.</td> 
      </tr>
     <tr>
  </tbody>
</table>

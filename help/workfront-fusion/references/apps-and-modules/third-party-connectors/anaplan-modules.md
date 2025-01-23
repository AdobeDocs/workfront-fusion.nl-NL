---
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Anaplan gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1616'
ht-degree: 0%

---

# [!DNL Anaplan] Modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Anaplan] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Vereisten

Voordat u de [!DNL Anaplan] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!UICONTROL Anaplan] account hebben.
* U moet Workspaces, Models en andere [!DNL Anaplan] -objecten in uw [!UICONTROL Anaplan] -account configureren voordat [!DNL Workfront Fusion] met deze objecten kan communiceren.

## API-informatie voor Anaplan

De Anaplan schakelaar gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://api.anaplan.com/2/0/
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.11.5/td&gt; 
 </tbody> 
</table>

## Verbinden [!DNL Anaplan] met [!DNL Workfront Fusion] {#connect-anaplan-to-workfront-fusion}

Verbinding maken voor uw [!DNL Anaplan] -modules:

1. Klik op **[!UICONTROL Add]** naast het vak [!UICONTROL Connection] .
1. Selecteer het verbindingstype.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>Voor het maken van een verbinding met [!DNL Anaplan] [!UICONTROL Basic] zijn alleen een e-mailadres en wachtwoord vereist. </p> <p>Voer een naam voor de verbinding in en voer vervolgens uw e-mailadres en het wachtwoord van uw [!DNL Anaplan] -account in.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>Een [!DNL Anaplan] [!UICONTROL CA Certificate] -verbinding vereist een [!UICONTROL Certificate Key] , [!UICONTROL Encoded Data] en [!UICONTROL Encoded Signed Data] . U kunt deze genereren in uw [!DNL Anaplan] -account. Zie de documentatie van [!DNL Anaplan] voor instructies.</p> <p>Voer een naam voor de verbinding in en voer vervolgens de [!UICONTROL Certificate Key] , [!UICONTROL Encoded Data] en [!UICONTROL Encoded Signed Data] in die u in uw [!DNL Anaplan] -account hebt gegenereerd.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## [!DNL Anaplan] modules en hun velden

Wanneer u [!DNL Anaplan] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Anaplan] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

#### [!DNL Watch records]

Deze triggermodule start een scenario wanneer een record van het gekozen type wordt gemaakt of bijgewerkt.

>[!NOTE]
>
>Deze module keert de gegevens van nieuwe verslagen terug. De gegevens van gewijzigde bestaande records worden niet geretourneerd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Anaplan] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type object dat moet worden gecontroleerd</td> 
   <td>Selecteer het type item dat u wilt controleren. Het scenario begint wanneer dit type record wordt gemaakt of bijgewerkt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">&lt;Object&gt;-id</td> 
   <td>Voer de id in van het object in Anaplan, zoals een model of module, dat is gekoppeld aan de objecten die u wilt controleren</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limiet</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module aan [actie] tijdens elke cyclus van de scenariouitvoering wilt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Create a list item]](#create-a-list-item)
* [[!UICONTROL Make a custom API Call]](#make-a-custom-api-call)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Run an action]](#run-an-action)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a file]](#upload-a-file)

#### [!UICONTROL Create a list item]

Deze actiemodule voegt een nieuw punt aan een lijst in Anaplan toe.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Connection]</td>
        <td>Zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Anaplan] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td>
    </tr>
    <tr>
        <td>[!UICONTROL Workspace ID]</td>
        <td>Selecteer of wijs identiteitskaart van Anaplan Workspace toe die de lijst bevat waar u een punt wilt toevoegen.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Model ID]</td>
        <td>Selecteer of wijs identiteitskaart van het Model toe dat de lijst bevat waar u een punt wilt toevoegen.</td>
    </tr>
    <tr>
        <td>[!UICONTROL List ID]</td>
        <td>Selecteer of wijs identiteitskaart van de Lijst toe waar u een punt wilt tot stand brengen.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Name]</td>
        <td>Voer een naam in voor het nieuwe item.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Code]</td>
        <td>Voer de code voor het nieuwe item in. Codes zijn door de gebruiker gegenereerde codes waarmee u onderscheid kunt maken tussen regelitems met dezelfde naam.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Parent]</td>
        <td>Voer de naam in van het bovenliggende item waarop u het nieuwe item wilt maken.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Properties]</td>
        <td>Als de lijst waaraan u een item wilt toevoegen aangepaste eigenschappen heeft, selecteert u de eigenschappen waarvoor u waarden wilt toevoegen en voegt u vervolgens de waarden toe.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Subsets]</td>
        <td>Als de lijst waaraan u items wilt toevoegen aangepaste subsets bevat, selecteert u de subsets waaraan u het item wilt toevoegen en selecteert u <b>[!UICONTROL Yes]</b> om het nieuwe item aan die subset toe te voegen.</td>
    </tr>
</table>

#### [!UICONTROL Make a custom API Call]

Met deze module kunt u een aangepaste API-aanroep naar de [!DNL Anaplan] API uitvoeren.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Anaplan] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Een pad invoeren ten opzichte van <code>https://api.anaplan.com/2/0/</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Voer de queryreeks voor de aanvraag in.</p> </td> 
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

#### [!UICONTROL Delete a record]

Met deze actiemodule verwijdert u een bestaande record.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Anaplan] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecteer of wijs identiteitskaart van Anaplan Workspace toe die het voorwerp bevat u wilt schrappen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>Voer de id in van het model dat het object bevat dat u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwijderen</td> 
   <td> <p>Selecteer het type object dat u wilt verwijderen.</p> 
    <ul> 
     <li> <p><b> Actie </b> </p> <p>Selecteer of wijs de actie toe om te schrappen.</p> </li> 
     <li> <p><b> het punt van de Lijst </b> </p> <p>Selecteer de lijst waarvan u een item wilt verwijderen en voer de id of de code in van het item dat u wilt verwijderen.</p>  </li> 
     <li> <p><b>[!UICONTROL File]</b> </p> <p>Selecteer of wijs het bestand toe dat u wilt verwijderen.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Deze actiemodule leest één record.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Anaplan] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecteer het type record dat u wilt lezen.</p> 
    <ul> 
     <li> <p><b> Model </b> </p> <p>Selecteer of wijs identiteitskaart van het Model toe u wilt lezen</p> </li> 
     <li> <p><b> Modellijst </b> </p> <p>Selecteer of wijs identiteitskaart van Workspace en Model toe die de Lijst bevatten u wilt lezen, dan de Lijst selecteren. Selecteer in het veld [!UICONTROL Data type] of u gegevens of metagegevens wilt lezen.</p> </li> 
     <li> <p><b> Modelversie </b> </p> <p>Selecteer of wijs identiteitskaart van het Model toe u wilt lezen.</p> </li> 
     <li> <p><b> Gebruiker </b> </p> <p>Selecteer of u gegevens wilt retourneren over de eigenaar van de account die wordt gebruikt, of een andere gebruiker. Als u een andere gebruiker selecteert, selecteert u de naam van de gebruiker.</p> </li> 
     <li> <p><b> Workspace </b> </p> <p>Selecteer of wijs identiteitskaart van Workspace toe u wilt lezen.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Run an action]

Met deze actiemodule kunt u een handeling importeren, exporteren, verwijderen of verwerken.

<table style="table-layout:auto"> 
     <col/>
     <col/>
     <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Zie <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect Anaplan to Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Workspace ID]</td>
        <td>Selecteer of wijs identiteitskaart van [!DNL Anaplan] Workspace toe waar u de actie wilt uitvoeren</td>
      </tr>
      <tr >
        <td role="rowheader">[!UICONTROL Model ID]</td>
        <td>Selecteer of wijs identiteitskaart van het Model toe waar u de actie wilt uitvoeren.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Action type]</td>
        <td>
          <p>Selecteer de handeling die u wilt uitvoeren</p>
            <ul>
              <li>
                <p><b>[!UICONTROL Delete]</b>
                </p>
                <p>Voer de id in van de handeling die u wilt verwijderen of wijs deze toe.</p>
              </li>
              <li>
                <p><b>[!UICONTROL Export]</b>
                </p>
                <p>Voer de id in van de exportdefinitie die u wilt gebruiken of wijs deze toe. U kunt exporteren naar de volgende bestandsindelingen:</p>
                  <ul>
                    <li>
                      <p>XLS</p>
                    </li>
                    <li>
                      <p>XLSX</p>
                    </li>
                    <li>
                      <p>CSV</p>
                    </li>
                  </ul>
                </li>
                <li>
                  <p><b>[!UICONTROL Import] </b>
                  </p>
                  <p style="font-weight: normal;">Voer de id in van de importdefinitie die u wilt gebruiken of wijs deze toe.</p>
                </li>
                <li>
                 <p><b>[!UICONTROL Process]</b>
                 </p>
                  <p>Voer de id in van het proces dat u wilt gebruiken of wijs deze toe. </p>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>


#### [!UICONTROL Update a record]

Deze actiemodule werkt één record bij in [!UICONTROL Anaplan] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Anaplan] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecteer het type record dat u wilt bijwerken.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL List item]</b> </p> <p>Voor gebieden, zie <a href="#create-a-list-item" class="MCXref xref"> een lijstitem </a> in dit artikel creëren.</p> </li> 
     <li> <p><b>[!UICONTROL Module cell data]</b> </p> <p>Wanneer u celgegevens bijwerkt, worden ook alle downstreamberekeningen bijgewerkt die die gegevens gebruiken.</p> <p>Vul de volgende velden in:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Model ID]</b> </p> <p>Selecteer of wijs het Model toe dat de cel bevat u wilt bijwerken.</p> </li> 
       <li> <p><b>[!UICONTROL Module ID]</b> </p> <p>Selecteer of wijs de Module toe die de cel bevat u wilt bijwerken</p> </li> 
       <li> <p><b>[!UICONTROL Line item name]</b> </p> <p>Selecteer of wijs het lijnpunt van de cel toe u wilt bijwerken</p> </li> 
       <li> <p style="font-weight: bold;">[!UICONTROL Dimension ID]</p> <p>Selecteer of wijs de afmeting toe die op het lijnpunt is.</p> 
       <p><b> Opmerking: </b> 
       <ul>
       <li> Dimension key (value) moet <code>dimensionName</code> (next) of <code>dimensionId</code> (ID) zijn.</li>
       <li>De itemsleutel (waarde) moet <code>itemName</code> (tekst), <code>itemCode</code> (tekst) of <code>itemId</code> (id) zijn.</li>
       <li>Dimension- en itemtoetsen moeten van hetzelfde type zijn (tekst of id).
       </ul>
        </p> 
        <p>Zoek naar Dimensionen in de [!DNL Anaplan Anapedia] voor informatie over de afmetingen.</p> </li> 
       <li> <p><b>[!UICONTROL Value]</b> </p> <p>Voer de nieuwe waarde voor de cel in of wijs deze toe.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Model current fiscal year]</b> </p> <p>Voer de Workspace-id en de model-id in van het model waarvoor u het boekjaar wilt bijwerken en voer vervolgens het nieuwe jaar voor het model in of wijs dit toe.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

Deze actiemodule uploadt een bestand naar Anaplan. Het bestand moet al zijn geüpload naar Anaplan. U kunt deze module gebruiken om het aan extra plaatsen binnen Anaplan te uploaden.
<table style="table-layout:auto">
<col>
<col>
<tbody>
<tr>
<td role="rowheader">[!UICONTROL Connection]</td>
<td>Zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Anaplan] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Workspace ID]</td>
<td>Selecteer of wijs identiteitskaart van [!DNL Anaplan] Workspace toe waar u een dossier wilt uploaden.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Model ID]</td>
<td>Selecteer of wijs identiteitskaart van het Model toe waar u een dossier wilt uploaden.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL File ID]</td>
<td>Selecteer of wijs identiteitskaart van het dossier toe u wilt uploaden.</td>
</tr>
</tbody>
</table>
</div>

### Zoekopdrachten

#### [!UICONTROL Get record]

Deze zoekmodule retourneert alle toegankelijke records van het geselecteerde type.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Anaplan] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Anaplan] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record types]</td> 
   <td> <p>Selecteer het type record dat u wilt ophalen.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Workspaces]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Models]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Line items]</b> </p> <p>Selecteer of wijs identiteitskaart van het Model toe dat de [!DNL line] punten bevat u wilt terugwinnen.</p> </li> 
       <li> <p><b>[!UICONTROL Model lists]</b> </p> <p>Selecteer of wijs identiteitskaart van Workspace en Model identiteitskaart toe die de Modellijsten bevatten u wilt terugwinnen.</p> </li> 
       <li> <p><b>[!UICONTROL Model calendar]</b> </p> <p>Selecteer of wijs identiteitskaart van Workspace toe die de Model kalender bevat u wilt terugwinnen.</p> </li> 
       <li> <p><b>[!UICONTROL Model versions]</b> </p> </li> 
       <li> <p>Selecteer of wijs identiteitskaart van het Model toe dat de Modelversies bevat u wilt terugwinnen.</p> </li> 
       <li> <p><b>[!UICONTROL Users]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Views]</b> </p> <p>Selecteer of u de mening door Module of door Model wilt kiezen, dan selecteer of kaart identiteitskaart van de Module of het Model dat de mening bevat u wilt terugwinnen.</p> </li> 
      </ul> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Return workspace size]</td> 
   <td>Schakel deze optie in om een schatting van de huidige grootte van de werkruimte te retourneren. Deze schatting is gebaseerd op de grootte van alle modules in de werkruimte.</td> 
  </tr> 
 </tbody> 
</table>

---
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Anaplan gebruiken en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1795'
ht-degree: 0%

---

# [!DNL Anaplan] Modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Anaplan] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Voordat u de [!DNL Anaplan] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!UICONTROL Anaplan] account hebben.
* U moet Workspaces, Models, en andere [!DNL Anaplan] voorwerpen in uw [!UICONTROL Anaplan] rekening vormen alvorens Workfront Fusion met hen kan interactie aangaan.

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
   <td>v1.11.5</td> 
 </tbody> 
</table>

## Verbinden [!DNL Anaplan] met Workfront Fusion {#connect-anaplan-to-workfront-fusion}

Verbinding maken voor uw [!DNL Anaplan] -modules:

1. Klik op **[!UICONTROL Add]** naast het vak [!UICONTROL Connection] .
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
          <p>Voer een naam in voor de nieuwe verbinding.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Selecteer of u verbinding maakt met een productieomgeving of niet.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL email]</td>
        <td>
          <p>Voer het e-mailadres voor dit Anaplan-account in</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Password]</td>
        <td>Voer het wachtwoord voor deze Anaplan-account in.</td>
      </tr>
     </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

<!--1. Click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box.
1. Select the connection type.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL Basic] connection requires only an email address and password to create the connection. </p> <p>Enter a name for the connection, then enter your email address and the password of your [!DNL Anaplan] account.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL CA Certificate] connection requires a [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data]. You can generate these in your [!DNL Anaplan] account. For instructions, see the [!DNL Anaplan] documentation.</p> <p>Enter a name for the connection, then enter the [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data] that you generated in your [!DNL Anaplan] account.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.-->

## [!DNL Anaplan] modules en hun velden

Wanneer u [!DNL Anaplan] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Anaplan] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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
   <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td> 
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
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Create a list item]](#create-a-list-item)
* [Een record verwijderen](#delete-a-record)
* [Gegevens exporteren](#export-data)
* [Gegevens importeren](#import-data)
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
        <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td>
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
        <td>Als de lijst waaraan u items wilt toevoegen aangepaste subsets bevat, selecteert u de subsets waaraan u het item wilt toevoegen.</td>
    </tr>
</table>

#### [!UICONTROL Delete a record]

Met deze actiemodule verwijdert u een bestaande record.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td> 
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
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer het type object dat u wilt verwijderen.</p> 
    <ul> 
     <li> <p><b> Actie </b> </p> <p>Selecteer of wijs de actie toe om te schrappen.</p> </li> 
     <li> <p><b> het punt van de Lijst </b> </p> <p>Selecteer de lijst waarvan u een item wilt verwijderen en voer de id of de code in van het item dat u wilt verwijderen.</p>  </li> 
     <li> <p><b>[!UICONTROL File]</b> </p> <p>Selecteer of wijs het bestand toe dat u wilt verwijderen.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Export data]

Deze actiemodule wint gegevens van Anaplan gebruikend de Definities van de Uitvoer terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecteer of wijs identiteitskaart van Anaplan Workspace toe die de gegevens bevat u wilt uitvoeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>Voer de id in van het model dat de gegevens bevat die u wilt exporteren of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Definitie-id exporteren</td> 
   <td> <p>Ga of kaart identiteitskaart van de definitie van de Uitvoer Anaplan in die u wilt gebruiken.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### Gegevens importeren

Deze actiemodule importeert gegevens in Anaplan.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Selecteer of wijs identiteitskaart van Anaplan Workspace toe waar u de gegevens wilt invoeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>Voer de id van het model in of wijs deze toe aan de locatie waar u de gegevens wilt importeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Definitie-id exporteren</td> 
   <td> <p>Ga of kaart identiteitskaart van de definitie van de Invoer Anaplan in die u wilt gebruiken.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make a custom API Call]

Met deze module kunt u een aangepaste API-aanroep naar de [!DNL Anaplan] API uitvoeren.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td> 
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
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion voegt automatisch machtigingsheaders toe.</p> </td> 
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

#### [!UICONTROL Read a record]

Deze actiemodule leest één record.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td> 
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
     <li> <p><b> Mening </b> </p> <p>Selecteer of wijs identiteitskaart van het Model toe dat de mening bevat u wilt lezen.</p> </li> 
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
        <td>Zie [!DNL Anaplan] in dit artikel voor instructies over het maken van een verbinding met <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect Anaplan to Workfront Fusion]</a> .</td>
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
   <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td> 
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
       <li> Dimension-sleutel (waarde) moet <code>dimensionName</code> (Volgende) of <code>dimensionId</code> (ID) zijn.</li>
       <li>De itemsleutel (waarde) moet <code>itemName</code> (tekst), <code>itemCode</code> (tekst) of <code>itemId</code> (id) zijn.</li>
       <li>Dimension- en itemsleutels moeten van hetzelfde type zijn (tekst of id).
       </ul>
        </p> 
        <p>Voor informatie over afmetingen, onderzoek naar Afmetingen in [!DNL Anaplan Anapedia].</p> </li> 
       <li> <p><b>[!UICONTROL Value]</b> </p> <p>Voer de nieuwe waarde voor de cel in of wijs deze toe.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Model current fiscal year]</b> </p> <p>Voer de Workspace-id en de model-id in van het model waarvoor u het boekjaar wilt bijwerken en voer vervolgens het nieuwe jaar voor het model in of wijs dit toe.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload file for action]

Deze actiemodule uploadt een bestaand bestand in Anaplan naar extra locaties in Anaplan.
<table style="table-layout:auto">
<col>
<col>
<tbody>
<tr>
<td role="rowheader">[!UICONTROL Connection]</td>
<td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td>
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
   <td>Voor instructies bij het creëren van een verbinding aan [!DNL Anaplan], zie <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Anaplan] met Workfront Fusion </a> in dit artikel.</td> 
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

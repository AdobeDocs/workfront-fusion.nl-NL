---
title: Adobe Workfront-planningsmodules
description: Met de  [!DNL Adobe Workfront Planning]  modules, kunt u een scenario beginnen van de Fusie van Adobe Workfront dat op gebeurtenissen in uw  [!DNL Adobe]  wordt gebaseerd de Plannende rekening van Workfront, overeenkomsten en andere verslagen tot stand brengen, lezen of bijwerken, onderzoek naar verslagen gebruikend criteria u plaatst, en documenten uploadt.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: a58a6c25751eb10365508c06ab1571ce7652d0c8
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%

---

# [!DNL Adobe Workfront Planning] modules

Met de [!DNL Adobe Workfront Planning] -modules kunt u een scenario activeren wanneer gebeurtenissen plaatsvinden in Workfront Planning. U kunt ook records maken, lezen, bijwerken en verwijderen of een aangepaste API-aanroep naar uw [!DNL Adobe Workfront Planning] -account uitvoeren.

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
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Vereisten

U moet het volgende hebben om tot de Planning van Workfront toegang te hebben:

* Een nieuw Workfront-pakket en -licentie. Workfront Planning is niet beschikbaar voor verouderde Workfront-pakketten of -licenties.
* Een Workfront-planningspakket.
* Het geval van Workfront van uw organisatie moet aan de Verenigde Ervaring van Adobe worden genegeerd.

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

## Workfront-planning verbinden met Workfront Fusion

De Workfront-planningsconnector gebruikt OAuth 2.0 om verbinding te maken met Workfront Planning.

U kunt rechtstreeks vanuit een Workfront Planning Fusion-module een verbinding maken met uw Workfront-planningsaccount.

* [Verbinding maken met Workfront-planning met client-id en clientgeheim](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [Verbinding maken met Workfront-planning via een server-naar-server verbinding](#connect-to-workfront--planning-using-a-server-to-server-connection)

### Verbinding maken met Workfront-planning met client-id en clientgeheim

1. In om het even welke module van de Planning van Adobe Workfront, voegt de klik **naast het gebied van de Verbinding toe.**
1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Selecteer <b> Adobe Workfront auth verbinding </b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Voer een naam in voor de nieuwe verbinding.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw Workfront-client-id in. Dit is te vinden in het gebied van Toepassingen OAuth2 van het gebied van de Opstelling in Workfront. Open de specifieke toepassing waarmee u verbinding maakt om de client-id weer te geven.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw Workfront-clientgeheim in. Dit is te vinden in het gebied van Toepassingen OAuth2 van het gebied van de Opstelling in Workfront. Als u geen geheim van de Cliënt voor uw toepassing OAuth2 in Workfront hebt, kunt u een andere produceren. Raadpleeg de documentatie bij Workfront voor instructies.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>Dit kan de standaardwaarde blijven of u kunt de URL van uw Workfront-instantie invoeren, gevolgd door <code>/integrations/oauth2</code> . <p>Voorbeeld: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>In de meeste gevallen moet deze waarde <code>origin</code> zijn.
      </tr>
    </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

   Als u niet bij de Planning van Workfront wordt aangemeld, wordt u geleid aan een login scherm. Nadat u zich hebt aangemeld, kunt u de verbinding toestaan.

>[!NOTE]
>
>* OAuth 2.0-verbindingen met de Workfront API zijn niet langer afhankelijk van API-sleutels.
>* Als u een verbinding met een Workfront Sandbox-omgeving wilt maken, moet u in die omgeving een OAuth2-toepassing maken en vervolgens de client-id en het clientgeheim gebruiken die door die toepassing zijn gegenereerd in uw verbinding.

### Verbinding maken met Workfront-planning via een server-naar-server verbinding

1. In om het even welke module van de Planning van Adobe Workfront, voegt de klik **naast het gebied van de Verbinding toe.**
1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Selecteer <b> Server-aan-Server verbinding van Adobe Workfront </b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Voer een naam in voor de nieuwe verbinding.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance name]</td>
        <td>
          <p>Voer de naam in van de instantie, ook wel bekend als uw domein.</p><p>Voorbeeld: als de URL <code>https://example.my.workfront.com</code> is, voert u <code>example</code> in.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance lane]</td>
        <td>
          <p>Voer het omgevingstype in waarmee deze verbinding verbinding verbinding maakt.</p><p>Voorbeeld: als de URL <code>https://example.my.workfront.com</code> is, voert u <code>my</code> in.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw Workfront-client-id in. Dit is te vinden in het gebied van Toepassingen OAuth2 van het gebied van de Opstelling in Workfront. Open de specifieke toepassing waarmee u verbinding maakt om de client-id weer te geven.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw Workfront-clientgeheim in. Dit is te vinden in het gebied van Toepassingen OAuth2 van het gebied van de Opstelling in Workfront. Als u geen geheim van de Cliënt voor uw toepassing OAuth2 in Workfront hebt, kunt u een andere produceren. Raadpleeg de documentatie bij Workfront voor instructies.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Voer het bereik in dat van toepassing is op deze verbinding.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>In de meeste gevallen moet deze waarde <code>origin</code> zijn.
      </tr>
    </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

   Als u niet bij de Planning van Workfront wordt aangemeld, wordt u geleid aan een login scherm. Nadat u zich hebt aangemeld, kunt u de verbinding toestaan.

>[!NOTE]
>
>* OAuth 2.0-verbindingen met de Workfront API zijn niet langer afhankelijk van API-sleutels.
>* Als u een verbinding met een Workfront Sandbox-omgeving wilt maken, moet u in die omgeving een OAuth2-toepassing maken en vervolgens de client-id en het clientgeheim gebruiken die door die toepassing zijn gegenereerd in uw verbinding.


## [!DNL Adobe Workfront Planning] modules en hun velden

Wanneer u Workfront-modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen er aanvullende Workfront-velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Acties](#actions)
* [Zoekopdrachten](#searches)
* [Niet gecategoriseerd](#uncategorized)

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
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
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
      <td> <p>U kunt filters instellen om alleen te controleren op records die voldoen aan de criteria die u selecteert.</p> <p>Voer voor elk filter het veld in dat door het filter moet worden geëvalueerd, de operator en de waarde die door het filter moet worden toegestaan. U kunt meer dan één filter gebruiken door EN regels toe te voegen.</p> <p>Opmerking: u kunt filters niet bewerken in bestaande Workfront-websites. Als u verschillende filters wilt instellen voor Workfront-gebeurtenisabonnementen, verwijdert u de huidige webhaak en maakt u een nieuwe.</p> <p>Voor meer informatie over gebeurtenisfilters, zie {de filters van het 0} Abonnement van de Gebeurtenis in Workfront &gt; <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref"> modules [!UICONTROL Watch Events] in het de moduleartikel van Workfront.</a></p> </td> 
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

### Acties

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
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Voer de id in van het recordtype dat u wilt verwijderen of wijs deze toe.</td> 
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
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
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
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion voegt automatisch machtigingsheaders toe.</p>
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


### Zoekopdrachten

#### Zoeken in records

Deze actiemodule wint een lijst van verslagen terug die op criteria worden gebaseerd u specificeert.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Typ of wijs de Workspace toe die de records bevat die u wilt doorzoeken.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Selecteer het recordtype dat u wilt zoeken.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record Fields]</p>
      </td>
      <td>Zoek voor elk veld dat u in de zoekopdracht wilt gebruiken dat veld, selecteer de operator en voer de waarde in die u wilt zoeken of wijs de waarde toe. Veld is beschikbaar op basis van het geselecteerde recordtype.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Condition for filters]</p>
      </td>
      <td>Selecteer de voorwaarde voor uw filters:<ul><li><b>EN</b><p>De module keert verslagen terug die <b> allen </b> van de gebiedswaarden ontmoeten u selecteerde.</p></li><li><b>OF</b><p>De module keert verslagen terug die <b> om het even welke </b> van de gebiedswaarden ontmoeten u selecteerde.</p></li></ul></td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Limit]</p>
      </td>
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
      </tr>
  </tbody>
</table>


### Niet gecategoriseerd


#### Een record maken

Met deze actie maakt u één record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
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
      <td>Voer de waarden in die u voor de nieuwe record wilt gebruiken. Deze velden zijn gebaseerd op het geselecteerde recordtype.</td> 
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
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Voer de id in van de record die u wilt verwijderen of wijs deze toe.</td> 
      </tr>
  </tbody>
</table>

### Een record ophalen

Deze actiemodule haalt één record op uit [!DNL Adobe Workfront Planning] , opgegeven door de id.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
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
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Selecteer of wijs de werkruimte toe die de verslagen bevat u wilt terugwinnen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Selecteer het type record dat u wilt ophalen.</td>
    </tr>
     <!--<tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> -->
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
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Selecteer of wijs de werkruimte toe die de recordtypes bevat u wilt terugwinnen.</td>
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
      <td>Zie [!DNL Adobe Workfront Planning] Verbinding maken met <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Workfront Planning]</a> .</td>
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
      <td>Voer de nieuwe waarden in die u voor de record wilt gebruiken. Deze velden zijn gebaseerd op het geselecteerde recordtype.</td> 
      </tr>
     <tr>
  </tbody>
</table>


## JSONata gebruiken voor leesbare `record-types` uitsplitsing

De volgende uitdrukking JSONata leidt tot een leesbare output van de vraag van de Planning die u de verslag-types indeling geeft. Hierdoor worden de naam van het recordtype, de veldnamen en de namen van veldopties (indien van toepassing) voor de mens leesbaar met een naam en blijft de rest van de structuur intact.

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

Voor informatie bij het gebruiken van modules JSONata, zie [ modules JSONata ](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md).


---
title: Jira-softwaremodules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die  [!DNL Jira]  Software gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 92cac080-d8f6-4770-a6a6-8934538c978b
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1809'
ht-degree: 0%

---

# [!DNL Jira Software] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Jira Software] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

<!-- Bob Fix this compared to original -->

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

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Vereisten

Als u [!DNL Jira] -modules wilt gebruiken, moet u een [!DNL Jira] -account hebben.

## Jira API-informatie

De Jira-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"></td> 
   <td> Jira Cloud</td> 
   <td> Jira Server</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersion</td> 
   <td> 2</td> 
   <td> 2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersionAgile</td> 
   <td> 1,0 </td> 
   <td> 1,0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>1.7.29.</td> 
   <td>1.0.19.</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Jira Software] met [!DNL Workfront Fusion]

De verbindingsmethode is gebaseerd op het feit of u [!DNL Jira Cloud] of [!DNL Jira Server] gebruikt.

* [Verbind  [!DNL Jira Cloud]  met de Fusie van Workfront](#connect-jira-cloud-to-workfront-fusion)
* [Verbind  [!DNL Jira Server]  met  [!DNL Workfront Fusion]](#connect-jira-server-to-workfront-fusion)

### Verbinden [!DNL Jira Cloud] met [!DNL Workfront Fusion]

Verbinden [!DNL Jira Cloud] met [!DNL Workfront Fusion]

Als u [!DNL Jira Software] wilt verbinden met [!DNL Workfront Fusion] , moet u een API-token maken en deze samen met de Service URL en de gebruikersnaam invoegen in het veld [!UICONTROL Create a connection] in [!DNL Workfront Fusion] .

#### Een API-token maken in [!DNL Jira]

1. Ga naar [ https://id.atlassian.com/manage/api-tokens ](https://id.atlassian.com/manage/api-tokens) en login.
1. Klik op **[!UICONTROL Create API token]**.
1. Typ een naam voor het teken, zoals *de Fusie van Workfront*.
1. Kopieer het token met de knop **[!UICONTROL Copy to clipboard]** .

   >[!IMPORTANT]
   >
   >U kunt het token niet meer weergeven nadat u dit dialoogvenster hebt gesloten.
1. Sla het gegenereerde token op een veilige plaats op.
1. Ga met [ verder vormen het  [!DNL Jira]  API teken in  [!DNL Workfront Fusion]](#configure-the-jira-api-token-in-workfront-fusion).

#### De API-token [!DNL Jira] configureren in [!DNL Workfront Fusion]

1. Voeg in [!DNL Workfront Fusion] een [!DNL Jira] -module toe aan een scenario om het vak **[!UICONTROL Create a connection]** te openen.
1. Geef de volgende informatie op:

   * **[!UICONTROL Service URL]:** dit is de basis-URL die u gebruikt om toegang te krijgen tot uw Jira-account. Voorbeeld: `yourorganization.atlassian.net`
   * **[!UICONTROL Username]**
   * **[!UICONTROL API token]:** dit is het API teken u in [ creeerde een API teken in  [!DNL Jira]](#create-an-api-token-in-jira) sectie van dit artikel.

1. Klik op [!UICONTROL Continue] om de verbinding te maken en terug te keren naar de module.

### Verbinden [!DNL Jira Server] met [!DNL Workfront Fusion]

<!--
<p style="color: #ff1493;">Becky: Find out and document how to find these things</p>
-->

Als u een verbinding tussen [!DNL Workfront Fusion] en [!DNL Jira Server] wilt autoriseren, hebt u uw gebruikersnaam, persoonlijke sleutel en service-URL nodig. Mogelijk moet u contact opnemen met de [!DNL Jira] -beheerder voor deze informatie.

* [Produceer Openbare en Privésleutels voor uw  [!DNL Jira]  verbinding](#generate-public-and-private-keys-for-your-jira-connection)
* [Vorm de cliënttoepassing als consument in  [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)
* [Creeer een verbinding aan  [!DNL Jira]  Server of het Centrum van Gegevens van Jira in  [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Openbare en persoonlijke sleutels voor uw [!DNL Jira] -verbinding genereren

Als u een persoonlijke sleutel voor uw [!DNL Workfront Fusion Jira] -verbinding wilt verkrijgen, moet u openbare en persoonlijke sleutels genereren.

1. Voer in uw terminal de volgende `openssl` -opdrachten uit.

   * `openssl genrsa -out jira_privatekey.pem 1024`

     Met deze opdracht wordt een persoonlijke sleutel van 1024 bits gegenereerd.

   * `openssl req -newkey rsa:1024 -x509 -key jira_privatekey.pem -out jira_publickey.cer -days 365`

     Met deze opdracht maakt u een X509-certificaat.

   * `openssl pkcs8 -topk8 -nocrypt -in jira_privatekey.pem -out jira_privatekey.pcks8`

     Met deze opdracht haalt u de persoonlijke sleutel (PKCS8-indeling) uit naar de `jira_privatekey.pcks8`
bestand.

   * `openssl x509 -pubkey -noout -in jira_publickey.cer  > jira_publickey.pem`

     Met deze opdracht haalt u de openbare sleutel uit het certificaat uit naar het `jira_publickey.pem` -bestand.

     >[!NOTE]
     >
     >Als u Windows gebruikt, moet u de openbare sleutel mogelijk handmatig in het `jira_publickey.pem` -bestand opslaan:
     >
     >1. In uw terminal, stel het volgende bevel in werking:
     >   
     >   `openssl x509 -pubkey -noout -in jira_publickey.cer`
     >   
     >1. Kopieer de terminaluitvoer (inclusief `-------BEGIN PUBLIC KEY--------` en `-------END PUBLIC KEY--------` )
     >   
     >1. Plak de einduitvoer in een bestand met de naam `jira_publickey.pem` .


1. Ga aan [ verder vormen cliëntapp als consument in  [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)

#### De client-app configureren als een consument in [!DNL Jira]

1. Meld u aan bij uw [!DNL Jira] -instantie.
1. Klik in het linkernavigatievenster op **[!UICONTROL [!DNL Jira] Settings]** ![](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **[!UICONTROL Applications]** > **[!UICONTROL Application links]** .
1. Typ in het veld **[!UICONTROL Enter the URL of the application you want to link]**

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. Klik op **[!UICONTROL Create new link]**. Negeer het foutbericht &quot;Er is geen reactie ontvangen van de URL die u hebt ingevoerd&quot;.
1. Voer in het venster **[!UICONTROL Link applications]** waarden in de velden **[!UICONTROL Consumer key]** en **[!UICONTROL Shared secret]** in.

   U kunt de waarden voor deze velden kiezen.

1. Kopieer de waarden van de velden **[!UICONTROL Consumer key]** en **[!UICONTROL Shared secret]** naar een beveiligde locatie.

   U zult deze waarden later in het configuratieproces vereisen.

1. Vul de URL-velden als volgt in:

   | Veld | Beschrijving |
   |---|---|
   | [!UICONTROL Request Token URL] | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | [!UICONTROL Authorization URL] | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | [!UICONTROL Access Token URL] | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. Schakel het selectievakje **[!UICONTROL Create incoming link]** in.
1. Klik op **[!UICONTROL Continue]**.
1. Vul in het venster **[!UICONTROL Link applications]** de volgende velden in:

   <table style="table-layout:auto"> 
    <col data-mc-conditions=""> 
    <col data-mc-conditions=""> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Consumer Key]</p> </td> 
      <td> Plak in de consumentensleutel die u naar een beveiligde locatie hebt gekopieerd.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer name]</td> 
      <td>Voer een naam van uw keuze in. Deze naam is voor uw eigen referentie.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Public key]</td> 
      <td>Plak de openbare sleutel uit het <code>[!DNL jira_publickey.pem]</code> -bestand.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]**.
1. Ga aan [ voort creeer een verbinding aan  [!DNL Jira Server]  of  [!DNL Jira Data Center]  binnen  [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Een verbinding maken met [!DNL Jira Server] of [!DNL Jira Data Center] in [!DNL Workfront Fusion]

>[!NOTE]
>
>Gebruik de app [!DNL Jira Server] om verbinding te maken met [!DNL Jira Server] of [!DNL Jira Data Center] .

1. Klik in een willekeurige [!DNL Jira Server] -module in [!DNL Workfront Fusion] op **[!UICONTROL Add]** naast het [!UICONTROL connection] -veld.
1. Vul in het deelvenster [!UICONTROL Create a connection] de volgende velden in:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Geef een naam op voor de verbinding</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer Key]</td> 
      <td>Plak in de sleutel van de consument die u aan een veilige plaats in <a href="#configure-the-client-app-as-a-consumer-in-jira" class="MCXref xref"> kopieerde vorm cliënt app als consument in [!DNL Jira]</a></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Private Key]</td> 
      <td>Plak in de privé sleutel van het <code>[!DNL jira_privatekey.pcks8]</code> dossier u in <a href="#generate-public-and-private-keys-for-your-jira-connection" class="MCXref xref"> creeerde produceert Openbare en Privé sleutels voor uw [!DNL Jira] verbinding </a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Service URL]</td> 
      <td>Voer de URL van de [!DNL Jira] -instantie in. Voorbeeld: <code>yourorganization.atlassian.net</code></td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL Jira Software] modules en hun velden

Wanneer u [!DNL Jira Software] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Jira Software] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

#### [!UICONTROL Watch for records]

Deze triggermodule start een scenario wanneer een record wordt toegevoegd, bijgewerkt of verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer de webhaak die u wilt gebruiken om te controleren op records. </p> <p>Een nieuwe webhaak toevoegen:</p> 
    <ol> 
     <li value="1">Klikken <strong>[!UICONTROL Add]</strong></li> 
     <li value="2">Voer een naam in voor de webhaak.</li> 
     <li value="3"> <p>Selecteer de verbinding die u voor uw webhaak wilt gebruiken. </p> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </li> 
     <li value="4"> <p>Selecteer het recordtype waarop u de software wilt letten:</p> 
      <ul> 
       <li>[!UICONTROL Comment] </li> 
       <li>[!UICONTROL Issue]</li> 
       <li>[!UICONTROL Project] </li> 
       <li>[!UICONTROL Sprint]</li> 
      </ul> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Add issue to sprint]](#add-issue-to-sprint)
* [[!UICONTROL Create a Record]](#create-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Update a record]](#update-a-record)

#### [!UICONTROL Add issue to sprint]

Deze actiemodule voegt een of meer uitgaven aan een sprint toe.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sprint ID]</td> 
   <td>Voer de Sprint-id in van de sprint waaraan u een uitgave wilt toevoegen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID or Keys]</td> 
   <td>Voeg een Issue ID of Key toe voor elke uitgave die u aan de sprint wilt toevoegen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Record]

Deze actiemodule maakt een nieuwe record in Jira.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat de module moet maken. Wanneer u een recordtype selecteert, worden andere velden die specifiek zijn voor dat recordtype, weergegeven in de module.</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Jira Software] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Jira Software] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Een pad invoeren ten opzichte van<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP-aanvraagmethoden in [!DNL Adobe Workfront Fusion]</a> voor meer informatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Hiermee voegt u de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a record]

Deze actiemodule verwijdert een bepaalde record.

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat de module moet verwijderen. </p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID or Key]</td> 
   <td>Voer de id of sleutel in of wijs deze toe aan de record die u wilt verwijderen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

Deze actiemodule downloadt een bepaalde bijlage.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van de bijlage die u wilt downloaden of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Deze actiemodule leest gegevens uit één record in [!DNL Jira Software] .

U geeft de id van de record op.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type [!DNL Jira] record dat u in de module wilt lezen.</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL User]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de uitvoer die u wilt ontvangen. Uitvoeropties zijn beschikbaar op basis van het type record dat is geselecteerd in het veld "[!UICONTROL Record Type]".</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Voer de unieke [!DNL Jira Software] -id in of wijs deze toe aan de record die u wilt lezen in de module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Deze actiemodule werkt een bestaand record bij, zoals een uitgave of project.

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat de module moet bijwerken. Wanneer u een recordtype selecteert, worden andere velden die specifiek zijn voor dat recordtype, weergegeven in de module.</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Transition issue]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID or Key]</td> 
   <td>Voer de id of sleutel in of wijs deze toe aan de record die u wilt bijwerken.</td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search for records]](#search-for-records)

#### [!UICONTROL List records]

Deze zoekmodule haalt alle items van een specifiek type op die overeenkomen met uw zoekopdracht

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat in de module moet worden vermeld. Wanneer u een recordtype selecteert, worden andere velden die specifiek zijn voor dat recordtype, weergegeven in de module.</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint issue]</li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Max Results]</p> </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugwinnen.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Enter or map the ID of the first item you want to retrieve details for. This is a way to paginate the records. If you enter the 5000th item as the offset, the module would return items 5000-9999.</td> 
   </tr>
  --> 
 </tbody> 
</table>

#### [!UICONTROL Search for records]

Deze zoekmodule zoekt naar records in een object in [!DNL Jira Software] dat overeenkomt met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL Jira Software] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Jira Software] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record waarnaar de module moet zoeken. Wanneer u een recordtype selecteert, worden andere velden die specifiek zijn voor dat recordtype, weergegeven in de module.</p> 
    <ul> 
     <li>[!UICONTROL Issues]</li> 
     <li> <p>[!UICONTROL Issues by JQL (Jira Query Lanuguage)] </p> <p>Voor meer informatie over JQL, zie <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers."> JQL </a> bij de Atlassiaanse hulpplaats. </p> </li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Project by issue]</li> 
     <li>[!UICONTROL User]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

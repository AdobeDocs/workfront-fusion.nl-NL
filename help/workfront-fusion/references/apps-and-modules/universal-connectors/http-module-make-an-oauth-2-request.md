---
title: HTTP &gt; een OAuth 2.0-aanvraagmodule maken
description: Om een  [!DNL Adobe Workfront Fusion]  HTTP(S) verzoek aan servers te maken die een vergunning OAuth 2.0 vereisen, moet u eerst een verbinding OAuth tot stand brengen. [!DNL Adobe Workfront Fusion]  zorgt ervoor dat alle vraag die met deze verbinding wordt gemaakt de aangewezen vergunningskopballen heeft en automatisch bijbehorende tokens verfrist wanneer vereist.
author: Becky
feature: Workfront Fusion
exl-id: a302a1d4-fddf-4a71-adda-6b87ff7dba4b
source-git-commit: d9d3f21279ba89f544adc0ffa9345543907aa777
workflow-type: tm+mt
source-wordcount: '1980'
ht-degree: 0%

---

# [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module

>[!NOTE]
>
>[!DNL Adobe Workfront Fusion] vereist een [!DNL Adobe Workfront Fusion] licentie naast een [!DNL Adobe Workfront] licentie.

Als u een [!DNL Adobe Workfront Fusion] HTTP(S)-aanvraag wilt indienen bij servers die een OAuth 2.0-verificatie vereisen, moet u eerst een OAuth-verbinding maken. [!DNL Adobe Workfront Fusion] zorgt ervoor dat alle vraag die met deze verbinding wordt gemaakt de aangewezen vergunningskopballen heeft en automatisch bijbehorende tokens verfrist wanneer vereist.

[!DNL Workfront Fusion] ondersteunt de volgende OAuth 2.0-verificatiestromen:

* Vergunningscode-stroom
* Impliciete stroom

Andere stromen, zoals de Stroom van de Referenties van het Wachtwoord van de Eigenaar van het Middel en de Stroom van de Referenties van de Cliënt, worden niet automatisch gesteund door deze module.

Voor meer informatie over OAuth 2.0 authentificatie, zie [ het Kader van de Vergunning OAuth 2.0 ](https://tools.ietf.org/html/rfc6749).

>[!NOTE]
>
>Als u verbinding maakt met een product van de Adobe dat momenteel geen speciale aansluiting heeft, raden we u aan de Adobe Authenticator-module te gebruiken.
>
>Voor meer informatie, zie [ module van Adobe Authenticator ](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
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

## Verbinding maken voor een [!DNL OAuth] -aanvraag

* [Algemene instructies voor het maken van een verbinding in HTTP > Een OAuth 2.0-aanvraagmodule maken](#general-instructions-for-creating-a-connection-in-the-http--make-an-oauth-20-request-module)
* [Instructies voor het creëren van een verbinding aan Google in HTTP > [!UICONTROL Make] een OAuth 2.0 verzoekmodule](#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module)
* [Instructies voor verbinding met de Microsoft Graph API via HTTP > Make an OAuth 2.0 request module](#instructions-for-connecting-to-microsoft-graph-api-via-the-http--make-an-oauth-20-request-module)

### Algemene instructies voor het maken van een verbinding in de module [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]

1. Maak een OAuth-client in de [!DNL target] -service waarmee [!DNL Adobe Workfront Fusion] moet communiceren. Deze optie is meestal te vinden in het gedeelte [!UICONTROL Developer] van de opgegeven service.

   1. Wanneer u een client maakt, voert u de juiste URL in het veld `[!UICONTROL Redirect URL]` of `[!UICONTROL Callback URL]` in:

      | Amerika/APAC | `https://app.workfrontfusion.com/oauth/cb/oauth2` |
      |---|---|
      | **EMEA** | `https://app-eu.workfrontfusion.com/oauth/cb/oauth2` |

   1. Nadat u de client hebt gemaakt, geeft de opgegeven service twee toetsen weer: `[!UICONTROL Client ID]` en `[!UICONTROL Client Secret]` . Sommige services roepen deze `[!UICONTROL App Key]` en `[!UICONTROL App Secret]` aan. Sla de sleutel en het geheim op een veilige locatie op, zodat u deze kunt opgeven wanneer u de verbinding maakt in Workfront Fusion.

1. Zoek naar `[!UICONTROL Authorize URI]` en `[!UICONTROL Token URI]` in de API-documentatie van de opgegeven service. Dit zijn URL-adressen waarmee [!DNL Workfront Fusion] communiceert met de [!DNL target] -service. De adressen dienen voor vergunning OAuth.

   >[!NOTE]
   >
   >Als de service impliciete stroom gebruikt, hebt u alleen de `[!UICONTROL Authorize URI]` nodig.

1. (Voorwaardelijk) als de doeldienst werkingsgebied (toegangsrechten) gebruikt, controleer hoe de dienst individueel werkingsgebied scheidt en zorg ervoor u de separator in de geavanceerde montages dienovereenkomstig plaatst. Als het scheidingsteken niet correct is ingesteld, kan de verbinding niet tot stand worden gebracht in [!DNL Workfront Fusion] en ontvangt u een ongeldige bereikfout.
1. Nadat u de bovenstaande stappen hebt uitgevoerd, kunt u de OAuth-verbinding maken in [!DNL Workfront Fusion] . Voeg HTTP > van OAuth 2 aanvraagmodule aan uw scenario toe.
1. Klik in het veld Verbinding van de module op **[!UICONTROL Add]** .

1. Vul de volgende velden in om een verbinding te maken:

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>Voer de naam van de verbinding in.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Environment] </td> 
      <td> <p>Selecteer of u een productie- of niet-productieomgeving gebruikt.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Type] </td> 
      <td> <p>Selecteer of u een serviceaccount of een persoonlijke account gebruikt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>Selecteer de stroom voor het verkrijgen van tokens.</p> 
       <ul> 
        <li><strong>[!UICONTROL Authorization Code]</strong>: Voer de <code>[!UICONTROL Authorize URI]</code> en <code>[!UICONTROL Token URI]</code> in uit de API-documentatie van de service.</li> 
        <li><strong>[!UICONTROL Implicit]</strong>: Voer de <code>[!UICONTROL Authorize URI]</code> in uit de API-documentatie van de service.</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>Afzonderlijk bereik toevoegen. U kunt deze informatie in de bepaalde de ontwikkelaar (API) documentatie van de dienst vinden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>Selecteer door welk bereik de bovenstaande gegevens moeten worden gescheiden. U kunt deze informatie in de bepaalde de ontwikkelaar (API) documentatie van de dienst vinden.</p> <p>Waarschuwing: als het scheidingsteken niet correct is ingesteld, kan de verbinding niet tot stand worden gebracht in [!DNL Workfront Fusion] en ontvangt u een ongeldige bereikfout.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>Voer de client-id in. U hebt de client-id opgehaald toen u een OAuth-client hebt gemaakt in de service waarmee u verbinding wilt maken.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p> Voer het clientgeheim in. U verkrijgt het Geheime punt van de Cliënt toen u een cliënt OAuth in de dienst creeerde u wilt verbinden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>Voeg om het even welke parameters toe die u in de vergunningsvraag wilt omvatten. De volgende standaardparameters worden altijd automatisch opgenomen en hoeven niet te worden toegevoegd.</p> <p>Standaardparameters:</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL response_type]</strong> </p> <p> <code>code </code>for [!UICONTROL Authorization Code flow] en <code>token </code> for [!UICONTROL Implicit flow]</p> </li> 
        <li> <p><strong>[!UICONTROL redirect_uri]</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">Amerika/APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong> </p> <p> De client-id die u hebt ontvangen bij het maken van de account</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Access token parameters]</p> </td> 
      <td> <p>Voeg om het even welke parameters toe die u in de symbolische vraag wilt omvatten. De volgende standaardparameters worden altijd automatisch opgenomen en hoeven niet te worden toegevoegd.</p> <p>Standaardparameters:</p> 
       <ul> 
        <li><strong>[!UICONTROL grant_type]</strong>: <code>authorization_code</code></li> 
        <li> <p><strong>[!UICONTROL redirect_uri]:</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">Amerika/APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li><strong>[!UICONTROL client_id]</strong>: De client-id die u hebt ontvangen bij het maken van de account, wordt automatisch opgenomen in de aanvraaginstantie</li> 
        <li><strong> client_geheime </strong>: Het geheim van de Cliënt u ontving toen het creëren van de rekening is automatisch inbegrepen in het verzoeklichaam</li> 
        <li><strong> code </strong>: De code die door het vergunningsverzoek is teruggekeerd</li> 
       </ul> <p>Opmerking:  <p>De norm OAuth 2.0 steunt minstens 2 methodes van cliëntauthentificatie tijdens deze stap (<code>[!UICONTROL client_secret_basic]</code> en <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] verzendt automatisch de opgegeven client-id en -geheim via de methode <code>[!UICONTROL client_secret_post]</code> . Daarom zijn deze parameters automatisch inbegrepen als deel van het symbolische verzoeklichaam. </p> <p>Voor meer informatie over OAuth 2.0 authentificatie, zie <a href="https://tools.ietf.org/html/rfc6749"> het Kader van de Vergunning OAuth 2.0 </a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Refresh token parameters]</p> </td> 
      <td> <p>Voeg om het even welke parameters toe die u in de symbolische vraag wilt omvatten. De volgende standaardparameters worden altijd automatisch opgenomen en hoeven niet te worden toegevoegd.</p> <p>Standaardparameters:</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL grant_type]</strong>: <code>refresh_token</code></p> </li> 
        <li> <p><strong>[!UICONTROL refresh_token]</strong>: De meest recente vernieuwingstoken die door de dienst wordt verkregen u met verbindt</p> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong>: De client-id die u hebt ontvangen bij het maken van de account, wordt automatisch opgenomen in de aanvraaginstantie</p> </li> 
        <li> <p><strong>[!UICONTROL client_secret]</strong>: Het clientgeheim dat u hebt ontvangen bij het maken van de account, wordt automatisch opgenomen in de aanvraaginstantie</p> </li> 
       </ul> <p>Opmerking:  <p>De norm OAuth 2.0 steunt minstens 2 methodes van cliëntauthentificatie tijdens deze stap (<code>[!UICONTROL client_secret_basic]</code> en <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] verzendt automatisch de opgegeven client-id en -geheim via de methode <code>[!UICONTROL client_secret_post]</code> . Daarom zijn deze parameters automatisch inbegrepen als deel van het symbolische verzoeklichaam. </p> <p>Voor meer informatie over OAuth 2.0 authentificatie, zie <a href="https://tools.ietf.org/html/rfc6749"> het Kader van de Vergunning OAuth 2.0 </a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Custom Headers]</p> </td> 
      <td> <p>Geef aanvullende sleutels en waarden op die u in de koptekst van de stappen [!UICONTROL Token] en R [!UICONTROL efresh Token] wilt opnemen.</p> <p>Opmerking:  <p>De norm OAuth 2.0 steunt minstens 2 methodes van cliëntauthentificatie tijdens deze stap (<code>[!UICONTROL client_secret_basic]</code> en <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] biedt niet automatisch ondersteuning voor de methode <code>[!UICONTROL client_secret_basic]</code> . Als de dienst die u verbindt om Cliënt te verwachten - identiteitskaart en Geheim om in één enkel koord worden gecombineerd en dan base64 die in de kopbal van de Vergunning wordt gecodeerd, dan zou u die kopbal en zeer belangrijke waarde hier moeten toevoegen.</p> <p> Voor meer informatie over OAuth 2.0 authentificatie, zie <a href="https://tools.ietf.org/html/rfc6749"> het Kader van de Vergunning OAuth 2.0 </a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Token placement]</p> </td> 
      <td> <p>Selecteer of het token in de map [!UICONTROL header] , [!UICONTROL query string] of in beide moet worden verzonden wanneer verbinding wordt gemaakt met de opgegeven URL.</p> <p>Tokens worden meestal verzonden in de verzoekkopbal.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Header token name] </td> 
      <td> <p>Voer de naam van het machtigingstoken in de koptekst in. Standaard: <code>[!UICONTROL Bearer]</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Query string parameter name] </td> 
      <td> <p>Voer de naam van het verificatietoken in de queryreeks in. Standaard: <code>[!UICONTROL access_token]</code>.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.
1. Ga aan [ te werk vormen doe een OAuth 2.0 verzoekmodule ](#configure-the-make-an-oauth-20-request-module).

### Instructies voor het maken van een verbinding met [!DNL Google] in [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request module]

In het volgende voorbeeld ziet u hoe u de aanvraagmodule [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0] gebruikt om verbinding te maken met [!DNL Google] .

1. Zorg ervoor dat u een project, gevormde montages OAuth hebt gecreeerd, en uw geloofsbrieven zoals die in artikel [ worden beschreven verbind  [!DNL Adobe Workfront Fusion]  met  [!DNL Google Services]  gebruikend een douaneOAuth cliënt ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md) geproduceerd.
1. Open de module [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]
1. Klik op **[!UICONTROL Add]** naast het verbindingsvak.
1. Voer de volgende waarden in:

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>Voer een naam in voor de verbinding.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Environment] </td> 
      <td> <p>Selecteer of u een productie- of niet-productieomgeving gebruikt.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Type] </td> 
      <td> <p>Selecteer of u een serviceaccount of een persoonlijke account gebruikt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>[!UICONTROL Authorization Code]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Authorize URI]</td> 
      <td><code>https://accounts.google.com/o/oauth2/v2/auth</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Token URI]</td> 
      <td><code>https://www.googleapis.com/oauth2/v4/token</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>Afzonderlijk bereik toevoegen. Voor meer informatie over werkingsgebied, zie <a href="https://developers.google.com/identity/protocols/oauth2/scopes"> OAuth 2.O Scopes voor [!DNL Google] APIs </a> in de [!DNL Google] documentatie.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>[!UICONTROL SPACE]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>Voer uw [!DNL Google] client-id in. </p> <p>Om een cliëntidentiteitskaart tot stand te brengen, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create-oauth-credentials" class="MCXref xref"> OAuth Credentials </a> in het artikel [!DNL Connect Adobe Workfront Fusion] tot [!DNL Google Services] gebruikend een cliënt van douaneOAuth </a> leiden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p>Voer uw [!DNL Google] clientgeheim in. </p> <p>Om een cliëntgeheim tot stand te brengen, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create-oauth-credentials" class="MCXref xref"> OAuth Credentials </a> in het artikel [!DNL Connect Adobe Workfront Fusion] aan [!DNL Google] de Diensten creëren gebruikend een cliënt van douaneOAuth </a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>Voeg <code>[!UICONTROL access_type]</code> toe - <code>[!UICONTROL offline] </code> zeer belangrijk-waardepaar.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-authentication-http.png"> </p> <p>Nota: Als u authentificatiekwesties, bijvoorbeeld met symbolische verfrissing ervaart, probeer toevoegend <code>[!UICONTROL prompt] </code> - <code>[!UICONTROL consent] </code> zeer belangrijk-waardepaar.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om verbindingsinstellingen op te slaan.
1. Ga aan [ te werk vormen doe een OAuth 2.0 verzoekmodule ](#configure-the-make-an-oauth-20-request-module).

## Vorm Make een OAuth 2.0 verzoekmodule

Nadat u een verbinding OAuth 2.0 hebt gevestigd, zet opstelling de module voort zoals gewenst. Alle toestemmingstokens worden automatisch inbegrepen in dit verzoek, en in een ander verzoek dat de zelfde verbinding gebruikt.

Wanneer u de module [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto">  
 <col> 
 <col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor informatie bij vestiging een verbinding, zie <a href="#create-a-connection-for-an-oauth-request" class="MCXref xref"> een verbinding voor een OAuth verzoek </a> in dit artikel creëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx)] </td> 
   <td> <p>Gebruik deze optie om foutafhandeling in te stellen.</p> <p>Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref"> de behandeling van de Fout </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Voer de URL in waarnaar u een aanvraag wilt verzenden, zoals een API-eindpunt, website, enzovoort.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object. Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Voer de gewenste sleutel-waardeparen voor de query in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>De hoofdtekst van HTTP is de gegevensbytes die in een HTTP- transactiebericht onmiddellijk na de kopballen worden overgebracht als er om het even welk zijn om worden gebruikt.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>Het type Raw-hoofdtekst is over het algemeen geschikt voor de meeste HTTP-hoofdtekstaanvragen, zelfs in situaties waarin in de documentatie van de ontwikkelaar geen gegevens zijn opgegeven die moeten worden verzonden.</p> <p>Geef een vorm voor het parseren van de gegevens op in het veld [!UICONTROL Content type] .</p> <p>Ondanks het geselecteerde inhoudstype, worden de gegevens ingevoerd in om het even welk formaat dat door de ontwikkelaarsdocumentatie wordt bepaald of wordt vereist.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>Dit hoofdtype is het POSTEN van gegevens met <code>[!UICONTROL application/x-www-form-urlencoded]</code> .</p> <p>Voor <code>[!UICONTROL application/x-www-form-urlencoded]</code> is de hoofdtekst van het HTTP-bericht dat naar de server wordt verzonden, in wezen één queryreeks. De sleutels en waarden worden gecodeerd in sleutel-waardeparen die door <code>&amp;</code> worden gescheiden en met een <code>=</code> tussen de sleutel en de waarde. </p> <p><code>use [!UICONTROL multipart/form-data]</code> voor binaire gegevens.</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b> Voorbeeld: </b></span></span> 
       <p>Voorbeeld van de resulterende HTTP-aanvraagindeling:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data] is een multipart HTTP-aanvraag die wordt gebruikt om bestanden en gegevens te verzenden. Het wordt doorgaans gebruikt om bestanden naar de server te uploaden.</p> <p>Voeg velden toe die in de aanvraag moeten worden verzonden. Elk veld moet een sleutelwaardepaar bevatten.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>Voer de sleutel en waarde in die binnen de aanvraaginstantie moeten worden verzonden.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Voer de sleutel in en geef het bronbestand op dat u wilt verzenden in de hoofdtekst van de aanvraag.</p> <p>Wijs het dossier toe u van de vorige module (zoals [!UICONTROL HTTP] &gt; [!UICONTROL Get a File]) wilt uploaden, of ga de dossier - naam en dossiergegevens manueel in.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Schakel deze optie in om reacties automatisch te parseren en JSON- en XML-reacties om te zetten, zodat u de modules [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON] of [!UICONTROL XML] &gt; [!UICONTROL Parse XML] niet hoeft te gebruiken.</p> <p>Voordat u geparseerde JSON- of XML-inhoud kunt gebruiken, voert u de module één keer handmatig uit, zodat de module de inhoud van de reactie herkent en deze in volgende modules kunt toewijzen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>Voer de time-out van het verzoek in seconden in (1-300). De standaardwaarde is 40 seconden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> Schakel deze optie in om cookies van de server te delen met alle HTTP-modules in uw scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p>Om een zelfondertekend certificaat of een privé sleutel voor TLS te gebruiken, klik <b> Extraheren </b> en verstrek het van het certificaat of privé sleutel dossier en wachtwoord.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>Schakel deze optie in om verbindingen die niet-geverifieerde TLS-certificaten gebruiken, te weigeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> Schakel deze optie in om de URL-omleidingen te volgen met 3xx-reacties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>Schakel deze optie in om de URL-omleidingen te volgen met alle antwoordcodes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>Standaard handelt [!DNL Workfront Fusion] meerdere waarden af voor dezelfde URL-querytekenreeks-parametersleutel als arrays. <code>www.test.com?foo=bar&amp;foo=baz</code> wordt bijvoorbeeld omgezet in <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code> . Activeer deze optie om deze functie uit te schakelen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> Schakel deze optie in om een gecomprimeerde versie van de website aan te vragen.</p> <p>Hiermee wordt een <code>[!UICONTROL Accept-Encoding]</code> -header toegevoegd om gecomprimeerde inhoud aan te vragen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>Schakel deze optie in om Wederzijdse TLS te gebruiken in de HTTP-aanvraag.</p> <p>Voor meer informatie over Wederzijdse TLS, zie <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref"> Gebruik Wederzijdse TLS in de modules van HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

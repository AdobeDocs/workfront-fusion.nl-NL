---
title: Adobe Target-modules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die  [!DNL Adobe Target], as well as connect it to multiple third-party applications and services. [!DNL Adobe Target]  modules gebruiken u toestaan om, verslagen tot stand te brengen te lezen bij te werken of te schrappen, van alle verslagen van een bepaald type, onderzoeksverslagen een lijst te maken die op criteria worden gebaseerd u specificeert, of een douane API vraag aan  [!DNL Adobe Target]  API uit te voeren.
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1959'
ht-degree: 0%

---

# [!DNL Adobe Target] Modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Adobe Target] gebruiken en deze koppelen aan meerdere toepassingen en services van derden. Met [!DNL Adobe Target] -modules kunt u records maken, lezen, bijwerken of verwijderen, alle records van een bepaald type weergeven, zoekrecords weergeven op basis van criteria die u opgeeft, of een aangepaste API-aanroep naar de [!DNL Adobe Target] API uitvoeren.


Als u instructies bij het creëren van een scenario nodig hebt, zie de artikelen onder [ een scenario creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Adobe Workfront-abonnement*</td>
      <td>
        <p>[!UICONTROL Pro] of hoger</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront-licentie*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
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
    </tr>
  </tbody>
</table>


Neem contact op met uw Workfront-beheerder om te weten te komen welk plan, licentietype of toegang u hebt.

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

Voordat u de [!DNL Adobe Target] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!DNL Adobe Target] account hebben.

## Adobe Target API-informatie

De Adobe Target-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.7.3</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken met [!DNL Adobe Target]

>[!IMPORTANT]
>
>Voor verbindingen die na 3 juni 2024 worden gemaakt, is een Adobe Target Server-naar-server verbinding vereist.
>
>* De bestaande verbindingen van de Rekening van de Dienst zullen tot Januari 2025 blijven werken. U moet uw verbindingen van de Rekening van de Dienst met server-aan-server van Adobe Target tegen Januari 2024 vervangen.
>* U moet een ontwikkelaar voor uw organisatie zijn om een server-aan-server verbinding van Adobe Target tot stand te brengen. De rol van ontwikkelaar wordt ingesteld in de Adobe Admin Console.

Verbinding maken voor uw [!DNL Adobe Target] -modules:

1. Klik in een willekeurige module op **[!UICONTROL Add]** naast het vak Verbinding.

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
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>Selecteer of u een verbinding van de Rekening van de Dienst of een server-aan-server verbinding van Adobe Target creeert.<p><b> BELANGRIJK </b>: De verbindingen die na 3 Juni, 2024 worden gecreeerd vereisen een server-aan-server verbinding van Adobe Target. De bestaande verbindingen van de Rekening van de Dienst zullen tot Januari 2025 blijven werken. U moet uw verbindingen van de Rekening van de Dienst met server-aan-server van Adobe Target tegen Januari 2024 vervangen.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!DNL Adobe] client-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] clientgeheim in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Voer uw [!DNL Adobe] technische account-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Voer uw [!DNL Adobe] Organisatie-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tenant]</td>
        <td>
          <p> Als u de huurder wilt zoeken, meldt u zich aan bij de [!DNL Adobe Experience Cloud] , opent u [!DNL Target] en klikt u op de [!DNL Target] -kaart. Gebruik de waarde van de huurder-id zoals vermeld in het URL-subdomein.</p>
          <p>Als uw URL bij het aanmelden bij [!DNL Adobe Target] bijvoorbeeld <code>&lt;https://mycompany.experiencecloud.adobe.com/...></code> is, is de id van uw huurder "mijn bedrijf".</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Enter <code>ent_marketing_sdk</code>       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Voer de persoonlijke sleutel in die is gegenereerd toen uw referenties werden gemaakt in de [!DNL Adobe Developer Console] . </p>
          <p>Uw persoonlijke sleutel of certificaat uitnemen:</p>
          <ol>
            <li value="1">
              <p>Klik op <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selecteer het type bestand dat u extraheert.</p>
            </li>
            <li value="3">
              <p>Selecteer het bestand dat de persoonlijke sleutel of het certificaat bevat.</p>
            </li>
            <li value="4">
              <p>Voer het wachtwoord voor het bestand in.</p>
            </li>
            <li value="5">
              <p>Klik op <b>[!UICONTROL Save]</b> om het bestand uit te pakken en terug te keren naar de verbindingsinstelling.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## [!DNL Adobe Target] modules en hun velden

Wanneer u [!DNL Adobe Target] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Target] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Handelingen](#actions)

* [Zoekopdrachten](#searches)


### Handelingen

* [[!UICONTROL Create a record]](#create-a-record)

* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)

* [[!UICONTROL Delete a record]](#delete-a-record)

* [[!UICONTROL Read a record]](#read-a-record)

* [[!UICONTROL Update a record]](#update-a-record)


#### [!UICONTROL Create a record]

Deze actiemodule leidt tot een activiteit AB of XT, een aanbieding, of een publiek.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Zie [!DNL Adobe Target] Verbinding maken met <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target]</a> .</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>
      <p>Selecteer het type record dat u wilt maken.</p>
      <ul>
        <li>
        <b> Bezit </b><p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Properties/operation/createProperty"> een bezit </a> in de documentatie van Adobe Target API creëren.</p>
        </li>
        <li>
        <b> Aanbeveling van de Aanbieding </b><p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Offers/operation/createOffer"> een nieuwe recs aanbieding </a> in de documentatie van Adobe Target API creëren.</p>
        </li>
        <li>
          <b>[!UICONTROL Offer JSON]</b>
          <p>Ga aan <a href="#offer-fields" class="MCXref xref" > gebieden van de Aanbieding </a> verder.</p>
        </li>
        <li>
          <b>[!UICONTROL Offer Content]</b>
          <p>Ga aan <a href="#offer-fields" class="MCXref xref" > gebieden van de Aanbieding </a> verder.</p>
        </li>
        <li>
        <b> Milieu </b><p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Environments/operation/createEnvironment"> milieu </a> in de documentatie van Adobe Target API creëren.</p>
        </li>
        <li>
          <b>[!UICONTROL Audience]</b>
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Audiences/operation/createAudience_1_1"> publiek </a> in de documentatie van Adobe Target API creëren.</p>
        </li>
        <li>
          <b>[!UICONTROL AB Activity]</b>
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1"> tot de activiteit van AB </a> in de documentatie van Adobe Target API leiden.</p>
        </li>
        <li>
          <b>[!UICONTROL XT Activity]</b>
          <p>Ga aan <a href="#xt-activity-fields" class="MCXref xref" > XT de gebieden van de Activiteit </a> verder.</p>
        </li>
        <li>
          <b>[!UICONTROL AP Activity]</b>
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_2"> AP activiteit </a> in de documentatie van Adobe Target API creëren.</p>
        </li>
        <li>
          <b>[!UICONTROL Response Token]</b>
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Response-tokens/operation/createResponseToken"> Create Token van de Reactie </a> in de documentatie van Adobe Target API.</p>
        </li>
      </ul>
    </td>
  </tr>
</tbody>
</table>

<!--

##### AB Activity fields

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this activity. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>For each option that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the option across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the option. The name must be no more than 250 characters.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Select or map the Offer associated with the option.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Mboxes]</td>
      <td>
        <p>For each Mbox that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selectors]</td>
      <td>
        <p>For each selector that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Selector]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>A list of locations on the page where the content offer is served. A location contains the following:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Enter or map the ID of the experience</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map the name of the experience
</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>For each audience that you want to see the experience, click <b>[!UICONTROL Add item]</b> and enter the Audience ID.
</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Enter or map the percentage of visitors that is allocated to the experience</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td><p>For details on metrics, see <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Create AB activity</a> in the Adobe Target API documentation.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Enter or map an ID to identify this activity. You can choose this ID. This ID must not be the same as another activity, and can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Enter or map the date and time to start the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Enter or map the date and time to end the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Enter or map the state of the activity.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Enter a number that defines the priority of the activity. Higher numbers have higher priority. This value must be between 0 and 999. The default value is 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Enable this option to auto-allocate traffic. Auto-allocating sends more traffic to the more successful experience.</p>
        <p>Select or map the evaluation criteria by which to judge which experience is more successful.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Enter or map the workspace that the activity is associated with</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>For each property that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and select or map the property's ID.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>For each reporting audience that you want to add to the activity, click [!UICONTROL Add item] and enter the following information:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the Reporting Audience across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Enter or map the Segment to be used in reporting</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the metric across API requests.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

-->

##### XT-activiteitvelden

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Voer een naam voor deze activiteit in of wijs een naam toe. De naam mag uit maximaal 250 tekens bestaan.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>Voor elke optie die u aan de activiteit wilt toevoegen, klik <b>[!UICONTROL Add item]</b> en vul de volgende gebieden in:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Voer een tekenreeks in of wijs een tekenreeks toe die moet worden gebruikt om de optie bij te houden voor verschillende API-aanvragen.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Voer een naam voor de optie in of wijs een naam toe. De naam mag niet meer dan 250 tekens bevatten.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Selecteer of wijs het Voorstel toe verbonden aan de optie.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Locations]</td>
      <td>
        <p>Voor elke box die u aan de activiteit wilt toevoegen, klik <b>[!UICONTROL Add item]</b> en vul de volgende gebieden in:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>Voor elk publiek dat u aan Mbox wilt toevoegen, klik <b>[!UICONTROL Add item]</b> en selecteer identiteitskaart van de Publiek</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Voer een tekenreeks in of wijs een tekenreeks toe die moet worden gebruikt om de locatie in API-verzoeken bij te houden.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Voer een naam voor de locatie in of wijs een naam toe. De naam mag niet meer dan 250 tekens bevatten.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>Een lijst met locaties op de pagina waar het inhoudsaanbod wordt weergegeven. Een locatie bevat het volgende:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Voer de id van de ervaring in of wijs deze toe</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Voer de naam van de ervaring in of wijs deze toe

</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>Voor elk publiek dat u de ervaring wilt zien, klik <b>[!UICONTROL Add item]</b> en ga identiteitskaart van de Publiek in.

</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Voer het percentage bezoekers dat aan de ervaring is toegewezen in of wijs dit percentage toe</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Voer een id in of wijs deze toe om deze activiteit te identificeren. U kunt deze id kiezen. Deze id mag niet hetzelfde zijn als een andere activiteit en mag uit maximaal 250 tekens bestaan.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Voer de datum en tijd in of wijs de datum en tijd toe waarop de activiteit moet worden gestart in de notatie <code>YYYY-MM-DD hh:mm:ss.z</code> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Voer de datum en tijd in of wijs de datum en tijd toe om de activiteit te beëindigen in de notatie <code>YYYY-MM-DD hh:mm:ss.z</code> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Voer de status van de activiteit in of wijs deze toe.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Voer een getal in dat de prioriteit van de activiteit definieert. Hogere getallen hebben een hogere prioriteit. Deze waarde moet liggen tussen 0 en 999. De standaardwaarde is 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Schakel deze optie in om automatisch verkeer toe te wijzen. De auto-toewijst verzendt meer verkeer naar de succesvolere ervaring.</p>
        <p>Selecteer of kaart de evaluatiecriteria aan om te beoordelen welke ervaring succesvoller is.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Voer de werkruimte in die aan de activiteit is gekoppeld of wijs deze toe</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>Voor elke eigenschap die u aan de activiteit wilt toevoegen, klikt u op <b>[!UICONTROL Add item]</b> en selecteert of wijst u de id van de eigenschap toe.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>Voor elk rapporterend publiek dat u aan de activiteit wilt toevoegen, klik [!UICONTROL Add item] en ga de volgende informatie in:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Ga of kaart een koord in dat moet worden gebruikt om het Publiek van de Rapportering over API verzoeken te volgen.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Typ of wijs het segment toe dat u wilt gebruiken voor de rapportage</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Voer een tekenreeks in of wijs een tekenreeks toe die moet worden gebruikt om de metrische gegevens in API-verzoeken bij te houden.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Velden aanbieden

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Voer een naam voor deze activiteit in of wijs een naam toe. De naam mag uit maximaal 250 tekens bestaan.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content]</td>
      <td>
        <p>Voer de inhoud van het aanbod in of wijs deze toe aan de gebruiker.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Voer de id van de werkruimte die aan de aanbieding is gekoppeld in of wijs deze toe. Als deze optie leeg blijft, wordt de aanbieding gekoppeld aan de standaardwerkruimte van de account. Deze functionaliteit is alleen van toepassing op [!DNL Target] Premium-accounts.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Voer de datum en het tijdstip in waarop deze aanbieding is gewijzigd of wijs de datum en tijd toe.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--

##### Audience fields

>[!NOTE]
>
>Audiences created through Workfront Fusion can only be edit in Fusion or through the API. They cannot be edited from within Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this audience. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Description]</td>
      <td>
        <p>Enter or map a description of this audience.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Origin]</td>
      <td>
        <p>Select whether this audience's origin is from Target or from the cloud.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Target Rule]</td>
      <td>
        <p>Enable the toggle to make rules AND, that is, all rules must be applied.</p>
        <p>For each rule that you want to apply to the audience, click <b>[!UICONTROL Add item]</b> and enter the JSON of the rule you want to apply. </p>
        <div class="example"><span class="autonumber"><span><b>Example: </b></span></span>
          <p>Example 1:</p>
          <p ><code>&lbrace;</code></p>
                    <p ><code>                "page": "url",</code>
                    </p>
                    <p><code>                "equals":&lbrack;</code>
                    </p>
                    <p ><code>                    "http://www.myhomepage.com/"</code>
                    </p>
                    <p><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;,</code>
                    </p>
                    <p>Example 2</p>
                    <p ><code>            &lbrace;</code>
                    </p>
                    <p><code>                "geo": "region",</code>
                    </p>
                    <p><code>                "matches": &lbrack;</code>
                    </p>
                    <p ><code>                    "california"</code>
                    </p>
                    <p ><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;</code>
                    </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Enter or map the ID of the workspace associated with the audience. If left blank, the offer is associated with the default workspace of the account. This functionality applies only to [!DNL Target Premium] accounts.</p>
      </td>
    </tr>
  </tbody>
</table>

-->

#### [!UICONTROL Make a custom API call]

Deze module maakt een aangepaste API-aanroep naar de [!DNL Adobe Target] API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Target] Verbinding maken met <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL [!DNL Target] Basis-URL]</td>
      <td>Voer de basis-URL van [!DNL Target] in of wijs deze toe.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Een pad invoeren ten opzichte van {baseURL}/</p>
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
        <p>Workfront Fusion voegt automatisch machtigingsheaders en x-api-sleutelkopballen toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Voer de queryreeks voor de aanvraag in.</p>
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

#### [!UICONTROL Delete a record]

Deze actiemodule schrapt één enkele activiteit van AB, activiteit XT, Aanbieding, of Publiek.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Zie [!DNL Adobe Target] Verbinding maken met <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target]</a> .</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Selecteer het type record dat u wilt verwijderen.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>Voer de id in van de record die u wilt verwijderen of wijs deze toe.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Read a record]

Deze actiemodule wint gegevens voor één enkele Activiteit, Aanbieding, Publiek, Bezit, of Rapport terug.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Zie [!DNL Adobe Target] Verbinding maken met <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target]</a> .</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Selecteer het type record dat u wilt lezen.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>Voer de id in van de record die u wilt lezen of wijs deze toe.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Update a record]

Deze actiemodule werkt een record bij in Doel.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Target] Verbinding maken met <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>
        <p>Selecteer het type record dat u wilt bijwerken.</p>
       </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Field names]</td>
      <td>Selecteer de velden die u wilt bijwerken. De velden worden hieronder weergegeven.
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/"> de documentatie van Adobe Target API </a>.</p>
      </td>
    </tr>
  </tbody>
</table>

### Zoekopdrachten

* [[!UICONTROL Get records]](#get-records)

* [[!UICONTROL Search]](#search)


#### [!UICONTROL Get records]

Deze zoekmodule haalt een lijst met records van het geselecteerde type op.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Target] Verbinding maken met <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Selecteer het type record dat u wilt bijwerken.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Sort by]</td>
      <td>Klik voor elk veld waarop u wilt sorteren op <b>[!UICONTROL Add item]</b> en selecteer het veld en geef aan of de geretourneerde resultaten oplopend of aflopend moeten zijn.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts At]</td>
      <td>
        <p>Voer de vroegste datum in waarvoor u records wilt ophalen. </p>
        <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends At]</td>
      <td>
        <p>Voer de laatste datum in waarvoor u records wilt ophalen. </p>
        <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Search]

Deze zoekmodule zoekt naar Activiteiten, Aanbiedingen of Soorten publiek op basis van criteria die u opgeeft.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Zie [!DNL Adobe Target] Verbinding maken met <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target]</a> .</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Selecteer het type record dat u wilt bijwerken.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Sort by]</td>
    <td>Klik voor elk veld waarop u wilt sorteren op <b>[!UICONTROL Add item]</b> en selecteer het veld en geef aan of de geretourneerde resultaten oplopend of aflopend moeten zijn.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Search criteria]</td>
    <td>Selecteer voor elke regel die u wilt instellen het veld, de operator en de waarde. Klik op <b>[!UICONTROL Add AND rule]</b> om extra regels te maken.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Offset]</td>
    <td>
      <p>Voer het nummer in van de eerste reactie die de module moet retourneren. De eerste geretourneerde reactie heeft een verschuiving van <code>0</code> . Gebruik dit veld in combinatie met het veld [!UICONTROL Maximum number of returned results] om de reacties te pagineren.</p>
      <p>Als u bijvoorbeeld de derde pagina met reacties wilt weergeven, stelt u [!UICONTROL Offset] in op 20 en [!UICONTROL Maximum number of returned] op 10 als elke pagina tien reacties heeft.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]</td>
    <td>
      <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren. Gebruik dit veld in combinatie met het veld [!UICONTROL Offset] om de reacties te pagineren.</p>
      <p>Als u bijvoorbeeld de derde pagina met reacties wilt weergeven, stelt u [!UICONTROL Offset] in op 20 en [!UICONTROL Maximum number of returned] op 10 als elke pagina tien reacties heeft.</p>
    </td>
  </tr>
</tbody>
</table>

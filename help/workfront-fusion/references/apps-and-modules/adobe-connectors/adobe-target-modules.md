---
title: Adobe Target-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die  [!DNL Adobe Target], as well as connect it to multiple third-party applications and services. [!DNL Adobe Target]  modules gebruiken u toestaan om, verslagen tot stand te brengen te lezen, bij te werken of te schrappen, van alle verslagen van een bepaald type een lijst te maken, onderzoeksverslagen die op criteria worden gebaseerd u specificeert, of een douane API vraag aan  [!DNL Adobe Target]  API uit te voeren.
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '2261'
ht-degree: 0%

---

# [!DNL Adobe Target] Modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Adobe Target] gebruiken en deze koppelen aan meerdere toepassingen en services van derden. Met [!DNL Adobe Target] -modules kunt u records maken, lezen, bijwerken of verwijderen, alle records van een bepaald type weergeven, zoekrecords weergeven op basis van criteria die u opgeeft, of een aangepaste API-aanroep naar de [!DNL Adobe Target] API uitvoeren.


Als u instructies bij het creëren van een scenario nodig hebt, zie de artikelen onder [ een scenario creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
      <td>
        <p>[!UICONTROL Pro] of hoger</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td>
      <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor een oudere licentie: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en -integratie] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">Product</td>
      <td>
   <p>Huidige productvereiste: als u het abonnement [!UICONTROL Select] of [!UICONTROL Prime] [!DNL Adobe Workfront] hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] is opgenomen in het abonnement [!UICONTROL Ultimate] [!DNL Workfront] .</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td>
    </tr>
    </tr>
  </tbody>
</table>


Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

1. In om het even welke module, voegt de klik **[!UICONTROL toe]** naast het vakje van de Verbinding.

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
        <td role="rowheader">[!UICONTROL -verbindingstype]</td>
        <td>Selecteer of u een verbinding van de Rekening van de Dienst of een server-aan-server verbinding van Adobe Target creeert.<p><b> BELANGRIJK </b>: De verbindingen die na 3 Juni, 2024 worden gecreeerd vereisen een server-aan-server verbinding van Adobe Target. De bestaande verbindingen van de Rekening van de Dienst zullen tot Januari 2025 blijven werken. U moet uw verbindingen van de Rekening van de Dienst met server-aan-server van Adobe Target tegen Januari 2024 vervangen.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL -omgeving]</td>
        <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL -type]</td>
        <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!DNL Adobe] client-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van de [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] clientgeheim in. Dit vindt u in de sectie [!UICONTROL Credentials details] van de [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Voer uw [!DNL Adobe] technische account-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van de [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL -organisatie-ID]</td>
        <td>Voer uw [!DNL Adobe] Organisatie-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van de [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL -huurder]</td>
        <td>
          <p> Als u de huurder wilt zoeken, meldt u zich aan bij de [!DNL Adobe Experience Cloud] , opent u [!DNL Target] en klikt u op de [!DNL Target] -kaart. Gebruik de waarde van de huurder-id zoals vermeld in het URL-subdomein.</p>
          <p>Als uw URL bij het aanmelden bij [!DNL Adobe Target] bijvoorbeeld <code>&lt;https://mycompany.experiencecloud.adobe.com/...></code> is, is de id van uw huurder "mijn bedrijf".</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL -metagegevensbereiken]</td>
        <td>Enter <code>ent_marketing_sdk</code>       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Persoonlijke sleutel]</td>
        <td>
          <p>Voer de persoonlijke sleutel in die is gegenereerd toen uw referenties werden gemaakt in de [!DNL Adobe Developer Console] . </p>
          <p>Uw persoonlijke sleutel of certificaat uitnemen:</p>
          <ol>
            <li value="1">
              <p>Klik <b> [!UICONTROL Extraheren] </b>.</p>
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
              <p>Klik <b> [!UICONTROL sparen] </b> om het dossier uit te halen en aan de verbindingsopstelling terug te keren.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. Klik **[!UICONTROL verdergaan]** om de verbinding te bewaren en aan de module terug te keren.

## [!DNL Adobe Target] modules en hun velden

Wanneer u [!DNL Adobe Target] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Target] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Handelingen](#actions)

* [Zoekopdrachten](#searches)


### Handelingen

* [[!UICONTROL &#x200B; creeer een verslag &#x200B;]](#create-a-record)

* [[!UICONTROL &#x200B; maak een douane API vraag &#x200B;]](#make-a-custom-api-call)

* [[!UICONTROL &#x200B; Schrap een verslag &#x200B;]](#delete-a-record)

* [[!UICONTROL &#x200B; las een verslag &#x200B;]](#read-a-record)

* [[!UICONTROL &#x200B; werk een verslag &#x200B;] bij](#update-a-record)


#### [!UICONTROL &#x200B; creeer een verslag &#x200B;]

Deze actiemodule leidt tot een activiteit AB of XT, een aanbieding, of een publiek.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL -verbinding]</td>
    <td>Zie <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > Verbinding maken met [!DNL Adobe Target]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target] .</td>
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
          <b>[!UICONTROL Offer JSON] </b>
          <p>Ga aan <a href="#offer-fields" class="MCXref xref" > gebieden van de Aanbieding </a> verder.</p>
        </li>
        <li>
          <b>[!UICONTROL -inhoud van aanbieding]</b>
          <p>Ga aan <a href="#offer-fields" class="MCXref xref" > gebieden van de Aanbieding </a> verder.</p>
        </li>
        <li>
        <b> Milieu </b><p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Environments/operation/createEnvironment"> milieu </a> in de documentatie van Adobe Target API creëren.</p>
        </li>
        <li>
          <b>[!UICONTROL Audience] </b>
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Audiences/operation/createAudience_1_1"> publiek </a> in de documentatie van Adobe Target API creëren.</p>
        </li>
        <li>
          <b>[!UICONTROL AB Activity] </b>
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1"> tot de activiteit van AB </a> in de documentatie van Adobe Target API leiden.</p>
        </li>
        <li>
          <b>[!UICONTROL XT Activity] </b>
          <p>Ga aan <a href="#xt-activity-fields" class="MCXref xref" > XT de gebieden van de Activiteit </a> verder.</p>
        </li>
        <li>
          <b> [!UICONTROL AP Activiteit] </b>
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_2"> AP activiteit </a> in de documentatie van Adobe Target API creëren.</p>
        </li>
        <li>
          <b>[!UICONTROL -responstoken]</b>
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
      <td role="rowheader">[!UICONTROL -naam]</td>
      <td>Voer een naam voor deze activiteit in of wijs een naam toe. De naam mag uit maximaal 250 tekens bestaan.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -opties]</td>
      <td>
        <p>Voor elke optie die u aan de activiteit wilt toevoegen, klik <b> [!UICONTROL voegt punt] </b> toe en vul de volgende gebieden in:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Optie lokale identiteitskaart] </b>
            </p>
            <p>Voer een tekenreeks in of wijs een tekenreeks toe die moet worden gebruikt om de optie bij te houden voor verschillende API-aanvragen.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name] </b>
            </p>
            <p>Voer een naam voor de optie in of wijs een naam toe. De naam mag niet meer dan 250 tekens bevatten.</p>
          </li>
          <li>
            <p><b>[!UICONTROL -aanbieding-id]</b>
            </p>
          </li>
          <li>
            <p>Selecteer of wijs het Voorstel toe verbonden aan de optie.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -locaties]</td>
      <td>
        <p>Voor elke Mbox die u aan de activiteit wilt toevoegen, klik <b> [!UICONTROL voegt punt] </b> toe en vul de volgende gebieden in:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>Voor elk publiek dat u aan Mbox wilt toevoegen, klik <b> [!UICONTROL voegt punt] </b> toe en selecteer identiteitskaart van het Publiek.</p>
          </li>
          <li>
            <p><b>[!UICONTROL lokale identiteitskaart van de Plaats] </b>
            </p>
            <p>Voer een tekenreeks in of wijs een tekenreeks toe die moet worden gebruikt om de locatie in API-verzoeken bij te houden.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name] </b>
            </p>
            <p>Voer een naam voor de locatie in of wijs een naam toe. De naam mag niet meer dan 250 tekens bevatten.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -ervaringen]</td>
      <td>
        <p>Een lijst met locaties op de pagina waar het inhoudsaanbod wordt weergegeven. Een locatie bevat het volgende:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Ervaar lokale identiteitskaart] </b>
            </p>
            <p>Voer de id van de ervaring in of wijs deze toe</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name] </b>
            </p>
            <p>Voer de naam van de ervaring in of wijs deze toe

</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>Voor elk publiek dat u de ervaring wilt zien, klik <b> [!UICONTROL voegt punt] </b> toe en ga identiteitskaart van het Publiek in.

</p>
          </li>
          <li>
            <p><b>[!UICONTROL -bezoekerspercentage] </b>
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
      <td role="rowheader">[!UICONTROL -ID VAN DERDEN]</td>
      <td>Voer een id in of wijs deze toe om deze activiteit te identificeren. U kunt deze id kiezen. Deze id mag niet hetzelfde zijn als een andere activiteit en mag uit maximaal 250 tekens bestaan.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL start bij]</td>
      <td>Voer de datum en tijd in of wijs de datum en tijd toe waarop de activiteit moet worden gestart in de notatie <code>YYYY-MM-DD hh:mm:ss.z</code> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL eindigt bij]</td>
      <td>Voer de datum en tijd in of wijs de datum en tijd toe om de activiteit te beëindigen in de notatie <code>YYYY-MM-DD hh:mm:ss.z</code> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Voer de status van de activiteit in of wijs deze toe.</p>
        <ul>
          <li>
            <p>[!UICONTROL goedgekeurd]</p>
          </li>
          <li>
            <p>[!UICONTROL gedeactiveerd]</p>
          </li>
          <li>
            <p>[!UICONTROL gepauzeerd]</p>
          </li>
          <li>
            <p>[!UICONTROL Opgeslagen] </p>
          </li>
          <li>
            <p>[!UICONTROL verwijderd]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Voer een getal in dat de prioriteit van de activiteit definieert. Hogere getallen hebben een hogere prioriteit. Deze waarde moet liggen tussen 0 en 999. De standaardwaarde is 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL wijst verkeer automatisch toe]</td>
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
      <td role="rowheader">[!UICONTROL , eigenschap-id's] </td>
      <td>Voor elk bezit dat u aan de activiteit wilt toevoegen, klik <b> [!UICONTROL voegt punt] </b> toe en selecteert of in kaart brengt identiteitskaart van het bezit.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -rapportagepubliek]</td>
      <td>
        <p>Voor elk rapporterend publiek dat u aan de activiteit wilt toevoegen, klik [!UICONTROL voeg punt] toe en ga de volgende informatie in:</p>
        <ul>
          <li>
            <p><b> [!UICONTROL Meldend de lokale identiteitskaart van het Publiek] </b>
            </p>
            <p>Ga of kaart een koord in dat moet worden gebruikt om het Publiek van de Rapportering over API verzoeken te volgen.</p>
          </li>
          <li>
            <p><b> [!UICONTROL Audience ID] </b>
            </p>
            <p>Typ of wijs het segment toe dat u wilt gebruiken voor de rapportage</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metrische lokale identiteitskaart] </b>
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
      <td role="rowheader">[!UICONTROL -naam]</td>
      <td>Voer een naam voor deze activiteit in of wijs een naam toe. De naam mag uit maximaal 250 tekens bestaan.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -inhoud]</td>
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

#### [!UICONTROL &#x200B; maak een douane API vraag &#x200B;]

Deze module maakt een aangepaste API-aanroep naar de [!DNL Adobe Target] API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > Verbinding maken met [!DNL Adobe Target]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL [!DNL Target] Basis-URL]</td>
      <td>Voer de basis-URL van [!DNL Target] in of wijs deze toe.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL -pad]</p>
      </td>
      <td>
        <p>Een pad invoeren ten opzichte van {baseURL}/</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL , methode]</p>
      </td>
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -kopteksten]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Hiermee worden automatisch machtigingsheaders en x-api-sleutelkoppen toegevoegd.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -queryreeks]  </td>
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

#### [!UICONTROL &#x200B; Schrap een verslag &#x200B;]

Deze actiemodule schrapt één enkele activiteit van AB, activiteit XT, Aanbieding, of Publiek.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL -verbinding]</td>
    <td>Zie <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > Verbinding maken met [!DNL Adobe Target]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target] .</td>
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

#### [!UICONTROL &#x200B; las een verslag &#x200B;]

Deze actiemodule wint gegevens voor één enkele Activiteit, Aanbieding, Publiek, Bezit, of Rapport terug.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL -verbinding]</td>
    <td>Zie <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > Verbinding maken met [!DNL Adobe Target]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target] .</td>
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

#### [!UICONTROL &#x200B; werk een verslag &#x200B;] bij

Deze actiemodule werkt een record bij in Doel.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > Verbinding maken met [!DNL Adobe Target]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>
        <p>Selecteer het type record dat u wilt bijwerken.</p>
       </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -veldnamen]</td>
      <td>Selecteer de velden die u wilt bijwerken. De velden worden hieronder weergegeven.
          <p>Voor details op gebieden, zie <a href="https://developer.adobe.com/target/administer/admin-api/"> de documentatie van Adobe Target API </a>.</p>
      </td>
    </tr>
  </tbody>
</table>

### Zoekopdrachten

* [[!UICONTROL &#x200B; krijgt verslagen &#x200B;]](#get-records)

* [[!UICONTROL &#x200B; Onderzoek &#x200B;]](#search)


#### [!UICONTROL &#x200B; krijgt verslagen &#x200B;]

Deze zoekmodule haalt een lijst met records van het geselecteerde type op.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > Verbinding maken met [!DNL Adobe Target]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Selecteer het type record dat u wilt bijwerken.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL sorteren op]</td>
      <td>Voor elk gebied dat u wilt sorteren door te klikken <b> [!UICONTROL voegt punt] </b> toe en selecteert het gebied en of de teruggekeerde resultaten zouden moeten oplopend of dalend zijn.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL start bij]</td>
      <td>
        <p>Voer de vroegste datum in waarvoor u records wilt ophalen. </p>
        <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL eindigt bij]</td>
      <td>
        <p>Voer de laatste datum in waarvoor u records wilt ophalen. </p>
        <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL &#x200B; Onderzoek &#x200B;]

Deze zoekmodule zoekt naar Activiteiten, Aanbiedingen of Soorten publiek op basis van criteria die u opgeeft.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL -verbinding]</td>
    <td>Zie <a href="#create-a-connection-to-adobe-target" class="MCXref xref" > Verbinding maken met [!DNL Adobe Target]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Target] .</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Selecteer het type record dat u wilt bijwerken.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL sorteren op]</td>
    <td>Voor elk gebied dat u wilt sorteren door te klikken <b> [!UICONTROL voegt punt] </b> toe en selecteert het gebied en of de teruggekeerde resultaten zouden moeten oplopend of dalend zijn.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL -zoekcriteria]</td>
    <td>Selecteer voor elke regel die u wilt instellen het veld, de operator en de waarde. Klik <b> [!UICONTROL voegt toe EN regel] </b> om extra regels tot stand te brengen.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL -verschuiving]</td>
    <td>
      <p>Voer het nummer in van de eerste reactie die de module moet retourneren. De eerste geretourneerde reactie heeft een verschuiving van <code>0</code> . Gebruik dit veld in combinatie met het veld [!UICONTROL Maximum aantal geretourneerde resultaten] om de reacties te pagineren.</p>
      <p>Als u bijvoorbeeld de derde pagina met reacties wilt weergeven, stelt u voor elke pagina tien reacties in op [!UICONTROL -verschuiving] op 20 en [!UICONTROL Maximum aantal geretourneerde reacties] op 10.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]</td>
    <td>
      <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren. Gebruik dit veld in combinatie met het veld [!UICONTROL Offset] om de reacties te pagineren.</p>
      <p>Als u bijvoorbeeld de derde pagina met reacties wilt weergeven, stelt u voor elke pagina tien reacties in op [!UICONTROL -verschuiving] op 20 en [!UICONTROL Maximum aantal geretourneerde reacties] op 10.</p>
    </td>
  </tr>
</tbody>
</table>

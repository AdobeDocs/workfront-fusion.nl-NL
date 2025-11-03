---
title: Salesforce-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die gebruikmaken van Salesforce, en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2698'
ht-degree: 0%

---

# [!DNL Salesforce] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Salesforce] gebruiken en er verbinding mee maken met meerdere toepassingen en services van derden.

Ga voor een video-introductie over de Salesforce-connector naar:

* [&#x200B; Salesforce &#x200B;](https://video.tv.adobe.com/v/3427027/){target=_blank}

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

>[!NOTE]
>
>* Niet alle versies van [!DNL Salesforce] hebben API-toegang. Zie voor meer informatie de informatie over [!DNL Salesforce] -edities met API-toegang op de [!DNL Salesforce] -communitysite.
>* Zie de API-documenten van [!DNL Salesforce] voor informatie over specifieke fouten die door de [!DNL Salesforce] API worden geretourneerd. U kunt ook de status van de [!DNL Salesforce] API controleren op mogelijke uitval van de service.
>

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

Als u [!DNL Salesforce] -modules wilt gebruiken, moet u een [!DNL Salesforce] -account hebben.

## Salesforce API-informatie

De Salesforce-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> &lbrace;{connection.instanceUrl}</td>
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v62,0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.15.14</td> 
  </tr>
 </tbody> 
 </table>

## Informatie over zoeken naar [!DNL Salesforce] -objecten

Bij het zoeken naar objecten kunt u afzonderlijke zoekwoorden invoeren of een complexere query maken met behulp van jokertekens en operatoren:

* Gebruik de asterisk wild card (\*) als vervanging voor nul of meer tekens. Als u bijvoorbeeld zoekt naar CA\*, worden items gevonden die met CA beginnen
* Wilde kaart met vraagteken gebruiken (?) als vervanging van één teken. Bijvoorbeeld, vindt een onderzoek naar Jo?n punten met de term John of Joan maar niet Jon
* Gebruik de operator voor aanhalingstekens (&quot; &quot;) om een exacte woordovereenkomst te zoeken. Bijvoorbeeld: &quot;Maandvergadering&quot;

Zie de [!DNL Salesforce] documentatie voor ontwikkelaars over SOQL en SOSL voor meer informatie over zoekmogelijkheden.

## Verbinding maken met [!DNL Salesforce]

Verbinding maken voor uw [!DNL Salesforce] -modules:

1. Klik in een willekeurige [!DNL Salesforce] -module op **[!UICONTROL Add]** naast het vak Verbinding.

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
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw Salesforce-client-id in.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw Salesforce-clientgeheim in. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Sandbox]</td>
        <td>Schakel deze optie in als dit een Sandbox-omgeving is.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL API Version]</td>
        <td>Voer de versie in van de Salesforce API die u wilt gebruiken. De standaardversie is 62.0.</td>
      </tr>
    </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.


## [!DNL Salesforce] modules en hun velden

* [&#x200B; Trekkers &#x200B;](#triggers)
* [&#x200B; Acties &#x200B;](#actions)
* [Zoekopdrachten](#searches)

### Triggers

* [[!UICONTROL Watch a field]](#watch-a-field)
* [[!UICONTROL Watch for Records]](#watch-for-records)
* [[!UICONTROL Watch Outbound Messages]](#watch-outbound-messages)

#### [!UICONTROL Watch a field]

Deze triggermodule start een scenario wanneer een veld wordt bijgewerkt in [!DNL Salesforce] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Selecteer het type record dat het veld bevat waarop de module moet letten. Kies een recordtype waarvoor [!UICONTROL Field History] is ingeschakeld in [!DNL Salesforce] . Voor meer informatie, zie <a href="https://help.salesforce.com/s/articleView?id=xcloud.tracking_field_history.htm&type=5"> het Volgen van de Geschiedenis van het Gebied </a> in de [!DNL Salesforce] documentatie. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td> <p>Selecteer de gebieden die u de module voor veranderingen wilt controleren. Beschikbare velden zijn afhankelijk van het geselecteerde recordtype.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal gebieden in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch for Records]

Deze triggermodule voert een scenario uit wanneer een record in een object wordt gemaakt of bijgewerkt. De module retourneert alle standaardvelden die zijn gekoppeld aan de record of records, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Selecteer het type [!DNL Salesforce] record dat u in de module wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Fields]</td> 
   <td>Selecteer de velden die u in de module wilt bekijken. Beschikbare velden zijn afhankelijk van het type record.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Bepaal of u het scenario alleen nieuwe records van het geselecteerde type wilt bekijken, of nieuwe records van het geselecteerde type en alle andere wijzigingen in records van dat type.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Outbound Messages]

Deze trekkermodule voert een scenario uit wanneer iemand een bericht verzendt. De module retourneert alle standaardvelden die zijn gekoppeld aan de record of records, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Voor deze module is extra installatie vereist. Er moet een Stroom zijn die voor uitgaande berichten wordt gevormd.

* Voor instructies op Stromen in Salesforce, zie [&#x200B; Taken met Stromen &#x200B;](https://help.salesforce.com/s/articleView?id=platform.flow.htm) in de documentatie van Salesforce automatiseren.
* Voor informatie bij het vormen van een uitgaand bericht in Salesforce, zie [&#x200B; een Uitgaand Bericht van Uw Verslag-teweeggebrachte Stroom &#x200B;](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_outbound_message.htm) in de documentatie van Salesforce verzenden

<!--

1. Go to the [!DNL Salesforce] setup page.

   To access the setup page, locate and click the button labeled "[!UICONTROL Setup]" in the upper-right hand corner of the [!DNL Salesforce] account. From the [!DNL Salesforce] setup page, locate the "[!UICONTROL Quick Find / Search]" bar on the left hand side. Search for "[!UICONTROL Workflow Rules]." 

1. Click **[!UICONTROL Workflow Rules]**. 
1. On the the [!UICONTROL Workflow Rules] page that appears, click **[!UICONTROL New Rule]** and select the object type the rule will apply to (such as "[!UICONTROL Opportunity]" if you are monitoring updates to Opportunity records).
1. Click **[!UICONTROL Next]**.
1. Set a rule name, evaluation criteria, and rule criteria, then click **[!UICONTROL Save]** and **[!UICONTROL Next]**.

1. Click **[!UICONTROL Done]**.
1. From the newly created Workflow rule, click **[!UICONTROL Edit]**..
1. From the **[!UICONTROL Add Workflow Action]** drop-down list, select **[!UICONTROL New Outbound Message]**.

1. Specify name, description, Endpoint URL, and fields you want to include in the new outbound message, then click **[!UICONTROL Save]**.

   The **[!UICONTROL Endpoint URL]** field contains the URL provided on the [!DNL Salesforce] [!UICONTROL Outbound Message] in Workfront Fusion.

1. Configure a scenario beginning with the [!UICONTROL Outbound Message] event. 

1. Click the **</>** icon in the bottom right and copy the provided URL.
1. Return to the **[!UICONTROL Workflow Rules]** page, locate the newly created rule, then click **[!UICONTROL Activate]**.

-->

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer de webhaak die u wilt gebruiken om uitgaande berichten te bekijken. Als u een webhaak wilt toevoegen, klikt u op <strong>[!UICONTROL Add]</strong> en voert u de naam en de verbinding van de webhaak in.</p> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies </a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Selecteer het type [!DNL Salesforce] record dat de module moet controleren voor uitgaande berichten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Fields]</td> 
   <td> <p>Selecteer de gebieden die u de module voor uitgaande berichten wilt letten. Beschikbare velden zijn afhankelijk van het type record.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Create a Record]](#create-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Download Attachment/Document]](#download-attachmentdocument)
* [[!UICONTROL Read a Record]](#read-a-record)
* [[!UICONTROL Upload Attachment/Document]](#upload-attachmentdocument)
* [Bestand uploaden](#upload-file)

#### [!UICONTROL Create a Record]

Deze actiemodule maakt een nieuwe record in een object.

In de module kunt u selecteren welke velden van het object beschikbaar zijn in de module. Dit vermindert het aantal gebieden u door moet scrollen wanneer vestiging de module.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>Selecteer het type [!DNL Salesforce] record dat u met de module wilt maken. Velden worden beschikbaar op basis van het type record dat is geselecteerd in het veld [!UICONTROL Record Type] . Deze velden zijn gebaseerd op de API van [!DNL Salesforce] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Selecteer de gebieden die u de module wilt vormen wanneer het creëren van het nieuwe verslag. De vereiste velden staan boven aan de lijst. </p> <p>De velden die u selecteert, worden geopend onder dit veld. U kunt nu waarden invoeren in deze velden.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Salesforce] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Salesforce] -modules kan worden uitgevoerd.

De module retourneert het volgende:

* **[!UICONTROL Status Code]** (nummer): Dit geeft aan of uw HTTP-aanvraag is geslaagd of mislukt. Dit zijn standaardcodes die u kunt opzoeken op internet.
* **[!UICONTROL Headers]** (object): een gedetailleerdere context voor de respons-/statuscode die geen betrekking heeft op de hoofdtekst van de uitvoer. Niet alle kopteksten in een antwoordkoptekst zijn reactiekoppen. Sommige koppen zijn daarom niet altijd even handig.

  De antwoordheaders zijn afhankelijk van de HTTP-aanvraag die u hebt gekozen bij het configureren van de module.

* **[!UICONTROL Body]** (object): afhankelijk van de HTTP-aanvraag die u hebt gekozen bij het configureren van de module, ontvangt u mogelijk gegevens terug. Die gegevens, zoals de gegevens van een [!UICONTROL GET] aanvraag, bevinden zich in dit object.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Ga een weg met betrekking tot <code> &lt;Instance URL&gt;/services/data/v62.0/</code> in.</p> <p>Voor de lijst van beschikbare eindpunten, verwijs naar de <a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm"> Gids van de Ontwikkelaar van de REST API van Salesforce </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object. Bijvoorbeeld <code>{"Content-type":"application/json"}</code> . Workfront Fusion voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object. Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
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

>[!BEGINSHADEBOX]

**Voorbeeld:** de volgende API vraag keert de lijst van alle gebruikers in uw [!DNL Salesforce] rekening terug:

* **URL**: `query`

* **Methode**: [!UICONTROL GET]

* **Koord van de Vraag**:

* **Sleutel**: `q`

* **Waarde**: `SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`

Overeenkomsten met de zoekopdracht vindt u in de sectie Uitvoer van de module onder **[!UICONTROL Bundle]> [!UICONTROL Body] >[!UICONTROL records]** .

In ons voorbeeld werden 6 gebruikers geretourneerd:

![&#x200B; Gelijken voor het onderzoek &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)

>[!ENDSHADEBOX]

#### [!UICONTROL Delete a Record]

Deze actiemodule verwijdert een bestaande record in een object.

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Selecteer het type [!DNL Salesforce] -record dat u wilt verwijderen door de module.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Voer de unieke [!DNL Salesforce] -id in of wijs deze toe aan de record die u wilt verwijderen door de module.</p> <p>Als u de id wilt ophalen, opent u het object [!DNL Salesforce] in uw browser en kopieert u de tekst aan het einde van de URL na de laatste schuine streep (/). Bijvoorbeeld: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download Attachment/Document]

Deze actiemodule downloadt een document of bijlage uit een record.

U geeft de id van de record op en het gewenste type download.

De module retourneert de id van de bijlage of het document en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Type of Download]</td>
    <td> <p>Geef het type bestand op dat u van Salesforce wilt downloaden.</p> 
     <ul> 
      <li>[!UICONTROL Attachment]</li> 
      <li>[!UICONTROL Document]</li> 
      <li>[!UICONTROL ContentDocument] (Dit is een document dat is geüpload naar een bibliotheek in [!DNL Saleforce CRM Content] of [!DNL Salesforce Files] .)</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[!UICONTROL ID] / </p> <p>[!UICONTROL Attachment ID] / </p> <p>[!UICONTROL ContentDocument ID]</p> </td>
    <td> <p>Voer de unieke [!DNL Salesforce] -id in of wijs deze toe aan de record die u wilt downloaden met de module.</p> <p>Als u de id wilt ophalen, opent u het object [!DNL Salesforce] in uw browser en kopieert u de tekst aan het einde van de URL na de laatste schuine streep (/). Bijvoorbeeld: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a Record]

Deze actiemodule leest gegevens van één object in [!DNL Salesforce] .

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Record Type]</td>
    <td>Selecteer het type [!DNL Salesforce] record dat u wilt lezen in de module.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Record Fields]</td>
    <td>Selecteer de velden die u in de module wilt lezen. U moet ten minste één veld selecteren. Beschikbare velden zijn afhankelijk van het type record.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL ID]</td>
    <td> <p>Voer de unieke [!DNL Salesforce] -id in of wijs deze toe aan de record die u wilt lezen in de module.</p> <p>Als u de id wilt ophalen, opent u het object [!DNL Salesforce] in uw browser en kopieert u de tekst aan het einde van de URL na de laatste schuine streep (/). Bijvoorbeeld: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Update a Record]

Deze actiemodule bewerkt een record in een object.

In de module kunt u selecteren welke velden van het object beschikbaar zijn in de module. Dit vermindert het aantal gebieden u door moet scrollen wanneer vestiging de module.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Voer de id in van de record die u wilt bijwerken of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>Selecteer het type [!DNL Salesforce] record dat u wilt bijwerken in de module. Velden worden beschikbaar op basis van het type record dat is geselecteerd in het veld Recordtype. Deze velden zijn gebaseerd op de API van [!DNL Salesforce] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Selecteer de gebieden die u de module wilt vormen wanneer het creëren van het nieuwe verslag. De vereiste velden staan boven aan de lijst. </p> <p>De velden die u selecteert, worden geopend onder dit veld. U kunt nu waarden invoeren in deze velden.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Upload Attachment/Document]

Deze actiemodule uploadt een bestand en koppelt het aan een record die u opgeeft, of uploadt een document.

De module retourneert de id van de bijlage of het document en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type of Upload]</td> 
   <td>Selecteer of u een bijlage of een document wilt uploaden in de module.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Voer de id in of wijs de id toe van het object waarnaar u een bijlage wilt uploaden.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td>Selecteer de map waarin u een document wilt uploaden. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Bestand uploaden

Deze actiemodule uploadt één bestand naar Salesforce.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL &#x200B; Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document linking]</td> 
   <td>Selecteer of u een koppeling naar een inhoudsdocument wilt toepassen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL linkedEntityId]</td> 
   <td>Als u documentkoppelingen gebruikt, voert u de id van het gekoppelde object in of wijst u deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ShareType]</td> 
   <td>Selecteer machtigingen voor het bestand als u documentkoppelingen gebruikt.<ul><li><b>Viewer-machtiging</b><p>De gebruiker kan het bestand weergeven.</p></li><li><b>Machtiging voor deelnemer</b><p>De gebruiker kan het bestand weergeven en bewerken.</p></li><li><b>Overgenomen machtigingen</b><p>Machtigingen zijn gebaseerd op de machtigingen van de gebruiker voor de verwante record, zoals een bibliotheek.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Als u documentkoppelingen gebruikt, voert u de zichtbaarheid van het document in of wijst u deze toe.<ul><li><b>AllUsers</b><p>Beschikbaar voor alle gebruikers met machtigingen</p></li><li><b>InternalUsers</b><p>Beschikbaar voor interne gebruikers met machtigingen.</p></li><li><b>SharedUsers</b><p>Beschikbaar voor gebruikers die de feed kunnen zien waarnaar het bestand is gepost.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

* [Zoeken](#search)
* [Zoeken met query](#search-with-query)

#### [!UICONTROL Search]

Deze actiemodule wint alle verslagen terug die aan een bepaalde criteria voldoen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL &#x200B; Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Selecteer het type object waarnaar u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Selecteer het veld waarnaar u wilt zoeken, de operator die u wilt gebruiken in de query en de waarde die u in het veld zoekt. U kunt vragen verbinden door EN of OF te gebruiken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de velden die u in de uitvoer van de module wilt opnemen. De velden zijn beschikbaar op basis van het recordtype.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Selecteer of u de module Alle Overeenkomende Verslagen, of het Eerste Overeenkomende slechts Verslag wilt terugkeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal]</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugwinnen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search with Query]

Deze zoekmodule zoekt naar records in een object in [!DNL Salesforce] dat overeenkomt met de zoekquery die u opgeeft. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Salesforce] rekening aan de Fusie van Workfront, zie <a href="#create-a-connection-to-salesforce"> een verbinding aan Salesforce </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search Type]</td> 
   <td> <p>Selecteer het type onderzoek u de module wilt uitvoeren:</p> 
    <ul> 
     <li> <p>[!UICONTROL Simple]</p> </li> 
     <li> <p>[!UICONTROL Using SOSL (Salesforce Object Search Language)]</p> </li> 
     <li> <p>[!UICONTROL Using SOQL (Salesforce Object Query Language)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Type] </p> </td> 
   <td> <p>Als u het eenvoudige zoektype hebt geselecteerd, kiest u het type [!DNL Salesforce] -record waarnaar u in de module wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] / [!UICONTROL SOSL Query] / [!UICONTROL SOQL Query]</td> 
   <td> <p>Voer de query in waarop u wilt zoeken.</p> <p>Voor meer informatie over SOSL, zie <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm"> Taal van het Onderzoek van de Objecten van Salesforce (SOSL) </a> in de [!DNL Salesforce] documentatie.</p> <p>Voor meer informatie over SOQL, zie <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm"> Taal van de Vraag van de Vraag van de Objecten van Salesforce (SOQL) </a> in de [!DNL Salesforce] documentatie.</p> <p>Nota: Gelieve te merken op dat de waarde van de parameter <code>RETURNING </code> de output van de module beïnvloedt. Als u <code>LIMIT</code> gebruikt, negeert [!DNL Fusion] de instellingen in het veld [!UICONTROL Maximal count of records] . Als u geen limiet instelt, voegt Fusion de waarde [!UICONTROL LIMIT = Maximal count of records] in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

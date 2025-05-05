---
title: Adobe Workfront-modules
description: Met de Adobe Workfront Fusion Adobe Workfront-connector kunt u uw processen in Workfront automatiseren. Als u een Workfront Fusion for Work Automation and Integration-licentie hebt, kunt u deze ook gebruiken om verbinding te maken met apps en services van derden.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: 6fa7ab493112351d9480b21b23b3b6b7b14f2230
workflow-type: tm+mt
source-wordcount: '7292'
ht-degree: 0%

---

# Adobe Workfront-modules

Met de Adobe Workfront Fusion Adobe Workfront-connector kunt u uw processen in Workfront automatiseren. U kunt Workfront ook verbinden met andere toepassingen en services.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Verouderd: alle </p>
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


>[!NOTE]
>
>* Als uw organisatie het oudere licentiepakket gebruikt (op basis van connectors), moet deze beschikken over een Workfront Fusion for Work Automation and Integration-licentie om verbinding te maken met apps en services van derden. De Workfront-aansluiting telt niet mee voor het aantal actieve apps dat beschikbaar is voor uw organisatie. Alle scenario&#39;s, zelfs als ze alleen de Workfront-app gebruiken, tellen wel mee voor het totale aantal scenario&#39;s van uw organisatie.

+++

## Workfront verbinden met Workfront Fusion

De Workfront-connector gebruikt OAuth 2.0 om verbinding te maken met Workfront.

U kunt rechtstreeks vanuit een Workfront Fusion-module een verbinding maken met uw Workfront-account.

1. In om het even welke module van Adobe Workfront, voegt de klik **naast het gebied van de Verbinding toe.**
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
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</p>
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

   Als u niet bij Workfront bent aangemeld, wordt u naar een aanmeldingsscherm geleid. Nadat u zich hebt aangemeld, kunt u de verbinding toestaan.

>[!NOTE]
>
>* OAuth 2.0-verbindingen met de Workfront API zijn niet langer afhankelijk van API-sleutels.
>* Als u een verbinding met een Workfront Sandbox-omgeving wilt maken, moet u in die omgeving een OAuth2-toepassing maken en vervolgens de client-id en het clientgeheim gebruiken die door die toepassing zijn gegenereerd in uw verbinding.

## Workfront-modules en hun velden

Wanneer u Workfront-modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen er aanvullende Workfront-velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Als de meest actuele velden in een Workfront-module niet worden weergegeven, kan dit worden veroorzaakt door cacheproblemen. Wacht een uur en probeer het opnieuw.
>* HTTP 429 statuscodes van Adobe Workfront moeten geen deactivaties veroorzaken, maar in plaats daarvan een korte uitvoeringspauze in het scenario teweegbrengen.

* [ Trekkers ](#triggers)
* [ Acties ](#actions)
* [Zoekopdrachten](#searches)

### Triggers

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Watch Events]**

Deze triggermodule voert in real-time een scenario uit wanneer objecten van een specifiek type worden toegevoegd, bijgewerkt of verwijderd in Workfront

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

1. Klik **[!UICONTROL Add]** aan het recht van de **doos Webhaak**.

1. Configureer de webhaak in het vak **[!UICONTROL Add a hook]** dat wordt weergegeven.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook name]</td> 
      <td>Geef een naam op voor de webhaak</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connection]</td> 
      <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Type]</td> 
      <td>Selecteer het type Workfront-record dat u in de module wilt bekijken.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL State]</td> 
      <td>Selecteer of u naar het oude of het nieuwe frame wilt kijken.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Trigger een scenario wanneer het verslag <b> in </b> een bepaalde waarde verandert.</p><p>Als de status bijvoorbeeld is ingesteld op [!UICONTROL New State] en het filter is ingesteld op [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress] , activeert de webhaak een scenario wanneer de [!UICONTROL Status] verandert in [!UICONTROL In Progress] , ongeacht wat de status daarvoor was. </p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Trigger een scenario wanneer het verslag <b> van </b> een bepaalde waarde verandert.</p><p>Als de status bijvoorbeeld is ingesteld op [!UICONTROL Old State] en het filter is ingesteld op [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress] , activeert de webhaak een scenario wanneer een [!UICONTROL Status] die momenteel [!UICONTROL In Progress] is, verandert in een andere status. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>U kunt filters instellen om alleen te controleren op records die voldoen aan de criteria die u selecteert.</p> <p>Voer voor elk filter het veld in dat door het filter moet worden geëvalueerd, de operator en de waarde die door het filter moet worden toegestaan. U kunt meer dan één filter gebruiken door EN regels toe te voegen.</p> <p><b> NOTA </b>: U kunt geen filters in bestaande websites van Workfront uitgeven. Als u verschillende filters wilt instellen voor Workfront-gebeurtenisabonnementen, verwijdert u de huidige webhaak en maakt u een nieuwe.</p> <p>Voor meer informatie over gebeurtenisfilters, zie <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref"> de abonnementfilters van de Gebeurtenis in Workfront &gt; [!UICONTROL Watch Events] modules </a> in dit artikel.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Exclusief gebeurtenissen die in dit verband worden gemaakt</td> 
      <td>Schakel deze optie in om gebeurtenissen uit te sluiten die zijn gemaakt of bijgewerkt met dezelfde connector die deze triggermodule gebruikt. Dit kan situaties verhinderen waar een scenario zich zou teweegbrengen, veroorzakend het om in een eindeloze lijn te herhalen.<p><b> NOTA </b>: Het type van het taakverslag omvat deze optie niet.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Origin]</td> 
      <td>
       <p>Kies of u het scenario wilt bekijken [!UICONTROL New Records Only], [!UICONTROL Updated Records Only], [!UICONTROL New and Updated Records] of [!DNL Deleted Records Only] .</p>
       <p><b> NOTA </b>: Als u [!UICONTROL New and Updated Records] kiest, leidt de WebHaak verwezenlijking tot 2 gebeurtenisabonnementen (voor het zelfde webhaakadres).</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Nadat WebHaak wordt gecreeerd, kunt u het adres van het eindpunt bekijken dat de gebeurtenissen worden verzonden naar.

Voor meer informatie, zie de sectie [ Voorbeelden van de Payloads van de Gebeurtenis ](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) in het Abonnement API van de artikelgebeurtenis in de documentatie van Workfront.

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++

+++ **[!UICONTROL Watch Field]**

Deze triggermodule voert een scenario uit wanneer een veld dat u opgeeft, wordt bijgewerkt. De module retourneert zowel de oude als de nieuwe waarde van het opgegeven veld. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record dat u in de module wilt bekijken.</p> <p>Selecteer bijvoorbeeld [!UICONTROL Task] als u wilt beginnen met het uitvoeren van het scenario telkens wanneer een recordveld in een taak wordt bijgewerkt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td>Selecteer het gebied dat u de module voor updates wilt letten. In deze velden staan de velden die uw Workfront-beheerder heeft ingesteld voor bijhouden.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td>Selecteer de objectvelden die u wilt opnemen in de uitvoerbundel voor deze module.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++

+++ **[!UICONTROL Watch Record]**

Deze triggermodule voert een scenario uit wanneer objecten van een specifiek type worden toegevoegd, bijgewerkt of beide. De module retourneert alle standaardvelden die zijn gekoppeld aan de record of records, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

In de uitvoer geeft de module aan of elke record nieuw of bijgewerkt is.

Records die zijn toegevoegd en bijgewerkt sinds de laatste keer dat het scenario werd uitgevoerd, worden geretourneerd als nieuwe records.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Kies of u het scenario wilt bekijken [!UICONTROL New Records Only], [!UICONTROL Updated Records Only] of [!UICONTROL New and Updated Records] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record dat u in de module wilt bekijken.</p> <p>Als u bijvoorbeeld elke keer dat een nieuw project wordt gemaakt het scenario wilt starten, selecteert u [!UICONTROL Project]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u wilt opnemen in de uitvoerbundel voor deze module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reference]</td> 
   <td> <p>Selecteer de referentievelden die u wilt opnemen in de uitvoerbundel voor deze module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de inzamelingsgebieden die u inbegrepen in de outputbundel voor deze module wilt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optional Filter]</td> 
   <td> <p>(Geavanceerd) Typ een API-codetekenreeks om aanvullende parameters of code te definiëren waarmee uw criteria worden verfijnen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++


### Handelingen

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL Convert object]**

Deze actiemodule maakt een van de volgende omzettingen:

* Probleem converteren naar project
* Probleem converteren naar taak
* Taak omzetten in project

>[!NOTE]
>
>Vanaf juli 2024 kunnen aangepaste formulieren worden opgenomen bij de conversie van een object.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Object type]</td> 
   <td> <p>Selecteer het type object dat u wilt omzetten. Dit is het type dat het object vóór de conversie heeft.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Convert to]</td> 
   <td>Selecteer het object waarnaar u het wilt omzetten. Dit is het type dat het object na de conversie heeft.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;Object> ID]</td> 
   <td> <p>Voer de id van het object in. </p> <p>Opmerking: wanneer u de id van een object opgeeft, kunt u de naam van het object beginnen te typen en het vervolgens in de lijst selecteren. De module gaat dan aangewezen identiteitskaart in het gebied in.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Template ID]</td> 
   <td> <p>Als u in een project omzet, selecteer identiteitskaart van het Malplaatje die u voor het project wilt gebruiken.</p> <p>Opmerking: wanneer u de id van een object opgeeft, kunt u de naam van het object beginnen te typen en het vervolgens in de lijst selecteren. De module gaat dan aangewezen identiteitskaart in het gebied in.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Custom forms]</td> 
   <td>Selecteer de aangepaste formulieren die u aan het nieuwe geconverteerde object wilt toevoegen en voer vervolgens waarden in voor de velden van het aangepaste formulier.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Options]</td> 
   <td> <p>Schakel de gewenste opties in wanneer u het object omzet. Welke opties beschikbaar zijn, is afhankelijk van het object waarnaar u converteert of van het object.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copy native fields]</td> 
   <td> <p>Schakel deze optie in om native velden van het oorspronkelijke object naar het nieuwe object te kopiëren.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copy custom forms]</td> 
   <td> <p>Schakel deze optie in om native velden van het oorspronkelijke object naar het nieuwe object te kopiëren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a record]**

In deze actiemodule wordt een object gemaakt, zoals een project, taak of uitgave in Workfront, en kunt u een aangepast formulier aan het nieuwe object toevoegen. In de module kunt u selecteren welke velden van het object beschikbaar zijn in de module.

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Zorg ervoor dat u het minimale aantal invoervelden opgeeft. Als u bijvoorbeeld een uitgave wilt maken, moet u een geldige bovenliggende project-id opgeven in het veld Project-id om aan te geven waar de uitgave in Workfront moet wonen. U kunt het toewijzingspaneel gebruiken om deze informatie van een andere module in uw scenario in kaart te brengen, of u kunt het manueel ingaan door in de naam te typen en dan het van de lijst te selecteren.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record dat de module moet maken.</p> <p>Als u bijvoorbeeld een project wilt maken, selecteert u [!UICONTROL Project] in de vervolgkeuzelijst.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Selecteer de velden die u beschikbaar wilt maken voor gegevensinvoer. Dit staat u toe om deze gebieden te gebruiken zonder het moeten door degenen scrollen u niet nodig hebt. Vervolgens kunt u gegevens in deze velden invoeren of toewijzen.</p> <p>Gebruik het veld <b>[!UICONTROL Attach Custom Form]</b> voor velden in aangepaste formulieren.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Attach Custom Form]</td> 
   <td>Selecteer de aangepaste formulieren die u aan het nieuwe object wilt toevoegen en voer vervolgens waarden voor die velden in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

>[!NOTE]
>
>* Wanneer u de id van een object opgeeft, kunt u de naam van het object beginnen te typen en het vervolgens in de lijst selecteren. De module gaat dan aangewezen identiteitskaart in het gebied in.
>* Wanneer u de tekst voor een aangepast veld of een [!UICONTROL Note] -object (Opmerking of Antwoord) invoert, kunt u HTML-tags in het [!UICONTROL Note Text] -veld gebruiken om RTF-tekst, zoals vette of cursieve tekst, te maken.
>

+++

+++ **[!UICONTROL Create Record (Legacy)]**

>[!IMPORTANT]
>
>Deze module is vervangen door de module Een record maken. Wij adviseren gebruikend die module in nieuwe scenario&#39;s.
>De bestaande scenario&#39;s die deze module gebruiken zullen blijven functioneren zoals verwacht. Deze module wordt in mei 2025 verwijderd uit de modulekiezer.

Deze actiemodule maakt een object, zoals een project, taak of uitgave in Workfront. In de module kunt u selecteren welke velden van het object beschikbaar zijn in de module.

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Zorg ervoor dat u het minimale aantal invoervelden opgeeft. Als u bijvoorbeeld een uitgave wilt maken, moet u een geldige bovenliggende project-id opgeven in het veld Project-id om aan te geven waar de uitgave in Workfront moet wonen. U kunt het toewijzingspaneel gebruiken om deze informatie van een andere module in uw scenario in kaart te brengen, of u kunt het manueel ingaan door in de naam te typen en dan het van de lijst te selecteren.

In deze module worden tijdens het maken van het object geen aangepaste formulieren gekoppeld. Met de module [!UICONTROL Create a record (attaching custom forms)] kunt u aangepaste formulieren toevoegen wanneer u een object maakt.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record dat de module moet maken.</p> <p>Als u bijvoorbeeld een project wilt maken, selecteert u [!UICONTROL Project] in de vervolgkeuzelijst.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>Selecteer de velden die u beschikbaar wilt maken voor gegevensinvoer. Dit staat u toe om deze gebieden te gebruiken zonder het moeten door degenen scrollen u niet nodig hebt.</td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

>[!NOTE]
>
>* Wanneer u de id van een object opgeeft, kunt u de naam van het object beginnen te typen en het vervolgens in de lijst selecteren. De module gaat dan aangewezen identiteitskaart in het gebied in.
>* Wanneer u de tekst voor een aangepast veld of een [!UICONTROL Note] -object (Opmerking of Antwoord) invoert, kunt u HTML-tags in het [!UICONTROL Note Text] -veld gebruiken om RTF-tekst, zoals vette of cursieve tekst, te maken.

+++

+++ **[!UICONTROL Custom API Call]**

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de Workfront API maken. Op deze manier kunt u een gegevensstroomautomatisering maken die niet door de andere Workfront-modules kan worden uitgevoerd.

De module retourneert de volgende informatie:

* **[!UICONTROL Status Code]** (nummer): Dit geeft aan of uw HTTP-aanvraag is geslaagd of mislukt. Dit zijn standaardcodes die u kunt opzoeken op internet.
* **[!UICONTROL Headers]** (object): een gedetailleerdere context voor de respons-/statuscode die geen betrekking heeft op de hoofdtekst van de uitvoer. Niet alle kopteksten in een antwoordkoptekst zijn reactiekoppen. Sommige koppen zijn daarom niet altijd even handig.

  De antwoordheaders zijn afhankelijk van de HTTP-aanvraag die u hebt gekozen bij het configureren van de module.

* **[!UICONTROL Body]** (object): afhankelijk van de HTTP-aanvraag die u hebt gekozen bij het configureren van de module, ontvangt u mogelijk gegevens terug. Deze gegevens, zoals de gegevens van een GET-aanvraag, bevinden zich in dit object.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Ga een weg met betrekking tot <code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code> in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Selecteer de versie van de Workfront API die de module moet gebruiken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes in de Fusie van Adobe Workfront </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object. Dit bepaalt het inhoudstype van het verzoek.</p> <p>Bijvoorbeeld:<code> {"Content-type":"application/json"}</code></p> <p>Opmerking: als u fouten krijgt en het moeilijk is om de oorsprong ervan te bepalen, kunt u overwegen koppen te wijzigen op basis van de documentatie van Workfront. Wanneer uw Aangepaste API-aanroep een HTTP-aanvraagfout van 422 retourneert, probeert u een header <code>"Content-Type":"text/plain"</code> te gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> <p>Tip: We raden u aan informatie via de JSON-hoofdtekst te verzenden in plaats van als queryparameters.</p> </td> 
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

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++

+++ **[!UICONTROL Delete Record]**

Met deze actiemodule verwijdert u een object, zoals een project, taak of uitgave in Workfront.

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Force delete]</td> 
   <td>Schakel deze optie in om ervoor te zorgen dat de record wordt verwijderd, zelfs als de Workfront-gebruikersinterface om bevestiging van de verwijdering zou vragen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Async delete]</td> 
   <td>Schakel deze optie in als u wilt dat de module asynchroon kan verwijderen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>Voer de unieke Workfront-id in van de record die u wilt verwijderen uit de module.</p> <p>Als u de id wilt ophalen, opent u het Workfront-object in uw browser en kopieert u de tekst aan het einde van de URL na "ID=". Bijvoorbeeld: https://my.workfront.com/project/view?ID=<i> 5e43010c03286a2a555e1d0a75d6a86e </i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>Selecteer het type Workfront-record dat u wilt verwijderen uit de module.</td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

>[!NOTE]
>
>Wij adviseren de volgende scenario configuratie om de mogelijkheid te vermijden dat verslagen niet wegens asynchrone verrichtingen worden geschrapt.
>
>1. Verwijder de record synchroon.
>1. Voeg foutafhandeling toe aan de module Record verwijderen om de fout te negeren die wordt veroorzaakt door de 40 tweede time-out.


+++

+++ **[!UICONTROL Download Document]**

Deze actiemodule downloadt een document uit Workfront.

U geeft de id van de record op.

De module retourneert de inhoud, de bestandsnaam, de bestandsextensie en de bestandsgrootte van het document. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Document ID]</td> 
   <td> <p>Voer de unieke Workfront-id in van het document dat u wilt downloaden of voer deze handmatig in.</p> <p>Als u de id wilt ophalen, opent u het Workfront-object in uw browser en kopieert u de tekst aan het einde van de URL na "ID=". Bijvoorbeeld: https://my.workfront.com/project/view?ID=<i> 5e43010c03286a2a555e1d0a75d6a86e </i></p> </td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++

+++ **[!UICONTROL Misc Action]**

Met deze actiemodule kunt u handelingen uitvoeren met de API.

>[!NOTE]
>
>Vanaf juli 2024 bevat de handeling `convertToProject` het veld `copyCategories` . Als u deze instelt op `TRUE` , worden aangepaste formulieren opgenomen in het project waarnaar de uitgave wordt geconverteerd.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record waarmee de module moet communiceren.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Action]</td> 
   <td> <p>Selecteer de actie u de module wilt uitvoeren.</p> <p>Afhankelijk van de opties [!UICONTROL Record Type] en [!UICONTROL Action] die u kiest, moet u mogelijk extra velden invullen. Sommige combinaties van deze twee instellingen vereisen mogelijk alleen een record-id, terwijl andere (zoals Project voor de <strong>[!UICONTROL Record Type]</strong> en [!UICONTROL Attach Template] for the <strong>[!UICONTROL Action]</strong> ) aanvullende informatie vereisen (zoals een object-id en een sjabloon-id).</p><p>Voor opties beschikbaar aan sommige acties, zie <a href="#misc-action-options" class="MCXref xref"> Diverse actieopties </a> in dit artikel.</p> <p>Voor details over individuele gebieden, zie de <a href="http://developer.workfront.com/"> de ontwikkelaarsdocumentatie van Workfront </a>. <p><strong> Nota </strong>: De plaats van de ontwikkelaardocumentatie omvat informatie slechts door API versie 14, maar bevat nog waardevolle informatie voor API vraag. </p> 
    <ol> 
     <li value="1"> <p>Selecteer het recordtype in de linkernavigatie op de documentatiepagina voor Workfront-ontwikkelaars. De volgende typen hebben hun eigen pagina's:</p> 
      <ul> 
       <li> <p>[!UICONTROL Projects]</p> </li> 
       <li> <p>[!UICONTROL Tasks]</p> </li> 
       <li> <p>[!UICONTROL Issues]</p> </li> 
       <li> <p>[!UICONTROL Users]</p> </li> 
       <li> <p>[!UICONTROL Documents]</p> </li> 
      </ul> <p>Selecteer <b>[!UICONTROL Other objects and endpoints]</b> voor alle andere recordtypen en zoek het recordtype op de alfabetische gesorteerde pagina's.</p> </li> 
     <li value="2"> <p>Zoek op de pagina van het juiste recordtype naar de handeling (Ctrl-F of Cmd-F).</p> </li> 
     <li value="3"> <p>Beschrijvingen weergeven voor beschikbare velden onder de geselecteerde handeling.</p> </li> 
    </ol> <p>Opmerking:  <p>Als u een proefdruk maakt via de Workfront [!UICONTROL Misc Action] -module, kunt u het beste een proefdruk maken zonder geavanceerde opties en de proefdruk vervolgens bijwerken met de [!DNL Workfront Proof] SOAP API.</p><p>Voor meer informatie bij het creëren van een proef met Workfront API (die deze module gebruikt), zie <a href="https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref"> geavanceerde het proefdrukken opties wanneer het creëren van een proef door Adobe Workfront API </a> toevoegen</p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>Voer de unieke Workfront-id in of wijs deze toe aan de record waarmee de module moet communiceren.<p>Als u de id wilt ophalen, opent u het Workfront-object in uw browser en kopieert u de tekst aan het einde van de URL na "ID=". Bijvoorbeeld: https://my.workfront.com/project/view?ID=<i> 5e43010c03286a2a555e1d0a75d6a86e </i></p></td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

#### Handelingsopties

##### Taak

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Handeling</th> 
   <th>Opties</th> 
  </tr> 
  <tr> 
   <td>Kopiëren</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignment</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Wist financiële gegevens</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Hiermee wist u herinneringsmeldingen</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Verplaatsen</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignment</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Wist financiële gegevens</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Hiermee wist u herinneringsmeldingen</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### Probleem

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Handeling</th> 
   <th>Opties</th> 
  </tr> 
  <tr> 
   <td>Kopiëren</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignment</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearPermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Omzetten in taak</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Behoud het oorspronkelijke probleem en koppel zijn resolutie aan deze taak</p></li>
   <li>preservePrimaryContact<p>De primaire contactpersoon van de problemen toegang geven tot deze taak</p></li>
   <li>preserveCompletionDate<p>Behoud de geplande afsluitdatum van de uitgave</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Omzetten in project</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Behoud het oorspronkelijke probleem en koppel zijn resolutie aan deze taak</p></li>
   <li>preservePrimaryContact<p>De primaire contactpersoon van de problemen toegang geven tot deze taak</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### Project

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Handeling</th> 
   <th>Opties</th> 
  </tr> 
  <tr> 
   <td>Kopiëren</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignment</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Wist financiële gegevens</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Hiermee wist u herinneringsmeldingen</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Sjabloon bijvoegen / Opslaan als sjabloon</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignment</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverables<p>Duidelijke doelstellingen</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Wist financiële gegevens</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>Wist wachtrijeigenschappen en configuratie van problemen</p></li>
   <li>clearPredecessors</li>
   <li>clearRisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>Hiermee wist u herinneringsmeldingen</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Read a Record]**

Deze actiemodule haalt gegevens op uit één record.

U geeft de id van de record op. U kunt ook opgeven welke verwante records u in de module wilt lezen.

Bijvoorbeeld, als het verslag dat de module leest een project is, kunt u specificeren dat u de taken van het project wilt lezen.

De module retourneert een array met gegevens uit de uitvoervelden die u hebt opgegeven.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>

<td>Kies het Workfront-objecttype dat u wilt lezen in de module.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>

<td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Output Custom Form]</td>
     <td> <p>Selecteer de aangepaste formulieren die u in de uitvoerbundel voor deze module wilt opnemen en selecteer vervolgens de specifieke velden uit de aangepaste formulieren die u in de uitvoer wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Selecteer de verwijzingsvelden die u in de uitvoer wilt opnemen.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Selecteer de verwijzingsvelden die u in de uitvoer wilt opnemen.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Voer de unieke Workfront-id in van de record die de module moet lezen.</p> <p>Als u de id wilt ophalen, opent u het Workfront-object in uw browser en kopieert u de tekst aan het einde van de URL na "ID=". Bijvoorbeeld: https://my.workfront.com/project/view?ID=<i> 5e43010c03286a2a555e1d0a75d6a86e </i></p> </td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++

+++ **[!UICONTROL Read a Record (Legacy)]**

>[!IMPORTANT]
>
>Deze module is vervangen door de module Een record lezen. Wij adviseren gebruikend die module in nieuwe scenario&#39;s.
>De bestaande scenario&#39;s die deze module gebruiken zullen blijven functioneren zoals verwacht. Deze module wordt in mei 2025 verwijderd uit de modulekiezer.

Deze actiemodule haalt gegevens op uit één record.

U geeft de id van de record op. U kunt ook opgeven welke verwante records u in de module wilt lezen.

Bijvoorbeeld, als het verslag dat de module leest een project is, kunt u specificeren dat u de taken van het project wilt lezen.

De module retourneert een array met gegevens uit de uitvoervelden die u hebt opgegeven.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>

<td>Kies het Workfront-objecttype dat u wilt lezen in de module.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>

<td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Selecteer de verwijzingsvelden die u in de uitvoer wilt opnemen.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Selecteer de verwijzingsvelden die u in de uitvoer wilt opnemen.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Voer de unieke Workfront-id in van de record die de module moet lezen.</p> <p>Als u de id wilt ophalen, opent u het Workfront-object in uw browser en kopieert u de tekst aan het einde van de URL na "ID=". Bijvoorbeeld: https://my.workfront.com/project/view?ID=<i> 5e43010c03286a2a555e1d0a75d6a86e </i></p> </td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++

+++ **de Versie van het Laden van de Gebeurtenissen van de Update**

Workfront heeft onlangs een nieuwe versie van zijn service voor gebeurtenisabonnementen uitgebracht. De nieuwe versie is geen wijziging in de Workfront API, maar een wijziging in de functionaliteit voor abonnementen voor gebeurtenissen. Deze actiemodule werkt de versie bij van de gebeurtenislading die voor dit scenario wordt gebruikt.

Voor meer informatie over de nieuwe versie van het gebeurtenisabonnement, zie [ het abonnementversioning van de Gebeurtenis ](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) in de documentatie van Workfront

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Version]</td> 
   <td> Selecteer de versie van het gebeurtenisabonnement die u voor deze lading wilt gebruiken. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **werk een verslag** bij


Deze actiemodule werkt een voorwerp, zoals een project, een taak, of een kwestie bij. In de module kunt u selecteren welke velden van het object beschikbaar zijn in de module.

U geeft de id van de record op.

De module retourneert de id van het object en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Voer de unieke Workfront-id in van de record die de module moet bijwerken.</p> <p>Als u de id wilt ophalen, opent u het Workfront-object in uw browser en kopieert u de tekst aan het einde van de URL na "ID=". Bijvoorbeeld: https://my.workfront.com/project/view?ID=<i> 5e43010c03286a2a555e1d0a75d6a86e </i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record dat de module moet bijwerken.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Selecteer de velden die u beschikbaar wilt maken voor gegevensinvoer. Dit staat u toe om deze gebieden te gebruiken zonder het moeten door degenen scrollen u niet nodig hebt. Vervolgens kunt u gegevens in deze velden invoeren of toewijzen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>Selecteer de aangepaste formulieren waarvoor u veldwaarden voor de nieuwe record wilt opgeven. Nadat u het formulier hebt geselecteerd, voert u de gegevens in voor de velden op dat formulier.<p> Als u veldwaarden wilt opgeven voor een formulier dat u in deze module bijvoegt, neemt u de aangepaste formulier-id op in de velden voor de sectie Toewijzing.</td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

>[!NOTE]
>
> Wanneer u de tekst voor een aangepast veld of een [!UICONTROL Note] -object (Opmerking of Antwoord) invoert, kunt u HTML-tags in het [!UICONTROL Note Text] -veld gebruiken om RTF-tekst, zoals vette of cursieve tekst, te maken.


+++

+++ **[!UICONTROL Update Record (Legacy)]**

>[!IMPORTANT]
>
>Deze module is vervangen met Update een verslagmodule. Wij adviseren gebruikend die module in nieuwe scenario&#39;s.
>De bestaande scenario&#39;s die deze module gebruiken zullen blijven functioneren zoals verwacht. Deze module wordt in mei 2025 verwijderd uit de modulekiezer.

Deze actiemodule werkt een voorwerp, zoals een project, een taak, of een kwestie bij. In de module kunt u selecteren welke velden van het object beschikbaar zijn in de module.

U geeft de id van de record op.

De module retourneert de id van het object en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Voer de unieke Workfront-id in van de record die de module moet bijwerken.</p> <p>Als u de id wilt ophalen, opent u het Workfront-object in uw browser en kopieert u de tekst aan het einde van de URL na "ID=". Bijvoorbeeld: https://my.workfront.com/project/view?ID=<i> 5e43010c03286a2a555e1d0a75d6a86e </i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record dat de module moet bijwerken.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Selecteer de velden die u beschikbaar wilt maken voor gegevensinvoer. Dit staat u toe om deze gebieden te gebruiken zonder het moeten door degenen scrollen u niet nodig hebt. Vervolgens kunt u gegevens in deze velden invoeren of toewijzen.</td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

>[!NOTE]
>
>* Wanneer u de id van een object opgeeft, kunt u de naam van het object beginnen te typen en het vervolgens in de lijst selecteren. De module gaat dan aangewezen identiteitskaart in het gebied in.
>* Wanneer u de tekst voor een aangepast veld of een [!UICONTROL Note] -object (Opmerking of Antwoord) invoert, kunt u HTML-tags in het [!UICONTROL Note Text] -veld gebruiken om RTF-tekst, zoals vette of cursieve tekst, te maken.

+++

+++ **[!UICONTROL Upload Document]**

Deze actiemodule uploadt een document naar een Workfront-object, zoals een project, taak of uitgave. Deze module uploadt het document in delen, waardoor het uploadproces voor Workfront soepeler verloopt.

Deze module kan grotere bestanden verwerken dan de oudere module en maakt deel uit van een gefaseerde uitrol naar organisaties met een Ultimate Workfront-pakket.

U geeft de locatie voor het document, het bestand dat u wilt uploaden en een optionele nieuwe naam voor het bestand op.

De module retourneert de id van het document en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Voer de unieke Workfront-id in van de record waarnaar u het document wilt uploaden.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Selecteer het type Workfront-record waarin u het document wilt uploaden door de module.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Afhankelijk van het type verwante record moet u mogelijk een map-id invoeren of toewijzen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++

+++ **[!UICONTROL Upload Document (Legacy)]**

Deze actiemodule uploadt een document naar een Workfront-object, zoals een project, taak of uitgave. Het gehele document tegelijk uploadt.

U geeft de locatie voor het document, het bestand dat u wilt uploaden en een optionele nieuwe naam voor het bestand op.

De module retourneert de id van het document en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Voer de unieke Workfront-id in van de record waarnaar u het document wilt uploaden.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Selecteer het type Workfront-record waarin u het document wilt uploaden door de module.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Afhankelijk van het type verwante record moet u mogelijk een map-id invoeren of toewijzen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

Zie een lijst van de objecten van Workfront types waarvoor u deze module in [ objecten van Workfront beschikbaar voor elke module van Workfront ](#workfront-object-types-available-for-each-workfront-module) kunt gebruiken.

+++

### Zoekopdrachten

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Read Related Records]**

Deze zoekmodule leest records die overeenkomen met de zoekquery die u opgeeft, in een bepaald bovenliggend object.

U geeft op welke velden u wilt opnemen in de uitvoer. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type bovenliggende record (Workfront-object) waarvan u de gekoppelde records wilt lezen.</p> <p>Zie een lijst van de objecten van Workfront types waarvoor u deze module in <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref"> objecten van Workfront beschikbaar voor elke module van Workfront </a> in dit artikel kunt gebruiken.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Parent Record ID]</td> 
   <td> <p>Voer de id in van de bovenliggende record waarvan u de gekoppelde records wilt lezen of wijs deze toe.</p> <p>Als u de id wilt ophalen, opent u het Workfront-object in uw browser en kopieert u de tekst aan het einde van de URL na "ID=". Bijvoorbeeld: https://my.workfront.com/project/view?ID=<i> 5e43010c03286a2a555e1d0a75d6a86e </i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Selecteer of wijs het type van kindverslag toe dat u de module wilt lezen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search]**

Deze zoekmodule zoekt naar records in een object in Workfront die overeenkomen met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record waarnaar de module moet zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom forms list]</td> 
   <td> <p>Selecteer ten minste één aangepast formulier. Velden van deze aangepaste formulieren zijn beschikbaar voor de zoekopdracht.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Selecteer een optie om op te geven of u wilt dat de module het eerste resultaat ophaalt dat overeenkomt met uw zoekcriteria of dat alle resultaten overeenkomen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria fields]</td> 
   <td> <p>Selecteer de velden die u voor de zoekcriteria wilt gebruiken. Deze velden zijn dan beschikbaar in het vervolgkeuzemenu Zoekcriteria.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Voer het veld in waarnaar u wilt zoeken, de operator die u in de query wilt gebruiken en de waarde waarnaar u in het veld zoekt.</p> <p>Opmerking: gebruik <code>username </code> niet in de zoekcriteria. Als u <code>username </code> opneemt in een API-query naar Workfront, wordt de gebruiker aangemeld bij Workfront en wordt de zoekopdracht niet uitgevoerd.</p> <p>Opmerking: <code>In</code> en <code>NotIn</code> werken met arrays. De invoer moet een arrayindeling hebben.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u in de uitvoer voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Selecteer de verwijzingsvelden die u in de zoekopdracht wilt opnemen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Selecteer de verzamelingen die u aan de zoekopdracht wilt toevoegen.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search (Legacy)]**

>[!IMPORTANT]
>
>Deze module is vervangen door de module Zoeken in records. Wij adviseren gebruikend die module in nieuwe scenario&#39;s.
>De bestaande scenario&#39;s die deze module gebruiken zullen blijven functioneren zoals verwacht. Deze module wordt in mei 2025 verwijderd uit de modulekiezer.

Deze zoekmodule zoekt naar records in een object in Workfront die overeenkomen met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw Workfront app aan Workfront Fusion, zie <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref"> Workfront met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type Workfront-record waarnaar de module moet zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Selecteer een optie om op te geven of u wilt dat de module het eerste resultaat ophaalt dat overeenkomt met uw zoekcriteria of dat alle resultaten overeenkomen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria fields]</td> 
   <td> <p>Selecteer de velden die u voor de zoekcriteria wilt gebruiken. Deze velden zijn dan beschikbaar in het vervolgkeuzemenu Zoekcriteria.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Voer het veld in waarnaar u wilt zoeken, de operator die u in de query wilt gebruiken en de waarde waarnaar u in het veld zoekt.</p> <p>Opmerking: gebruik <code>username </code> niet in de zoekcriteria. Als u <code>username </code> opneemt in een API-query naar Workfront, wordt de gebruiker aangemeld bij Workfront en wordt de zoekopdracht niet uitgevoerd.</p> <p>Opmerking: <code>In</code> en <code>NotIn</code> werken met arrays. De invoer moet een arrayindeling hebben.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u in de uitvoer voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Selecteer de verwijzingsvelden die u in de zoekopdracht wilt opnemen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Selecteer de verzamelingen die u aan de zoekopdracht wilt toevoegen.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## Workfront-objecttypen beschikbaar voor elke Workfront-module

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**types van Objecten beschikbaar voor elke de trekkermodule van Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Watch Record]</th> 
   <th>[!UICONTROL Watch Field]</th> 
   <th>[!UICONTROL Watch Events]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Goedkeuringsproces</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Toewijzing</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Basislijn</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Factureringsrecord </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Factureringsgraad</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Bedrijf</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dashboard</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Document</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documentmap</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Documentaanvraag</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Documentversie</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Kosten</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Type uitgave</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Groep</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Uur</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Uurtype</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Probleem</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iteratie</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Functie</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Dagboekinvoer</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Mijlsteen</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Mijlpad</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Opmerking</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Notititietag</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programma</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Project</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projectgebruiker</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Goedkeuring proefdrukken</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Gereserveerde tijd* </td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Rapport</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Risico</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type risico</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Stap fiatteur</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taak</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Sjabloon</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Sjabloontaak</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tijdschema</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Gebruiker</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Bijwerken</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**de types van Objecten beschikbaar voor elke de actiemodule van Workfront**

>[!NOTE]
>
>De module [!UICONTROL Download Document] is niet opgenomen in deze tabel omdat objecttypen in Workfront geen deel uitmaken van de configuratie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Create a record]</th> 
   <th>[!UICONTROL Update a record]</th> 
   <th>[!UICONTROL Delete a record]</th> 
   <th>[!UICONTROL Upload Document]</th> 
   <th>[!UICONTROL Read a record]</th> 
   <th>[!UICONTROL Custom API Call]</th> 
   <th>[!UICONTROL Misc Action]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Goedkeuringsproces</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Toewijzing</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Basislijn</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>Factureringsrecord</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Factureringsgraad</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Bedrijf</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Document</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documentmap</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documentversie</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Wisselkoers</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Kosten</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Type uitgave</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Extern document</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Groep</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Uur</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Uurtype</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Probleem</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iteratie</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Functie</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Dagboekinvoer</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Mijlsteen</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Mijlpad</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Opmerking</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Notititietag</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programma</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Project</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projectgebruiker</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Gereserveerde tijd* </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risico</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type risico</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Stap fiatteur</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taak</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Sjabloon</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Sjabloontaak</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tijdschema</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Gebruiker</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Bijwerken</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**de types van Objecten beschikbaar voor elke het onderzoeksmodule van Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Search]</th> 
   <th>[!UICONTROL Read Related Records]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Goedkeuringsproces</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Toewijzing</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Factureringsrecord</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Factureringsgraad</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Bedrijf</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Document</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documentmap</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documentversie</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Kosten</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type uitgave</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Groep</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Uur</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Uurtype</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Probleem</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iteratie</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Functie</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Dagboekinvoer</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Mijlsteen</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Mijlpad</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Opmerking</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Notititietag</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programma</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Project</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projectgebruiker</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Gereserveerde tijd* </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risico</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type risico</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Stap fiatteur</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taak</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Sjabloon</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Sjabloontaak</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tijdschema</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Gebruiker</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Gebruikersdelegatie</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

Wij adviseren dat u tweemaal controleert om ervoor te zorgen dit werkt zoals u het zou verwachten.

+++

## Abonnementsfilters voor gebeurtenissen in de Workfront > [!UICONTROL Watch Events] -modules

>[!NOTE]
>
>We raden u ten zeerste aan filters voor gebeurtenisabonnementen in uw [!UICONTROL Watch Events] -modules te gebruiken.

De Workfront [!UICONTROL Watch Events] -module activeert scenario&#39;s op basis van een webhaak die een gebeurtenisabonnement maakt in de Workfront API. Het gebeurtenisabonnement is een gegevensset die bepaalt welke gebeurtenissen naar de webhaak worden verzonden. Als u bijvoorbeeld een module [!UICONTROL Watch Events] instelt die op problemen let, verzendt het gebeurtenisabonnement alleen gebeurtenissen die met problemen te maken hebben.

Door gebeurtenisabonnementfilters te gebruiken, kunnen Fusion-gebruikers gebeurtenisabonnementen maken die beter geschikt zijn voor hun gebruik. U kunt bijvoorbeeld een gebeurtenisabonnement instellen in de Workfront API om alleen problemen te verzenden die zich in een specifiek project bevinden naar de webhaak. Zo zorgt u ervoor dat de module [!UICONTROL Watch Events] alleen wordt geactiveerd voor problemen in dat project. De mogelijkheid om smallere triggers te maken verbetert het ontwerp van scenario&#39;s door het aantal irrelevante triggers te verminderen.

Dit is anders dan het instellen van een filter in het Workfront Fusion-scenario. Zonder een gebeurtenisabonnementfilter ontvangt uw webhaak alle gebeurtenissen die betrekking hebben op het objecttype dat u selecteert. De meeste van deze gebeurtenissen zijn niet relevant voor het scenario en moeten worden uitgefilterd voordat het scenario kan worden voortgezet.

De volgende operatoren zijn beschikbaar in het filter Workfront > Watch-gebeurtenissen:

* Gelijk
* Niet gelijk
* Groter dan
* Minder dan
* Groter dan of gelijk aan
* Kleiner dan of gelijk aan
* Bevat
* Exists
   * Deze operator heeft geen waarde nodig en het waardeveld ontbreekt.
* Is niet bestaand
   * Deze operator heeft geen waarde nodig en het waardeveld ontbreekt.
* Gewijzigd
   * Deze operator heeft geen waarde nodig en het waardeveld ontbreekt.
   * Deze operator negeert het veld Frame.
   * Wanneer het gebruiken van `Changed`, selecteer **Bijgewerkte Gebeurtenissen slechts** op het **gebied van de Oorsprong van het Verslag**.

>[!IMPORTANT]
>
>U kunt filters niet bewerken in bestaande Workfront-websites. Als u verschillende filters wilt instellen voor Workfront-gebeurtenisabonnementen, verwijdert u de huidige webhaak en maakt u een nieuwe.

>[!INFO]
>
>**Voorbeeld:** overweeg een scenario dat nieuwe kwesties verwerkt die aan een specifieke gebruiker, Ana worden toegewezen.
>
>### Gebeurtenissen filteren met behulp van een gebeurtenisabonnementfilter (aanbevolen)
>
>Met het gebeurtenisfilter kunt u de webhaak zo instellen dat het scenario wordt geactiveerd wanneer een uitgave aan Ana wordt toegewezen wanneer de uitgave wordt gemaakt. Ana heeft de gebruikersnaam b378489d8f7cd3cee0539260720a84b7.
>
>![ de filter van de Gebeurtenis ](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>Als 100 kwesties in een dag worden gecreeerd, maar slechts twee van hen worden toegewezen aan Ana, zou het scenario tweemaal uitvoeren.
>
>### Gebeurtenissen filteren in het scenario (niet aanbevolen)
>
>Als u gebeurtenissen wilt filteren zodat alleen uitgaven worden verwerkt die aan Ana zijn toegewezen, kunt u een filter maken na de module [!UICONTROL Watch Events] .
>
>![ Zonder gebeurtenisfilter ](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>Als er in een dag 100 problemen worden gemaakt, maar slechts twee ervan worden toegewezen aan Ana, wordt het scenario 100 keer uitgevoerd. 98 van de uitvoeringen zouden bij de filter ophouden, maar de trekkermodule verbruikt nog steeds gegevens en voert bewerkingen uit in alle uitvoeringen.

Voor meer informatie over de gebeurtenisabonnementen van Workfront, zie [ FAQs - de Abonnementen van de Gebeurtenis ](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq).

Voor meer informatie over websites, zie [ Onmiddellijke trekkers (webhooks) in de Fusie van Adobe Workfront ](/help/workfront-fusion/references/modules/webhooks-reference.md)

Voor meer informatie over filters in scenario&#39;s, zie [ een filter aan een scenario ](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md) toevoegen.

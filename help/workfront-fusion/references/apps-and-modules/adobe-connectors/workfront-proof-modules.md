---
title: Workfront Proof-modules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die  [!DNL Workfront Proof] gebruiken, evenals het verbinden met veelvoudige derdetoepassingen en de diensten.
author: Becky
feature: Workfront Fusion, Workfront Proof, Digital Content and Documents
exl-id: 9e556ae5-e672-4872-9c40-8c8e5f0305be
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '2724'
ht-degree: 0%

---

# [!DNL Workfront Proof] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Workfront Proof] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Dit is handig als u taken wilt uitvoeren die momenteel niet worden ondersteund voor proefdrukken in Workfront of in [!DNL Workfront Proof] , zoals het bijwerken van proefdrukken op basis van bepaalde gebeurtenissen en het zoeken naar ontvangers van een proefdruk.

De aansluiting van [!DNL Workfront Proof] telt niet mee voor het aantal actieve apps dat beschikbaar is voor uw organisatie. Alle scenario&#39;s, zelfs als ze alleen de [!DNL Workfront Proof] -app gebruiken, tellen niet mee voor het totale aantal scenario&#39;s van uw organisatie.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

+++## Workfront Proof-gegevens

De Workfront Proof-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> 21.3.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.8.92</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Workfront Proof] met Workfront Fusion

U kunt rechtstreeks vanuit een Workfront Fusion-module verbinding maken met uw [!DNL Workfront Proof] -account.

1. In om het even welke module van de Fusie van Workfront, klik [!UICONTROL **toevoegen**] naast het [!UICONTROL Connection] gebied

2. Vul de volgende velden in:

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name]</p>
                </td>
                <td>Voer een naam in voor de verbinding.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Environment]</td>
                <td>Selecteer of dit een productieomgeving of een niet-productieomgeving zoals Voorvertoning of Sandbox is.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Type]</td>
                <td>Selecteer of dit een serviceaccount of een persoonlijke account is.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Email / Username]</td>
                <td>Voer een gebruikersnaam in voor uw [!DNL Workfront Proof] -account.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Password]</td>
                <td>Voer het wachtwoord voor uw [!DNL Workfront Proof] -account in.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Tenant ID]</td>
                <td><strong> Nota </strong>: De klanten die geen BYOK gebruiken moeten dit gebied leeg verlaten. <p>Voer de id van de huurder voor dit account in. Neem contact op met Customer Support van Workfront als je hulp nodig hebt bij het zoeken naar je huurnummer.</p></td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Domain Extension]</td>
                <td>Voer de extensie in voor de URL waarmee u toegang krijgt tot uw account. <p>Voorbeeld: <code>com</code> of <code>eu</code></p></td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Production, Preview, or Custom Environment]</td>
                <td>De productie, voorproef, of douanemilieu dat u met wilt verbinden.</td>
            </tr>
        </tbody>
    </table>


3. Klik [!UICONTROL **verdergaan**] om de verbinding te bewaren en aan de module terug te keren

## [!DNL Workfront Proof] modules en hun velden

Wanneer u [!DNL Workfront Proof] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Workfront Proof] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

* [Overzicht van PDF bekijken](#watch-for-pdf-summary)
* [[!UICONTROL Watch Proof Activity]](#watch-proof-activity)
* [Proefdrukken controleren](#watch-proofs)

#### [!UICONTROL Watch for PDF Summary]

Deze instant triggermodule voert een scenario uit wanneer iemand een PDF-overzicht maakt voor een proefdruk.

In deze module is een webhaak vereist.

De module retourneert alle standaardvelden die aan de proefdruk zijn gekoppeld, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. Er wordt ook een nieuw gebeurtenisabonnement voor PDF-overzichten gemaakt en de inhoud van het kenmerk `pdf_url` dat in de payload wordt verzonden, wordt uitgevoerd. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook name]</td> 
   <td>Voer een naam in of wijs een naam toe aan de nieuwe webhaak</td> 
  </tr> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Proof Activity]

Deze triggermodule voert een scenario uit waarin een bepaalde activiteit plaatsvindt op een proefdruk.

De module retourneert alle standaardvelden die aan de proefdruk zijn gekoppeld, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. Er wordt ook een nieuw gebeurtenisabonnement voor PDF-overzichten gemaakt en de inhoud van het kenmerk `pdf_url` dat in de payload wordt verzonden, wordt uitgevoerd. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Activity type]</td> 
   <td>Selecteer of u een nieuwe beslissing wilt bekijken (inclusief wijzigingen in de proefdrukstatus) of alleen wijzigingen in de proefdrukstatus.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Proofs]

Deze geplande trekkermodule voert een scenario uit wanneer iemand creeert of een besluit over een bewijs neemt.

De module keert een lijst van alle verslagen terug het tijdens de periode vindt u, samen met hun types specificeert. De waarde van de velden die u opgeeft, wordt ook geretourneerd. Als de module besluiten vond die op het bewijs werden gemaakt, omvat het zowel de vorige als de huidige waarden, in afzonderlijke gebieden. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Dit gebeurt op een regelmatig gepland interval dat u specificeert.

U moet over voldoende rechten beschikken om toegang te krijgen tot de proefdrukken of proefdrukken in [!DNL Workfront Proof] om deze gegevens op te halen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td>Selecteer of u op nieuwe proefdrukken of op nieuwe algemene proefdrukbeslissingen wilt letten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Limiet</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Items per pagina</td> 
   <td> <p>Als u resultaten wilt pagineren, voert u in of wijst u het aantal geretourneerde resultaten toe dat op elke resultatenpagina moet worden weergegeven. Dit getal moet kleiner zijn dan of gelijk zijn aan 100.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Create Proof]](#create-proof)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download Proof]](#download-proof)
* [[!UICONTROL Read a Record]](#read-a-record)
* [[!UICONTROL Request PDF Summary]](#request-pdf-summary)
* [[!UICONTROL Update Proof]](#update-proof)
* [[!UICONTROL Upload File]](#upload-file)

#### [!UICONTROL Create Proof]

<!--Cannot test Jan 2025-->

Deze actiemodule maakt een nieuwe proefdruk of een nieuwe proefversie in [!DNL Workfront Proof] .

U geeft de parameters voor de nieuwe proefdruk op en de bronproefdruk als u een nieuwe versie maakt.

De module retourneert de id van de nieuwe proefdruk- of proefdrukversie. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Type]</td> 
   <td> <p>Geef op of u een standaardworkflow of een [!UICONTROL Automated Workflow] wilt instellen voor de proefdruk.</p> <p>Vul vervolgens de velden in die worden weergegeven voor het gekozen proefdruktype. Als u bijvoorbeeld [!UICONTROL Automated Workflow] kiest, vult u het veld <strong>[!UICONTROL Workflow Stages]</strong> in om de fasen te configureren.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Allow original file to be downloaded]</td> 
   <td>Selecteer of u het oorspronkelijke bestand wilt downloaden waarvan de proefdruk is gemaakt.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Classic Proof Viewer]</td> 
   <td>Selecteer of u de Klassieke Kijker van het Bewijs gebruikt.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Combine all files into single proof]</td> 
   <td>Schakel deze optie in om alle bestanden te combineren tot één proefdruk van meerdere pagina's.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create a new proof version]</td> 
   <td>Selecteer deze optie als u wilt dat de module een nieuwe versie van een bestaande proefdruk maakt. Wijs vervolgens in het veld <strong>[!UICONTROL Existing Proof ID]</strong> dat de unieke id van de proefdruk weergeeft of voer deze in.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link Label]</td> 
   <td>Voer een label in of wijs een label toe voor de aangepaste proefdrukkoppeling.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link URL]</td> 
   <td>Voer de URL voor de aangepaste koppeling in of wijs deze toe.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>Typ een van de volgende nummers om aan te geven welke standaardinstellingen voor e-mailmeldingen u wilt gebruiken voor de proefdruk die wordt gemaakt.
    <ul>
     <li><strong> 1 </strong> - Alle nieuwe commentaren en antwoorden</li>
     <li><strong> 2 </strong> - antwoordt op mijn commentaren</li>
     <li><strong> 3 </strong> - Dagelijkse samenvatting</li>
     <li><strong> 4 </strong> - Uursamenvatting</li>
     <li><strong> 5 </strong> - Besluiten slechts</li>
     <li><strong> 9 </strong> - Gehandicapten</li>
    </ul></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Excel Summary]</td> 
   <td>Selecteer of u de mogelijkheid wilt uitschakelen om proefdrukopmerkingen te downloaden naar een Excel-bestand.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable PDF Summary]</td> 
   <td>Selecteer of u de mogelijkheid wilt uitschakelen om proefdrukopmerkingen te downloaden naar een PDF-bestand.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>Selecteer of u de e-mail met abonnement voor deze proefdruk wilt uitschakelen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Embed Player]</td> 
   <td>Selecteer of u de ingesloten speler wilt inschakelen voor deze proefdruk.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>Selecteer of personen die geen deelnemers zijn, zich mogen abonneren op de proefdruk.<br> als u deze optie selecteert, kunt u de StandaardRol voor abonnees, zoals die in deze lijst wordt beschreven ook selecteren.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>Selecteer of u validatie van e-mailabonnementen wilt inschakelen. Als deze optie is ingeschakeld, moet de abonnee op een koppeling in een e-mailbericht klikken om toegang te krijgen tot een proefdruk.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>Selecteer of u wilt dat de proef die wordt gecreeerd het team URL verbergen of tonen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Hash] <span style="font-weight: normal;">of</span> [!UICONTROL File Hashes]</td> 
   <td>Voeg de id toe van het bestand of de bestanden waaruit u een proefdruk of proefdrukken wilt maken.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Names]</td> 
   <td>Voeg de bestandsnaam of namen toe voor de proefdruk die is gemaakt. Dit is een verplicht veld.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>Geef op of u wilt dat het gemaakte bewijs wordt vergrendeld nadat alle vereiste beslissingen zijn genomen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Notify recipients about this proof]</td> 
   <td>Selecteer een optie om aan te geven of ontvangers op de hoogte moeten worden gesteld wanneer de proefdruk wordt gemaakt.&gt;</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof name]</td> 
   <td>Typ een naam voor de proefdruk die wordt gecreeerd Dit is een vereist gebied. Gebruik een pijpsymbool (|) aan afzonderlijke namen voor veelvoudige proeven.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof owner ID]</td> 
   <td>Voer de id van de eigenaar van het bewijs in of wijs deze toe. Als dit veld niet wordt ingevuld, wordt de eigenaar van de proefdruk ingesteld op de huidige gebruiker.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reference ID]</td> 
   <td>Voer de referentie-id voor de proefdruk in.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require electronic signature]</td> 
   <td>Selecteer of u wilt dat eenieder die een beslissing neemt over een bewijs, een elektronische handtekening indient.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>Geef op of u een aanmeldingsnaam wilt opgeven voor de proefdruk die wordt gemaakt. </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Resolution ID]</td> 
   <td>Voer de id in van de resolutie die u voor de proefdruk wilt gebruiken. Voor een lijst van resolutie IDs, zie de [!DNL Workfront Proof] <a href="https://api.proofhq.com/home/objects/soapworkflowproofobject.html"> API documentatie </a>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL SWF]</td> 
   <td>Voer het type SWF-proefdruk in.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Show] [item]</td> 
   <td>Geef voor elk item aan of u het wilt weergeven in de proefdruk.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Workspace ID]</td> 
   <td>Voer de id in van de werkruimte waarin u de proefdruk wilt maken. </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Recipients]</td> 
   <td>Voeg de e-mailadressen toe van de ontvangers die u wilt gebruiken voor de proefdruk die wordt gemaakt.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>Geef de gewenste deadline op voor de proefdruk die wordt gemaakt. Gebruik de volgende datumnotatie:</p> <p><code>YYYY-MM-DD hh:mm</code></p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Workfront Proof] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Workfront Proof] -modules kan worden uitgevoerd.

De module retourneert de statuscode, kopteksten en tekst. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Method]</td> 
   <td>Stel de handeling in voor de API-aanroep. Voor beschikbare acties, zie de <a href="https://api.proofhq.com/"> documentatie van API van het Bewijs </a>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Body (XML)]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Voorbeeld:**
>
>![ Proef API modulevoorbeeld ](/help/workfront-fusion/references/apps-and-modules/assets/wfp-api-module-example-350x586.png)

#### [!UICONTROL Download Proof]

Deze actiemodule downloadt het bronbestand van een bepaald bewijs dat u met zijn ID identificeert.

U geeft de id van de proefdruk op.

De module keert de inhoud van het brondossier terug dat wordt gebruikt om tot de proef te leiden.U kunt deze informatie in verdere modules in het scenario in kaart brengen.

U moet over voldoende machtigingen beschikken om toegang te krijgen tot de record in [!DNL Workfront Proof] om deze gegevens op te halen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Typ de unieke id van de proefdruk op de pagina [!UICONTROL Proof Details] .  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a Record]

Deze actiemodule leest gegevens uit één proefdruk in [!DNL Workfront Proof] .

U geeft de id van de proefdruk op en de gegevens die u uit de proefdruk wilt halen.

De module retourneert de waarden van de velden die u kiest voor de proefdruk en de typen velden. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

U moet over voldoende machtigingen beschikken om toegang te krijgen tot de record in [!DNL Workfront Proof] om deze gegevens op te halen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>Selecteer of u een proefdruk, proefdrukopmerkingen of proefdrukrevisoren wilt lezen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Voer de unieke [!DNL Workfront Proof] -id in of wijs deze toe aan de record die u wilt lezen in de module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Request PDF Summary]

In deze actiemodule wordt het PDF-overzicht opgevraagd voor een bepaalde proefdruk in [!DNL Workfront Proof] .

U geeft de id van de proefdruk op.

De module retourneert de overzichtsgegevens van PDF. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

U moet over voldoende machtigingen beschikken om toegang te krijgen tot de record in [!DNL Workfront Proof] om deze gegevens op te halen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Voer de unieke [!DNL Workfront Proof] -id in van de proefdruk waarvoor u een PDF-overzicht wilt aanvragen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Callback URL]</td> 
   <td>Voer de URL in of wijs deze toe op de plaats waar u het PDF-overzicht wilt verzenden.</td> 
  </tr> 
 </tbody> 
</table>

##### Mogelijke fout

* **Fout**: &quot;[!UICONTROL You do not have privilege to perform this request. The stage must contain at least one recipient.]&quot;
* **Oplossing**: Zorg ervoor u niet slechts aan de stadia van het werkschema wordt toegewezen. Er moet een andere gebruiker zijn toegewezen aan de fasen van de workflow.

#### [!UICONTROL Update Proof]

Deze actiemodule werkt een bestaande proefdruk bij in [!DNL Workfront Proof] .

U geeft de id en het recordtype van de proefdruk op en geeft aan welke velden u in de uitvoer wilt opnemen.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

U moet over voldoende machtigingen beschikken om toegang te krijgen tot de record in [!DNL Workfront Proof] om deze gegevens op te halen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Typ de unieke id van de proefdruk op de pagina [!UICONTROL Proof Details] . </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>Geef de gewenste deadline op voor de proefdruk die wordt gemaakt. Gebruik de datumnotatie <code>YYYY-MM-DD hh:mm</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>Selecteer welke van de volgende standaardinstellingen voor e-mailmeldingen u wilt gebruiken voor de proefdruk die wordt gemaakt.
    <ul>
     <li> [!UICONTROL All new comments and replies]</li>
     <li>[!UICONTROL Replies to my comments]</li>
     <li>[!UICONTROL Daily summary]</li>
     <li> [!UICONTROL Hourly summary]</li>
     <li> [!UICONTROL Decisions only]</li>
     <li> [!UICONTROL Disabled]</li>
    </ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default Role]</td> 
   <td>Selecteer de standaardrol voor de proef.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>Selecteer of u de e-mail met abonnement voor deze proefdruk wilt uitschakelen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>Selecteer of personen die geen deelnemers zijn, zich mogen abonneren op de proefdruk.<br> als u deze optie selecteert, kunt u een optie op het [!UICONTROL Default Role] gebied ook selecteren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>Selecteer of u validatie van e-mailabonnementen wilt inschakelen. Als deze optie is ingeschakeld, moet de abonnee op een koppeling in een e-mailbericht klikken om toegang te krijgen tot een proefdruk.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>Selecteer of u wilt dat de proef die wordt gecreeerd het team URL verbergen of tonen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>Geef op of u wilt dat het gemaakte bewijs wordt vergrendeld nadat alle vereiste beslissingen zijn genomen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Message]</td> 
   <td>Typ of wijs een bericht toe dat u bij de proefdruk wilt vergezellen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID] </td> 
   <td>Voer de id in van de proefdruk die u wilt bijwerken of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Name]</td> 
   <td>Voer de naam in van de proefdruk die u wilt bijwerken of wijs deze aan.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>Geef op of u een aanmeldingsnaam wilt opgeven voor de proefdruk die wordt gemaakt. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show Versions Like]</td> 
   <td>Selecteer of u een koppeling naar andere versies van deze proefdruk wilt weergeven.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Voer het onderwerp van de proefdruk in of kaart</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload File]

Deze actiemodule uploadt een bestand voor gebruik met de module [!UICONTROL Create Proof] in [!DNL Workfront Proof] .

De module retourneert een hash-id voor het geüploade bestand. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

* [[!UICONTROL List Workflow Templates]](#list-workflow-templates)
* [[!UICONTROL Search]](#search)

#### [!UICONTROL List Workflow Templates]

In deze zoekmodule worden alle beschikbare werkstroomsjablonen weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal malplaatjes in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search]

Deze zoekmodule zoekt naar records in een object in [!DNL Workfront Proof] dat overeenkomt met de zoekquery die u opgeeft.

De module retourneert de id van de proefdruk als deze op zoek is naar een proefdruk. Of de gebruikers-id&#39;s, e-mails, namen, posities en e-mailaliassen van de ontvangers worden geretourneerd als deze naar ontvangers zoeken. U kunt deze informatie in volgende modules in het scenario toewijzen.

U moet over voldoende machtigingen beschikken om toegang te krijgen tot de record in [!DNL Workfront Proof] om deze gegevens op te halen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Workfront Proof] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Search for]</td> 
   <td> <p>Selecteer het type record waarnaar de module moet zoeken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Proof]</strong> </p> <p>Voer de proefdruknaam in van de proefdrukproef waarnaar u wilt zoeken.</p> </li> 
     <li> <p><strong>[!UICONTROL Recipient]</strong> </p> <p>Voer het e-mailadres in van de ontvanger waarnaar u wilt zoeken.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Geef aan of de module naar <strong>[!UICONTROL All Matching Records]</strong> of alleen naar <strong>[!UICONTROL First Matching Record]</strong> zoekt.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort By]</td> 
   <td>Selecteer het veld waarop u de resultaten wilt sorteren.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sorting Direction]</td> 
   <td> <p>Selecteer of u resultaten wilt sorteren oplopend of aflopend.</p> </td> 
  </tr> 
 </tbody> 
</table>


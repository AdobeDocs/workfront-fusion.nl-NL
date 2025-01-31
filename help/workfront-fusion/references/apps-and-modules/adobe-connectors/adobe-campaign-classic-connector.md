---
title: Adobe Campaign v7/v8-modules
description: Met de  [!DNL Adobe Campaign]  modules, kunt u een  [!DNL Adobe Workfront Fusion]  scenario beginnen dat op gebeurtenissen in uw  [!DNL Adobe Campaign]  rekening wordt gebaseerd, overeenkomsten en andere verslagen tot stand brengen, lezen of bijwerken, onderzoek naar verslagen gebruikend criteria u plaatst, en documenten uploadt.
author: Becky
feature: Workfront Fusion
exl-id: 9fdff26c-c7c0-4eb8-a36f-4aeaf432b333
source-git-commit: 9bcda2cc1a5f483a8db49eae8e4f3d10f0d39c67
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# [!DNL Adobe Campaign] modules

Met de [!DNL Adobe Campaign] -modules kunt u een [!DNL Adobe Workfront Fusion] -scenario starten op basis van gebeurtenissen in uw [!DNL Adobe Campaign v7/v8] -account, records maken, lezen of bijwerken, records zoeken aan de hand van criteria die u instelt en aangepaste API-aanroepen uitvoeren.

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

## Vereisten

U moet de Fusion IP-adressen toevoegen aan [!DNL Adobe Campaign] .

* Voor instructies bij het toevoegen van IP adressen aan uw lijst van gewenste personen van de Campagne, zie [ Toevoegend IP adressen aan de lijst van gewenste personen ](https://experienceleague.adobe.com/en/docs/control-panel/using/sftp-management/ip-range-allow-listing#adding-ip-addresses-allow-list) in de documentatie van Adobe Campaign.
* Voor een lijst van IP adressen om aan de lijst van gewenste personen toe te voegen, zie [ IP Adressen voor Fusie in de lijst van gewenste personen van uw organisatie ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md) vormen.

## Adobe Campaign API-informatie

De Adobe Campaign-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.7.2</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Adobe Campaign] met [!DNL Adobe Workfront Fusion]

>[!IMPORTANT]
>
>We raden u ten zeerste aan een server-naar-server verbinding te maken. Adobe Campaign heeft hun API bijgewerkt zodat alleen server-naar-server verbindingen worden geaccepteerd. Als u met versie 8 van de Campagne of hoger verbindt, moet u **** een server-aan-server verbinding tot stand brengen.
>
>Voor meer informatie over de nieuwe verbindingsvereisten van de Campagne, zie [ Migratie van de technische exploitanten van de Campagne aan Adobe Developer Console ](https://experienceleague.adobe.com/docs/campaign/technotes-ac/tn-new/ims-migration.html) in de documentatie van de Campagne.

1. Klik in een willekeurige [!DNL Adobe Campaign] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
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
            <p>Selecteer of u een basisverbinding of een server-aan-server verbinding creeert.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Voer een naam in voor deze verbinding.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Base URL]</td>
          <td>Voer de basis-URL in die u gebruikt om verbinding te maken met de instantie [!DNL Adobe Campaign] .</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Username]</td>
          <td>Voer uw Adobe Campaign-gebruikersnaam in als u een basisverbinding maakt.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Password]</td>
          <td>Als u een basisverbinding maakt, voert u uw Adobe Campaign-wachtwoord in.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Als u een server-naar-server verbinding maakt, voert u uw [!DNL Adobe] [!UICONTROL Client ID] in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Als u een server-naar-server verbinding maakt, voert u uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
        </tr>
     </tbody>
    </table>
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL Adobe Campaign] modules en hun velden

Wanneer u [!DNL Adobe Campaign] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Campaign] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<!--* [Triggers](#triggers)-->
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

<!--### Triggers

#### [!UICONTROL Watch records]

This scheduled trigger module starts a scenario when a record changes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Create a connection to [!DNL Adobe Campaign]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Select whether you want to watch for new records, updated records, or both.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Select the resource that you want to watch for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output]</td> 
   <td>Select the fields that you want to include in the module's output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>For each custom field that you want to include in output, click <b>[!UICONTROL Add]</b> and enter the name of the custom field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>-->


### Handelingen

* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Delete a record]](#delete-record)
* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)
* [[!UICONTROL Perform an action]](#perform-an-action)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Subscribe or unsubscribe]](#subscribe-or-unsubscribe)
* [[!UICONTROL Update a record]](#update-record)

#### [!UICONTROL Create a record]

Deze actiemodule maakt een nieuwe record in [!DNL Adobe Campaign] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Zie <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" > Verbinding maken met [!DNL Adobe Campaign]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecteer het type [!DNL Adobe Campaign] record dat u wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>Selecteer de velden waarvoor u waarden wilt instellen wanneer de record wordt gemaakt en vul vervolgens de waarden voor die velden in. Velden variëren op basis van het type record dat u selecteert.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> Voor elk aangepast veld dat u aan de nieuwe record wilt toevoegen, klikt u op <b>[!UICONTROL Add item]</b> en voert u de naam en waarde van het veld in of wijst u deze toe. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Record]

Deze actiemodule verwijdert één record uit [!DNL Adobe Campaign] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Zie <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" > Verbinding maken met [!DNL Adobe Campaign]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecteer het type bron dat u wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van de bron die u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make a custom API call]

Deze module maakt een aangepaste API-aanroep naar de [!DNL Adobe Campaign] API

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Zie <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" > Verbinding maken met [!DNL Adobe Campaign]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Action]</td>
      <td><p>Selecteer de handeling die de API-aanroep moet uitvoeren.</p>
      <p>[!UICONTROL Execute query]</p>
      <p>[!UICONTROL Write]</p>
      <p>[!UICONTROL Get entity if more recent]</p>
      <p>[!UICONTROL Select all]</p>
      <p>[!UICONTROL Push event]</p>
    </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] voegt automatisch de [!UICONTROL x-security] token-header toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL XML Body]</td>
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in XML, zonder het sessieelement. </td>     </tr>
  </tbody>
</table>


#### [!UICONTROL Perform an action]

Deze actiemodule voert een geselecteerde actie uit op een object in de [!DNL Adobe Campaign] API.

Voor informatie over specifieke acties en gebieden, zie [[!DNL Adobe Campaign]  - API Documentatie ](https://experienceleague.adobe.com/developer/campaign-api/api/p-14.html).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Zie <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" > Verbinding maken met [!DNL Adobe Campaign]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td><p>Selecteer de handeling die op het object moet worden uitgevoerd.</p>
   <ul>
   <li><p><b>[!DNL List]</b></p><p> Zie <a href="#search" class="MCXref xref" >[!UICONTROL Search]</a> in dit artikel voor beschikbare velden. </p></li>
     <li><p><b>[!UICONTROL Get]</b></p><p> Zie <a href="#search" class="MCXref xref" >[!UICONTROL Search]</a> in dit artikel voor beschikbare velden. </p></li> 
   <li><p><b>[!UICONTROL Create]</b></p><p> Zie <a href="#create-a-record" class="MCXref xref" >[!UICONTROL Create a record]</a> in dit artikel voor beschikbare velden. </p></li>
   <li><p><b>[!UICONTROL Update]</b></p><p> Zie <a href="#update-record" class="MCXref xref" >[!UICONTROL Update a record]</a> in dit artikel voor beschikbare velden. </p></li>
   <li><p><b>[!UICONTROL Delete]</b></p><p> Zie <a href="#delete-record" class="MCXref xref" >[!UICONTROL Delete a record]</a> in dit artikel voor beschikbare velden. </p></li>
   </ul>
   </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Deze actiemodule leest een record uit [!DNL Adobe Campaign] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Zie <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" > Verbinding maken met [!DNL Adobe Campaign]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecteer het type [!DNL Adobe Campaign] record dat u wilt lezen.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Voer een kaart in met de id van de record die u wilt lezen.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output] </td> 
   <td>Selecteer de velden die u in de uitvoer van de module wilt opnemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>Voor elk aangepast veld dat u in de uitvoer wilt opnemen, klikt u op <b>[!UICONTROL Add]</b> en voert u de naam van het aangepaste veld in.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Subscribe or unsubscribe]

Deze actiemodule abonneert een gebruiker aan of unsubscribes een gebruiker van een informatiedienst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Zie <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" > Verbinding maken met [!DNL Adobe Campaign]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe or unsubscribe]</td> 
   <td>Geef op of u zich wilt abonneren op de informatieservice of het abonnement wilt opzeggen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service name]</td> 
   <td>Selecteer de service waarvan u een abonnement wilt nemen of waarvan u een abonnement wilt opzeggen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipient email address] </td> 
   <td>Voer het e-mailadres in of wijs het e-mailadres toe van de gebruiker die u wilt abonneren op de informatieservice of het abonnement opzeggen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update record]

Deze actiemodule werkt één record bij in [!DNL Adobe Campaign] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Zie <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" > Verbinding maken met [!DNL Adobe Campaign]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecteer het type [!DNL Adobe Campaign] record dat u wilt maken.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Voer de toewijzing in van de id van de record die u wilt bijwerken.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>Selecteer de velden waarvoor u de waarden wilt bijwerken en vul vervolgens de waarden voor die velden in. Velden variëren op basis van het type record dat u selecteert.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> Voor elk aangepast veld dat u wilt bijwerken, klikt u op <b>[!UICONTROL Add item]</b> en voert u de naam en waarde van het veld in of wijst u deze toe. </td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

#### [!UICONTROL Search]

Deze zoekmodule retourneert records die op de opgegeven criteria zijn gebaseerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Zie <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" > Verbinding maken met [!DNL Adobe Campaign]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Selecteer het type [!DNL Adobe Campaign] record dat u wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Voer de velden en waarden in die u voor de zoekopdracht wilt gebruiken. Velden zijn afhankelijk van de geselecteerde bron.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tr> 
 </tbody> 
</table>

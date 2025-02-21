---
title: HubSpot CRM-modules
description: De  [!DNL Adobe Workfront Fusion]  modules van HubSpot CRM laten u toe om gebeurtenissen, verslagen, contacten, overeenkomsten, dossier en vormvoorlegging te controleren, of, verslagen, contacten, overeenkomsten, gebeurtenissen, of dossiers in uw  [!DNL HubSpot CRM]  rekening te creëren, terug te winnen, bij te werken en te schrappen.
author: Becky
feature: Workfront Fusion
exl-id: b8a1bbcd-337e-4c92-a1a6-d6d4bab1f440
source-git-commit: 9cea5de748873720247db39161cea12c7e9c7186
workflow-type: tm+mt
source-wordcount: '5530'
ht-degree: 0%

---

# [!DNL HubSpot CRM] modules

Met de modules [!DNL Adobe Workfront Fusion] [!DNL HubSpot CRM] kunt u gebeurtenissen, records, contactpersonen, services, bestanden en formulierverzendingen controleren, of records, contactpersonen, services, gebeurtenissen of bestanden in uw [!DNL HubSpot CRM] -account maken, ophalen, bijwerken en verwijderen.

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

Als u [!DNL HubSpot CRM] -modules wilt gebruiken, moet u een [!DNL HubSpot CRM] -account hebben.

## HubSpot CRM API-informatie

De schakelaar van CRM HubSpot gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://api.hubapi.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v2.0.14</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Adobe Workfront Fusion] met [!DNL HubSpot CRM]

Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie [ een verbinding tot stand brengen  [!DNL Adobe Workfront Fusion]  - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Wanneer het vormen van een verbinding, selecteer het **verbindingstype van 0} HubSpot CRM {.** Het (Afgekeurde) type van HubSpot CRM steunt bestaande verbindingen, maar wij adviseren niet gebruikend het om nieuwe verbindingen tot stand te brengen.

## [!DNL HubSpot CRM] modules en hun velden

Wanneer u [!DNL Hubspot CRM] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Hubspot CRM] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [CRM-objecten](#crm-objects)
* [Records (Deals, Contacten, en Bedrijven)](#records-deals-contacts-and-companies)
* [Contactpersonen](#contacts)
* [Overeenkomsten](#deals)
* [Bedrijven](#companies)
* [Engages](#engagements)
* [Gebeurtenissen en meldingen](#events-and-notifications)
* [Bestanden](#files)
* [Taken](#tasks)
* [Gebruikers](#users)
* [Tickets](#tickets)
* [Forms](#forms)
* [Sociale media (uitzending)](#social-media-broadcast)
* [ Blogberichten ](#blog-posts)
  <!--* [Workflows]()-->
* [ Abonnementen ](#subscriptions)
  <!--* [Associations]()-->
* [Overige](#other)

### CRM-objecten

<!--* [Search for CRM objects](#search-for-crm-objects)
* [Watch CRM objects](#watch-crm-objects)-->

+++ **[!UICONTROL Search for CRM Objects]**

Deze zoekmodule zoekt naar CRM-objecten op aangepaste eigenschappen of op query. Als u naar producten of lijnitems wilt zoeken, gebruikt u een speciale verbinding met een vereist aangepast bereik.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Ga of kaart het maximumaantal punten in dat de module in één uitvoeringscyclus zal terugkeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type to Search]</td> 
   <td>Selecteer het type van voorwerp van Hubspot CRM dat u naar wilt zoeken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer van de module wilt weergeven. De beschikbare velden zijn afhankelijk van het object dat u hebt geselecteerd.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by] </td> 
   <td> <p>Selecteer hoe u de zoekopdracht wilt filteren</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>De query invoeren of toewijzen</p> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Voer de groepen of filters voor uw zoekopdracht in.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Klik als u de resultaten wilt sorteren. Als u de resultaten wilt sorteren, worden de volgende velden weergegeven. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Property name]</strong> </p> <p>Selecteer de eigenschap waarmee u de resultaten wilt sorteren</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>Kies of u de resultaten in oplopende of aflopende richting wilt sorteren.</p> </li> 
    </ul> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Verschuiving beginnen</td> 
    <td>Voer de id in of wijs de id toe van het eerste item waarvoor u details wilt ophalen. Deze module retourneert slechts maximaal 5000 resultaten tegelijk. Als u een beginverschuiving instelt, kunt u andere items ophalen dan de eerste 5000. Als de begincompensatie 5000 is, zou de module punten 5000-9999 terugkeren.</td> 
   </tr>
 </tbody> 
</table>

+++

+++ **de voorwerpen van CRM van het Horloge**

Deze activeringsmodule start een scenario wanneer een CRM-object wordt gemaakt of bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Ga of kaart het maximumaantal punten in dat de module in één uitvoeringscyclus zal terugkeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object type to search]</td> 
   <td> <p>Selecteer het type object waarnaar u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer voor deze module wilt opnemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created/Updated]</td> 
   <td>Selecteer of u de gemaakte (nieuwe) of bijgewerkte (gewijzigde) objecten wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by]</td> 
   <td>U kunt een filter toevoegen om ervoor te zorgen dat het scenario slechts begint wanneer bepaalde voorwaarden worden voldaan.<ul><li><b>Query</b><p>Voer de query in waarop u wilt filteren.</li><li><b>Eigenschappen</b><p>Voor elk bezit dat u aan filterresultaten wilt gebruiken, <b> toevoegen punt </b> en ga de bezitsnaam, de exploitant, en bezitswaarde in.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Records (Deals, Contacten, en Bedrijven)

<!--* [Create a Record](#create-a-record)
* [[!UICONTROL Create a Record (Legacy)]](#create-a-record-legacy)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Get a Record]](#get-a-record)
* [[!UICONTROL Get a Record Property]](#get-a-record-property)
* [List Records](#list-records)
* [[!UICONTROL Update a Record]](#update-a-record)
* [[!UICONTROL Watch Records]](#watch-records)-->

+++ **creeer een verslag**

Deze actiemodule leidt tot een contact, een bedrijf, of een overeenkomst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Selecteer voor elke eigenschap die u wilt toevoegen bij het maken van de record de groep waarin de eigenschap is gevonden. De groep eigenschappen wordt geopend en u kunt de waarde voor de eigenschappen invullen. Welke groepen en eigenschappen beschikbaar zijn, is afhankelijk van het type record dat u wilt maken.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Record (Legacy)]**

Deze actiemodule leidt tot contact, een bedrijf, of een overeenkomst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Vul de eigenschappen in die u voor de record wilt instellen. De beschikbare velden zijn afhankelijk van het type record dat u wilt maken.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Record]**

Deze actiemodule schrapt een contact, een bedrijf, of een overeenkomst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecteer het type record dat u wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Ga identiteitskaart van het contact, het bedrijf, of de overeenkomst in u wilt schrappen. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ [!UICONTROL Get a Record]

Deze actiemodule krijgt details van een contact, een bedrijf, of een overeenkomst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het recordtype.</p> 
    <ul> 
     <li>[!UICONTROL Contact]</li> 
     <li>[!UICONTROL Company] </li> 
     <li>[!UICONTROL Deal]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td>Als u contact krijgt, selecteer of u het door identiteitskaart of door E-mailadres wilt identificeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Ga identiteitskaart van het contact, het bedrijf of de overeenkomst in die u wilt terugwinnen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Voer het e-mailadres in van de contactpersoon waarvan u de gegevens wilt ophalen. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Record Property]**

Deze actiemodule krijgt meta-gegevens voor een specifiek verslagbezit door zijn (interne) naam.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecteer het type record met de eigenschap waarvoor u metagegevens wilt ophalen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property Name]</td> 
   <td>Selecteer de eigenschap waarvoor u metagegevens wilt ophalen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Option ID]</td> 
   <td> <p> Sommige eigenschappen hebben een set beschikbare opties die een gebruiker als eigenschapswaarde kan selecteren. Voer de id in van de optie die de eigenschapwaarde vertegenwoordigt die u wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Verslagen van de Lijst**

Deze onderzoeksmodule keert een lijst van contacten, bedrijven of overeenkomsten terug. De productie is beperkt tot 5000 contacten, 12.500 bedrijven, of 12.500 overeenkomsten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Selecteer het type record dat u wilt retourneren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer voor deze module wilt opnemen.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update a Record]**

Deze actiemodule werkt een contact, een bedrijf, of een overeenkomst bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecteer het type record dat u wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td> <p>Als u een contact krijgt, selecteer hoe u het verslag wilt identificeren:</p> 
    <ul> 
     <li> <p>[!UICONTROL ID]</p> </li> 
     <li> <p>[!UICONTROL Email]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van de contactpersoon, het bedrijf of de deal die u wilt bijwerken. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Voer het e-mailadres in van de contactpersoon waarvan u de gegevens wilt bijwerken. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Vul de eigenschappen in die u voor de record wilt instellen. De beschikbare velden zijn afhankelijk van het type record dat u wilt maken.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Records]**

Deze trekkermodule begint een scenario wanneer een contact, bedrijf, of overeenkomst binnen de laatste 30 dagen is gewijzigd of gecreeerd. De uitvoer is beperkt tot 10.000 records.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selecteer het type record met de eigenschap die u wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Selecteer of u onlangs gewijzigde of onlangs tot stand gebrachte verslagen wilt letten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer van de module wilt opnemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Contactpersonen

<!--* [[!UICONTROL Add Contacts to a List]](#add-contacts-to-a-list)
* [Create/Update a contact](#createupdate-a-contact)
* [[!UICONTROL Create/Update a Contact (Legacy)]](#createupdate-a-contact-legacy)
* [[!UICONTROL Create/Update a Group of Contacts]](#createupdate-a-group-of-contacts)
* [[!UICONTROL List Contacts]](#list-contacts)
* [[!UICONTROL List Contacts of a Company]](#list-contacts-of-a-company)
* [[!UICONTROL Merge contacts]](#merge-contacts)
* [[!UICONTROL Remove a Contact from a List]](#remove-a-contact-from-a-list)
* [[!UICONTROL Search for Contacts]](#search-for-contacts)
* [Watch Contacts Added to a List](#watch-contacts-added-to-a-list)-->

+++ **[!UICONTROL Add Contacts to a List]**

Deze module voegt contactverslagen toe die reeds in het systeem aan een contactlijst zijn gecreeerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Selecteer identiteitskaart van de lijst waaraan u de contact wilt toevoegen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs/Emails] </td> 
   <td> <p>Selecteer hoe u de contacten wilt identificeren u aan de lijst wilt toevoegen:</p> 
    <ul> 
     <li> <p>[!UICONTROL IDs]</p> <p>Voeg identiteitskaarts van de contacten toe die u aan de lijst wilt toevoegen.</p> </li> 
     <li> <p>[!UICONTROL Emails]</p> <p>Voeg de e-mailadressen toe van de contactpersonen die u aan de lijst wilt toevoegen.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **creeer/werk een Contact** bij

Deze actiemodule leidt tot een contact als het niet in een portaal bestaat. Als het contact in het portaal bestaat, werkt deze module het met de verstrekte waarden bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Voor elk bezit dat u wilt toevoegen wanneer het creëren van het contact, selecteer de groep waar het bezit wordt gevonden. De groep eigenschappen wordt geopend en u kunt de waarden voor de eigenschappen invullen.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create/Update a Contact (Legacy)]**

Creeert een contact als het niet in een portaal reeds bestaat, of werkt het met de recentste bezitswaarden bij als het in een portaal bestaat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Vul om het even welke eigenschappen in die u voor het contact wilt plaatsen of bijwerken. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create/Update a Group of Contacts]**

Creeert een groep contacten of werkt hen bij als zij reeds bestaan. De prestaties zijn het best wanneer de partijgrootte tot 100 contacten of minder wordt beperkt. De veranderingen die door dit eindpunt worden aangebracht worden verwerkt asynchroon, zodat kan het verscheidene notulen voor veranderingen nemen die op contactverslagen moeten worden toegepast.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Batch of Contacts to Create/Update] </td> 
   <td> <p>Voeg de partij contacten toe.</p> <p>Klik op <strong>[!UICONTROL Add item]</strong> om een nieuwe contactpersoon toe te voegen. Voer in het venster dat wordt weergegeven de volgende gegevens in of wijs deze toe:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search Type]</strong> </p> <p>Selecteer hoe u de contactpersoon wilt identificeren:</p> 
      <ul> 
       <li> <p>[!UICONTROL ID]</p> <p>Voer de id in van de contactpersoon die u wilt maken of bijwerken. </p> </li> 
       <li> <p>[!UICONTROL Email]</p> <p>Voer het e-mailadres in van de contactpersoon die u wilt maken of bijwerken. </p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Vul om het even welke eigenschappen in die u voor het contact wilt plaatsen of bijwerken.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Contacts]**

Keert alle contacten terug die in het portaal zijn gecreeerd. De output is beperkt tot 5000 contacten. Als u vorige of volgende contactpersonen wilt vermelden, gebruikt u de parameter [!UICONTROL advanced] om de lijst te verschuiven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Het maximumaantal contacten [!DNL Workfront Fusion] zou tijdens één cyclus van de scenariouitvoering moeten terugkeren. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer van de module wilt weergeven. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Contactpersoon-id [beginverschuiving] </td> 
    <td>Voer de id in van de gebruiker die u de lijst wilt starten of wijs deze toe. Bijvoorbeeld, zal het plaatsen van identiteitskaart van het Contact als identiteitskaart van het 101ste contact de module toestaan om van contacten 101-5100 eerder dan 1-5000 een lijst te maken. </td> 
   </tr>
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Contacts of a Company]**

Wint een lijst van contacten in het bedrijf terug. De output is beperkt tot 5000 contacten. Als u vorige of volgende contactpersonen wilt vermelden, gebruikt u de parameter [!UICONTROL advanced] om de lijst te verschuiven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Ga identiteitskaart van het bedrijf in waarvan contacten u wilt een lijst maken. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Het maximumaantal contacten [!DNL Workfront Fusion] zou tijdens één cyclus van de scenariouitvoering moeten terugkeren. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Contactpersoon-id [beginverschuiving] </td> 
    <td>Voer de id in van de gebruiker die u de lijst wilt starten of wijs deze toe. Bijvoorbeeld, zal het plaatsen van identiteitskaart van het Contact als identiteitskaart van het 101ste contact de module toestaan om van contacten 101-5100 eerder dan 1-5000 een lijst te maken. </td> 
   </tr>
 </tbody> 
</table>

+++

+++ **[!UICONTROL Merge contacts]**

In deze actiemodule worden contactpersonen samengevoegd

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 1] </td> 
   <td>Ga identiteitskaart van één van de contacten in u wilt samenvoegen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 2] </td> 
   <td>Voer de id in van de andere contactpersoon die u wilt samenvoegen.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Remove a Contact from a List]**

Hiermee verwijdert u een contactpersoon uit een lijst met contactpersonen.

>[!NOTE]
>
>U kunt contactpersonen niet handmatig uit een dynamische lijst verwijderen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Selecteer identiteitskaart van de lijst waarvan u de contact wilt verwijderen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID] </td> 
   <td>Voer de id in van de contactpersoon die u uit de lijst wilt verwijderen. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Contacts]**

Haalt een lijst met contactpersonen op met de zoekquery.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Voer de zoekquery in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Ga of kaart het maximumaantal contacten in [!DNL Workfront Fusion] zou tijdens één cyclus van de scenariouitvoering moeten terugkeren. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch contacts added to a list]**

Deze trekkermodule begint een scenario wanneer een nieuw contact aan een lijst wordt toegevoegd. Dit is alleen beschikbaar voor gebruikers met een betaalde marketingaccount.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Ga of kaart identiteitskaart van de lijst in die de contacten bevat u wilt letten op.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer van de module wilt opnemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Overeenkomsten

<!--* [[!UICONTROL Get a Deal's CRM Pipeline]](#get-a-deals-crm-pipeline)
* [[!UICONTROL List Deal/Ticket Pipelines]](#list-dealticket-pipelines)-->

+++ **[!UICONTROL Get a Deal's CRM Pipeline]**

Keert een specifieke overeenkomstenpijpleiding terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pipeline ID] </td> 
   <td>Ga of kaart identiteitskaart van de pijpleiding in u details voor wilt terugwinnen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stage ID] </td> 
   <td>Voer de id in van het werkgebied waarvoor u details wilt ophalen of wijs deze toe. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Deal/Ticket Pipelines]**

Retourneert alle deal- en kaartpijpleidingen voor een bepaald portaal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type] </td> 
   <td>Selecteer of u deals of tickets wilt weergeven.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Bedrijven

+++ **[!UICONTROL Search for Companies by domain]**

Haalt een lijst op van bedrijven die op een nauwkeurige gelijke met het domeinbezit worden gebaseerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Domain] </td> 
   <td>Voer het domein in van de bedrijven waarnaar u wilt zoeken, zoals <code>[!DNL hubspot].com</code> . </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Het maximumaantal bedrijven [!DNL Workfront Fusion] moet worden geretourneerd tijdens één uitvoeringscyclus van het scenario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer van de module wilt weergeven. </td> 
  </tr> 
 </tbody> 
</table>

+++

### Engages

<!--* [Associate an Engagement with a CRM object](#associate-an-engagement-with-a-crm-object)
* [Create an Engagement](#create-an-engagement)
* [Delete an Engagement](#delete-an-engagement)
* [Watch Engagements](#watch-engagements)-->

+++ **associeer een Betrokkenheid met een voorwerp van CRM**

Deze actiemodule associeert een overeenkomst met een contact, een bedrijf, of een overeenkomst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selecteer het type CRM-record waaraan u een betrokkenheid wilt koppelen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Engagement ID]</td> 
  <td>Voer de id in van de betrokkenheid die u aan het object wilt koppelen of wijs deze toe.</td> 
   </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
  <td>Voer de id in van de record waaraan u de betrokkenheid wilt koppelen of wijs deze toe.</td> 
   </tr> 
 </tbody> 
</table>

+++

+++ **creeer een Betrokkenheid**

Deze actiemodule leidt tot een overeenkomst (zoals een nota, een taak, of een activiteit) met een voorwerp van CRM in HubSpot. De overeenkomsten zijn om het even welke interactie met een contact dat in CRM zou moeten worden geregistreerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Is Active?]</td> 
   <td>Schakel deze optie in als de nieuwe betrokkenheid actief wordt wanneer deze wordt gemaakt. Een betrokkenheid moet actief zijn om in de tijdlijn te verschijnen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
  <td>Selecteer het type betrokkenheid dat u wilt maken.
  <ul>
  <li><b>E-mail</b><p></p>Ga aan <a href="#email-metadata" class="MCXref xref" > meta-gegevens E-mail </a> verder.</p></li>
  <li><b>Bellen</b><p>Ga aan <a href="#call-metadata" class="MCXref xref" > meta-gegevens van de Vraag </a> verder.</p></li>
  <li><b>Vergadering</b><p>Ga aan <a href="#meeting-fields" class="MCXref xref" > gebieden van de Vergadering </a> verder.</p></li>
  <li><b>Taak</b><p>Ga aan <a href="#task-fields" class="MCXref xref" > gebieden van de Taak </a> verder.</p></li>
  <li><b>Opmerking</b><p>Voer in het veld Hoofdtekst de tekst van de notitie in.</p></li>
  </ul>
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Tijdstempel</td> 
   <td>Voer een tijdstempel voor de service in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eigenaar-id</td> 
   <td>Voer de Eigenaar-id in of wijs deze toe aan de persoon aan wie de betrokkenheid wordt toegewezen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UID</td> 
   <td>Voer een id voor de betrokkenheid in of wijs deze toe. Deze id kan worden gebruikt voor verschillende objecttypen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Portal-id</td> 
   <td>Voer de id van het portaal in of wijs deze toe. Dit is handig als uw organisatie meerdere portalen heeft.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bijbehorende contactpersonen</td> 
   <td>Voor elk contact dat u deze overeenkomst met wilt associëren, <b> toevoegen punt </b> en ingaan identiteitskaart van het Contact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verbonden ondernemingen</td> 
   <td>Voor elk bedrijf dat u deze overeenkomst met wilt associëren, <b> toevoegen punt </b> en ingaan identiteitskaart van het Bedrijf.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bijbehorende deals</td> 
   <td>Voor elke overeenkomst die u deze overeenkomst met wilt associëren, klik <b> toevoegen punt </b> en ga identiteitskaart van de Overeenkomst in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gekoppelde Tickets</td> 
   <td>Voor elk kaartje dat u deze overeenkomst met wilt associëren, <b> toevoegen punt </b> en ingaan identiteitskaart van de Ticket.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bijlagen</td> 
   <td>Voor elke gehechtheid die u deze overeenkomst met wilt associëren, <b> toevoegt punt </b> en gaat identiteitskaart van het Dossier van het dossier in u wilt vastmaken.</td> 
  </tr> 
 </tbody> 
</table>

#### E-mailmetagegevens

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL From > Email]</p> </td> 
   <td> <p>Voer het e-mailadres in of wijs het toe dat de e-mail wordt verzonden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First Name]</td> 
   <td>Voer de voornaam in van de persoon van wie de e-mail wordt verzonden of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Last Name]</td> 
  <td>Voer de achternaam in of wijs de achternaam toe van de persoon van wie de e-mail wordt verzonden.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Naar</td> 
   <td>Voor elk e-mailadres dat u e-mail naar wilt verzenden, klik <b> toevoegen punt </b> en ga of kaart het e-mailadres in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cc</td> 
   <td>Voor elk e-mailadres dat u e-mail aan wilt Cc, <b> klikken voegt punt </b> toe en gaat of wijst het e-mailadres in kaart.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bcc</td> 
   <td>Voor elk e-mailadres dat u e-mail aan wilt BCC, <b> toevoegen punt </b> klikken en het e-mailadres ingaan of in kaart brengen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Onderwerp</td> 
   <td>De tekst van het e-mailonderwerp invoeren of toewijzen</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML</td> 
   <td>Als u een e-mailbericht met HTML-indeling wilt verzenden, voert u de tekst van de e-mail in of wijst u deze toe, inclusief HTML-tags.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tekst</td> 
   <td>Als u een e-mailbericht met alleen tekst wilt verzenden, voert u de tekst van de hoofdtekst van de e-mail in of wijst u deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Metagegevens aanroepen

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL To Number]</p> </td> 
   <td> <p>Ga of kaart het telefoonnummer in dat de vraag zal worden gemaakt aan.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From Number]</td> 
   <td>Ga of kaart het telefoonnummer in dat de vraag van zal worden gemaakt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
  <td>Selecteer de status van de vraag.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Lichaam</td> 
   <td>Ga of kaart de details of de nota's voor de vraag in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Externe id</td> 
   <td>Dit gebied vertegenwoordigt interne identiteitskaart van een vraag die in HubSpot wordt gemaakt. Er is geen actie voor nodig.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Duur</td> 
   <td>Ga of kaart de lengte van de vraag in milliseconden in</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Externe account-id</td> 
   <td>Dit gebied vertegenwoordigt interne rekening ID van een vraag die in HubSpot wordt gemaakt. Er is geen actie voor nodig.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL van opname</td> 
   <td>Voer de URL van het opnamebestand in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Vergaderingsvelden

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Title]</p> </td> 
   <td> <p>Ga of kaart de titel of het onderwerp van de vergadering in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Voer de tekst van de beschrijving van de vergadering in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Time]</td> 
  <td>Voer de begintijd van de vergadering in of wijs deze toe als een UNIX-tijdstempel.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Eindtijd</td> 
   <td>Voer de eindtijd van de vergadering in of wijs deze toe als een UNIX-tijdstempel.</td> 
  </tr> 
 </tbody> 
</table>

#### Taakvelden

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Subject]</p> </td> 
   <td> <p>Voer de titel of het onderwerp van de taak in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Voer de tekst van de taakbeschrijving in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Status</td> 
   <td>Selecteer de status van de taak.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL For Object Type]</td> 
  <td>Voer <code>CONTACT</code> of <code>COMPANY</code> in.
  </td> 
   </tr> 
 </tbody> 
</table>

+++

+++ **Schrap een Betrokkenheid**

Deze actiemodule verwijdert een betrokkenheid met de id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Voer de id in van de betrokkenheid die u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **van het 0} Horloge Afspraken**

Deze triggermodule start een scenario wanneer een nieuwe betrokkenheid wordt gemaakt in een portal. Deze module retourneert alleen records die in de laatste 30 dagen zijn gemaakt, of de 10.000 records die het laatst zijn gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Het maximumaantal bedrijven [!DNL Workfront Fusion] moet worden geretourneerd tijdens één uitvoeringscyclus van het scenario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>Voer de vroegste datum in waarvoor u gebeurtenissen wilt bekijken of wijs deze datum toe. Gebruik de indeling <code>MM/DD/YYYY h:mm</code> .</td> 
  </tr> 
 </tbody> 
</table>

+++

### Gebeurtenissen en meldingen

<!--* [Create / Update a Timeline Event](#create--update-a-timeline-event)
* [List Timeline Event Types](#list-timeline-event-types)
* [Watch Calendar Events](#watch-calendar-events)
* [Watch Notifications](#watch-notifications)-->

+++ **creeer/werk een Gebeurtenis van de Chronologie bij**

In deze actiemodule wordt een tijdlijngebeurtenis gemaakt of bijgewerkt. Deze module kan slechts met een ontwikkelaarverbinding worden gebruikt die uw gebruikersherkenningsteken, uw sleutel van HubSpot API, identiteitskaart van de Cliënt, en Geheim van de Cliënt omvat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Voer de id in van de toepassing waartoe deze gebeurtenis behoort of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>Voer een id voor deze gebeurtenis in of wijs deze toe. Gebeurtenis-id's worden niet gegenereerd door het systeem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Type ID]</td> 
   <td>Voer de id van het gebeurtenistype van deze gebeurtenis in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Voer het e-mailadres in of wijs het e-mailadres toe van de contactpersoon waarvoor u de gebeurtenis maakt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object ID]</td> 
   <td>Voer de id in van de contactpersoon waarvoor u de gebeurtenis maakt of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp]</td> 
   <td>Voer het tijdstempel voor deze gebeurtenis in of wijs dit toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom data]</td> 
   <td>Voor elk punt van douanegegevens dat u aan deze gebeurtenis wilt toevoegen, <b> toevoegen punt </b> en ga de naam en de waarde van het punt in.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **de Types van Gebeurtenis van de Chronologie van de Lijst**

Deze zoekmodule retourneert een lijst met alle tijdlijngebeurtenissen voor een specifieke toepassing. Deze module kan slechts met een ontwikkelaarverbinding worden gebruikt die uw gebruikersherkenningsteken, uw sleutel van HubSpot API, identiteitskaart van de Cliënt, en Geheim van de Cliënt omvat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Voer de id in van de toepassing waartoe deze gebeurtenissen behoren of wijs deze toe. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Gebeurtenissen van de Kalender van het Controle**

Deze triggermodule start een scenario wanneer een nieuwe gebeurtenis aan een kalender wordt toegevoegd. Het omvat tot 500 taken in het interval tussen de begin en einddatum. Deze module kan slechts met een ontwikkelaarverbinding worden gebruikt die uw gebruikersherkenningsteken, uw sleutel van HubSpot API, identiteitskaart van de Cliënt, en Geheim van de Cliënt omvat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Events Type]</td> 
   <td>Selecteer of u sociale gebeurtenissen, inhoudsgebeurtenissen of alle gebeurtenissen wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal dossiers in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Voer de begindatum in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Voer de einddatum in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **de Meldingen van het Controle**

Deze triggermodule start een scenario wanneer een nieuw bericht over wijzigingen wordt verzonden.  Het omvat tot 500 taken in het interval tussen de begin en einddatum. Deze module kan slechts met een ontwikkelaarverbinding worden gebruikt die uw gebruikersherkenningsteken, uw sleutel van HubSpot API, identiteitskaart van de Cliënt, en Geheim van de Cliënt omvat. U kunt slechts één webhaak URL per ontwikkelaarstoepassing in HubSpot hebben.

Om een webhaak voor deze module tot stand te brengen, **voeg** naast het WebHaakgebied toe en vul de volgende gebieden uit:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Voer de toepassings-id in die u voor deze website wilt gebruiken. U kunt identiteitskaart in uw HubSpot ontwikkelaarsportaal vinden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscriptions]</td> 
   <td> <p>Voor elk type van bericht dat u wilt letten, <b> toevoegen punt </b> klikken en het abonnementstype selecteren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Force to Remove Old Subscriptions]</td> 
   <td>Schakel deze optie in om oude abonnementen die aan deze webhaak zijn gekoppeld, los te koppelen of te verwijderen.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Bestanden

<!--* [[!UICONTROL Create a Folder]](#create-a-folder)
* [Delete a File](#delete-a-file)
* [[!UICONTROL Delete a Folder]](#delete-a-folder)
* [List Files](#list-files)
* [[!UICONTROL Move a File]](#move-a-file)
* [Upload a file](#upload-a-file)
* [Watch files](#watch-files)-->

+++ **[!UICONTROL Create a Folder]**

Deze module maakt een map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Name] </td> 
   <td>Voer een naam voor de nieuwe map in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID] </td> 
   <td>Selecteer de id van de bovenliggende map voor de map die u maakt. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Schrap een Dossier**

In deze actiemodule worden een bestand en alle bijbehorende gegevens en miniaturen permanent verwijderd uit het bestandsbeheer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Voer de id in van het bestand dat u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Folder]**

Hiermee markeert u een map als verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van de map die u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **de Dossiers van de Lijst**

Deze zoekmodule retourneert een lijst met bestanden die zijn opgeslagen in het bestandsbeheer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal dossiers in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Voer de id in of wijs deze toe aan de map met de bestanden die u wilt weergeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Als u alleen bestanden met specifieke tekens in de bestandsnaam wilt opnemen, voert u de tekens in die de bestandsnaam moet bevatten of wijst u deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Move a File]**

Hiermee verplaatst u een bestand naar een andere map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID] </td> 
   <td>Voer de id in van het bestand dat u wilt verplaatsen of wijs deze toe. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Selecteer de id van de map waarin u het bestand wilt verplaatsen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Voer een naam in voor het verplaatste bestand.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **upload een Dossier**

Deze actiemodule uploadt een bestand naar het bestandsbeheer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access type] </td> 
   <td>Selecteer of u het bestand privé, openbaar maar niet indexeerbaar of openbaar en indexeerbaar wilt maken. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Selecteer de id van de map waarin u het bestand wilt uploaden. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Schakel deze optie in om het bestand te overschrijven als dit al in de map bestaat.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **de Dossiers van het Controle**

Deze triggermodule start een scenario wanneer een nieuw bestand wordt opgeslagen in het bestandsbeheer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal dossiers in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Voer de id in van de map met de bestanden die u wilt controleren of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Als u alleen bestanden met specifieke tekens in de bestandsnaam wilt opnemen, voert u de tekens in die de bestandsnaam moet bevatten of wijst u deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Taken

<!--* [Create a Calendar Task](#create-a-calendar-task)
* [Delete a Calendar Task](#create-a-calendar-task)
* [Watch Task Events](#watch-task-events)-->

+++ **creeer een taak van de Kalender**

Deze actiemodule maakt een nieuwe taak voor een kalender. De verbinding die in deze module wordt gebruikt moet de geloofsbrieven van een gebruiker met een betaalde rekening van de Marketing gebruiken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Voer een naam in of wijs een naam toe aan de nieuwe kalendertaak.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Voer een beschrijving voor de nieuwe kalendertaak in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td>Voer de eigenaar-id in of wijs deze toe aan de gebruiker die aan deze taak is toegewezen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Date]</td> 
   <td>Voer de datum voor deze taak in of wijs deze toe.<p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Selecteer het type gebeurtenis.<ul><li><b>Blogbericht</b><p>Voer de id van de inhoudsgroep in. Dit is de id van de blogpagina.</p></li><li><b>E-mail</b><p>Voer het pad in of wijs het toe aan de e-mailsjabloon die u wilt gebruiken.</li><li><b>Openingspagina</b><p>Voer het pad in of wijs het toe aan de sjabloon van de bestemmingspagina die u wilt gebruiken.</li><li><b>Aangepast</b></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Voer in of de gebeurtenis zich in de status "Aan" of "Gereed" bevindt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign GUID]</td> 
   <td>Ga of kaart interne identiteitskaart HubSpot van de campagne in dat deze gebeurtenis deel van uitmaakt.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Schrap een Taak van de Kalender**

Met deze actiemodule verwijdert u een kalendertaak. De verbinding die in deze module wordt gebruikt moet de geloofsbrieven van een gebruiker met een betaalde rekening van de Marketing gebruiken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van de taak die u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Gebeurtenissen van de Taak van het Controle**

Deze triggermodule start een scenario wanneer er een nieuwe taakgebeurtenis in een kalender plaatsvindt. De verbinding die in deze module wordt gebruikt moet de geloofsbrieven van een gebruiker met een betaalde rekening van de Marketing gebruiken. De module retourneert maximaal 500 gebeurtenissen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal dossiers in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Voer de vroegste datum in waarvoor u gebeurtenissen wilt bekijken of wijs deze datum toe. Gebruik de indeling <code>MM/DD/YYYY h:mm</code> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Voer de laatste datum in of wijs deze toe waarvoor u gebeurtenissen wilt bekijken. Gebruik de indeling <code>MM/DD/YYYY h:mm</code> .</td> 
  </tr> 
 </tbody> 
</table>

+++

### Gebruikers

<!--* [Get an Owner](#get-an-owner)
* [List Owners](#list-owners)-->

+++ **krijgt een Eigenaar**

Deze actiemodule retourneert details van een eigenaar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td> <p>Voer de id van de eigenaar in of wijs deze toe waarvoor u details wilt retourneren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Eigenaars van de Lijst**

Deze onderzoeksmodule keert een lijst van alle eigenaars in een rekening HubSpot terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Tickets

<!--* [Create a Ticket]-->
<!--* [Delete a Ticket](#delete-a-ticket)-->
<!--* [Create a Ticket]-->
<!--* [Create a Ticket]-->
<!--* [Create a Ticket]-->
<!--* [Create a Ticket]-->

<!-- Create a Ticket Need to find a working connection-->

+++ **[!UICONTROL Delete a Ticket]**

Verwijdert een bestaand ticket met zijn id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van het ticket dat u wilt verwijderen. </td> 
  </tr> 
 </tbody> 
</table>

+++

<!-- Get a Ticket  Need to find a working connection-->

<!-- List Tickets  Need to find a working connection-->

&lt;!— Werk een Ticket bij die een werkende verbinding moet vinden—>

<!-- Watch Tickets Need to find a working connection-->

### Forms

<!--* [Get a File Uploaded via Form](#get-a-file-uploaded-via-form)
* [List Forms](#list-forms)-->
<!--* [Submit Data to a Form]-->
<!--* [Watch Submissions for a Form]-->

+++ **krijg een Dossier dat via Vorm** wordt geupload

Deze actiemodule retourneert een bestand dat via een formulier is geüpload.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td>Voer de URL in of wijs deze toe aan het bestand dat u wilt ophalen. Dit vindt u in de metagegevens van het formulier.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Lijst Forms**

Deze actiemodule retourneert alle formulieren die zijn gemaakt in de account die is gekoppeld aan de verbinding die voor deze module wordt gebruikt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Voer in of wijs het maximumaantal formulieren toe dat de module in één uitvoeringscyclus retourneert.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--#### Submit Data to a Form Need to find a working connection-->



&lt;!—#### Controle verzenden voor een formulier—U moet een werkende verbinding zoeken>—>

### Sociale media (uitzending)

<!--* [Cancel a Broadcast Message](#cancel-a-broadcast-message)
* [Create a Broadcast Message](#create-a-broadcast-message)
* [Watch Broadcast Messages](#watch-broadcast-messages)-->

+++ **annuleert een Bericht van de Uitzending**

Deze actiemodule annuleert een geplande uitzending, zoals een tweet of een Facebook-bericht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Ga of kaart identiteitskaart van de uitzending in die u wilt annuleren.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **creeer een Bericht van de Uitzending**

Deze actiemodule maakt en publiceert onmiddellijk een bericht op het opgegeven sociale-mediakanaal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel ID]</td> 
   <td>Ga of kaart identiteitskaart van het kanaal in dat u voor deze uitzending wilt gebruiken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Ga of kaart een titel voor deze uitzending in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Ga of kaart de tekst van de uitzending in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Photo URL]</td> 
   <td>Typ of wijs de URL toe van een foto die u in de uitzending wilt opnemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thumbnail URL]</td> 
   <td>Voer de URL in van een miniatuur die u voor deze uitzending wilt gebruiken of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trigger at]</td> 
   <td>Ga of kaart de datum en de tijd in dat u de uitzending wilt worden verzonden. Als dit leeg wordt gelaten, wordt de uitzending onmiddellijk verzonden.<p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **de Berichten van de Uitzending van de Controle**

Deze trekkermodule begint een scenario wanneer een bericht van HubSpot aan het gespecificeerde sociale media kanaal wordt gepost.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Ga of kaart het maximumaantal punten in dat de module in één uitvoeringscyclus zal terugkeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Status]</td> 
   <td>Om het scenario slechts te beginnen wanneer het bericht in een specifieke status is, selecteer de status.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Channel]</td> 
   <td>Om het scenario slechts te beginnen wanneer het bericht op een specifiek kanaal is, selecteer het kanaal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Als u het scenario alleen wilt starten wanneer het bericht zich op of na een bepaalde datum bevindt, voert u de datum in de notatie <code>MM/DD/YYYY</code> in of wijst u deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Blogberichten

<!--* [Create a Blog Post]-->
<!--* [Delete a Blog Post](#delete-a-blog-post)-->
<!--* [List Blog Posts]-->
&lt;!—* [ publiceert/publiceert een Blogpost ](#publish--unpublish-a-blog-post)—>
<!--* [Watch Blog Posts]-->

<!--
#### Create a Blog Post May need connection
-->


+++ **Schrap een Blogpost**

Met deze actiemodule verwijdert u één blogbericht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van het blogbericht dat u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--#### List Blog Posts May need connection

This search module retrieves posts from a HubSpot blog.-->

+++ **publiceer/unpublish een Blogbericht**

Deze actiemodule plant of annuleert het publiceren van een blogbericht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van het blogbericht dat u wilt plannen of annuleren of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Selecteer of u het blogbericht wilt plannen of een eerder gepland blogbericht wilt annuleren.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--#### Watch Blog PostsMay need connection-->

<!--+++**Workflows**>

<!--### Workflows May need connection

#### Add a Contact to a Workflow


#### Remove a Contact from a Workflow

-->

<!--+++-->

### Abonnementen

<!--* [Update Email Subscription](#update-email-subscription)
* [Watch Subscriptions Timeline for a Portal](#watch-subscriptions-timeline-for-a-portal)-->

+++ **Update E-mailabonnement**

Deze actiemodule werkt een e-mailabonnement in HubSpot bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Voer het e-mailadres in of wijs het e-mailadres toe van het abonnement dat u wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Statuses]</td> 
   <td>Voor elke status die u het abonnement voor wilt bijwerken, <b> toevoegen punt </b> en ingaan identiteitskaart van de status, en of het e-mailadres aan die status zal worden ingetekend.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Status]</td> 
   <td>Als u de rechtsgrondslag voor dit abonnement op GDPR wilt vastleggen, selecteert u de juridische status van dit abonnement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Basis Explanation]</td> 
   <td>Als u een opmerking wilt toevoegen over de rechtsgrondslag voor dit abonnement op de GDPR, voert u de tekst van de notitie in of wijst u deze toe.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **de Chronologie van Abonnementen van het Controle voor een Portaal**

Deze triggermodule start een scenario wanneer een nieuw abonnement op de e-mailtijdlijn wordt toegevoegd aan de portal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Ga of kaart het maximumaantal punten in dat de module in één uitvoeringscyclus zal terugkeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Timestamp]</td> 
   <td>Als u resultaten wilt retourneren vanaf of na een bepaalde datum, voert u de datum in de notatie in <code>MM/DD/YYYY.</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Timestamp]</td> 
   <td>Als u resultaten wilt retourneren vanaf of vóór een bepaalde datum, voert u de datum in de notatie in <code>MM/DD/YYYY.</code></td> 
  </tr> 
 </tbody> 
</table>

+++

<!--+++**Associations**-->

<!--### Associations-->

<!--#### Associate CRM Objects  May need connection

This action module associates two CRM objects.-->

<!--#### Associate Multiple CRM Objects  May need connection-->



<!--#### Delete an Association May need connection-->



<!--#### Delete Multiple Associations between CRM Objects May need connection-->



<!--#### List Associations for a CRM Object May need connection-->

<!--+++-->

### Overige

+++ **[!UICONTROL Make an API Call]**

Hiermee kunt u een aangepaste API-aanroep uitvoeren.

>[!NOTE]
>
>De volgende eindpunten werden afgekeurd in HubSpot API op 31 Augustus, 2023, en kunnen niet meer in de modules van de Fusie worden gebruikt.
>
>* Gebeurtenissen voor inhoud weergeven
>* Sociale gebeurtenissen weergeven
>* Taakgebeurtenissen voor agenda weergeven
>* Alle kalendergebeurtenissen weergeven
>* Kalendertaak maken
>* Kalendertaak ophalen op id
>* Kalender bijwerken
>* Een kalendertaak verwijderen

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL HubSpot CRM] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van https://api.hubapi.com/. Bijvoorbeeld /contacten/v1/lists/all/contacten/all</p> <p>Raadpleeg de <a href="https://legacydocs.hubspot.com/docs/overview">[!DNL HubSpot] API-documentatie </a> voor de lijst met beschikbare eindpunten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP-methode die u wilt gebruiken:</p> <p>[!UICONTROL GET]</p> <p>om informatie voor een ingang terug te winnen.</p> <p>[!UICONTROL POST]</p> <p>om een nieuw item te maken.</p> <p>[!UICONTROL PUT]</p> <p>om een bestaand item bij te werken of te vervangen.</p> <p>[!UICONTROL PATCH]</p> <p>om een gedeeltelijke ingsupdate te maken.</p> <p>[!UICONTROL DELETE]</p> <p>om een item te verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p> Voer de gewenste aanvraagheaders in. Je hoeft geen autorisatieheaders toe te voegen; dat hebben we al voor je gedaan.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Voer de queryreeks voor de aanvraag in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst van de API-aanroep toe in de vorm van een standaard JSON-object. Plaats de aanhalingstekens buiten de voorwaardelijke instructie wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Voorbeeld:** de volgende API vraag keert alle contacten in uw [!DNL HubSpot] rekening terug:
>
>**URL**: `/contacts/v1/lists/all/contacts/all`
>
>**Methode**: `GET`
>
>![ Hubspot API configuratie ](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-config.png)
>
>Overeenkomsten met de zoekopdracht vindt u in de sectie Uitvoer van de module onder [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL contacts] .
>
>In ons voorbeeld, zijn 3 contacten teruggekeerd:
>
>![ Uitvoer van hubspot API ](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-output.png)

+++

## Een nieuwe toepassing maken

1. Meld u aan bij uw [!DNL HubSpot] -ontwikkelaarsaccount.
1. Selecteer de optie **[!UICONTROL Create an App]** .
1. Voer de toepassingsnaam en het dialoogvenster [!UICONTROL Save] in.
1. Selecteer het bereik dat u nodig hebt voor uw webhaak.

   Bijvoorbeeld, voeg contactwerkingsgebied voor het teweegbrengen van de module toe wanneer een nieuw contact wordt gecreeerd of geschrapt.

   De [!UICONTROL contacts scope] is alles wat u nodig hebt om contactpersonen, deals en webpagina&#39;s voor bedrijfsgebeurtenissen te ontvangen.

   >[!IMPORTANT]
   >
   >Vul het veld [!UICONTROL Redirect URL] niet in.

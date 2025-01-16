---
title: Airtable-modules
description: Adobe Workfront Fusion vereist naast een Adobe Workfront-licentie een Adobe Workfront Fusion-licentie.
author: Becky
feature: Workfront Fusion
exl-id: 3b445b50-5812-4ded-9788-f467991e0b52
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 0%

---

# Airtable-modules


Met de [!DNL Airtable] -connector voor [!DNL Adobe Workfront Fusion] kunt u een scenario starten op basis van gebeurtenissen in uw [!DNL Airtable] -account, records maken, uploaden en bijwerken, records zoeken en aangepaste API-aanroepen naar de Airtable API uitvoeren.

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
   <td> <p>[!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en -integratie] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>Uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

U moet een Airtable-account hebben om de functionaliteit in dit artikel te kunnen gebruiken.

<!--
<p>For more information, see the tutorial .</p>
-->

## Airtable API-informatie

De Airtable schakelaar gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://api.airtable.com/v0</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v3.3.28</td> 
  </tr>
 </tbody> 
 </table>

## Airtable aansluiten op Workfront Fusion {#connect-airtable-to-workfront-fusion}

<!--

1. Log in to your Airtable account.
1. Open your account overview and generate the API key.
-->
1. Open de Fusie van Workfront en **creeer een verbinding** dialoog van de gewenste module.
1. Voer een naam in voor de verbinding.
1. (Optioneel) Klik op Geavanceerde instellingen tonen en voer uw Airtable client-id en clientgeheim in.
1. Klik op de knop **Doorgaan** om de verbinding te maken en terug te keren naar de module.

## Airtable-modules en hun velden

### Records

* [ creeer een Verslag ](#create-a-record)
* [ Schrap een Verslag ](#delete-a-record)
* [ krijg een verslag ](#get-a-record)
* [ Verslagen van het Onderzoek ](#search-records)
* [ werk een Verslag ](#update-a-record) bij
* [ Upsert een Verslag ](#upsert-a-record)
* [Controleregisters](#watch-records)
* [Reacties controleren](#watch-responses)
* [Een API-aanroep maken](#make-an-api-call)

#### Een record maken {#create-a-record}

Deze actiemodule maakt een nieuwe record.

U geeft de gegevens op die u in de record wilt opnemen en waar u deze wilt opslaan.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Airtable rekening aan de Fusie van Workfront, zie <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref"> Airtable aan de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Selecteer de basis waartoe de nieuwe record behoort.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabel </td> 
   <td> <p>Selecteer de tabel waartoe de nieuwe record behoort.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Opnemen</p> </td> 
   <td> <p>Voer de waarden voor de nieuwe record in. Beschikbare velden zijn gebaseerd op de tabel die u hebt geselecteerd.</p> <!--<p>For more information on field types, search for "Supported field types" in the Airtable documentation.</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>Multiple lines of text, which may contain "mention tokens", for example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong> : Add the attachment. Airtable will download the file from the provided <code>url</code> and keep its own copy of it. If the File name field is left empty, Airtable generates the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05 (ISO 8601 formatted date)</li> 
     <li>Phone number:</li> 
     <li><strong>Emails</strong>: A valid email address.</li> 
     <li><strong>URL</strong>: A valid URL (for example, airtable.com or https://airtable.com/universe).</li> 
     <li><strong>Number</strong>: Enter a number.</li> 
     <li><strong>Currency</strong>: Currency value.</li> 
     <li><strong>Percent</strong>: A percentage value. Must be higher than or equal to 0.</li> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation. </li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs will be reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Slimme koppelingen</td> 
   <td> <p>Schakel deze optie in om namen in te voeren in plaats van record-id's naar velden die een koppeling naar een andere tabel bevatten. De record wordt automatisch gemaakt in de gekoppelde tabel als er geen overeenkomst is.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een record verwijderen {#delete-a-record}

Deze actiemodule verwijdert een bepaalde record.

U geeft de id en de locatie van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Airtable rekening aan de Fusie van Workfront, zie <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref"> Airtable aan de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Selecteer de basis die de record bevat die u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabel </td> 
   <td> <p>Selecteer de tabel die de record bevat die u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td>Record-id</td> 
   <td> <p>Ga of kaart unieke Airtable identiteitskaart van het verslag in dat u de module wilt schrappen. U kunt de id bijvoorbeeld ophalen met de module Zoeken in records.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een record ophalen {#get-a-record}

In deze actiemodule worden recorddetails opgehaald.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Airtable rekening aan de Fusie van Workfront, zie <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref"> Airtable aan de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Selecteer de basis die de tabel bevat met de record die u wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabel</td> 
   <td> <p> Selecteer de tabel met de record waarvoor u de details wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>Record-id</td> 
   <td> <p> Voer de id in van de record waarvoor u details wilt ophalen of wijs deze id toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Zoeken in records {#search-records}

Deze zoekmodule zoekt naar records in een object in Airtable die overeenkomen met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Airtable rekening aan de Fusie van Workfront, zie <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref"> Airtable aan de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Selecteer de basis waarnaar u records wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabel </td> 
   <td> <p>Selecteer de tabel die u wilt zoeken naar records.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Formule</p> </td> 
   <td> <p>Een formule die wordt gebruikt om records te filteren. De formule wordt geëvalueerd voor elke record en als het resultaat niet <code>0</code> , <code>false</code> , <code>""</code> , <code>NaN</code> , <code>[]</code> of <code>#Error!</code> is, wordt de record opgenomen in de reactie.</p> <p>Als deze worden gecombineerd met de <code>view</code> , worden alleen records in die weergave geretourneerd die aan de formule voldoen.</p> <p>Als u bijvoorbeeld alleen records wilt opnemen waarin de naam niet leeg is, geeft u het volgende door:<code> NOT({Name} = '')</code></p> <p>Voor meer informatie, onderzoek naar informatie over de verwijzingen van het formulegebied in de Airtable steundocumentatie.</p> </td> 
  </tr> 
  <tr> 
   <td>Sorteren </td> 
   <td> <p>Selecteer de sorteerrichting en het veld waarop u de resultaten wilt sorteren.</p> </td> 
  </tr> 
  <tr> 
   <td>Weergave </td> 
   <td> <p>Selecteer de weergave waarnaar u records wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>Limiet</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een record bijwerken {#update-a-record}

Deze actiemodule werkt een bepaalde record bij.

U geeft de id van de record op en de nieuwe gegevens die u in de record wilt opnemen.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Airtable rekening aan de Fusie van Workfront, zie <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref"> Airtable aan de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Selecteer de basis die de record bevat die u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabel </td> 
   <td> <p>Selecteer de tabel die de record bevat die u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td>Record-id </td> 
   <td> <p>Ga of kaart unieke Airtable identiteitskaart van het verslag in dat u de module wilt bijwerken. U kunt de id bijvoorbeeld ophalen met de module Zoeken in records.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Opnemen</p> </td> 
   <td> <p>Voer de waarden voor de nieuwe record in. Welke velden beschikbaar zijn, is afhankelijk van de tabel die u hebt geselecteerd.</p> <!--<p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Slimme koppelingen</td> 
   <td> <p>Geef namen op in plaats van record-id's voor velden die een koppeling naar een andere tabel bevatten. De record wordt automatisch gemaakt in de gekoppelde tabel als er geen overeenkomst is.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een record bijwerken

Deze actiemodule werkt een bepaalde record bij of voegt deze in.

U geeft de id van de record op en de nieuwe gegevens die u in de record wilt opnemen.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Airtable rekening aan de Fusie van Workfront, zie <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref"> Airtable aan de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Selecteer de basis die de record bevat die u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabel </td> 
   <td> <p>Selecteer de tabel die de record bevat die u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td>Record-id </td> 
   <td> <p>Als u een record bijwerkt, voert u de unieke Airtable-id in of wijst u deze toe aan de record die u wilt bijwerken in de module. U kunt de id bijvoorbeeld ophalen met de module Zoeken in records.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Opnemen</p> </td> 
   <td> <p>Voer de waarden voor de nieuwe record in. Welke velden beschikbaar zijn, is afhankelijk van de tabel die u hebt geselecteerd.</p> <!-- <p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Slimme koppelingen</td> 
   <td> <p>Geef namen op in plaats van record-id's voor velden die een koppeling naar een andere tabel bevatten. De record wordt automatisch gemaakt in de gekoppelde tabel als er geen overeenkomst is.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Controleregisters {#watch-records}

Deze triggermodule start een scenario wanneer een record wordt gemaakt of bijgewerkt in de opgegeven tabel.

>[!NOTE]
>
>Als u deze module wilt gebruiken, moet u het veld Gemaakt tijd of Laatst gewijzigd tijdstip in uw tabel maken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Airtable rekening aan de Fusie van Workfront, zie <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref"> Airtable aan de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Selecteer de basis u voor nieuwe verslagen wilt letten.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabel </td> 
   <td> <p>Selecteer de tabel die u wilt controleren voor nieuwe records.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Configuratie activeren</p> </td> 
   <td> <p>Triggerveld</p> <p>Een <code>Created Time</code> - of <code>Last Modified Time</code> -veld dat wordt gebruikt om records te sorteren. Als u geen <code>Created Time</code> of <code>Last Modified Time</code> gebied in uw schema hebt, moet u tot stand brengen. </p> <p>Veld Label</p> <p>Een veld dat wordt gebruikt als label voor een record, bijvoorbeeld in het dialoogvenster Kies waar u wilt beginnen.</p> </td> 
  </tr> 
  <tr> 
   <td>Limiet</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt letten.</p> </td> 
  </tr> 
  <tr> 
   <td>Weergave</td> 
   <td> <p>Selecteer de gewenste weergave.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Formule</p> </td> 
   <td> <p>Een formule die wordt gebruikt om records te filteren. De formule wordt geëvalueerd voor elke record en als het resultaat niet <code>0</code> , <code>false</code> , <code>""</code> , <code>NaN</code> , <code>[]</code> of <code>#Error!</code> is, wordt de record opgenomen in de reactie.</p> <p>Als deze worden gecombineerd met de <code>view</code> , worden alleen records in die weergave geretourneerd die aan de formule voldoen.</p> <p>Als u bijvoorbeeld alleen records wilt opnemen waarin de naam niet leeg is, geeft u het volgende door:<code> NOT({Name} = '')</code></p> <p>Voor meer informatie, zie de informatie over de verwijzingen van het formuleringsgebied in de Airtable steundocumentatie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Reacties controleren

Deze triggermodule start een scenario wanneer een formulier wordt verzonden.

>[!NOTE]
>
>Deze functionaliteit is alleen beschikbaar voor betaald Airtable Pro-abonnement.

De URL van de webhaak moet worden gegenereerd in Workfront Fusion en vervolgens worden toegevoegd aan de formulierconfiguratie in Airtable.

1. Voeg de module Nieuwe reacties controleren toe aan uw Workfront Fusion-scenario.
1. Genereer en kopieer de URL van de webhaak.

   <!--For instructions, see [Instant triggers (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->

1. Meld u aan bij uw Airtable-account.
1. Open de basis en de tabel die u voor het formulier wilt gebruiken en maak een formulierweergave.
1. Stel het formulier naar wens in, schuif omlaag in het formulier en schakel de optie Omleiden naar URL in nadat het formulier is verzonden.
1. Ga Webhaak URL in die in stap 2 aan de getoonde dialoogdoos wordt geproduceerd en voeg ?record_id= {record_id} enkel na Webhaak URL toe om identiteitskaart van het Verslag in de output van de module te omvatten, dan sparen te klikken. De resulterende URL ziet er bijvoorbeeld als volgt uit:
1. Ga terug naar uw scenario van de Fusie van Workfront en stel de module van de Reacties van het Controle slechts in werking om gebieden van Airtable te laden en die gebieden in de andere modules in kaart te kunnen brengen.
1. Verzend het formulier in Airtable waar de optie Omleiden naar URL nadat het formulier is verzonden is ingeschakeld en WebHaak-URL is toegevoegd (stap 6 hierboven).

   De module Reacties controleren wordt geactiveerd en de gewenste gegevens worden geladen.

1. Voeg Airtable > krijgt een module van het Verslag enkel na Airtable > de module van de Reacties van het Controle toe en kaart record_id aan het gebied van identiteitskaart van het Verslag.

Telkens wanneer het formulier wordt verzonden, wordt de module Reacties controleren in uw Workfront Fusion-scenario geactiveerd en retourneert de module Een record ophalen de verzonden formuliergegevens.

#### Een API-aanroep maken

#### Aangepaste API-aanroep

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Airtable] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Airtable] -modules kan worden uitgevoerd.

De handeling is gebaseerd op het door u opgegeven eenheidstype (allocadia-objecttype).

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Verbinding</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw Airtable rekening aan de Fusie van Workfront, zie <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref"> Airtable aan de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://api.airtable.com/</code> . Voorbeeld: <code>v0/{base}/{table}</code> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Methode</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP-aanvraagmethoden in [!DNL Adobe Workfront Fusion]</a> voor meer informatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kopteksten</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Hiermee voegt u de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tekenreeks query</td> 
   <td> <p>Voeg de vraag voor de API vraag in de vorm van een Sleutel en een Waarde toe</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lichaam</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

---
title: CSV
description: Met de Adobe Workfront Fusion CSV-modules kunt u CSV-bestanden maken en CSV-tekst parseren op basis van een ontvangen tekstwaarde of een bestand.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# CSV

Met de modules [!DNL Adobe Workfront Fusion] [!UICONTROL CSV] kunt u CSV-bestanden maken en CSV-tekst parseren op basis van een ontvangen tekstwaarde of een bestand.

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
   <p>Vereiste voor verouderde licentie: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en -integratie], [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering]</p>
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

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## [!UICONTROL Create CSV]

Met de aggregator [!UICONTROL Create CSV] kunt u een CSV-tekst maken van ontvangen tekstwaarden.

Voor meer informatie over aggregators, zie [ de module van de Samenvoegaar ](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Selecteer de module die u gebruikt om de velden samen te voegen die u nodig hebt.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Aggregated Fields]</td>
        <td>Selecteer de velden die u wilt samenvoegen in de lijst met beschikbare velden.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Include headers in the first row]</td>
        <td>Selecteer deze optie om de kopteksten in het resultaat op te nemen.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Group by]</td>
        <td>Voer het filter in om de resultaten te groeperen. Voer bijvoorbeeld een datum in.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Stop processing after an empty aggregation]</td>
        <td>Selecteer deze optie om het scenario te stoppen als er geen resultaten zijn.</td>
    </tr>
</table>

## [!UICONTROL Create CSV (advanced)]

Met de [!UICONTROL Create CSV (advanced)] -aggregator kunt u een CSV-tekst maken van ontvangen tekstwaarden. Er wordt een gegevensstructuur gebruikt die de CSV-kolommen in het resulterende CSV-bestand definieert. Zodra bepaald, verschijnen de kolommen als gebieden in de CSV moduleopstelling, en kunnen aan recentere module in het scenario worden in kaart gebracht.

Voor meer informatie over aggregators, zie [ de module van de Samenvoegaar in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td>Selecteer de toepassingsmodule die u gebruikt om de velden samen te voegen die u nodig hebt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Selecteer de gegevensstructuur om de velden op de gewenste manier samen te voegen. Nadat u de gegevensstructuur hebt gedefinieerd, kunt u de items toewijzen aan de corresponderende velden.</p> <p>Zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref"> Gegevensstructuren in [!DNL Adobe Workfront Fusion]</a> voor meer informatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include headers in the first row] </td> 
   <td>Selecteer deze optie om de kopteksten in het resultaat op te nemen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by] </td> 
   <td>Voer het filter in om de resultaten te groeperen. Voer bijvoorbeeld een datum in. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation] </td> 
   <td>Selecteer deze optie om het scenario te stoppen als er geen resultaten zijn. </td> 
  </tr> 
 </tbody> 
</table>


<p>Laten we aannemen dat u uw Google-contactpersonen wilt exporteren naar een CSV-bestand met twee kolommen Volledige naam en E-mail. De uitvoerbundel van de module [!UICONTROL Google Contacts] &gt; [!UICONTROL Get contacts from a group] heeft de volgende structuur. De e-mailadressen worden opgeslagen in het item <code>[!UICONTROL Emails[]]</code> . Dit is een array van verzamelingen. Elke verzameling bevat twee items: <code>Label</code> en <code>Email</code> .</p>
<p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png" style="width: 350;height: 546;"> </p>
<p>Als u de eenvoudige module [!DNL Create CSV] gebruikt, krijgt u een lijst met selectievakjes die overeenkomen met de items op hoofdniveau van een bundel. Wanneer u probeert items <code>Full name</code> en <code>Emails</code> aan te kruisen, produceert de module [!UICONTROL Create CSV] de volgende uitvoer, wat waarschijnlijk niet uw bedoeling is:</p>
<p>"emails","fullName"</p>
<p>"[object Object]","Winner delen"</p>
<p>"[object Object]","Lizeth Fulmore"</p>
<p>"[object Object]","Hilario Gullatt"</p>
<p>"[Object Object Object]","Abby Eisenbarth"</p>
<p>Aangezien het item <code>Full Name</code> van het eenvoudige type Tekst is, wordt het net prima geëxporteerd. Maar het item <code>Emails</code>, dat van een complex type Array van Verzamelingen is, wordt geëxporteerd als [object Object], dat aangeeft hoe Verzamelingen en arrays standaard worden getransformeerd naar tekst. Voor meer informatie, zie {de gegevenstypes van 0} Punt in de Fusie van Adobe Workfront </a>.<a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref"></p>
<p>Als u inhoud van het <code>Email </code> -item van de eerste verzameling van de <code>Emails[]</code> -array wilt exporteren, moet u de [!UICONTROL Create CSV (advanced)] -module gebruiken. De module laat u toe om individuele kolommen van uw Csv- dossier te bepalen en punten aan hen, met inbegrip van genestelde degenen in kaart te brengen.</p>
<ol>
<li value="1">Voeg de module [!UICONTROL Create CSV (advanced)] in een scenario in en open de configuratie ervan.</li>
<li value="2">Klik op de knop <strong>[!UICONTROL Add]</strong> naast het veld [!UICONTROL Data structure] om een nieuwe gegevensstructuur te maken.</li>
<li value="3"> <p>Schrijf een naam voor de gegevensstructuur in en klik op de knop <strong>[!UICONTROL Add item]</strong> om de afzonderlijke kolommen toe te voegen. Als u twee kolommen wilt exporteren: "Volledige naam" en "E-mail", ziet de resulterende gegevensstructuur er als volgt uit:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png" style="width: 350;height: 524;"> </p> </li>
<li value="4"> <p>Nadat u de gegevensstructuur hebt gedefinieerd, worden de velden die overeenkomen met elke afzonderlijke kolom weergegeven in de configuratie van de module [!UICONTROL Create CSV (advanced)] , zodat u de items kunt toewijzen. Neem het eerste item van de array <code>[!UICONTROL Emails[]]</code> en wijs het item <code>Email </code> ervan toe aan het veld/de kolom-e-mail:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png" style="width: 350;height: 308;"> </p> </li>
<li value="5"> <p>Voer het scenario uit. Aangezien het item <code>Emails[1]: Email</code> dat is toegewezen aan kolom "E-mail" van het eenvoudige type Tekst is, wordt het nu correct geëxporteerd:</p> <p>"Volledige naam","E-mail"</p> <p>"Shon Winer","Shon@Winer.com"</p> <p>"Lizeth Fulmore","Lizeth@Fulmore.com"</p> <p>"Hilario Gullatt","Hilario@Gullatt.com"</p> <p>"Abby Eisenbarth","Abby@Eisenbarth.com"</p> </li>
</ol>
</div>

## [!UICONTROL Parse CSV]

Met de transformator [!UICONTROL Parse CSV] kunt u CSV-tekst uit een ontvangen tekstwaarde of een bestand parseren.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of columns]</td> 
   <td>Geef het aantal kolommen op in het CSV-bestand.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV contains headers]</td> 
   <td> <p>Selecteer deze optie als de eerste rij van de CSV-tekst kopteksten bevat.</p> <p>Opmerking: de module gebruikt deze headers niet om de kolommen in de uitvoer van een label te voorzien. In plaats daarvan zorgt dit veld ervoor dat de kopteksten niet worden opgenomen in de uitvoergegevens.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>Selecteer het scheidingsteken voor het CSV-bestand. Het scheidingsteken is het tekstteken dat de grens tussen afzonderlijke waarden of velden aangeeft.</p> 
    <ul> 
     <li>[!UICONTROL Comma]</li> 
     <li>[!UICONTROL Tab]</li> 
     <li> <p>[!UICONTROL Other]</p> <p>Als u [!UICONTROL Other] selecteert, voert u het scheidingsteken in dat het CSV-bestand gebruikt om waarden van elkaar te scheiden. U moet precies één teken invoeren.<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve quotes inside unquoted field]</td> 
   <td>Schakel deze optie in om de aanhalingstekens te behouden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>Voer het CSV-bestand in of wijs het toe dat u wilt parseren.<p>Opmerking: <p>Als uw gegevens binair zijn (doorgaans uit een bestand), moet u de functie ` toString()` gebruiken om de binaire gegevens om te zetten in [!UICONTROL String] :</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png" style="width: 350;height: 123;"></p></p></td> 
  </tr> 
 </tbody> 
</table>

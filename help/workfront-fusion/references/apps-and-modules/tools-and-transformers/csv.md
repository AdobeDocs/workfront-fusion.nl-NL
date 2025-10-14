---
title: CSV
description: Met de Adobe Workfront Fusion CSV-modules kunt u CSV-bestanden maken en CSV-tekst parseren op basis van een ontvangen tekstwaarde of een bestand.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# CSV

Met de Adobe Workfront Fusion [!UICONTROL CSV] -modules kunt u CSV-bestanden maken en CSV-tekst parseren op basis van een ontvangen tekstwaarde of een bestand.

Omdat dit een transformator is, vereisen deze modules geen verbinding.

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
   <p>Geen Workfront Fusion-licentievereiste</p>
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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## [!UICONTROL Create CSV]

Met de aggregator [!UICONTROL Create CSV] kunt u een CSV-tekst maken van ontvangen tekstwaarden.

Voor meer informatie over aggregators, zie [&#x200B; de module van de Samenvoegaar &#x200B;](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Selecteer de module die de velden uitvoert die u wilt gebruiken om de CSV te maken.</td>
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

Voor meer informatie over aggregators, zie [&#x200B; de module van de Samenvoegaar &#x200B;](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
        <td>Selecteer de module die de velden uitvoert die u wilt gebruiken om de CSV te maken.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Selecteer de gegevensstructuur om de velden op de gewenste manier samen te voegen. Nadat u de gegevensstructuur hebt gedefinieerd, kunt u de items toewijzen aan de corresponderende velden.</p> <p>Voor meer informatie, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref"> structuren van Gegevens </a>.</p> </td> 
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


>[!BEGINSHADEBOX]

**Voorbeeld**:

In dit voorbeeld wordt getoond hoe u Google-contactpersonen exporteert naar een CSV-bestand met twee kolommen met de naam Volledige naam en E-mail. De uitvoerbundel van de module [!UICONTROL Google Contacts] > [!UICONTROL Get contacts from a group] heeft de volgende structuur. De e-mailadressen worden opgeslagen in de <code>[!UICONTROL Emails[]]</code> punt, dat een serie van inzamelingen is, elke inzameling die twee punten bevat: <code> Etiket</code> en <code> E-mail</code>.
![&#x200B; het Transformeren &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

De eenvoudige module [!DNL Create CSV] biedt een lijst met selectievakjes die overeenkomen met de items op hoofdniveau van een bundel. Als u <code> Volledige naam probeert te selecteren</code> en <code> E-mails</code> De module [!UICONTROL Create CSV] geeft de volgende uitvoer, die u mogelijk niet wilt gebruiken:

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

Omdat het punt <code> Volledige Naam</code> is van het eenvoudige type Tekst, wordt het uitgevoerd zoals verwacht. Het punt <code> E-mails</code>, die van een complexe typeSerie van Inzamelingen is, wordt uitgevoerd als [ objectenVoorwerp ], dat is hoe de Inzamelingen en de Arrays aan tekst door gebrek worden omgezet.

Voor meer informatie, zie {de gegevenstypes van 0} Punt [.](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)


Inhoud van <code> e-mail uitvoeren </code>punt van de eerste inzameling van <code> E-mail []</code> in plaats daarvan moet U de module [!UICONTROL Create CSV (advanced)] gebruiken. Met deze module kunt u afzonderlijke kolommen van uw CSV-bestand definiëren en items toewijzen aan deze kolommen, inclusief de geneste kolommen.

1. Voeg de module [!UICONTROL Create CSV (advanced)] in een scenario in.
1. Klik op de knop <strong>[!UICONTROL Add]</strong> naast het veld [!UICONTROL Data structure] om een nieuwe gegevensstructuur te maken.
1. Voer een naam voor de gegevensstructuur in en klik op <strong>[!UICONTROL Add item]</strong> om de afzonderlijke kolommen toe te voegen. Als u twee kolommen wilt exporteren: &quot;Volledige naam&quot; en &quot;E-mail&quot;, ziet de resulterende gegevensstructuur er als volgt uit:

   ![&#x200B; de output van Contactpersonen van Google &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. Nadat u de gegevensstructuur hebt gedefinieerd, worden de velden voor elke kolom weergegeven in de configuratie van de module [!UICONTROL Create CSV (advanced)] , zodat u de items kunt toewijzen. Het eerste item uit de <code>[!UICONTROL Emails[]] halen</code> serie en kaart zijn punt <code> E-mail </code>in het veld/de kolom E-mail:

   ![&#x200B; creeer CSV Geavanceerde module &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png)

1. Voer het scenario uit. Omdat het punt <code> E-mails [ ]: E-mail</code> toegewezen aan kolom &quot;E-mail&quot; is van het eenvoudige type Tekst, wordt het correct uitgevoerd.

```
"Full Name","Email"
"Shon Winer","Shon@Winer.com"
"Lizeth Fulmore","Lizeth@Fulmore.com"
"Hilario Gullatt","Hilario@Gullatt.com"
"Abby Eisenbarth","Abby@Eisenbarth.com"
```

>[!ENDSHADEBOX]

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
   <td>Voer het CSV-bestand in of wijs het toe dat u wilt parseren.<p>Opmerking: <p>Als uw gegevens binair zijn (doorgaans uit een bestand), moet u de functie ` toString()` gebruiken om de binaire gegevens om te zetten in [!UICONTROL String] :</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>

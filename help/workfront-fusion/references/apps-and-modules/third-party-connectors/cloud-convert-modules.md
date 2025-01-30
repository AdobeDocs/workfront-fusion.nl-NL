---
title: CloudConvert-modules
description: CloudConvert-modules
author: Becky
feature: Workfront Fusion
exl-id: 52c4d18a-8bee-44d6-9a2c-cc9e157e1dde
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '2498'
ht-degree: 0%

---

# [!DNL CloudConvert] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die gebruik maken van CloudConvert en deze koppelen aan meerdere toepassingen en services van derden. Met de [!DNL CloudConvert] -modules kunt u taken, taken en bestanden in uw [!DNL CloudConvert] -account beheren en importeren en exporteren.

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
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
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

## CloudConvert API-informatie

De CloudConvert-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.cloudconvert.com/v2/</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v2.14.22</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL CloudConvert] met [!DNL Workfront Fusion] {#connect-cloudconvert-to-workfront-fusion}

Als u uw [!DNL CloudConvert] -account wilt verbinden met [!DNL Workfront Fusion] , moet u de API-sleutel verkrijgen via uw [!DNL CloudConvert] -account.

1. Meld u aan bij uw [!DNL CloudConvert] -account en open uw [!UICONTROL Dashboard] .
1. Open de sectie **[!UICONTROL Authorization]>[!UICONTROL API Keys]** .
1. Klik op **[!UICONTROL Create New API key]**.
1. Voer de naam voor de API-sleutel in, schakel het bereik in dat u wilt gebruiken en klik op **[!UICONTROL Create]** .
1. Kopieer het meegeleverde token en sla het op een veilige plaats op.
1. Maak in [!DNL Workfront Fusion] een scenario en open het dialoogvenster [!DNL CloudConvert] module **[!UICONTROL Create a connection]** .

   Voor instructies, zie [ een scenario in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md) creëren.

1. Voer het token in dat u in stap 5 hebt opgeslagen en klik op **[!UICONTROL Continue]** om de verbinding tot stand te brengen.

## [!DNL CloudConvert] modules en hun velden {#cloudconvert-modules-and-their-fields}

Wanneer u [!DNL CloudConvert] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL CloudConvert] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [ Gemeenschappelijke taken ](#common-tasks)
* [ Banen ](#jobs)
* [ Taken ](#tasks)
* [Overige](#other)

### Algemene taken

* [ Vang een Website ](#capture-a-website)
* [[!UICONTROL Convert a file]](#convert-a-file)
* [ creeer een Archief ](#create-an-archive)
* [ de Dossiers van de Fusie ](#merge-files)
* [Een bestand optimaliseren](#optimize-a-file)

#### [!UICONTROL Capture a Website]

In deze actiemodule wordt een opgegeven website vastgelegd en opgeslagen in de indeling PDF, JPG of PNG.

U geeft de URL van de website en andere informatie op, zoals waar u de gegevens wilt opslaan.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer de URL in van de website die u wilt vastleggen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>Selecteer of u de vastgelegde website wilt opslaan in de PNG-, JPG- of PDF-indeling. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td>Voer een bestandsnaam (inclusief extensie) in voor het doeluitvoerbestand.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>(Optioneel) Geef aanvraagheaders op. </p> <p>Dit is bijvoorbeeld handig wanneer de opgegeven URL autorisatie vereist. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>Geef opties op voor conversie en de engine. Zie de <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API </a> -documentatie voor <code>input_format</code> en <code>output_format</code> voor informatie over de beschikbare opties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>Schakel deze optie in als u ook bestandsgegevens wilt opnemen in de uitvoer van de module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Convert a file]

Een bestand wordt omgezet in een geselecteerde uitvoerindeling.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input file]</td> 
   <td>Selecteer of u een bestand wilt uploaden met [!DNL Workfront Fusion] of geef de URL op waaruit het bestand wordt geüpload.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a File from URL]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Voer de URL in van het bestand dat u wilt converteren.</p> </li> 
     <li> <p><strong>[!UICONTROL Headers]</strong></p> <p>Aanvraagheaders definiëren (optioneel). Dit is bijvoorbeeld handig wanneer de opgegeven URL de autorisatie vereist.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Format]</td> 
   <td>Selecteer of u de invoerindeling wilt opgeven van het bestand dat u wilt converteren. Indien niet opgegeven, wordt de extensie van het invoerbestand gebruikt als de invoerindeling.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Input Format]</td> 
   <td>Selecteer de huidige indeling van het bestand.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td>Selecteer de doelbestandsindeling waarnaar u het bestand wilt converteren.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL File Name]</td> 
   <td>Kies een bestandsnaam (inclusief extensie) voor het doeluitvoerbestand.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>Geef opties op voor conversie en de engine. Zie de <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API </a> -documentatie voor <code>input_format</code> en <code>output_format</code> voor informatie over de beschikbare opties.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>Schakel deze optie in als u ook bestandsgegevens wilt opnemen in de uitvoer van de module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an Archive]

Hiermee kunt u een of meer bestanden toevoegen aan het archief ZIP, RAR, 7Z, TAR, TAR.GZ of TAR.BZ2.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>Geef de bestanden op die u aan het archief wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Voer de URL in van het bestand dat u wilt archiveren.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>Aanvraagheaders definiëren (optioneel). Dit is bijvoorbeeld handig wanneer de opgegeven URL de autorisatie vereist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> Selecteer de doelindeling van het gearchiveerde bestand.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> Voer de bestandsnaam (inclusief extensie) voor het doeluitvoerbestand in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>Geef opties op voor conversie en de engine. Zie de <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API </a> -documentatie voor <code>input_format</code> en <code>output_format</code> voor informatie over de beschikbare opties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>Schakel deze optie in als u ook bestandsgegevens wilt opnemen in de uitvoer van de module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Merge Files]

Voegt minstens twee bestanden samen tot één PDF. Als invoerbestanden geen PDF zijn, worden ze automatisch omgezet in PDF.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>Geef de bestanden op die u wilt samenvoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Voer de URL in van het bestand dat u wilt archiveren.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>Aanvraagheaders definiëren (optioneel). Dit is bijvoorbeeld handig wanneer de opgegeven URL de autorisatie vereist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> Selecteer de doelindeling van het samengevoegde bestand.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> Voer de bestandsnaam (inclusief extensie) voor het doeluitvoerbestand in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>Geef opties op voor conversie en de engine. Zie de <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API </a> -documentatie voor <code>input_format</code> en <code>output_format</code> voor informatie over de beschikbare opties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>Schakel deze optie in als u ook bestandsgegevens wilt opnemen in de uitvoer van de module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Optimize a File]

Deze actiemodule optimaliseert en comprimeert een bestand in de indeling PDF, PNG of JPG.

U geeft het bestand en de parameters op voor het optimaliseren en opslaan ervan.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input File]</td> 
   <td>Selecteer of u een bestand wilt uploaden met Workfront Fusion of de URL wilt opgeven van waaruit het bestand wordt geüpload.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Upload a File]</p> </td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a file from URL] </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: Voer de URL in van het bestand dat u wilt converteren.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (Optioneel) Geef aanvraagheaders op. Dit is bijvoorbeeld handig wanneer de opgegeven URL autorisatie vereist.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optimization for] </td> 
   <td> <p>Selecteer het optimalisatieprofiel voor specifieke doelbehoeften.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Web]</strong>: Optimalisatie voor het web (standaard)</p> 
      <ul> 
       <li>Verwijder overtollige en onnodige gegevens voor het Web</li> 
       <li>Afbeeldingen downsamplen, knippen en intelligent comprimeren</li> 
       <li>Lettertypen samenvoegen en subset maken</li> 
       <li>Kleuren converteren naar RGB</li> 
      </ul> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Print]</strong>: Optimalisatie voor afdrukken</p> 
      <ul> 
       <li> <p>Overbodige en overbodige gegevens verwijderen voor afdrukken</p> </li> 
       <li> <p>Afbeeldingen downsamplen, knippen en intelligent comprimeren</p> </li> 
       <li> <p>Lettertypen samenvoegen en subset maken</p> </li> 
       <li> <p>Kleuren converteren naar CMYK</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Archive]</strong>: Optimalisatie voor archiveringsdoeleinden</p> 
      <ul> 
       <li> <p>Verwijder overtollige en onnodige gegevens voor archivering</p> </li> 
       <li> <p>Afbeeldingen intelligent comprimeren</p> </li> 
       <li> <p>Lettertypen samenvoegen en subset maken</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Scanned images]</strong>: Optimalisatie voor gescande afbeeldingen</p> 
      <ul> 
       <li> <p>Profiel geoptimaliseerd voor PDF die voornamelijk bestaan uit rasterafbeeldingen</p> </li> 
       <li> <p>De afbeeldingen comprimeren zonder de visuele kwaliteit aanzienlijk te verlagen</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL maximal size reduction]</strong>: Optimalisatie voor maximale reductie van grootte</p> 
      <ul> 
       <li> <p>Maximale compressie gebruiken</p> </li> 
       <li> <p>De visuele kwaliteit kan verminderen</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input format] </td> 
   <td>Selecteer de indeling van het invoerbestand dat u wilt optimaliseren. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p>Voer een bestandsnaam (inclusief extensie) in voor het doeluitvoerbestand.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options]</td> 
   <td> <p>Geef opties op voor conversie en de engine. Zie de <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API </a> -documentatie voor <code>input_format</code> en <code>output_format</code> voor informatie over de beschikbare opties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file]</td> 
   <td> <p>Schakel deze optie in als u ook bestandsgegevens wilt opnemen in de uitvoer van de module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Taken

* [[!UICONTROL Create a Job (advanced)]](#create-a-job-advanced)
* [[!UICONTROL New Job Event]](#new-job-event)
* [[!UICONTROL List Jobs]](#list-jobs)
* [[!UICONTROL Get a Job]](#get-a-job)
* [[!UICONTROL Delete a Job]](#delete-a-job)

#### [!UICONTROL Create a Job (advanced)]

Deze module maakt een taak. Een taak kan een of meer taken zijn die in het veld [!UICONTROL Name] worden geïdentificeerd en die via het veld [!UICONTROL Input] met elkaar zijn verbonden.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input Files]</td> 
   <td> <p>Selecteer of u een bestand wilt uploaden met [!DNL Workfront Fusion] of geef de URL op vanwaar het bestand wordt geüpload.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a File from URL]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: Voer de URL in van het bestand dat u wilt verwerken.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (Optioneel) Geef aanvraagheaders op. Dit is bijvoorbeeld handig wanneer de opgegeven URL autorisatie vereist.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tasks]</p> </td> 
   <td> <p>Voeg taken toe die binnen de taak worden uitgevoerd.</p> <p>Zie de beschrijvingen van de velden van de bewerkingen in de bijbehorende sectie.</p> 
    <ul> 
     <li><a href="#convert-a-file" class="MCXref xref">[!UICONTROL Convert a file]</a> </li> 
     <li><a href="#capture-a-website" class="MCXref xref">[!UICONTROL Capture a Websit] e </a> </li> 
     <li><a href="#optimize-a-file" class="MCXref xref">[!UICONTROL Optimize a File]</a> </li> 
     <li><a href="#create-an-archive" class="MCXref xref">[!UICONTROL Create an Archive]</a> </li> 
     <li><a href="#merge-files" class="MCXref xref">[!UICONTROL Merge Files]</a> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Execute a Command]</strong> </p> <p>Zie de <a href="https://cloudconvert.com/api/v2/command#command-tasks">[!DNL CloudConvert] API-documentatie </a> voor meer informatie over het uitvoeren van een opdracht.</p> </li> 
     <li> <p><strong>[!UICONTROL Export a File to Temporary URL]</strong> </p> <p> Geef de naam van de taak en de naam van de invoertaak op (bijvoorbeeld Conversie).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag] </td> 
   <td> <p>Voer een tag in. Tags zijn willekeurige tekenreeksen om de taak te identificeren. Ze hebben geen effect en kunnen worden gebruikt om de taak aan een id te koppelen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Job]

Deze module verwijdert een taak, inclusief alle taken en gegevens.

>[!NOTE]
>
>Banen worden 24 uur na afloop automatisch verwijderd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>Voer de id in van de taak die u wilt verwijderen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Job]

Deze module haalt taakdetails op.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>Voer de id in van de taak waarover u details wilt ophalen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Jobs]

Deze module haalt alle taken op die in uw account zijn uitgevoerd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Selecteer de taakstatus om geretourneerde taken te filteren op.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Stel het aantal taken in dat Workfront Fusion 2.0 tijdens één uitvoeringscyclus retourneert.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL New Job Event]

Triggers worden geactiveerd wanneer een taak in uw account of taak wordt gemaakt, voltooid of mislukt.

>[!NOTE]
>
>* De baan die door de [!UICONTROL Create a Job (advanced)] module wordt gecreeerd bestaat uit *verscheidene* taken.
>* De [!UICONTROL New Job Event] trekker wordt ook teweeggebracht wanneer een *individuele* taak wordt gecreeerd, gebeëindigd is, of ontbroken.
>

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhhook name]</td> 
   <td>Voer de naam van de webhaak in. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>Selecteer of u de vastgelegde website wilt opslaan in de PNG-, JPG- of PDF-indeling. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event]</td> 
   <td>Selecteer of de module wordt geactiveerd wanneer de taak of taak wordt gemaakt, voltooid of mislukt.</td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Als u met de Arrayaggregator werkt (u hebt bijvoorbeeld veel bestanden in verschillende indelingen die moeten worden omgezet), gebruikt u de optie **[!UICONTROL I don't know the input format]** in het dialoogvenster [!UICONTROL Add a task] . Anders wordt de fout geretourneerd.
>* Taken in de taak koppelen (naam > invoer, naam > invoer,...):
>
>  ![ het Verbinden naam over banen ](/help/workfront-fusion/references/apps-and-modules/assets/linking-name-across-jobs-350x808.png)>

### Taken

* [[!UICONTROL Get a Task]](#get-a-task)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL List Tasks]](#list-tasks)
* [[!UICONTROL Retry a Task]](#retry-a-task)
* [[!UICONTROL Cancel a Task]](#cancel-a-task)
* [[!UICONTROL Delete a Task]](#delete-a-task)

#### [!UICONTROL Cancel a Task]

Deze module annuleert een taak die een status van wachten of verwerking heeft.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Voer de id in van de taak die u wilt annuleren of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Task]

Een taak verwijderen, inclusief alle gegevens.

>[!NOTE]
>
>Taken worden 24 uur na afloop automatisch verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Voer de id in van de taak die u wilt verwijderen (kaart).</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Deze module wint dossier - naam en dossiergegevens van de gespecificeerde taak terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Voer de id in van de taak waarvan u het bestand wilt downloaden of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Task]

Deze module wint taakdetails terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p>Voer de id in van de taak waarover u details wilt ophalen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Tasks]

Deze module haalt alle taken in uw account op basis van filterinstellingen op.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Selecteer de taakstatus om geretourneerde taken te filteren op.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID] </td> 
   <td> <p>Voer de taak-id in of wijs deze toe om alleen taken binnen de opgegeven taak te retourneren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>Voer het type bewerking in om alleen taken met de opgegeven bewerking te retourneren. </p> <p>Opmerking: gebruik de module [!UICONTROL List Possible Operations] om bewerkingen op te halen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Retry a Task]

Deze module leidt tot een nieuwe taak, die op de montages (lading) van een andere taak wordt gebaseerd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Voer de id in van de taak waarvan u een nieuwe taak wilt maken of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Overige

* [[!UICONTROL Get My Info]](#get-my-info)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Get My Info]

Hiermee worden geverifieerde accountgegevens over de huidige gebruiker opgehaald.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL CloudConvert] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL CloudConvert] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Hiermee kunt u een aangepaste API-aanroep uitvoeren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [Fusion App] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van <code>https://api.cloudconvert.com/</code> . Bijvoorbeeld: <code>/v2/tasks</code></p> <p>Zie de <a href="https://cloudconvert.com/api/v2">[!DNL CloudConvert] API v2-documentatie </a> voor een lijst met beschikbare eindpunten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion 2.0 voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst van de API-aanroep toe in de vorm van een standaard JSON-object. Plaats de aanhalingstekens buiten de voorwaardelijke instructie wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld:** de Taken van de Lijst

De volgende API-aanroep retourneert alle taken van uw CloudFront-account:

URL: `/v2/tasks`

Methode: `GET`

![ API voorbeeldinput ](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-input.png)

Overeenkomsten met de zoekopdracht vindt u in de sectie Uitvoer van de module onder [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL data] .

In ons voorbeeld werden 6 taken geretourneerd:

![ API voorbeeldoutput ](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-output.png)

## Problemen oplossen {#troubleshooting}

Zie de volgende tabel voor mogelijke fouten en de bijbehorende oplossingen:

<table style="table-layout:auto">
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> <p>Fout</p> </th> 
   <th>Volgende stappen</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL The output file size exceeds the limit allowed for your scenario.]</span> </p> </td> 
   <td> <p>Raadpleeg de maximale bestandsgrootte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL You have exceeded the maximum conversion time.]</span> </p> </td> 
   <td> <p>Het gratis abonnement van [!DNL CloudConvert] biedt dagelijks 25 conversiminuten. Als uw gebruik de limiet van het gratis abonnement overschrijdt, kunt u overschakelen op een (prepaid) pakket of abonnement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Failed to read frame size: Could not seek to 1508. �/output/JLIADSA00137P0.mp3: Invalid argument.]</span> </p> </td> 
   <td> <p>Deze fout treedt op bij bijvoorbeeld het omzetten van bestanden van MP3 in WAV. Zorg ervoor dat u het juiste gebied hebt geselecteerd omdat er verwijzingen naar bestanden worden gevonden, maar niet alleen het juiste bestand.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL RuntimeError:] </p> <p><span style="font-weight: normal;">[!UICONTROL Maximum number of repeats exceeded.]</span> </p> </td> 
   <td> <p>Zoek de bijbehorende [!DNL CloudConvert] -taak in de lijst met taken van het [!DNL CloudConvert] -dashboard en controleer de duur van de taak:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-duration-350x177.png" style="width: 350;height: 177;"> </p> <p>De time-out van de module [!DNL CloudConvert] &gt; [!UICONTROL Convert a File] is ingesteld op 3 minuten. Als de duur van de taak langer is dan 3 minuten (mogelijk als gevolg van een tijdelijke overbelasting van de service [!DNL CloudConvert] ), genereert de module de hierboven vermelde fout.</p> <p>Overweeg in dit geval een van de volgende opties:</p> 
    <ul> 
     <li>Schakel de optie <strong>[!UICONTROL Allow storing of Incomplete Executions]</strong> in de scenario-instellingen in om de onvolledige uitvoeringen op te slaan voor latere handmatige resolutie. U kunt desgewenst een foutafhandelingsroute aan de module [!DNL CloudConvert] koppelen met de aanwijzing [!UICONTROL Break] om de onvolledige uitvoeringen automatisch op te lossen.</li> 
     <li>Schakel de optie <strong>[!UICONTROL Download a file] </strong> uit in de module [!DNL CloudConvert] &gt; [!UICONTROL Convert a file] . In dit geval wacht de module niet op het omzettingsresultaat. Maak een nieuw scenario en gebruik de trigger [!DNL CloudConvert] &gt; [!UICONTROL New Job Event] om het omzettingsresultaat te verkrijgen.</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld van een workflow voor [!DNL CloudConvert] -connector

>[!INFO]
>
>**Voorbeeld:** Converterend een video van MOV in formaat MP4
>
>1. Bezoek [ https://cloudconvert.com/video-converter](https://>cloudconvert.com/video-converter)
>1. Klik op **[!UICONTROL Select File]** en kies het MOV-voorbeeldbestand.
>1. Klik op de vervolgkeuzelijst naast **[!UICONTROL Convert to]** en kies **[!UICONTROL MP4]** .
>
>1. Klik op het pictogram **[!UICONTROL wrench]** .
>1. Configureer de compressie-instellingen voor MP4 naar wens.
>1. Klik op **[!UICONTROL Convert]**.
>1. Klik op **[!UICONTROL Download]** als de conversie is voltooid.
>1. Controleer de omgezette video.
>1. Herhaal stap 1 tot en met 8 totdat u de optimale conversie-instellingen voor stap 5 hebt gevonden.
>1. Bezoek [ https://cloudconvert.com/api/v2/convert#convert-tasks](https://cloudconvert.com/api/v2/convert#convert-tasks)
>1. Kies **[!UICONTROL mov]** voor het veld **[!UICONTROL input_format]** .
>
>1. Kies **[!UICONTROL mp4]** voor het veld **[!UICONTROL output_format]** .
>
>1. Een lijst met alle mogelijke parameters, zoals video_codec, crf, enz. wordt weergegeven.
>1. Voeg in Workfront Fusion 2.0 de module **[!UICONTROL CloudConvert]** > **[!UICONTROL Convert a File]** in uw scenario in.
>
>1. Open de instellingen van de module.
>1. Configureer de module zoals hieronder wordt weergegeven:
>
>   ![ CloudConvert voorbeeld ](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-mp4-example.png)
>
>1. Zorg ervoor dat u alle instellingen opneemt in het veld Conversie en motorspecifieke opties: zoek voor elke instelling in stap 5 de corresponderende parameter uit stap 13 en de bijbehorende waarde.

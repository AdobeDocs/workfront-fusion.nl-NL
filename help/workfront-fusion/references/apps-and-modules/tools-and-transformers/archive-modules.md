---
title: Modules archiveren
description: In een Adobe Workfront Fusion-scenario kunt u een archief, zoals een gecomprimeerd bestand, verbinden met meerdere toepassingen en services van derden. U kunt bijvoorbeeld een scenario configureren dat
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# [!UICONTROL Archive] modules

In een Adobe Workfront Fusion-scenario kunt u een archief, zoals een gecomprimeerd bestand, in uw scenario gebruiken, zodat u het in uw automatisering of integratie kunt gebruiken.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## [!UICONTROL Archive] modules en hun velden

Wanneer u [!UICONTROL Archive] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!UICONTROL Archive] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Handelingen](#actions)
* [Samenvoegapparatuur](#aggregators)
* [Transformatoren](#transformers)

## Handelingen

### [!UICONTROL Extract an archive]

Deze actiemodule extraheert een bestand dat u uit een archief identificeert.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>  <p>Selecteer een bronbestand uit een vorige module of wijs de brongegevens toe.</p></p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Voorbeeld:** krijg het dossier van het PIT van de bepaalde [!DNL Dropbox] omslag (bijvoorbeeld, Archives), haalt het uit gebruikend de [!UICONTROL Archive] module en verzendt geciteerde dossiers naar het gewenste e-mailadres als gehechtheid met [!UICONTROL Email] of [!DNL Gmail] module.

![&#x200B; Voorbeeld Dropbox &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

>[!ENDSHADEBOX]

## Samenvoegapparatuur

### [!UICONTROL Create an archive]

Deze aggregatormodule voegt de gewenste bestanden toe aan een [!UICONTROL ZIP] -, GZIP- of [!UICONTROL TAR] -archief.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module]</td> 
   <td> <p> Selecteer de module waarvan u de bestanden wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Selecteer of u bestanden wilt toevoegen aan een [!UICONTROL ZIP] -, GZIP- of [!UICONTROL TAR] -archief.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Voer een opmerking in die u aan het archief wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Group by]</td> 
   <td> <p>Definieer een expressie waarop u de geaggregeerde uitvoer wilt groeperen. Deze expressie kan een of meer toegewezen items bevatten. De geaggregeerde gegevens worden vervolgens in groepen verdeeld op basis van de waarde van deze expressie. Elke groep voert als een afzonderlijke bundel met een sleutel (de geëvalueerde uitdrukking) en een waarde (de samengevoegde tekst) uit. U kunt de sleutel als filter in verdere modules gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Selecteer deze optie om het scenario te stoppen als er geen resultaten zijn.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Archive name]</td> 
   <td> <p> Voer een naam in voor het gemaakte archief. Voeg geen extensie toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Voorbeeld:** bekijk inkomende e-mails gebruikend [!DNL Gmail] > [!UICONTROL Watch emails] module. Als een e-mail wordt ontvangen, worden de bijlagen herhaald in afzonderlijke bundels, vervolgens naar het [!DNL ZIP] -bestand gearchiveerd en in de gedefinieerde Dropbox-map opgeslagen.

![&#x200B; Gmail van het Voorbeeld &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

>[!ENDSHADEBOX]

## Transformatoren

* [[!UICONTROL Deflate]](#deflate)
* [[!UICONTROL Inflate]](#inflate)

### [!UICONTROL Deflate]

Deze transformatormodule comprimeert binaire gegevens met behulp van een deflatiealgoritme.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Voer de gegevens in die u wilt comprimeren of wijs deze toe met de functie deflate.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Inflate]

Deze transformatormodule decomprimeert binaire gegevens met behulp van een inflatiealgoritme.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Voer de gegevens in die u wilt decomprimeren of wijs deze toe met behulp van de inflate-functie.</p> </td> 
  </tr> 
 </tbody> 
</table>

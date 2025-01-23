---
title: Microsoft OneDrive-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die OneDrive gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: d21eafad-9c67-4f42-b718-0aa4223846e6
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL OneDrive] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

Als u [!DNL OneDrive] -modules wilt gebruiken, moet u een [!DNL Microsoft OneDrive] -account hebben.



## OneDrive API-informatie

De OneDrive-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://graph.microsoft.com/v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>


## De service [!DNL OneDrive] verbinden met [!DNL Workfront Fusion]

Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!UICONTROL Workfront Fusion], zie [ een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Sommige Microsoft-toepassingen gebruiken dezelfde verbinding, die is gekoppeld aan individuele gebruikersmachtigingen. Daarom bij het creëren van een verbinding, toont het scherm van de toestemmingstoestemming om het even welke toestemmingen die eerder aan de verbinding van deze gebruiker werden verleend, naast om het even welke nieuwe toestemmingen nodig voor de huidige toepassing.
>
>Bijvoorbeeld, als een gebruiker &quot;Gelezen lijst&quot;toestemmingen heeft die via de schakelaar van Excel worden verleend en dan een verbinding in de schakelaar van Vooruitzichten creeert om e-mails te lezen, zal het scherm van de toestemmingstoestemming zowel de reeds verleende &quot;Gelezen lijst&quot;toestemming en de onlangs vereiste &quot;Schrijf e-mail&quot;toestemming tonen.

## [!DNL Microsoft OneDrive] modules en hun velden

Wanneer u [!DNL OneDrive] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL OneDrive] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Bestand/map](#filefolder)
* [Overige](#other)

### Bestand/map

* [[!UICONTROL Watch Files/Folders]](#watch-filesfolders)
* [[!UICONTROL Search Files/Folders]](#search-filesfolders)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Download a file]](#download-a-file)
* [[!UICONTROL Upload a file]](#upload-a-file)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Get a Share Link]](#get-a-share-link)
* [[!UICONTROL Move a File/Folder]](#move-a-filefolder)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File/Folder]](#delete-a-filefolder)

#### [!UICONTROL Watch Files/Folders]

Deze triggermodule start een scenario wanneer een bestand of map wordt gemaakt of bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Files/Folders]</td> 
   <td> <p>Selecteer hoe u bestanden of mappen wilt bekijken:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL By Created Time]</b> </p> <p>Controleren op nieuwe bestanden of mappen.</p> </li> 
     <li> <p><b>[!UICONTROL By Updated Time]</b> </p> <p>Controleren op bijgewerkte bestaande bestanden of mappen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie die u wilt controleren:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station waarop u de module wilt letten.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> <p>Navigeer naar de map die u in de module wilt bekijken. U kunt ook een query invoeren om de geretourneerde resultaten te filteren.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Shared With Me]</b> </p> <p>De module controleert bestanden die met de eigenaar van het station zijn gedeeld.</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de SharePoint-site waarop u de module wilt controleren. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan de aandrijving u de module wilt letten op.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose an Item Type]</td> 
   <td> <p>Selecteer of u bestanden, mappen of beide wilt bekijken.</p> <p>Opmerking: u kunt niet controleren op mappen in een [!UICONTROL Shared With Me] -station.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Search Files/Folders]

Deze zoekmodule retourneert bestanden en mappen op basis van criteria die u instelt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie die u wilt zoeken:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station waarnaar u de module wilt zoeken.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> <p>Navigeer naar de map waarnaar u in de module wilt zoeken. U kunt ook een query invoeren om de geretourneerde resultaten te filteren.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Shared With Me]</b> </p> <p>De module zoekt bestanden die met de eigenaar van het station zijn gedeeld.</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de [!DNL SharePoint] -site waarnaar u in de module wilt zoeken. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan de aandrijving u de module wilt zoeken.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose an Item Type]</td> 
   <td> <p>Selecteer of u naar bestanden, mappen of beide wilt zoeken.</p> <p>Opmerking: u kunt niet zoeken naar mappen in een [!UICONTROL Shared With Me] -station.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Deze actiemodule krijgt de meta-gegevens van een gespecificeerd dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>Selecteer of u het bestand wilt identificeren aan de hand van de bestands-id of het bestandspad.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Selecteer hoe u de bestands-id of het bestandspad wilt invoeren:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Selecteer deze optie als u de id of het pad rechtstreeks wilt invoeren of u het pad vanuit een vorige module wilt toewijzen.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Selecteer deze optie als u bestanden of paden in een lijst wilt selecteren. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie die u wilt zoeken:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station dat het bestand bevat dat u wilt ophalen.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de SharePoint-site met het bestand dat u wilt ophalen. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan het station het bestand bevat dat u wilt ophalen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer of wijs de aandrijving toe die het dossier bevat u wilt krijgen. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Als u [!UICONTROL Enter Manually] hebt geselecteerd, voert u de bestands-id of het pad in van het bestand dat u wilt ophalen.</p> <p>Als u [!UICONTROL Select from the list] hebt geselecteerd, selecteert u het bestand dat u wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a file]

Deze actiemodule downloadt het opgegeven bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>Selecteer of u het bestand wilt identificeren aan de hand van de bestands-id of het bestandspad.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bestands-id/bestandspad opgeven</td> 
   <td> <p>Selecteer hoe u de bestands-id of het bestandspad wilt invoeren:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Selecteer deze optie als u de id of het pad rechtstreeks wilt invoeren of u het pad vanuit een vorige module wilt toewijzen.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Selecteer deze optie als u bestanden of paden in een lijst wilt selecteren. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie die het bestand bevat dat u wilt downloaden:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station dat het bestand bevat dat u wilt downloaden.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de SharePoint-site met het bestand dat u wilt downloaden. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan het station het bestand bevat dat u wilt downloaden.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer of wijs de aandrijving toe die het dossier bevat u wilt downloaden. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td>
   <td> <p>Als u [!UICONTROL Enter Manually] hebt geselecteerd, voert u de bestands-id of het pad in van het bestand dat u wilt downloaden.</p> <p>Als u [!UICONTROL Select from the list] hebt geselecteerd, selecteert u het bestand dat u wilt downloaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Convert to PDF]</td> 
   <td> <p>Schakel deze optie in om het bestand om te zetten in een PDF-bestand. U kunt de volgende bestandstypen converteren:</p> 
    <table style="table-layout:auto"> 
     <col> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td> 
        <ul> 
         <li> <p> <p>CSV</p> </p> </li> 
         <li> <p> <p>DOC</p> </p> </li> 
         <li> <p> <p>DOCX</p> </p> </li> 
         <li> <p> <p>ODP</p> </p> </li> 
         <li> <p> <p>ODS</p> </p> </li> 
         <li> <p> <p>ODT</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p> <p>POT</p> </p> </li> 
         <li> <p> <p>POTM</p> </p> </li> 
         <li> <p> <p>POTX</p> </p> </li> 
         <li> <p> <p>PPS</p> </p> </li> 
         <li> <p> <p>PPSX</p> </p> </li> 
         <li> <p> <p>PPSXM</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p>PPT</p> </li> 
         <li> <p>PPTM</p> </li> 
         <li> <p>PPTX</p> </li> 
         <li> <p>RTF</p> </li> 
         <li> <p>XLS</p> </li> 
         <li> <p>XLSX</p> </li> 
        </ul> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

Deze actiemodule uploadt een bestand naar de opgegeven map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enter (locatie-id en pad van map)</td> 
   <td>Selecteer of u de doelmap wilt identificeren aan de hand van een id of een pad.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie waar u een bestand wilt uploaden:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Selecteer het station dat het bestand bevat dat u wilt ophalen.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de [!DNL SharePoint] -site die de map bevat waarin u een bestand wilt uploaden. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan het station de map bevat waarin u een bestand wilt uploaden.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer het station dat de map bevat waarnaar u een bestand wilt uploaden. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL If the File with the Same Name Exists]</td> 
   <td>Selecteer hoe u wilt doorgaan als er al een bestand met dezelfde naam bestaat.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Voeg een beschrijving toe aan het geüploade bestand.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

Deze actiemodule maakt een nieuwe map in het opgegeven station.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie waar u een map wilt maken:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Selecteer het station waarop u een map wilt maken.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de [!DNL SharePoint] -site waarop u een map wilt maken. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep die eigenaar is van het stuurprogramma waarop u een map wilt maken.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer het station waarop u een map wilt maken. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Als u wilt dat de nieuwe map een submap is, navigeert u naar de map waarin u een submap wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Folder Name]</td> 
   <td> <p>Voer een naam voor de nieuwe map in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL If the Folder with the Same Name Exists]</td> 
   <td>Selecteer hoe u wilt doorgaan als er al een bestand met dezelfde naam bestaat.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Share Link]

Deze actiemodule retourneert een gedeelde koppeling voor het opgegeven bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>Selecteer of u het bestand wilt identificeren aan de hand van de bestands-id of het bestandspad.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Selecteer hoe u de bestands-id of het bestandspad wilt invoeren:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Selecteer deze optie als u de id of het pad rechtstreeks wilt invoeren of u het pad vanuit een vorige module wilt toewijzen.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Selecteer deze optie als u bestanden of paden in een lijst wilt selecteren. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie waarvoor u een koppeling voor delen wilt ophalen:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station met het bestand waarvoor u een gedeelde koppeling wilt ophalen.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de SharePoint-site met het bestand waarvoor u een gedeelde koppeling wilt ophalen. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan het station het bestand bevat waarvoor u een gedeelde koppeling wilt ophalen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer of wijs de aandrijving toe die het dossier bevat u een aandeelverbinding voor wilt terugwinnen. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Als u [!UICONTROL Enter Manually] hebt geselecteerd, voert u de bestands-id of het pad in van het bestand waarvoor u een gedeelde koppeling wilt ophalen.</p> <p>Als u [!UICONTROL Select] hebt geselecteerd in de lijst, selecteert u het bestand waarvoor u een gedeelde koppeling wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permission Type]</td> 
   <td> <p>Selecteer of u wilt dat personen met de koppeling het bestand kunnen lezen en schrijven of alleen kunnen lezen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td>Selecteer of u het bestand beschikbaar wilt maken voor iedereen met de koppeling, of alleen voor leden van uw organisatie die over de koppeling beschikken.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder]

Met deze handelingsmodule wordt een bestand of map naar een nieuwe maplocatie verplaatst

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>Selecteer of u het bestand wilt identificeren aan de hand van de bestands-id of het bestandspad.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID / File Path]</td> 
   <td> <p>Selecteer hoe u de bestands-id of het bestandspad wilt invoeren:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Selecteer deze optie als u de id of het pad rechtstreeks wilt invoeren of u het pad vanuit een vorige module wilt toewijzen.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Selecteer deze optie als u bestanden of paden in een lijst wilt selecteren. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie die het bestand of de map bevat die u wilt verplaatsen:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station dat het bestand of de map bevat dat u wilt verplaatsen.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de [!DNL SharePoint] -site die het bestand of de map bevat die u wilt verplaatsen. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan het station het bestand of de map bevat die u wilt verplaatsen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer of wijs de aandrijving toe die het dossier of de omslag bevat die u wilt bewegen. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Selecteren [!UICONTROL File/Folder]</td> 
   <td>Selecteer of u een bestand of een map wilt verplaatsen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</p> <p role="rowheader">[!UICONTROL Folder] / [!UICONTROL Folder ID] / [!UICONTROL Folder Path]</p> </td> 
   <td> <p>Als u [!UICONTROL Enter Manually] hebt geselecteerd, voert u de id of het pad in van het bestand of de map die u wilt verplaatsen.</p> <p>Als u [!UICONTROL Select] in de lijst hebt geselecteerd, selecteert u het bestand of de map die u wilt verplaatsen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a New Folder Location]</td> 
   <td> <p>Selecteer hoe u de locatie wilt opgeven waarnaar u het bestand of de map wilt verplaatsen:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Selecteer deze optie als u de id of het pad rechtstreeks wilt invoeren of u het pad vanuit een vorige module wilt toewijzen.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Selecteer deze optie als u bestanden of paden in een lijst wilt selecteren. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie waar u het bestand of de map wilt verplaatsen:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station waarnaar u het bestand of de map wilt verplaatsen.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de [!DNL SharePoint] -site waarnaar u het bestand of de map wilt verplaatsen. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarnaar u het bestand of de map wilt verplaatsen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer of wijs het station toe dat de map bevat waarnaar u het bestand of de map wilt verplaatsen. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> <p>Als u dit leeg laat, kan het bestand of de map alleen binnen dezelfde [!DNL OneDrive] worden verplaatst.</p> <p>U kunt bestanden en mappen verplaatsen van [!UICONTROL My Drive] naar een [!UICONTROL Site's Drive] of een [!UICONTROL Group's Drive] . </p> <p>U kunt bestanden van een [!UICONTROL Site's Drive] alleen naar hetzelfde station op dezelfde site verplaatsen.</p> <p>U kunt bestanden van een [!UICONTROL Group's Drive] alleen naar hetzelfde station in dezelfde groep verplaatsen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Voer de map in of wijs de map toe waarnaar u het bestand of de map wilt verplaatsen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

Deze actiemodule kopieert een bestand naar een nieuwe maplocatie

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>Selecteer of u het bestand wilt identificeren aan de hand van de bestands-id of het bestandspad.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Selecteer hoe u de bestands-id of het bestandspad wilt invoeren:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Selecteer deze optie als u de id of het pad rechtstreeks wilt invoeren of u het pad vanuit een vorige module wilt toewijzen.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Selecteer deze optie als u bestanden of paden in een lijst wilt selecteren. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie die het bestand bevat dat u wilt kopiëren:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station dat het bestand of de map bevat dat u wilt kopiëren.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de SharePoint-site die het bestand bevat dat u wilt verplaatsen. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan het station het bestand bevat dat u wilt kopiëren.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer of wijs de aandrijving toe die het dossier bevat dat u wilt kopiëren. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</p> </td> 
   <td> <p>Als u [!UICONTROL Enter Manually] hebt geselecteerd, voert u de id of het pad in van het bestand dat u wilt kopiëren.</p> <p>Als u [!UICONTROL Select] in de lijst hebt geselecteerd, selecteert u het bestand dat u wilt kopiëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a New Folder Location]</td> 
   <td> <p>Selecteer hoe u de locatie wilt invoeren waarnaar u het bestand wilt kopiëren of waarnaar:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Selecteer deze optie als u de id of het pad rechtstreeks wilt invoeren of u het pad vanuit een vorige module wilt toewijzen.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Selecteer deze optie als u een keuze wilt maken in een lijst met beschikbare mappen. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New OneDrive location]</td> 
   <td> <p>Selecteer de locatie waar u het filter wilt kopiëren. Deze optie is beschikbaar als u de nieuwe maplocatie in een lijst wilt selecteren.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station waarnaar u het bestand wilt kopiëren.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de [!DNL SharePoint] -site waarop u het bestand wilt kopiëren. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarnaar u het bestand wilt kopiëren.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer of wijs het station toe dat de map bevat waarnaar u het bestand wilt kopiëren. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> <p>Als u dit leeg laat, kan het bestand of de map alleen worden gekopieerd binnen dezelfde [!UICONTROL OneDrive] .</p> <p>U kunt bestanden en mappen kopiëren van [!UICONTROL My Drive] naar een [!UICONTROL Site's Drive] of een [!UICONTROL Group's Drive] . </p> <p>U kunt bestanden van een [!UICONTROL Site's Drive] alleen naar hetzelfde station op dezelfde site kopiëren.</p> <p>U kunt bestanden van een [!UICONTROL Group's Drive] alleen naar hetzelfde station in dezelfde groep kopiëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Voer de map in waarin u de kopie of map wilt verplaatsen of wijs de map toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Copied File Name]</td> 
   <td> <p>Voer een naam in of wijs een naam toe aan de nieuwe kopie van het bestand. U kunt dit leeg laten als u de oorspronkelijke bestandsnaam niet wilt wijzigen.</p> <p>De naam moet de bestandsextensie bevatten. Voorbeeld:<code> file.txt</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File/Folder]

In deze actiemodule wordt het geselecteerde bestand verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File/Folder ID & Path)]</td> 
   <td>Selecteer of u het bestand wilt identificeren aan de hand van de bestands-id of het bestandspad.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File/Folder ID /Enter a File/Folder Path]</td> 
   <td> <p>Selecteer hoe u de bestands-id of het bestandspad wilt invoeren:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Selecteer deze optie als u de id of het pad rechtstreeks wilt invoeren of u het pad vanuit een vorige module wilt toewijzen.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Selecteer deze optie als u bestanden of paden in een lijst wilt selecteren. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] locatie]</td> 
   <td> <p>Selecteer de locatie die u wilt zoeken:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Selecteer of de module een station-id moet invoeren.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Voer de id in van het station dat het bestand of de map bevat die u wilt verwijderen.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Selecteer de [!DNL SharePoint] -site die het bestand of de map bevat die u wilt verwijderen. Beschikbare sites zijn sites die worden gevolgd door de aangemelde gebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Selecteer de groep waarvan het station het bestand of de map bevat die u wilt verwijderen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer of wijs het station toe dat het bestand of de map bevat die u wilt verwijderen. Dit veld is niet beschikbaar als u [!UICONTROL No] in het veld [!UICONTROL Enable to Enter a Drive ID] hebt geselecteerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Selecteren [!UICONTROL File/Folder]</td> 
   <td>Selecteer of u een bestand of map wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td>
   <td> <p>Als u [!UICONTROL Enter Manually] hebt geselecteerd, voert u de bestands-id of het pad in van het bestand dat u wilt verwijderen.</p> <p>Als u [!UICONTROL Select] in de lijst hebt geselecteerd, selecteert u het bestand dat u wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Overige

#### [!UICONTROL Make an API Call]

Deze module voert een aangepaste API-aanroep uit.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL OneDrive] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://graph.microsoft.com</code> . Voorbeeld:<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
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



## Als u een bestand niet kunt uploaden of bijwerken

Er zijn verschillende mogelijke problemen wanneer het uploaden of bijwerken van een bestand mislukt:

* Het geüploade bestand is te groot en overschrijdt de maximale bestandsgroottelimiet voor uw [!DNL OneDrive] -abonnement of u hebt de volledige opslaglimiet van uw [!DNL OneDrive] -account gebruikt. Als u meer opslagruimte wilt, verwijdert u bestaande bestanden uit [!DNL OneDrive] of werkt u een upgrade uit op uw [!DNL OneDrive] -account.
* OneDrive staat het uploaden van twee bestanden met dezelfde naam naar één map niet toe. Als de doelmap een bestand bevat met dezelfde naam als het bestand dat wordt geüpload, wordt de uitvoering van het scenario afgesloten met een fout. U kunt de naam wijzigen van het bestand dat wordt geüpload. Gebruik de handeling [!UICONTROL Update a file] als u een bestand wilt bijwerken.
* De eerder geselecteerde map, waarnaar het bestand wordt geüpload, bestaat niet meer. Het scenario stopt en u moet de doelmap opnieuw selecteren.

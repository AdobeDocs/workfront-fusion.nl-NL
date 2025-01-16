---
title: Box-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Doos gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden. bewaakt een opgegeven map om te controleren op bestandswijzigingen, om bestaande bestanden te wijzigen en te verwijderen of om nieuwe bestanden te uploaden naar een map.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 0%

---

# Box-modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Box] gebruiken en deze koppelen aan meerdere toepassingen en services van derden. bewaakt een opgegeven map om te controleren op bestandswijzigingen, om bestaande bestanden te wijzigen en te verwijderen of om nieuwe bestanden te uploaden naar een map.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

Als u [!DNL Box] -modules wilt gebruiken, moet u een [!DNL Box] -account hebben.

## Box API-informatie

De Box-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] modules en hun velden

Wanneer u [!DNL Box] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Box] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Triggers

* [[!UICONTROL New event]](#new-event)
* [[!UICONTROL Watch files]](#watch-files)

#### [!UICONTROL New event]

Deze instant trigger-module start een scenario wanneer een bestand wordt toegevoegd, verplaatst, gekopieerd, verwijderd, vergrendeld of ontgrendeld.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer de webhaak die u wilt gebruiken om uitgaande berichten te bekijken. Als u een webhaak wilt toevoegen, klikt u op <strong>[!UICONTROL Add]</strong> en voert u de naam en de verbinding van de webhaak in.</p> <p> Voor instructies over het verbinden van uw [!UICONTROL Box] rekening met [!UICONTROL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> verbinden met de dienst - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Maximum number of returned events]</p> </td> 
   <td> <p>Ga het hoogste aantal gebeurtenissen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch files]

Deze triggermodule start een scenario wanneer een nieuw bestand wordt toegevoegd of een bestaand bestand wordt bijgewerkt in een map die wordt gecontroleerd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  <tr> 
   <td role="rowheader">Controle</td> 
   <td> <p>Selecteer het type bestanden dat u wilt bekijken.</p> 
    <ul> 
     <li> <p><strong> slechts nieuwe dossiers </strong> </p> <p>Het scenario wordt gestart wanneer een nieuw bestand wordt toegevoegd.</p> </li> 
     <li> <p><strong> Nieuwe dossiers en alle veranderingen </strong> </p> <p>Het scenario begint wanneer een dossier wordt toegevoegd, of wanneer de dossierinhoud of een dossierattribuut (zoals zijn naam) wordt gewijzigd.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Maximumaantal gedownloade bestanden</p> </td> 
   <td> <p>Ga het hoogste aantal dossiers in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Upload] een bestand](#upload-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)

#### [!UICONTROL Upload a file]

Deze actiemodule uploadt een bestand.

U geeft het bestand op. U kunt ook een nieuwe bestandsnaam voor het bestand opgeven.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Als deze module niet succesvol is, overweeg het volgende:
>
>* De grootte van het bestand kan de maximale bestandsgroottelimiet voor uw [!DNL Box] -abonnement overschrijden, of u hebt de volledige opslaglimiet van uw [!DNL Box] -account gebruikt. Als u meer opslagruimte wilt, verwijdert u bestaande bestanden uit [!DNL Box] of werkt u een upgrade uit op uw [!DNL Box] -account.
>* [!DNL Box] uploadt niet meer dan één bestand met dezelfde naam naar één map. Als de doelmap een bestand bevat met dezelfde naam als het bestand dat wordt geüpload, wordt de uitvoering van het scenario afgesloten met een fout. U kunt dit voorkomen door de naam van het bestand te wijzigen. Gebruik de module **[!UICONTROL Update a file]** als u het bestand wilt bijwerken.

#### [!UICONTROL Update a file]

Deze actiemodule werkt een bestand bij.

U geeft de id van het bestand op.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Voer de unieke id in of wijs deze toe aan het bestand dat u wilt bijwerken in de module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

Met deze actiemodule verwijdert u een bestand.

U geeft de id van het bestand op.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Voer de unieke id in of wijs deze toe aan het bestand dat u wilt bijwerken in de module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Deze actiemodule downloadt een bestand.

U geeft de id van het bestand op.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

>[!NOTE]
>
>Deze module is nuttig om dossiers aan verdere modules te verstrekken.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Voer de unieke id in of wijs deze toe aan het bestand dat u wilt bijwerken in de module.</td> 
  </tr> 
 </tbody> 
</table>

<!--
<h2>Possible problems</h2>

<p style="color: #ff1493;">This is drafted out because we don't have a download module for Box yet</p>


<h3>Watch files trigger module doesn't download a file contained in the folder.</h3>

<p>There are several situations when downloading a file fails:</p>



  <li>The current file lock setting does not allow the file to be downloaded or the downloading of the file is disabled. In this case, the file is ignored.</li>



  <li>When the scenario started, the file was being uploaded to the server and was not ready to be downloaded. The scenario run gets stopped and Workfront Fusion tries downloading the file again during the next execution of the scenario.</li>
  
-->

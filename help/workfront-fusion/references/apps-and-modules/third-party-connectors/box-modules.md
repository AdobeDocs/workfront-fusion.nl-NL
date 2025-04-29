---
title: Box-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Doos gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden. bewaakt een opgegeven map om te controleren op bestandswijzigingen, om bestaande bestanden te wijzigen en te verwijderen of om nieuwe bestanden te uploaden naar een map.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: f02c4df01c7fad6bb9cdf4911512eef97e71c82b
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---

# Box-modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Box] gebruiken en deze koppelen aan meerdere toepassingen en services van derden. bewaakt een opgegeven map om te controleren op bestandswijzigingen, om bestaande bestanden te wijzigen en te verwijderen of om nieuwe bestanden te uploaden naar een map.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Huidig: Geen Workfront Fusion-licentievereisten</p>
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

* [Triggers](#triggers)
* [Handelingen](#actions)

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
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  <tr> 
   <td role="rowheader">Map</td> 
   <td> <p>Selecteer de map die u wilt controleren. Een scenario kan op één enkele omslag letten.</p> 
   </td> 
  </tr> 
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

* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Upload] een bestand](#upload-a-file)

#### [!UICONTROL Delete a file]

Met deze actiemodule verwijdert u een bestand.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Voer de unieke id in van het bestand dat u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Deze actiemodule downloadt een bestand.

U geeft de id van het bestand op.

>[!NOTE]
>
>Deze module is nuttig om dossiers aan verdere modules te verstrekken.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Ga of kaart unieke identiteitskaart van het dossier in dat u de module wilt terugwinnen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a file]

Deze actiemodule werkt een bestand bij.

U geeft de id van het bestand op.

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

#### [!UICONTROL Upload a file]

Deze actiemodule uploadt een bestand.

U geeft het bestand op. U kunt ook een nieuwe bestandsnaam voor het bestand opgeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Box] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selecteer de map waarin u het bestand wilt uploaden.</p> </td> 
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

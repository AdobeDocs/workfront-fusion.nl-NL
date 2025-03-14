---
title: Adobe Workfront Boards-modules
description: U kunt de Adobe Workfront Boards-connector gebruiken om uw processen in Workfront Boards te automatiseren en deze aan te sluiten op apps en services van derden.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: dcc5044d-8fdf-4a74-b664-e965e714ce92
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2659'
ht-degree: 0%

---

# [!DNL Adobe Workfront] Modules van kamers

>[!NOTE]
>
>De Boards Fusion-connector bevindt zich in een bètastatus. Hierdoor is de ondersteuning voor deze aansluiting beperkt en kan deze veranderen als gevolg van de toekomstige ontwikkeling van de Boards. Bovendien kunnen er zonder kennisgeving wijzigingen in de GraphQL API zijn die van invloed kunnen zijn op het proces van de Fusion-connector.

Adobe Workfront Boards zijn flexibele hulpmiddelen die teamsamenwerking toestaan door toegang tot een gedeelde raad te verlenen die kolommen en kaarten bevat.

U kunt de modules van de Boards van Adobe Workfront gebruiken om verslagen te lezen of bij te werken, een API vraag aan de Workfront Boards API te maken, of een scenario teweeg te brengen wanneer een actie op een raad voorkomt.

<!--For general information on Workfront Boards, see [Boards overview](/help/quicksilver/agile/boards-overview.md).-->

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

U moet een board in Adobe Workfront hebben gevormd alvorens u met het kunt verbinden.

## API-informatie voor Adobe Workfront Boards

De Adobe Workfront Boards-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.23.6</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken met Workfront-kaarten

>[!NOTE]
>
>U kunt een Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een aparte Workfront Boards-verbinding maken.

Een Workfront Boards-verbinding maken:

1. Klik in een willekeurige [!DNL Adobe Workfront Boards] -module op **[!UICONTROL Add]** naast het vak Verbinding.

1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Voer een naam in voor deze verbinding.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Environment]</td>
          <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Type]</td>
          <td>Geef op of u verbinding wilt maken met een serviceaccount of een persoonlijke account.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(Optioneel)</p></td>
          <td>Voer uw [!DNL Adobe] [!UICONTROL Client ID] in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Optioneel)</p></td>
          <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(Optioneel)</p></td>
          <td>Voer de URL in die uw instantie van Workfront gebruikt om deze verbinding te verifiëren. <p>De standaardwaarde is <code>https://oauth.my.workfront.com/integrations/oauth2</code> .</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>Voer het hostvoorvoegsel in.<p>De standaardwaarde is <code>origin-</code> .</p>
        </tr>
      </tbody>
    </table>
1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## Modules van de Adobe Workfront Boards en hun velden

Wanneer u Workfront Boards-modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen er extra velden in Workfront Boards worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Kaarten](#cards)
* [Borden](#boards)
* [Kolommen](#columns)
* [Tags](#tags)
* [Opmerkingen](#comments)
* [Overige](#other)

### Kaarten

* [Item voor checklist toevoegen](#add-checklist-item)
* [Subtaak toevoegen](#add-subtask)
* [Een kaart maken](#create-a-card)
* [Een kaart verplaatsen](#move-a-card)
* [Een kaart lezen](#read-a-card)
* [Een kaart bijwerken](#update-a-card)

#### Item voor checklist toevoegen

In deze actiemodule wordt een item uit de controlelijst toegevoegd aan de opgegeven kaart.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Voer de id in van de kaart waaraan u een controlelijstitem wilt toevoegen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Checklist items]</td> 
   <td>Klik voor elk item in de controlelijst dat u wilt toevoegen op Item toevoegen, voer de naam van het item in de controlelijst in en selecteer of het item is voltooid.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Subtaak toevoegen

Deze actiemodule voegt een subtaak aan een kaart in Boards toe. De kaart moet een aangesloten kaart zijn. De subtaak wordt ook toegevoegd aan de Workfront-taak die de kaart vertegenwoordigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Parent card ID]</td> 
   <td>Voer de id in van de kaart waaraan u een subtaak wilt toevoegen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Voer de id in van de kaart die de kaart bevat waaraan u een subtaak wilt toevoegen.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Ga of kaart een naam voor nieuwe subtask in.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Een kaart maken

Met deze actiemodule maakt u een nieuwe kaart op een Workfront-kaart.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Voer de id in van het bord waaraan u een kaart wilt toevoegen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>Voer de id in van de kolom waaraan u een subtaak wilt toevoegen of wijs deze toe.<p>U kunt kolom ID in de informatie vinden die van Gelezen een bordmodule is teruggekeerd.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Voer een naam voor de nieuwe kaart in of wijs een naam toe.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Een kaart verplaatsen

Met deze actiemodule verplaatst u een kaart naar een andere kolom op hetzelfde bord.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Voer de id in van de kaart die u wilt verplaatsen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Voer de id in of wijs deze toe aan het bord met de kaart die u wilt verplaatsen.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination column ID]</td> 
   <td>Voer de id in van de kolom waarnaar u de kaart wilt verplaatsen of wijs deze toe.<p>U kunt kolom ID in de informatie vinden die van Gelezen een bordmodule is teruggekeerd.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To index]</td> 
   <td>Typ of wijs de positie toe die de kaart in de nieuwe kolom moet hebben.<p>De bovenste positie in de kolom in index 0.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Een kaart lezen

Deze actiemodule wint informatie over een specifieke kaart terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Voer de id in van de kaart die u wilt lezen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Voer de id in van de kaart die de kaart bevat die u wilt lezen.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Een kaart bijwerken

Deze actiemodule werkt informatie bij voor een kaart die u opgeeft.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Voer de id in van de kaart die u wilt bijwerken of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Voer de id in van de kaart die de kaart bevat die u wilt bijwerken.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Voer een nieuwe naam voor de kaart in of wijs deze toe.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Voer een nieuwe beschrijving voor de kaart in of wijs deze toe.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Estimation]</td> 
   <td>Voer een schatting in of geef een overzicht van de tijd die nodig is om deze kaart te voltooien.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Due date]</td> 
   <td>Voer de vervaldatum voor deze kaart in of wijs deze toe.</p>
   <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</p>
   </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Status]</td> 
   <td>Selecteer een nieuwe status voor de kaart.</p></td> 
  </tr> 
 </tbody> 
</table>

### Borden

* [Een board maken](#create-a-board)
* [Een bord lezen](#read-a-board)

#### Een board maken

Deze actiemodule maakt een board in Workfront. U kunt opgeven welk type board u wilt maken.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board name]</td> 
   <td>Voer een naam in voor het nieuwe bord of wijs een naam toe.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Template]</td> 
   <td>Selecteer de sjabloon voor het type board dat u wilt maken.</td> 
  </tr> 
 </tbody> 
</table>

#### Een bord lezen

Deze actiemodule retourneert informatie over één board, zoals de kaarten, kolommen, codes en leden van het toetsenbord.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Ga of kaart identiteitskaart van de raad in die u informatie voor wilt terugwinnen.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
 </tbody> 
</table>

### Kolommen

* [Een kolom maken](#create-a-column)
* [Zoeken naar een kolom](#search-for-a-column)
* [Een kolom bijwerken](#update-a-column)

#### Een kolom maken

Deze actiemodule leidt tot een nieuwe kolom op de gespecificeerde raad.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Voer de id in van het bord waaraan u een kolom wilt toevoegen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>Voer de id in van de kolom die u wilt bijwerken of wijs deze toe.<p>U kunt kolom ID in de informatie vinden die van Gelezen een bordmodule is teruggekeerd.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column name]</td> 
   <td>Voer een nieuwe naam voor de kolom in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Zoeken naar een kolom

Deze zoekmodule geeft informatie over de kolom met de opgegeven naam.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Ga of kaart identiteitskaart van de raad in die de kolom bevat u wilt terugwinnen.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Name]</td> 
   <td>Voer de naam in of wijs de naam toe van de kolom die u wilt ophalen.</td> 
  </tr> 
 </tbody> 
</table>

#### Een kolom bijwerken

Deze actiemodule werkt de naam of de grens van WIP van de gespecificeerde kolom bij.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Ga of kaart identiteitskaart van de raad in die de kolom bevat u wilt terugwinnen.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Name]</td> 
   <td>Voer de naam in of wijs de naam toe van de kolom die u wilt ophalen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL WIP Limit]</td> 
   <td>Voer een nieuwe WIP-limiet voor de kolom in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

### Tags

* [Een tag toevoegen aan een kaart](#add-a-tag-to-a-card)
* [Een tag maken](#create-a-tag)

#### Een tag toevoegen aan een kaart

Deze actiemodule voegt een tag toe aan een kaart.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Voer de id in van de kaart waaraan u een tag wilt toevoegen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Voer de id in van het bord met de kaart waaraan u een tag wilt toevoegen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag ID]</td> 
   <td>Voer de id in van de tag die u wilt toevoegen of wijs deze toe.<p>U kunt de tag-id vinden in de informatie die wordt geretourneerd uit de module Een bord lezen.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Een tag maken

Deze actiemodule maakt een nieuw label en wijst er een kleur aan toe.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Voer de id in van het bord waarvoor u een tag wilt maken of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag name]</td> 
   <td>Voer de naam van de nieuwe tag in of wijs deze toe.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag Color]</td> 
   <td>Selecteer de kleur voor deze tag.</td> 
  </tr> 
 </tbody> 
</table>

### Opmerkingen

* [Een opmerking maken](#create-a-comment)
* [Opmerkingen van creditcard lezen](#read-card-comments)

#### Een opmerking maken

Deze actiemodule heeft een opmerking gemaakt op de opgegeven kaart.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Voer de id in van de kaart waaraan u een opmerking wilt toevoegen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Voer de tekst in van de opmerking die u wilt toevoegen of wijs deze toe.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Opmerkingen van creditcard lezen

Deze actiemodule wint de commentaren van de gespecificeerde kaart terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Voer de id in van de kaart waarvoor u de opmerkingen wilt ophalen of wijs deze toe.<p>U kunt de kaart-id in de URL vinden wanneer u de kaart in Workfront bekijkt.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Voer het maximumaantal opmerkingen in dat de module in één uitvoeringscyclus mag retourneren.</p></td> 
  </tr> 
 </tbody> 
</table>

### Overige

#### Een aangepaste API-aanroep maken

Deze actiemodule maakt een aangepaste aanroep naar de Workfront Boards API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Ga een weg met betrekking tot <code> https://&lt;WORKFRONT_DOMAIN&gt;/boards-service/graphql?</code> in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p><p>Voor de meeste Borden roept de methode POST is. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object. Dit bepaalt het inhoudstype van het verzoek.</p> <p>Bijvoorbeeld:<code> { "Content-type":"application/json-stringify()"}</code></p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Voor Workfront Boards is deze sectie meestal leeg.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een ingesloten JSON-grafiek </p> <p>Voorbeeld:</p><p>In dit voorbeeld wordt een kolomnaam bijgewerkt. U kunt <code>boardId</code> en <code>columnId</code> als GUIDs of hard coded of in kaart gebracht van een vorige module omvatten.<p><pre><br> "query": "mutation { updateColumn(boardId: \"\", columnId: \"\", updateColumnInput: { name: \"\" }) { id name}"<br></pre><p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


#### Een aangepaste GraphQL API-aanroep maken

Deze handelingsmodule doet een aangepaste GraphQL-aanvraag voor de Workfront Boards API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>U kunt een bestaande Workfront-verbinding gebruiken om verbinding te maken met Workfront Boards of u kunt een specifieke Workfront Boards-verbinding gebruiken. </p><p>Voor instructies over het verbinden van uw [!DNL Workfront] app aan [!DNL Workfront Fusion], zie <a href="#create-a-connection-to-workfront-boards" class="MCXref xref"> een verbinding aan de Borden van Workfront </a> in dit artikel tot stand brengen.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de methode voor deze vraag. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation name]</td> 
   <td> <p>Voer een naam in voor deze bewerking. Dit kan het vinden en het zuiveren van de vraag gemakkelijker maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variables data source]</td> 
   <td> <p>Selecteer of de variabelen uit een formulier of uit een verzameling moeten komen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variables]</td> 
   <td> <p>Voor elke variabele die u wilt toevoegen, <b> toevoegen punt </b> klikken en de sleutel en de waarde van de variabele ingaan.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
   </tr> 
 </tbody> 
</table>

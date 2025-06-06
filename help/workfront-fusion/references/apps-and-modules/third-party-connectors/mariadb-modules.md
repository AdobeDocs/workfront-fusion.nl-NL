---
title: MariaDB-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die  [!DNL MariaDB] gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
source-git-commit: 8a4e54a4c1783e4bc679778c6fcf21dcb4d3d537
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# [!DNL MariaDB] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL MariaDB] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

Als u [!DNL MariaDB] -modules wilt gebruiken, moet u een [!DNL MariaDB] -account hebben.

## Verbinden [!DNL MariaDB] met [!DNL Workfront Fusion]

U kunt rechtstreeks vanuit een [!DNL MariaDB] -module verbinding maken met uw [!DNL MariaDB] -account.

1. Klik in een willekeurige [!DNL MariaDB] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Configureer de volgende velden:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Voer een naam in voor de nieuwe verbinding.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Selecteer of deze verbinding voor een productie of een non-productie milieu is.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Host]</td> 
      <td> <p>Voer het IP-adres of de hostnaam van uw databaseinstantie in. Deze gastheer moet van buiten uw netwerk toegankelijk zijn.</p> <p>Voorbeeld: <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Port]</td> 
      <td>De standaardpoort is 3306. Als u een niet-standaardhaven gebruikt, plaats dit aantal aan uw haven. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Database &#x200B;]</td> 
      <td>Voer de naam in van de database waarmee u wilt communiceren.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL User]</td> 
      <td>Voer uw gebruikersnaam in.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>Voer uw wachtwoord in.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL MariaDB] Modules en de bijbehorende velden

Wanneer u [!DNL MariaDB] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL MariaDB] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Een query uitvoeren (geavanceerd)

Deze actiemodule wint informatie van uw gegevensbestand terug, die op een vraag wordt gebaseerd u verstrekt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL MariaDB] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL MariaDB] -account met [!DNL Workfront Fusion] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Ga de SQL vraag in die u de module wilt gebruiken om gegevens terug te winnen.</p> <p>Belangrijk: de variabelen die in de query worden gebruikt, worden niet ontsmet. Zorg ervoor dat u variabelen goed ontsmet om SQL-injectie te voorkomen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Select rows from a table (advanced)]

Deze module leest verslag van uw gegevensbestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL MariaDB] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL MariaDB] -account met [!DNL Workfront Fusion] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table]</td> 
   <td> <p>Selecteer de tabel die de records bevat die u wilt lezen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Het filter instellen waarmee u rijen wilt selecteren</p> 
    <ul> 
     <li> <p>Selecteer het veld waarnaar u wilt zoeken</p> </li> 
     <li> <p>Selecteer de operator die u voor de zoekopdracht wilt gebruiken</p> </li> 
     <li> <p>Voer de waarde in of wijs de waarde toe waarnaar u wilt zoeken.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort] </td> 
   <td> <p>Voor elk niveau waarop u de resultaten wilt sorteren, klikt u op <strong>[!UICONTROL Add item]</strong> en selecteert u het veld waarop u de resultaten wilt sorteren en of u oplopend of aflopend wilt sorteren</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

---
title: SFTP-modules
description: De  [!DNL Adobe Workfront Fusion SFTP]  modules staan u toe om dossierveranderingen in een geselecteerde omslag/subfolder te controleren, nieuwe dossiers aan de gewenste omslag te uploaden, bestaande dossiers te wijzigen of te schrappen die reeds in een omslag zijn, of dossiertoestemmingen te veranderen.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '2077'
ht-degree: 0%

---

# SFTP-modules

De [!DNL Adobe Workfront Fusion] SF  modules van TP staan u toe om dossierveranderingen in een geselecteerde omslag/subfolder te controleren, nieuwe dossiers aan de gewenste omslag te uploaden, bestaande dossiers te wijzigen of te schrappen die reeds in een omslag zijn, of dossiertoestemmingen te veranderen.

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
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
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

Als u SFTP met [!DNL Workfront Fusion] wilt gebruiken, hebt u een SFTP-account nodig (zoals [!DNL GoDaddy] webhosting).

## SFTP verbinden met [!DNL Workfront Fusion] {#connect-sftp-to-workfront-fusion}

Als u uw SFTP-account wilt verbinden met [!DNL Workfront Fusion] , moet u een verbinding maken die de doel-host en de SFTP-referenties opgeeft (gebruikersnaam en wachtwoord of gebruikersnaam en sleutel).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection name]</td> 
   <td> <p> Voer de naam in voor uw SFTP-verbinding.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL-omgeving]</td>
    <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL-type]</td>
    <td>Geef op of u verbinding wilt maken met een serviceaccount of een persoonlijke account.</td>
  </tr>
  <tr>
   <td role="rowheader"> <p>[!UICONTROL-host]</p> </td> 
   <td> <p>Voer de hostnaam in van de SFTP-server waarmee u verbinding wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-poort] </td> 
   <td> <p>Voer de SFTP-serverpoort in. Bijvoorbeeld 22.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Auth type]</p> </td> 
   <td> <p>Selecteer de machtigingsmethode die u wilt gebruiken om verbinding te maken met de SFTP-server.</p> 
    <ul> 
     <li><strong> [!UICONTROL - Gebruikersnaam en wachtwoord] </strong>: ga uw geloofsbrieven in.</li> 
     <li> <p><strong>[!UICONTROL - Gebruikersnaam en sleutel] </strong>: ga uw gebruikersnaam en privé sleutel/certificaat in</p> <p>Upload de persoonlijke sleutel om de clientverificatie te gebruiken of upload uw certificaat (P12- of PFX-bestand) als u TLS wilt gebruiken met uw zelfondertekende certificaat. Als u de client-side certificaatautorisatie gebruikt, kunt u hier uw CA-certificaat invoeren.</p> <p>[!DNL Workfront Fusion] bewaart of bewaart geen gegevens (dossiers, wachtwoorden) u hier verstrekt. Bestand en wachtwoord worden alleen gebruikt om een persoonlijke sleutel of certificaat te extraheren.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Key Exchange-algoritmen] </td> 
   <td> <p>U kunt een reeks algoritmen voor sleuteluitwisseling ingaan. De module geeft prioriteit aan algoritmen op basis van de volgorde waarin ze zijn toegevoegd. Voor elk algoritme wilt u toevoegen, <b> toevoegen punt </b> en selecteren het algoritme.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-CIFERS] </td> 
   <td> <p>U kunt een reeks ciphers voor zeer belangrijke uitwisseling ingaan. De module geeft ciphers prioriteit op basis van de volgorde waarin ze zijn toegevoegd. Voor elk cijfer wilt u toevoegen, <b> toevoegen punt </b> en selecteren het cijfer.</p> </td> 
  </tr> 
 </tbody> 
</table>

Na het ingaan van de verbindingsinformatie, ga **** verder om een verbinding te vestigen.

## [!UICONTROL  SFTP ] modules en hun gebieden

Wanneer u [!UICONTROL  SFTP ] modules vormt, [!DNL Workfront Fusion] toont de hieronder vermelde gebieden. Samen met deze, zouden de extra [!UICONTROL  SFTP ] gebieden, afhankelijk van factoren zoals uw toegangsniveau in app of de dienst kunnen tonen. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Triggers

* [Bestanden in een map controleren](#watch-files-in-a-folder)
* [Submappen controleren in een map](#watch-subfolders-in-a-folder)

#### [!UICONTROL  de Dossiers van het Controle in een Omslag ]

Hiermee worden bestanden met details geretourneerd wanneer een bestand in een opgegeven map wordt gemaakt of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Voer de map in die u wilt controleren. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> , of u kunt een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Buffergrootte [B]</td> 
   <td> <p> Voer de buffergrootte in bytes in. De waarde definieert de grootte van overgedragen blokken van de server. Sommige servers kunnen problemen veroorzaken of bestanden beschadigen wanneer de waarde te hoog is.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum aantal geretourneerde bestanden]</td> 
   <td> <p> Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  Controle Subfolders in een Omslag ]

Retourneert mappen met details wanneer een map wordt gemaakt of gewijzigd in een opgegeven map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Voer de map in die u wilt controleren of wijs deze toe. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum aantal geretourneerde bestanden]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [Een map maken](#create-a-folderr)
* [Een bestand verwijderen](#delete-a-file)
* [Een map verwijderen](#delete-a-folder)
* [Een bestand ophalen](#get-a-file)
* [Bestanden ophalen](#get-files)
* [De inhoud van een map weergeven](#list-a-folders-content)
* [Een bestand verplaatsen](#move-a-file)
* [De naam van een bestand wijzigen](#rename-a-file)
* [Bestandsmachtigingen bijwerken](#update-file-permissions)
* [Een bestand uploaden](#upload-a-file)

#### [!UICONTROL  creeer een omslag ]

Deze actiemodule maakt een nieuwe map op de opgegeven locatie.

>[!NOTE]
>
>Als de map al bestaat, genereert de module een fout. Om de stroom ononderbroken voort te zetten, maak een route van de foutenmanager aan de module vast om de fout te vangen en de [!UICONTROL  1} richtlijn van het Hervatten {aan te wenden om de stroom voort te zetten. ] Voor informatie over het vastmaken van een route van de foutenmanager, zie [ de behandeling van de Fout in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md). Voor informatie over de route van de foutenmanager, zie [ Richtlijnen voor fout behandeling in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Geef een bestaande map op als opslaglocatie voor de nieuwe map. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-mapnaam]</td> 
   <td> <p> Voer de mapnaam in.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-machtigingen]</p> </td> 
   <td> <p>Stel de gewenste mapmachtigingen in. Gebruik chmod-parameters. Bijvoorbeeld <code>777</code> of <code>-rwxrwxrwx</code> .</p> <p>Deze machtigingen moeten overeenkomen met het patroon <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Voor meer informatie over chmod, zie de <a href="https://ss64.com/bash/chmod.html"> documentatie van het kosmod </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  Schrap een dossier ]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-bestandspad]</td> 
   <td> <p> Voer het pad in naar het bestand dat u wilt verwijderen. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  Schrap een omslag ]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> Geef het pad op naar de map die u wilt verwijderen. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  krijg een dossier ]

In deze module worden de bestandsgegevens opgehaald, inclusief de gegevens van een bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!grootte UICONTROL-buffer [B]]</td> 
   <td> <p> Voer de buffergrootte in bytes in. De waarde definieert de grootte van overgedragen blokken van de server. Sommige servers kunnen problemen veroorzaken of bestanden beschadigen wanneer de waarde te hoog is.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-bestandspad] </td> 
   <td> <p>Voer het pad naar het bestand in. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  krijgt dossiers ]

Deze module retourneert bestanden uit een opgegeven map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!grootte UICONTROL-buffer [B]]</td> 
   <td> <p> Voer de buffergrootte in bytes in. De waarde definieert de grootte van overgedragen blokken van de server. Sommige servers kunnen problemen veroorzaken of bestanden beschadigen wanneer de waarde te hoog is.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Voer de map in of wijs de map toe die de bestanden of mappen bevat die u wilt weergeven. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in of wijs deze toe. Als u bijvoorbeeld naar bestanden met de bestandsextensie .txt wilt zoeken, voert u <code>.txt</code> in. U kunt ook de naam van het bestand invoeren of toewijzen waarnaar u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL sorteren op]</td> 
   <td> <p> Selecteer of u de resultaten wilt sorteren op de bestandsnaam, grootte, datum van laatste toegang of datum van laatste wijziging.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-sorteervolgorde]</td> 
   <td> <p> Selecteer of het resultaat in oplopende of aflopende volgorde moet worden geretourneerd.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL gaat de uitvoering van de route voort zelfs als de module geen resultaten terugkeert]</p> </td> 
   <td>Schakel deze optie in om ervoor te zorgen dat deze module het scenario niet stopt als het geen resultaten retourneert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum aantal geretourneerde resultaten]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  maak een lijst van de inhoud van een omslag ]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tonen] </td> 
   <td> <p>Selecteer of u bestanden, mappen of beide wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Voer de map in of wijs de map toe die de bestanden of mappen bevat die u wilt weergeven. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in of wijs deze toe. Als u bijvoorbeeld naar bestanden met de bestandsextensie .txt wilt zoeken, voert u <code>.txt</code> in. U kunt ook de naam van het bestand invoeren of toewijzen waarnaar u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL sorteren op]</td> 
   <td> <p> Selecteer of u de resultaten wilt sorteren op bestandsnaam, grootte, datum van laatste toegang of datum van laatste wijziging.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-sorteervolgorde] </td> 
   <td> <p>Selecteer of het resultaat in oplopende of aflopende volgorde moet worden geretourneerd.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL gaat de uitvoering van de route voort zelfs als de module geen resultaten terugkeert]</p> </td> 
   <td>Schakel deze optie in om ervoor te zorgen dat deze module het scenario niet stopt als het geen resultaten retourneert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum aantal geretourneerde resultaten]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  Beweeg een Dossier ]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-bestandspad]</td> 
   <td> <p> Voer het pad in naar het bestand dat u wilt verplaatsen. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nieuwe map]</td> 
   <td> <p> Voer het pad naar de nieuwe locatie van het bestand in. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  noem een Dossier ] anders

Wijzigt de naam van een bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-bestandspad]</td> 
   <td> <p> Voer het pad in naar het bestand waarvan u de naam wilt wijzigen. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL - Nieuwe bestandsnaam]</td> 
   <td> <p> Voer de nieuwe naam voor het bestand in, inclusief de bestandsextensie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  het dossiertoestemmingen van de Update ]

Hiermee kunt u machtigingen voor het bestand wijzigen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-bestandspad]</td> 
   <td> <p> Voer het pad in naar het bestand dat u wilt verplaatsen. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-machtigingen]</p> </td> 
   <td> <p>Stel de gewenste bestandsmachtigingen in. Gebruik chmod-parameters. Bijvoorbeeld <code>777</code> of <code>-rwxrwxrwx</code> .</p> <p>Deze machtigingen moeten overeenkomen met het patroon <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Voor meer informatie over chmod, zie de <a href="https://ss64.com/bash/chmod.html"> documentatie van het kosmod </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  upload een Dossier ]

Met deze module kunt u een bestand uploaden naar de SFTP-server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td>
   <td> <p>Zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP verbinden met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw SFTP-account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Geef een bestaande map op als opslaglocatie voor het bestand. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-bestand]</td> 
   <td> <p> Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-machtigingen]</p> </td> 
   <td> <p>Stel de gewenste machtigingen in voor het bestand of de map. Gebruik chmod-parameters. Bijvoorbeeld <code>777</code> of <code>-rwxrwxrwx</code> .</p> <p>Deze machtigingen moeten overeenkomen met het patroon <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Voor meer informatie over chmod, zie de <a href="https://ss64.com/bash/chmod.html"> documentatie van het kosmod </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

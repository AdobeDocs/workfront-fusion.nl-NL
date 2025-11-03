---
title: SFTP-modules
description: De  [!DNL Adobe Workfront Fusion SFTP]  modules staan u toe om dossierveranderingen in een geselecteerde omslag/subfolder te controleren, nieuwe dossiers aan de gewenste omslag te uploaden, bestaande dossiers te wijzigen of te schrappen die reeds in een omslag zijn, of dossiertoestemmingen te veranderen.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: 54c368d335b30f55cab19595a5b4740dde6013a7
workflow-type: tm+mt
source-wordcount: '1995'
ht-degree: 0%

---

# SFTP-modules

De modules SF van de Fusie van Adobe Workfront  TP staan u toe om dossierveranderingen in een geselecteerde omslag/subfolder te controleren, nieuwe dossiers aan de gewenste omslag te uploaden, bestaande dossiers te wijzigen of te schrappen die reeds in een omslag zijn, of dossiertoestemmingen te veranderen.

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
   <td role="rowheader">Adobe Workfront Fusion-licentie</td> 
   <td>
   <p>Exploitatie gebaseerd: geen Workfront Fusion-licentievereisten</p>
   <p>Connectorgebaseerde (verouderde): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Als u SFTP met Workfront Fusion wilt gebruiken, moet u beschikken over een SFTP-account (zoals [!DNL GoDaddy] webhosting).

## SFTP verbinden met Workfront Fusion {#connect-sftp-to-workfront-fusion}

Als u uw SFTP-account wilt verbinden met Workfront Fusion, moet u een verbinding maken die de doel-host en de SFTP-referenties opgeeft (gebruikersnaam en wachtwoord of gebruikersnaam en sleutel).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection name]</td> 
   <td> <p> Voer de naam in voor uw SFTP-verbinding.</p> </td> 
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
   <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
   <td> <p>Voer de hostnaam in van de SFTP-server waarmee u verbinding wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Port] </td> 
   <td> <p>Voer de SFTP-serverpoort in. Bijvoorbeeld 22.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Auth type]</p> </td> 
   <td> <p>Selecteer de machtigingsmethode die u wilt gebruiken om verbinding te maken met de SFTP-server.</p> 
    <ul> 
     <li><strong>[!UICONTROL User name and password]</strong>: Voer uw referenties in.</li> 
     <li> <p><strong>[!UICONTROL User name and key]</strong>: Voer uw gebruikersnaam en persoonlijke sleutel/certificaat in</p> <p>Upload de persoonlijke sleutel om de clientverificatie te gebruiken of upload uw certificaat (P12- of PFX-bestand) als u TLS wilt gebruiken met uw zelfondertekende certificaat. Als u de client-side certificaatautorisatie gebruikt, kunt u hier uw CA-certificaat invoeren.</p> <p>Workfront Fusion bewaart of slaat geen gegevens (bestanden, wachtwoorden) op die u hier opgeeft. Bestand en wachtwoord worden alleen gebruikt om een persoonlijke sleutel of certificaat te extraheren.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Key exchange algorithms] </td> 
   <td> <p>U kunt een reeks algoritmen voor sleuteluitwisseling ingaan. De module geeft prioriteit aan algoritmen op basis van de volgorde waarin ze zijn toegevoegd. Voor elk algoritme wilt u toevoegen, <b> toevoegen punt </b> en selecteren het algoritme.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ciphers] </td> 
   <td> <p>U kunt een reeks ciphers voor zeer belangrijke uitwisseling ingaan. De module geeft ciphers prioriteit op basis van de volgorde waarin ze zijn toegevoegd. Voor elk cijfer wilt u toevoegen, <b> toevoegen punt </b> en selecteren het cijfer.</p> </td> 
  </tr> 
 </tbody> 
</table>

Nadat u de verbindingsgegevens hebt ingevoerd, klikt u op **[!UICONTROL Continue]** om een verbinding tot stand te brengen.

### Ondersteunde verbindingsopties

De SFTP-connector ondersteunt het volgende bij het maken van een verbinding:

#### Sleuteluitwisselingsalgoritmen (KEX)

* `ecdh-sha2-nistp256`
* `ecdh-sha2-nistp384`
* `ecdh-sha2-nistp521`
* `diffie-hellman-group-exchange-sha256`
* `diffie-hellman-group14-sha256`
* `diffie-hellman-group16-sha512`
* `diffie-hellman-group18-sha512`
* `diffie-hellman-group14-sha1`

#### Schoenen

* `aes256-gcm@openssh.com`
* `aes256-gcm`
* `aes128-gcm@openssh.com`
* `aes128-gcm`
* `aes256-ctr`
* `aes192-ctr`
* `aes128-ctr`
* `aes256-cbc`
* `aes192-cbc`
* `aes128-cbc`
* `blowfish-cbc`

#### Serverhostsleutelindelingen

* `ssh-ed25519`
* `ecdsa-sha2-nistp256`
* `ecdsa-sha2-nistp384`
* `ecdsa-sha2-nistp521`
* `ssh-rsa`
* `ssh-dss`
<!--
* `rsa-sha2-256`
* `rsa-sha2-512`
-->

## [!UICONTROL SFTP] modules en hun velden

Wanneer u [!UICONTROL SFTP] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!UICONTROL SFTP] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Triggers

* [Bestanden in een map controleren](#watch-files-in-a-folder)
* [Submappen controleren in een map](#watch-subfolders-in-a-folder)

#### [!UICONTROL Watch Files in a Folder]

Hiermee worden bestanden met details geretourneerd wanneer een bestand in een opgegeven map wordt gemaakt of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Voer de map in die u wilt controleren. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> , of u kunt een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Buffergrootte [B]</td> 
   <td> <p> Voer de buffergrootte in bytes in. De waarde definieert de grootte van overgedragen blokken van de server. Sommige servers kunnen problemen veroorzaken of bestanden beschadigen wanneer de waarde te hoog is.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Subfolders in a Folder]

Retourneert mappen met details wanneer een map wordt gemaakt of gewijzigd in een opgegeven map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Voer de map in die u wilt controleren of wijs deze toe. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
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

#### [!UICONTROL Create a folder]

Deze actiemodule maakt een nieuwe map op de opgegeven locatie.

>[!NOTE]
>
>Als de map al bestaat, genereert de module een fout. Als u de stroom zonder onderbreking wilt voortzetten, koppelt u een fouthandlerroute aan de module om de fout af te vangen en past u de instructie [!UICONTROL Resume] toe om de stroom voort te zetten. Voor informatie over het vastmaken van een route van de foutenmanager, zie [&#x200B; de behandeling van de Fout in de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md). Voor informatie over de route van de foutenmanager, zie [&#x200B; Richtlijnen voor fout behandeling in de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Geef een bestaande map op als opslaglocatie voor de nieuwe map. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name]</td> 
   <td> <p> Voer de mapnaam in.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Stel de gewenste mapmachtigingen in. Gebruik chmod-parameters. Bijvoorbeeld <code>777</code> of <code>-rwxrwxrwx</code> .</p> <p>Deze machtigingen moeten overeenkomen met het patroon <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Voor meer informatie over chmod, zie de <a href="https://ss64.com/bash/chmod.html"> documentatie van het kosmod </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Voer het pad in naar het bestand dat u wilt verwijderen. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> Geef het pad op naar de map die u wilt verwijderen. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

In deze module worden de bestandsgegevens opgehaald, inclusief de gegevens van een bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Voer de buffergrootte in bytes in. De waarde definieert de grootte van overgedragen blokken van de server. Sommige servers kunnen problemen veroorzaken of bestanden beschadigen wanneer de waarde te hoog is.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path] </td> 
   <td> <p>Voer het pad naar het bestand in. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get files]

Deze module retourneert bestanden uit een opgegeven map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Voer de buffergrootte in bytes in. De waarde definieert de grootte van overgedragen blokken van de server. Sommige servers kunnen problemen veroorzaken of bestanden beschadigen wanneer de waarde te hoog is.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Voer de map in of wijs de map toe die de bestanden of mappen bevat die u wilt weergeven. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in of wijs deze toe. Als u bijvoorbeeld naar bestanden met de bestandsextensie .txt wilt zoeken, voert u <code>.txt</code> in. U kunt ook de naam van het bestand invoeren of toewijzen waarnaar u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Selecteer of u de resultaten wilt sorteren op de bestandsnaam, grootte, datum van laatste toegang of datum van laatste wijziging.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order]</td> 
   <td> <p> Selecteer of het resultaat in oplopende of aflopende volgorde moet worden geretourneerd.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Schakel deze optie in om ervoor te zorgen dat deze module het scenario niet stopt als het geen resultaten retourneert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List a folder's content]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Selecteer of u bestanden, mappen of beide wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Voer de map in of wijs de map toe die de bestanden of mappen bevat die u wilt weergeven. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in of wijs deze toe. Als u bijvoorbeeld naar bestanden met de bestandsextensie .txt wilt zoeken, voert u <code>.txt</code> in. U kunt ook de naam van het bestand invoeren of toewijzen waarnaar u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Selecteer of u de resultaten wilt sorteren op bestandsnaam, grootte, datum van laatste toegang of datum van laatste wijziging.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order] </td> 
   <td> <p>Selecteer of het resultaat in oplopende of aflopende volgorde moet worden geretourneerd.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Schakel deze optie in om ervoor te zorgen dat deze module het scenario niet stopt als het geen resultaten retourneert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Voer het pad in naar het bestand dat u wilt verplaatsen. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New Folder]</td> 
   <td> <p> Voer het pad naar de nieuwe locatie van het bestand in. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rename a File]

Wijzigt de naam van een bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Voer het pad in naar het bestand waarvan u de naam wilt wijzigen. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New file name]</td> 
   <td> <p> Voer de nieuwe naam voor het bestand in, inclusief de bestandsextensie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update file permissions]

Hiermee kunt u machtigingen voor het bestand wijzigen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Voer het pad in naar het bestand dat u wilt verplaatsen. U kunt een absoluut pad opgeven, zoals <code>/home/user/file.txt</code> . U kunt ook een relatief pad opgeven dat wijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./file.txt</code> .</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Stel de gewenste bestandsmachtigingen in. Gebruik chmod-parameters. Bijvoorbeeld <code>777</code> of <code>-rwxrwxrwx</code> .</p> <p>Deze machtigingen moeten overeenkomen met het patroon <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Voor meer informatie over chmod, zie de <a href="https://ss64.com/bash/chmod.html"> documentatie van het kosmod </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

Met deze module kunt u een bestand uploaden naar de SFTP-server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening SFTP aan de Fusie van Workfront, zie <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref"> SFTP met de Fusie van Workfront </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Geef een bestaande map op als opslaglocatie voor het bestand. U kunt een absoluut pad opgeven, zoals <code>/home/user/</code> . U kunt ook een relatief pad opgeven dat verwijst naar een specifieke map van de aangemelde gebruiker, zoals <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td> <p> Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Stel de gewenste machtigingen in voor het bestand of de map. Gebruik chmod-parameters. Bijvoorbeeld <code>777</code> of <code>-rwxrwxrwx</code> .</p> <p>Deze machtigingen moeten overeenkomen met het patroon <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Voor meer informatie over chmod, zie de <a href="https://ss64.com/bash/chmod.html"> documentatie van het kosmod </a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Buffer size (B)]</p> </td> 
   <td> <p>Stel de grootte (in bytes) van elk segment in wanneer u het bestand uploadt. Dit is handig voor grote bestanden of wanneer de geheugenlimieten van de server kleinere uploads vereisen. Als deze waarde niet is ingesteld, wordt het bestand in één bewerking geschreven.</p> </td> 
  </tr> 
 </tbody> 
</table>

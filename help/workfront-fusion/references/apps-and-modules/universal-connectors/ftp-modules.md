---
title: FTP-modules
description: Met FTP-modules kunt u bestandswijzigingen in een geselecteerde map controleren, nieuwe bestanden naar de gewenste map uploaden en bestaande bestanden die zich al in een map bevinden, wijzigen of verwijderen.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: 54c368d335b30f55cab19595a5b4740dde6013a7
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 0%

---

# FTP-modules

Met FTP-modules kunt u bestandswijzigingen in een geselecteerde map controleren, nieuwe bestanden naar de gewenste map uploaden en bestaande bestanden die zich al in een map bevinden, wijzigen of verwijderen.

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

Als u FTP-modules wilt gebruiken, moet u over een account bij een FTP-service beschikken.

## Verbinding maken in een FTP-module {#create-a-connection}

1. In om het even welke module van FTP, voegt de klik **toe** naast de verbindingsdoos.
1. Vul de volgende velden in.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Connection name]</td> 
      <td> <p> Voer de naam in voor uw FTP-verbinding.</p> </td> 
     </tr> 
     <tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td> <p>Selecteer of u een productie- of niet-productieomgeving gebruikt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Type]</p> </td> 
      <td> <p>Selecteer of u een serviceaccount of een persoonlijke account gebruikt.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Host] </td> 
      <td> <p>Voer de hostnaam van de FTP-server in. Voorbeeld: <code>myftp123.server.com</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Port] </td> 
      <td> <p>Voer het poortnummer van de FTP-server in. Voorbeeld: <code>21</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL User name] </td> 
      <td> <p>Voer de gebruikersnaam van uw FTP-account in.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Password] </td> 
      <td> <p>Voer het wachtwoord voor uw FTP-account in.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Een beveiligde verbinding (TLS) gebruiken</p> </td> 
      <td> <p>Selecteer of u een veilige verbinding wilt gebruiken.</p> <ul><li><p><b>[!UICONTROL No]</b></p> <p>De verbinding is niet beveiligd.</p></li><li> <p><b> Expliciete encryptie </b> of <b> Impliciete encryptie </b></p> <p>De verbinding wordt beveiligd met SSL.</p> </td> 
     </tr> 
    <tr> 
   <td> <p>[!UICONTROL Reject unauthorized certificates]</p> </td> 
   <td> <p>Schakel deze optie in om het FTP-servercertificaat te verifiëren. Als de verificatie mislukt, wordt er geen verbinding gemaakt. Om voor de verificatie te slagen, moet het certificaat aan een van de volgende criteria voldoen:</p> 
    <ul> 
     <li>worden ondertekend door een basiscertificeringsinstantie</a></li> 
     <li>worden ondertekend door een intermediaire certificeringsinstantie. In dit geval moeten alle tussentijdse certificaten op de FTP-server zijn geïnstalleerd.</li> 
     <li>Een zelfondertekend certificaat zijn dat wordt opgegeven in het veld [!UICONTROL Self-signed certificate] (zie hieronder)</li> </ul>
     <p>Als deze optie is uitgeschakeld, wordt het FTP-servercertificaat niet geverifieerd. Wij raden u ten zeerste aan de optie niet uit te schakelen, omdat hierdoor de verbinding onveilig wordt en een ernstig veiligheidsrisico ontstaat.</p></td>
    </tr> 
    <tr> 
     <td> <p>[!UICONTROL Self-signed certificate]</p> </td> 
     <td> <p>Klik op de knop <b>[!UICONTROL Extract]</b> om het dialoogvenster voor uploaden te openen.</p> <p>Upload het certificaat om het TLS te gebruiken met uw zelfondertekende certificaat. Workfront Fusion bewaart of slaat geen gegevens op die u opgeeft, zoals bestanden en wachtwoorden. Bestand en wachtwoord worden alleen gebruikt om het certificaat te extraheren.</p> </td> 
    </tr> 
   </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## FTP-modules en de bijbehorende velden

* [Triggers](#triggers)
* [Handelingen](#actions)

### Triggers

#### [!UICONTROL Watch files]

[!UICONTROL Watch files] is de enige triggermodule voor FTP. De inhoud van de geselecteerde map wordt gecontroleerd. De trigger wordt uitgevoerd wanneer een nieuw bestand aan de opgegeven map wordt toegevoegd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#create-a-connection" class="MCXref xref">[!UICONTROL Create a connection] in een module van FTP </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Selecteer de map die u wilt controleren.</p> <p><b> Nota:</b> slechts één omslag per scenario wordt toegestaan. Submappen worden genegeerd.</p> <p><b> Uiteinde:</b> om veelvoudige omslagen te letten, creeer een afzonderlijk scenario voor elk van hen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files] </td> 
   <td> <p>Stel het maximale aantal resultaten in waarmee de module tijdens één cyclus moet werken. Als de waarde te hoog is ingesteld, kan de verbinding aan de zijkant van de FTP-server worden onderbroken. Workfront Fusion heeft daar geen invloed op. Wij adviseren dat u een lagere waarde plaatst en of een hogere waarde voor het maximumaantal cycli bepaalt of het scenario vaker in werking stelt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Change permissions]](#change-permissions)
* [[!UICONTROL Create a folder]](#create-a-folder)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Delete a folder]](#delete-a-folder)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL List of files in a folder]](#list-of-files-in-a-folder)
* [[!UICONTROL Move a file or folder]](#move-a-file-or-folder)
* [[!UICONTROL Upload] een bestand](#upload-a-file)

#### [!UICONTROL Change permissions]

In deze handelingsmodule worden de machtigingsinstellingen van een bestand of map gewijzigd.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in een module van FTP </a> in dit artikel.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Change permission settings of]</td>
            <td>
               <p>Selecteer of u de instellingen voor een bestand of map wilt wijzigen.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL File path]</td>
            <td>Voer het bestandspad in of wijs het toe aan de map of het bestand.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Permissions]</td>
            <td>
               <p>Stel de gewenste bestands- of mapmachtigingen in. Gebruik de parameters chmod. Bijvoorbeeld: <code>777 </code> of <code>-rwxrwxrwx</code> .</p>
               <p>Rechten moeten overeenkomen met het patroon <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code> .</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Create a folder]

Deze actiemodule maakt een nieuwe map.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in een module van FTP </a> in dit artikel.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Folder path]</td>
            <td>Voer het bestandspad in of wijs het toe aan de nieuwe map.</td>
         </tr>
         <tr>
            <td>[!UICONTROL New folder name]</td>
            <td>
               <p>Voer een naam voor de nieuwe map in of wijs deze toe.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Delete a file]

Deze actiemodule verwijdert een bestand uit de opgegeven map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
            <td>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in een module van FTP </a> in dit artikel.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de FTP-map waaruit u een bestand wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td> <p> Voer de bestandsnaam in, inclusief de bestandsnaamextensie. Voorbeeld: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

Deze actiemodule verwijdert de opgegeven map permanent.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in een module van FTP </a> in dit artikel.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Folder]</td>
            <td>
               <p>Selecteer de FTP-map waaruit u een bestand wilt verwijderen.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Get a file]

Deze actiemodule haalt een bestand op van de FTP-server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#creating-the-ftp-connection" class="MCXref xref"> Creërend de Verbinding van FTP </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File path]</td> 
   <td> <p> Voer het pad in van het bestand dat u wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List of files in a folder]

Deze actiemodule haalt bestand- en/of mapinformatie op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#creating-the-ftp-connection" class="MCXref xref"> Creërend de Verbinding van FTP </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de FTP-map waarin u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Selecteer of u informatie over bestanden of mappen of beide wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in. Als er geen zoekterm wordt ingevoerd, worden alle bestanden of mappen uit de opgegeven map opgehaald.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p>Ga of kaart het maximumaantal resultaten in dat u de module tijdens één cyclus wilt werken met.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a file or folder]

Deze actiemodule verplaatst een bestand of map naar een andere locatie.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in een module van FTP </a> in dit artikel.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Old file path]</td>
            <td>
               <p>Voer het pad in waaruit u het bestand wilt verplaatsen. Voorbeeld: <code>/folder1/document.txt</code> .</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL New file path]</td>
            <td>
               <p>Voer het pad in waarnaar u het bestand wilt verplaatsen. Voorbeeld: <code>/folder2/document.txt</code> .</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Upload a file]

Uploadt een bestand naar de FTP-server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#creating-the-ftp-connection" class="MCXref xref"> Creërend de Verbinding van FTP </a> in dit artikel.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de FTP-map waarnaar u het bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file] </td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Append to an already existing file]</td> 
   <td> <p>Als deze optie is ingeschakeld en het bestand al op de FTP-server staat, wordt de inhoud van het bestand aan het bestaande bestand toegevoegd. Als deze optie niet is ingeschakeld, wordt de inhoud van het bestand overschreven.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create folders if don't exist] </td> 
   <td> <p>Als deze optie is ingeschakeld en de map die u in het veld Map hebt ingevoerd, niet bestaat op de FTP-server, maakt de module de map</p> </td> 
  </tr> 
 </tbody> 
</table>

## Problemen oplossen {#troubleshooting}

Als u problemen ondervindt met de FTP-toepassing tijdens het maken van de verbinding of tijdens het uitvoeren van een module, probeert u een van de populaire FTP-clients te gebruiken en probeert u dezelfde actie uit te voeren (bijvoorbeeld het maken van een verbinding of het weergeven van bestanden in een map). met de FTP-client. Als u dezelfde problemen ook ondervindt met de FTP-client, is de reden mogelijk een verkeerde configuratie van de FTP-server.

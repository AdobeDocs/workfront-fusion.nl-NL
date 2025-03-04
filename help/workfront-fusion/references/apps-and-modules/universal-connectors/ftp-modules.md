---
title: FTP-modules
description: Met FTP-modules kunt u bestandswijzigingen in een geselecteerde map controleren, nieuwe bestanden naar de gewenste map uploaden en bestaande bestanden die zich al in een map bevinden, wijzigen of verwijderen.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: c5e9c643c828e5556e386a5f46e1d17680b7d4e9
workflow-type: tm+mt
source-wordcount: '1328'
ht-degree: 0%

---

# FTP-modules

Met FTP-modules kunt u bestandswijzigingen in een geselecteerde map controleren, nieuwe bestanden naar de gewenste map uploaden en bestaande bestanden die zich al in een map bevinden, wijzigen of verwijderen.

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

Als u FTP-modules wilt gebruiken, hebt u een FTP-account nodig.

## Verbinding maken in een FTP-module {#create-a-connection}

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection name]</td> 
   <td> <p> Voer de naam in voor uw FTP-verbinding.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-host] </td> 
   <td> <p>Voer de hostnaam van de FTP-server in. E.g. <code>myftp123.server.com</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-poort] </td> 
   <td> <p>Voer het poortnummer van de FTP-server in. E.g. <code>21</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-gebruikersnaam] </td> 
   <td> <p>Voer de gebruikersnaam van uw FTP-account in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-wachtwoord] </td> 
   <td> <p>Voer het wachtwoord voor uw FTP-account in.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Een beveiligde verbinding (TLS) gebruiken</p> </td> 
   <td> <p>Selecteer of u een veilige verbinding wilt gebruiken.</p> <p style="font-weight: bold;">[!UICONTROL-nr.]</p> <p>De verbinding is niet beveiligd.</p> <p style="font-weight: bold;">[!UICONTROL Expliciete encryptie of Impliciete encryptie]</p> <p>De verbinding wordt beveiligd met SSL.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL onbevoegde certificaten afwijzen]</p> </td> 
   <td> <p>Schakel deze optie in om het FTP-servercertificaat te verifiëren. Als de verificatie mislukt, wordt er geen verbinding gemaakt. Om voor de verificatie te slagen, moet het certificaat aan een van de volgende criteria voldoen:</p> 
    <ul> 
     <li>worden ondertekend door aRoot <a href="https://en.wikipedia.org/wiki/Certificate_authority"> Instantie van het Certificaat </a></li> 
     <li>worden ondertekend door een Directe Instantie van het Certificaat (zie b.v. <a href="https://knowledge.digicert.com/solution/SO16297.html"> hoe de certificaatketens </a> voor verdere verklaring werken). In dit geval moeten alle tussentijdse certificaten op de FTP-server zijn geïnstalleerd.</li> 
     <li>Een zelfondertekend certificaat zijn dat wordt geleverd in het veld [!UICONTROL Zelfondertekend certificaat] (zie hieronder)</li> </ul>

Als deze optie is uitgeschakeld, wordt het FTP-servercertificaat niet geverifieerd. Wij raden u ten zeerste aan de optie niet uit te schakelen, omdat hierdoor de verbinding onveilig wordt en een ernstig veiligheidsrisico ontstaat.</td>
</tr> 
  <tr> 
   <td> <p>[!UICONTROL Zelfondertekend certificaat]</p> </td> 
   <td> <p>Klik <b> [!UICONTROL Extraheren] </b> knoop om de upload dialoog te openen.</p> <p>Upload het certificaat om het TLS te gebruiken met uw zelfondertekende certificaat. [!DNL Workfront Fusion] bewaart of bewaart geen gegevens u, zoals dossiers en wachtwoorden verstrekt. Bestand en wachtwoord worden alleen gebruikt om het certificaat te extraheren.</p> </td> 
  </tr> 
 </tbody> 
</table>

## FTP-modules en de bijbehorende velden

* [Triggers](#triggers)
* [Handelingen](#actions)

### Triggers

#### [!UICONTROL  de dossiers van het Controle ]

[!UICONTROL  de dossiers van het Controle ] is de enige trekkermodule voor FTP. De inhoud van de geselecteerde map wordt gecontroleerd. De trigger wordt uitgevoerd wanneer een nieuw bestand in de opgegeven map wordt ingevoegd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#create-a-connection" class="MCXref xref"> [!UICONTROL creeer een verbinding] in een module van FTP </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-map]</p> </td> 
   <td> <p>Selecteer de map die u wilt controleren.</p> <p><b> Nota:</b> slechts één omslag per scenario wordt toegestaan. Submappen worden genegeerd.</p> <p><b> Uiteinde:</b> om spoor van veelvoudige omslagen te houden, creeer een onafhankelijk scenario voor elk van hen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum aantal geretourneerde bestanden] </td> 
   <td> <p>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt. Als de waarde te hoog is ingesteld, kan de verbinding aan de kant van de opgegeven service van derden (timeout) worden onderbroken. [!DNL Workfront Fusion] heeft hier geen invloed op. Wij adviseren dat u een lagere waarde plaatst en of een hogere waarde voor het maximumaantal cycli bepaalt of het scenario vaker in werking stelt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL  toestemmingen van de Verandering ]](#change-permissions)
* [[!UICONTROL  creeer een omslag ]](#create-a-folder)
* [[!UICONTROL  Schrap een dossier ]](#delete-a-file)
* [[!UICONTROL  Schrap een omslag ]](#delete-a-folder)
* [[!UICONTROL  krijg een dossier ]](#get-a-file)
* [[!UICONTROL  Lijst van dossiers in een omslag ]](#list-of-files-in-a-folder)
* [[!UICONTROL  Beweeg een dossier of een omslag ]](#move-a-file-or-folder)
* [[!UICONTROL  upload ] een dossier](#upload-a-file)

#### [!UICONTROL  toestemmingen van de Verandering ]

In deze handelingsmodule worden de machtigingsinstellingen van een bestand of map gewijzigd.

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL-verbinding]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" > [!UICONTROL creeer een verbinding] in een module van FTP </a> in dit artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Wijzig machtigingsinstellingen van]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">
               <p>Selecteer of u de instellingen voor een bestand of map wilt wijzigen.</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL-bestandspad]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Voer het bestandspad in of wijs het toe aan de map of het bestand.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-MediumGray" role="rowheader">[!UICONTROL-machtigingen]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-MediumGray">
               <p>Stel de gewenste bestands- of mapmachtigingen in. Gebruik de parameters chmod. Bijvoorbeeld: <code>777 </code> of <code>-rwxrwxrwx</code> .</p>
               <p>Rechten moeten overeenkomen met het patroon <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code> .</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL  creeer een omslag ]

Deze actiemodule maakt een nieuwe map.

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL-verbinding]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" > [!UICONTROL creeer een verbinding] in een module van FTP </a> in dit artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!Pad naar map UICONTROL]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">Voer het bestandspad in of wijs het toe aan de nieuwe map.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">[!UICONTROL Nieuwe mapnaam]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">
               <p>Voer een naam voor de nieuwe map in of wijs deze toe.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL  Schrap een dossier ]

Hiermee wordt een bestand uit de opgegeven map verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" > [!UICONTROL creeer een verbinding] in een module van FTP </a> in dit artikel.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Selecteer de FTP-map waaruit u een bestand wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-bestandsnaam]</td> 
   <td> <p> Voer de bestandsnaam in, inclusief de bestandsnaamextensie. Voorbeeld: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  Schrap een omslag ]

Deze actiemodule verwijdert de opgegeven map permanent.

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL-verbinding]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" > [!UICONTROL creeer een verbinding] in een module van FTP </a> in dit artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL-map]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-MediumGray">
               <p>Selecteer de FTP-map waaruit u een bestand wilt verwijderen.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL  krijg een dossier ]

Hiermee wordt een bestand opgehaald van de FTP-server dat verder kan worden verwerkt, bijvoorbeeld geüpload naar de [!DNL Dropbox] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#creating-the-ftp-connection" class="MCXref xref"> Creërend de Verbinding van FTP </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-bestandspad]</td> 
   <td> <p> Voer het pad in van het bestand dat u wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  Lijst van dossiers in een omslag ]

Hiermee worden bestands- en/of mapgegevens opgehaald.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#creating-the-ftp-connection" class="MCXref xref"> Creërend de Verbinding van FTP </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Selecteer de FTP-map waarin u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tonen] </td> 
   <td> <p>Selecteer of u informatie over bestanden of mappen of beide wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in. Als er geen zoekterm is ingevoerd, worden alle bestanden en mappen uit de opgegeven map opgehaald.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum aantal geretourneerde bestanden]</td> 
   <td> <p> Stel het maximumaantal opgehaalde bestanden in door deze module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  Beweeg een dossier of een omslag ]

Deze actiemodule verplaatst een bestand of map naar een andere locatie.

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL-verbinding]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#Create" class="MCXref xref" > [!UICONTROL creeer een verbinding] in een module van FTP </a> in dit artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-MediumGray" style="font-weight: bold;">[!Pad naar oud bestand UICONTROL]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-MediumGray">
               <p>Voer het pad in waaruit u het bestand wilt verplaatsen. Voorbeeld: <code>/folder1/document.txt</code> .</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-LightGray" style="font-weight: bold;">[!Pad naar nieuw bestand UICONTROL]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-LightGray">
               <p>Voer het pad in waarnaar u het bestand wilt verplaatsen. Voorbeeld: <code>/folder2/document.txt</code> .</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL  upload een dossier ]

Uploadt een bestand naar de FTP-server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td>Voor instructies bij het vestigen van een verbinding aan de rekening van FTP, zie <a href="#creating-the-ftp-connection" class="MCXref xref"> Creërend de Verbinding van FTP </a> in dit artikel.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Selecteer de FTP-map waarnaar u het bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-bestand] </td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Toevoegen aan een bestaand bestand]</td> 
   <td> <p>Als deze optie is ingeschakeld en het bestand al op de FTP-server staat, wordt de inhoud van het bestand aan het bestaande bestand toegevoegd. Als deze optie niet is ingeschakeld, wordt de inhoud van het bestand overschreven.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL leidt omslagen als niet bestaat] </td> 
   <td> <p>Als deze optie is ingeschakeld en de map die u in het veld Map hebt ingevoerd, niet bestaat op de FTP-server, maakt de module de map</p> </td> 
  </tr> 
 </tbody> 
</table>

## Problemen oplossen {#troubleshooting}

Als u problemen ondervindt met de FTP-toepassing tijdens het maken van de verbinding of tijdens het uitvoeren van een module, probeert u een van de populaire FTP-clients te gebruiken en probeert u dezelfde actie uit te voeren (bijvoorbeeld het maken van een verbinding of het weergeven van bestanden in een map). met de FTP-client. Als u dezelfde problemen ook ondervindt met de FTP-client, is de reden mogelijk een verkeerde configuratie van de FTP-server.

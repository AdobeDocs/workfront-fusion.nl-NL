---
title: Adobe Experience Manager Assets-modules
description: Met de Adobe Experience Manager Assets-connector voor Adobe Workfront Fusion kunt u elementen maken, uploaden en bijwerken en mappen en elementen kopiëren of verplaatsen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: 190c35629f1fc1e07eef4110f3f4f771af1065fb
workflow-type: tm+mt
source-wordcount: '3727'
ht-degree: 0%

---

# Adobe Experience Manager Assets-modules

Met de Adobe Experience Manager Assets-connector voor Adobe Workfront Fusion kunt u elementen maken, uploaden en bijwerken en mappen en elementen kopiëren of verplaatsen.

Ga voor een video-introductie over de Adobe Experience Manager Assets-connector naar:

* [&#x200B; Adobe Experience Manager Assets &#x200B;](https://video.tv.adobe.com/v/3427034/){target=_blank}

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
   <p>Verouderd: Workfront Fusion for Automation and Integration </p>
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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

* U moet een Adobe Experience Manager Assets-account hebben om deze modules te kunnen gebruiken.
* U moet server-aan-server stroom in de console van Adobe Developer plaatsen.

  Voor instructies bij vestiging server-aan-server stroom in de console van Adobe Developer, zie [&#x200B; Genererend de Tokens van de Toegang voor de Kant APIs van de Server &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
* Je technische Adobe Experience Manager-account moet schrijfmachtigingen hebben.

  Voor instructies bij het toevoegen van schrijven toestemmingen aan uw technische rekening van Adobe Experience Manager, zie &lbrace;de geloofsbrieven van de Dienst [&#x200B; in de documentatie van Adobe Experience Manager.](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials)

## Adobe Experience Manager Assets API-informatie

De Adobe Experience Manager Assets-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Adobe Experience Manager Assets verbinden met Workfront Fusion {#connect-adobe-experience-manager-assets-to-workfront-fusion}

Verbinding maken voor uw Adobe Experience Manager Assets-modules:

1. Klik naast het vak Verbinding op Toevoegen.

2. Selecteer het type verbinding dat u maakt:

   * **AEM Assets as a Cloud Service**

     Voor deze configuratie is informatie van de Adobe Admin Console vereist.

   * **Basis van AEM Assets (Adobe Managed Services)**

     Voor deze configuratie zijn een gebruikersnaam en wachtwoord vereist.

3. Vul de velden in voor het type verbinding dat u maakt.

   Voor AEM Assets as a Cloud Service, zie [&#x200B; de verbinding voor AEM Assets as a Cloud Service &#x200B;](#configure-the-connection-for-aem-assets-as-a-cloud-service) vormen.

   Voor AEM Assets Basis (Adobe Managed Services), zie [&#x200B; de verbinding voor AEM Assets Basis &#x200B;](#configure-the-connection-for-aemassets-basic-adobe-managed-services) vormen.

4. Klik **verdergaan** om de verbinding te bewaren en aan de module terug te keren.


### De verbinding voor AEM Assets as a Cloud Service configureren

>[!NOTE]
>
>* De informatie voor deze velden wordt gegenereerd als onderdeel van het instellen van server-naar-server flow op de Adobe Developer Console. U kunt deze waarden vinden in het JSON-bestand met servicereferenties dat is gegenereerd als onderdeel van die instelling.
>
>   Voor instructies bij vestiging server-aan-server stroom op Adobe Developer Console, zie [&#x200B; Genererend de Tokens van de Toegang voor de Kant APIs van de Server &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
>
>* Je technische Adobe Experience Manager-account moet schrijfmachtigingen hebben.
>
>   Voor instructies bij het toevoegen van schrijven toestemmingen aan uw technische rekening van Adobe Experience Manager, zie &lbrace;de geloofsbrieven van de Dienst [&#x200B; in de documentatie van Adobe Experience Manager.](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials)


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">Verbindingsnaam</td>
                  <td>
                      <p>Voer een naam in voor deze verbinding.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">Instantie-URL zonder slash</td>
                  <td>Voer de URL voor uw Adobe Experience Manager-instantie in. Plaats geen schuine streep <code>/</code> aan het einde van de URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">Opties voor het invullen van accountdetails</td>
                  <td>Selecteer of u JSON wilt opgeven met een beschrijving van uw accountgegevens of dat u de gegevens handmatig wilt invoeren.</td>
              </tr>
              <tr>
                  <td role="rowheader">Technische accountgegevens in JSON-indeling</td>
                  <td>Als u JSON opgeeft, voert u de JSON in of plakt u deze met een beschrijving van uw accountgegevens.</td>
              </tr>
              <tr>
                  <td role="rowheader">Client-id</td>
                  <td>Als het ingaan van details manueel, ga identiteitskaart van de Cliënt in die in de server-aan-server opstelling wordt geproduceerd.</td>
              </tr>
              <tr>
                  <td role="rowheader">Clientgeheim</td>
                  <td>Als het ingaan van details manueel, ga het Geheim van de Cliënt in die in de server-aan-server opstelling wordt geproduceerd.</td>
              </tr>
              <tr>
                  <td role="rowheader">Technische account-id</td>
                  <td>Voer de id van de technische account in als u de gegevens handmatig invoert. Dit is het veld "id" in het JSON-bestand met clientreferenties.</td>
              </tr>
              <tr>
                  <td role="rowheader">Org-id</td>
                  <td class="">Voer de id van uw organisatie in als u de gegevens handmatig invoert. Dit is het veld "org" in het JSON-bestand met clientreferenties.</td>
              </tr>
              <tr>
                  <td role="rowheader">Meta-modellen</td>
                  <td>Voer de Meta-modellen in die in de serverinstellingen worden gegenereerd.</td>
              </tr>
              <tr>
                  <td role="rowheader">Persoonlijke sleutel</td>
                  <td>Voer de gegenereerde persoonlijke sleutel in om de setup van server naar server te verkrijgen. Als u de persoonlijke sleutel wilt extraheren, klikt u op Extraheren en voert u het bestand in dat u wilt extraheren en het wachtwoord voor het bestand.</td>
              </tr>
              <tr>
                  <td role="rowheader">Verificatie-URL</td>
                  <td>Voer de verificatie-URL voor dit account in.</td>
              </tr>
          </tbody>
      </table>


### De verbinding configureren voor AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">Verbindingsnaam</td>
                <td>
                    <p>Voer een naam in voor deze verbinding.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">Instantie-URL zonder slash</td>
                <td>Voer de URL voor uw Adobe Experience Manager-instantie in. Plaats geen schuine streep <code>/</code> aan het einde van de URL.</td>
            </tr>
            <tr>
                <td role="rowheader">Gebruikersnaam</td>
                <td>Voer de gebruikersnaam in voor de AEM Assets-account die door deze verbinding wordt gebruikt.</td>
            </tr>
            <tr>
                <td role="rowheader">Wachtwoord</td>
                <td>Voer het wachtwoord in voor de AEM Assets-account die door deze verbinding wordt gebruikt.</td>
            </tr>
        </tbody>
    </table>


## Adobe Experience Manager Assets-modules en hun velden

Wanneer u Adobe Experience Manager Assets-modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen er aanvullende Adobe Experience Manager Assets-velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Bestandsbewerkingen](#files-operations)
* [Overige](#other)
* [Assets (auteur-API)](#assets-author-api)
* [Gebeurtenissen (auteur-API)](#events-author-api)
* [Metagegevens (auteur-API)](#metadata-author-api)
* [Importeren (auteur-API)](#import-author-api)
* [Relaties (auteur-API)](#relations-author-api)
* [Mappen (API voor mappen)](#folders-folders-api)

### Bestandsbewerkingen

* [Uploaden voltooien](#complete-upload)
* [Vooraf ondertekende opslag ophalen](#get-presigned-storage)
* [Uploaden starten](#initiate-upload)
* [Middelen uploaden](#upload-an-asset)

#### Uploaden voltooien

Deze actiemodule voltooit een upload die is gestart nadat alle delen van het bestand zijn geüpload.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bestandsnaam</td> 
   <td> <p>Voer een naam in voor het geüploade bestand of wijs een naam toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Token uploaden</td> 
   <td>Ga of kaart het uploadteken voor binair getal in, zoals die door de inleiding wordt verstrekt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">MIME-type</td> 
   <td>Voer het MIME-type voor het voltooide bestand in of wijs dit toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Volledige URI</td> 
   <td>Voer de volledige URI voor het bestand in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>


#### Vooraf ondertekende opslag ophalen

In deze actiemodule wordt een tijdelijke vooraf ondertekende URL gemaakt voor het veilig uploaden of downloaden van bestanden van AEM zonder dat directe referenties nodig zijn.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type opzoeken</td> 
   <td> <p>Selecteer of u het element wilt opzoeken op basis van het pad of de id.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element</td> 
   <td>Selecteer het pad naar het element.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>Voer de UDID voor het element in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Uploaden starten

Deze actiemodule start het uploaden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bestemming</td> 
   <td> <p>Selecteer de map waarin u een bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bestandsnaam</td> 
   <td> <p>Een naam voor het geüploade bestand invoeren of toewijzen</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Max. bestandsgrootte</td> 
   <td>Voer de grootte van het geüploade bestand in (in bytes) in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>


#### Middelen uploaden

Deze actiemodule uploadt een middel naar uw Adobe Experience Manager Assets-account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bestemming</td> 
   <td> <p>Selecteer de map waarin u middelen wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source-bestand</td> 
   <td>Voer de naam en gegevens van het bronbestand in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

### Overige


* [Een map of element kopiëren](#copy-a-folder-or-asset)
* [Een record maken](#create-a-record)
* [Een map, element of uitvoering verwijderen](#delete-a-folder-asset-or-rendition)
* [Een mappenlijst ophalen](#get-a-folder-listing)
* [Een aangepaste API-aanroep maken](#make-a-custom-api-call)
* [Een map of element verplaatsen](#move-a-folder-or-asset)
* [Een record bijwerken](#update-a-record)



#### Een map of element kopiëren

Deze actiemodule kopieert een map of middel naar een andere locatie in uw Adobe Experience Manager Assets-account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer of u een map of een element wilt kopiëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Map/element</td> 
   <td>Selecteer of wijs de omslag of de activa toe die u wilt kopiëren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Doelpad</td> 
   <td>Selecteer of wijs het pad toe aan de locatie voor de nieuwe map of het nieuwe element.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Naam van gekopieerde map/element</td> 
   <td>Voer een naam in voor de nieuwe map of het nieuwe middel. De mapnaam die in Adobe Experience Manager Assets wordt weergegeven, is gelijk aan de oorspronkelijke naam. De hier ingevoerde naam wordt weergegeven in de URL van de nieuwe map of het nieuwe middel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Onderliggende objecten kopiëren</td> 
   <td>Als u een map kopieert, schakelt u deze optie in om submappen of elementen in de map te kopiëren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overschrijven</td> 
   <td>Schakel deze optie in om mappen of middelen op de doellocatie te overschrijven die dezelfde naam hebben als de map of het element dat wordt gekopieerd.</td> 
  </tr> 
 </tbody> 
</table>



#### Een record maken

In deze actiemodule wordt een map of elementcommentaar gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Objecttype</td> 
   <td> <p>Selecteer of u een map of een opmerking over een element wilt maken.</p> 
    <ul> 
     <li> <p>Map</p> <p>Vul de volgende velden in:</p> 
      <ul> 
       <li> <p>Naam</p> <p>Voer een naam in voor de map. Deze naam wordt weergegeven in het bestandspad. Spaties of andere tekens worden dus niet opgenomen. </p> </li> 
       <li> <p>Titel</p> <p>Voer een titel voor de map in, die u kunt weergeven in plaats van de naam.</p> </li> 
      </ul> </li> 
     <li> <p>Opmerking element</p> <p>Vul de volgende velden in:</p> 
      <ul> 
       <li> <p>Elementselectie</p> <p>Selecteer of wijs identiteitskaart van de activa toe u een commentaar aan wilt toevoegen.</p> </li> 
       <li> <p>Opmerking</p> <p>Voer de tekst van de opmerking in.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Een map, element of uitvoering verwijderen

Met deze actiemodule verwijdert u een map, element of uitvoering.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer of u een map, element of uitvoering wilt verwijderen.</p> 
    <ul> 
     <li> <p>Map</p> <p>Selecteer de map die u wilt verwijderen door de mappen in het bijbehorende pad te selecteren.</p> </li> 
     <li> <p>Element</p> <p>Selecteer het element door de mappen in het bijbehorende pad te selecteren en vervolgens het element dat u wilt verwijderen.</p> </li> 
     <li> <p>Vertoning</p> <p>Selecteer de vertoning door de mappen in het bijbehorende pad te selecteren.</p> <p>Voer de naam van de vertoning in of wijs deze toe.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Een mappenlijst ophalen

Deze actiemodule wint een vertegenwoordiging van een bestaande omslag en van zijn kindentiteiten (omslagen of activa) terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Map</td> 
   <td>Selecteer of wijs de omslag toe die u wilt terugwinnen. Als u submappen aan het pad wilt toevoegen, klikt u op het plusteken en selecteert u de submap.</td> 
  </tr> 
 </tbody> 
</table>

#### Een aangepaste API-aanroep maken

Deze actiemodule maakt een aangepaste API-aanroep naar de Adobe Experience Manager Assets API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van de basis-URL van de Adobe Experience Manager.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Methode</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kopteksten</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tekenreeks query</td> 
   <td> <p>Voer de queryreeks voor de aanvraag in. Voor Elk zeer belangrijk/paar van de Waarde, klik <b> voeg punt </b> toe en ga de Sleutel en de Waarde in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lichaam</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een map of element verplaatsen

Met deze actiemodule verplaatst u het element of de map op het opgegeven pad naar een nieuwe locatie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer of u een map of element wilt verplaatsen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Map/element</td> 
   <td>Selecteer of wijs de map of middelen toe die u wilt verplaatsen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Doelpad</td> 
   <td>Selecteer of wijs het pad toe aan de locatie waarnaar u de map of het element wilt verplaatsen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Naam van verplaatste map/middel</td> 
   <td>Voer een nieuwe naam in voor de verplaatste map of het verplaatste middel. De mapnaam die in Adobe Experience Manager Assets wordt weergegeven, is gelijk aan de oorspronkelijke naam. De hier ingevoerde naam wordt weergegeven in de URL van de verplaatste map of het verplaatste middel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overschrijven</td> 
   <td>Schakel deze optie in om mappen of middelen op de doellocatie te overschrijven die dezelfde naam hebben als de map of het element dat wordt verplaatst.</td> 
  </tr> 
 </tbody> 
</table>

#### Een record bijwerken

Deze actiemodule werkt een bestaande record bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer of u metagegevens van elementen of een elementuitvoering wilt verwijderen.</p> 
    <ul> 
     <li> <p>Metagegevens van element</p> 
      <ul> 
       <li> <p>Selecteer het element waarvoor u metagegevens wilt bijwerken.</p> </li> 
       <li> <p>Voer de nieuwe titel van het element in.</p> </li> 
      </ul> </li> 
     <li> <p>Elementuitvoering</p> 
      <ul> 
       <li> <p>Selecteer het element waarvoor u de vertoning wilt bijwerken.</p> </li> 
       <li> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Assets (auteur-API)

* [Element verwijderen](#delete-asset)
* [Taakstatus ophalen](#get-job-status)

#### Element verwijderen

Met deze actiemodule verwijdert u één element op basis van de id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element-id</td> 
   <td> <p>Voer de id in van het element dat u wilt verwijderen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kracht</td> 
   <td>Schakel deze optie in om te forceren dat het element wordt verwijderd, zelfs als er naar wordt verwezen.</td> 
  </tr> 
 </tbody> 
</table>

#### Taakstatus ophalen

Deze actiemodule krijgt de huidige status van een asynchrone baan.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Taak-id</td> 
   <td> <p>Voer de id in van de taak waarvoor u de status wilt ophalen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Gebeurtenissen (auteur-API)

#### Gebeurtenissen van Let

Deze triggermodule start een scenario wanneer een gebeurtenis plaatsvindt in AEM Assets.

De module bevat één veld: Webhaak. Selecteer een bestaande webhaak die u voor deze gebeurtenissen wilt gebruiken of maak een nieuwe.

Een nieuwe webhaak maken:

1. Klik **toevoegen** naast het gebied van de Webhaak.
1. Vul de volgende velden in:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">Webhaak-naam</td>
        <td>Voer een naam in voor deze webhaak.</td>
       </tr>
       <tr>
         <td role="rowheader">Verbinding</td>
        <td>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</td>
       </tr>
     </tbody>
   </table>

1. Klik op Opslaan om de webhaak op te slaan en terug te keren naar de module.


### Metagegevens (auteur-API)

* [Metagegevens van middelen ophalen](#get-asset-metadata)
* [Metagegevens van elementen bijwerken](#update-asset-metadata)

#### Metagegevens van middelen ophalen

Deze actiemodule wint meta-gegevens over het gespecificeerde element terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element-id</td> 
   <td> <p>Voer de id in van het element waarvoor u de metagegevens wilt ophalen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Metagegevens van elementen bijwerken

Deze actiemodule werkt metagegevens voor het opgegeven element bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element-id</td> 
   <td> <p>Voer de id in van het element waarvoor u de metagegevens wilt bijwerken of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Updates</td> 
   <td> <p>Voor elk meta-gegevenspunt dat u wilt bijwerken, <b> toevoegen punt </b> en selecteren de verrichting. Andere velden in het vak Item toevoegen zijn afhankelijk van de geselecteerde bewerking.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Importeren (auteur-API)

* [Resultaten van importtaak ophalen](#get-import-job-results)
* [Status van importtaak ophalen](#get-import-job-status)
* [Middelen uploaden via een URL](#upload-an-asset-from-a-url)

#### Resultaten van importtaak ophalen

Deze actiemodule haalt de resultaten voor de opgegeven importtaak op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Taak-id importeren</td> 
   <td> <p>Voer de id in van de taak waarvoor u resultaten wilt ophalen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Status van importtaak ophalen

Deze actiemodule haalt de status van de opgegeven importtaak op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Taak-id importeren</td> 
   <td> <p>Voer de id in van de taak waarvan u de status wilt ophalen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Middelen uploaden via een URL

Deze actiemodule uploadt een nieuw element door bestanden van de opgegeven URL&#39;s te importeren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Titel</td> 
   <td> <p>Voer een titel voor het element in of wijs een titel toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschrijving</td> 
   <td> <p>Voer een beschrijving voor het element in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Onderwerp</td> 
   <td> <p>Voer een onderwerp voor het element in of wijs dit toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maker</td> 
   <td> <p>Voer de maker van het element in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vervaldatum</td> 
   <td> <p>Voer de vervaldatum voor het element in of wijs deze toe.</p><p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aangepaste metagegevens</td> 
   <td> <p>Voor elk punt van douanemetagegevens dat u aan de activa wilt toevoegen, klik <b> toevoegen punt </b> en ga de naam en de waarde van meta-gegevens in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mappad of id</td> 
   <td> <p>Selecteer of u de doelmap wilt opgeven op basis van het pad of de id en selecteer vervolgens het pad of voer de id in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Te importeren bestanden</td> 
   <td> <p>Voor elk dossier dat u wilt invoeren, <b> toevoegen punt &lt;/&gt; en vult de details voor het dossier in. <code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### Relaties (auteur-API)

* [Elementrelaties maken](#create-asset-relations)
* [Elementrelatie verwijderen](#create-asset-relations)
* [Elementrelatietypen ophalen](#get-asset-relation-types)
* [Middelenrelaties ophalen](#get-asset-relations)

#### Elementrelaties maken

Deze actiemodule maakt nieuwe elementrelaties voor het geselecteerde element.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element-id</td> 
   <td> <p>Voer het id-element in of wijs het toe dat u aan andere elementen wilt koppelen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwante activa</td> 
   <td> <p>Voor elk element dat u op het geselecteerde element wilt betrekking hebben, klik <b> toevoegen punt </b> en ga of kaart identiteitskaart van het element en het relatietype in.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Elementrelatie verwijderen

In deze actiemodule wordt een elementrelatie voor een element verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element-id</td> 
   <td> <p>Voer het id-element in of wijs het toe waaruit u een relatie wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwante activa</td> 
   <td> <p>Typ of wijs het type relatie toe dat u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Geef de specifieke id op van het gerelateerde element dat moet worden verwijderd</td> 
   <td> <p>Schakel dit selectievakje in als u een specifieke relatie wilt verwijderen. Als dit vak niet is ingeschakeld, worden alle relaties van het geselecteerde type verwijderd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwant element-id</td> 
   <td> <p>Als u een bepaalde relatie verwijdert, voert u de id in van de relatie die u wilt verwijderen of wijst u deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Elementrelatietypen ophalen

Deze module geeft een overzicht van de elementrelatietypen die voor het opgegeven element bestaan.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element-id</td> 
   <td> <p>Voer het id-element in of wijs het toe waarvoor u relatietypen wilt opgeven.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Middelenrelaties ophalen

Deze module geeft een overzicht van de relaties tussen elementen voor het opgegeven element.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Element-id</td> 
   <td> <p>Voer het id-element in of wijs het toe waarvoor u relaties wilt opgeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Relatietypen</td> 
   <td> <p>Voer een door komma's gescheiden lijst in of wijs een door komma's gescheiden lijst toe van de relatietypen waarvoor u de relaties wilt opgeven.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Mappen (API voor mappen)

* [Mappen maken](#create-folders)
* [Map verwijderen op id](#delete-a-folder-by-id)
* [Mappen per pad verwijderen](#delete-folders-by-path)
* [Taakresultaten voor mappen ophalen](#get-folders-job-results)
* [Taakstatus van mappen ophalen](#get-folders-job-status)
* [Lijstmappen](#list-folders)

#### Mappen maken

Deze actiemodule maakt een nieuwe map in Adobe Experience Manager Assets.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Te maken mappen</td> 
   <td> <p>Voor elke omslag die u wilt tot stand brengen, <b> voeg punt </b> toe en ga de volgende informatie in:</p>
   <ul>
   <li><b>Nieuwe maplocatie</b><p>Selecteer het pad naar de locatie waar u de nieuwe map wilt maken.</p></li>
       <li> <b> Naam </b> <p>Voer een naam in voor de map. Deze naam wordt weergegeven in het bestandspad. Spaties of andere tekens worden dus niet opgenomen. </p> </li> 
       <li> <b> Titel </b> <p>Voer een titel voor de map in, die u kunt weergeven in plaats van de naam.</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Map verwijderen op id

Met deze actiemodule verwijdert u de Adobe Experience Manager Assets-map met de opgegeven id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Map-id</td> 
   <td> Voer de id in van de map die u wilt verwijderen of wijs deze toe.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Submappen verwijderen</td> 
   <td> Schakel deze optie in om de map en alle bijbehorende submappen te verwijderen.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Kracht</td> 
   <td> Schakel deze optie in om de mappen te forceren te verwijderen, zelfs als er naar wordt verwezen.</td>
  </tr> 
 </tbody> 
</table>

#### Mappen per pad verwijderen

Met deze actiemodule verwijdert u de Adobe Experience Manager Assets-mappen op de opgegeven paden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mappaden</td> 
   <td>Voor elke omslag die u wilt schrappen, <b> toevoegen punt </b> en selecteren de weg van de omslag.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Submappen verwijderen</td> 
   <td> Schakel deze optie in om de map en alle bijbehorende submappen te verwijderen.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Kracht</td> 
   <td> Schakel deze optie in om te forceren dat het element wordt verwijderd, zelfs als er naar wordt verwezen.</td>
  </tr> 
 </tbody> 
</table>

#### Taakresultaten voor mappen ophalen

Deze module haalt de resultaten op van een asynchrone baan die door de omslag API van Adobe Experience Manager Assets wordt gecreeerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Taak-id</td> 
   <td> Voer de id in van de taak waarvoor u resultaten wilt ophalen of wijs deze toe.</td>
  </tr> 
 </tbody> 
</table>

#### Taakstatus van mappen ophalen

Deze module haalt de status op van een asynchrone taak die door de Adobe Experience Manager Assets-map-API is gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Taak-id</td> 
   <td> Voer de id in van de taak waarvoor u de status wilt ophalen of wijs deze toe.</td>
  </tr> 
 </tbody> 
</table>


#### Lijstmappen

Deze module maakt een lijst van subfolders van de gespecificeerde omslag.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het verbinden van uw Adobe Experience Manager Assets rekening met Workfront Fusion, zie <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref"> Adobe Experience Manager Assets met Workfront Fusion </a> in dit artikel verbinden.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Mappad of id</td> 
   <td> <p>Selecteer of u de doelmap wilt opgeven op basis van het pad of de id en selecteer vervolgens het pad of voer de id in.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
i! I added a lot of modules to the AEM Assets connector and we need new documentation for them. The connector is available in the QA environment. Heres the added modules and a brief description of them, more info about them can be found in the Assets Author Api docs and the Folders Api docs. Im not fully confident that i kept all the best practices for naming things :sweat_smile:, i hope you can take a look at that as well. Let me know if theres anything i can tell about the modules and thanks again in advance!
Author API
Assets
Delete Asset
Deletes an asset when provided an Asset ID, There is a force parameter that when toggled will delete the folder regardless if it's referenced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get assets job status
Given an assets job ID will return the state that the job is currently in (PROCESSING, COMPLETED, etc.)
Events
AEM Assets events
The costumer can create a web hook in this module and register it in the Adobe admin console
Metadata
Get asset metadata
Given asset ID returns assets metadata.
Update asset metadata
Given asset ID, there are 6 patch operations that can be done with the metadata. The operations are visible in the module as well as the documentation.
Import
Get import job results
Given Job ID returns it's result.
Get import job status
Given Job ID returns its status.
Upload an asset from url
Takes global metadata which applies to all the assets and local ones which apply individually.In both it is also possible to specify custom metadata.
Also takes the folder path or folder ID to place the assets there and url-s of the assets.
Relations
Create asset relation
Given asset ID and a list of related asset ID as well as the relation types creates those relationships.
Delete asset relations
Given asset ID and relation type deletes all relations of that type. Can also specify a related asset to target only that.
 there is a checkbox that is checked by default and when unchecked reveals a field where the user can specify the related user ID.
Get asset relation types
Given asset ID returns all the relation types that the asset has.
Get asset relations
Given asset ID returns all relations. Can also specify a specific type of relation.
Folders API
Create folders
Given a list of folders with their path, name, title, creates them.
Delete a folder by ID
Given Folder ID deletes the folder. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Delete folders by path
Given a list of paths, deletes everything in them. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get folders job results
Given job ID returns its result.
Get folders job status
Given job ID returns its status.
List Folders
List folders under the given folder. In the module you can choose the root folder either by ID or by Path.
-->


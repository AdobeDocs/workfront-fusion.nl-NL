---
title: AWS S3-modules
description: De  [!DNL Adobe Workfront Fusion AWS]  S3 modules laten u verrichtingen op uw S3 emmers uitvoeren.
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1310'
ht-degree: 0%

---

# AWS S3-modules

Met de [!DNL Adobe Workfront Fusion AWS] S3-modules kunt u bewerkingen op uw S3-emmers uitvoeren.

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

Als u [!UICONTROL AWS S3] -modules wilt gebruiken, hebt u een [!DNL Amazon Web Service] -account nodig.

## AWS S3 API-informatie

De AWS S3-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://s3.&lbrace;{{parameters.region}}.amazonaws.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL AWS] met Workfront Fusion {#connect-aws-to-workfront-fusion}

Als u [!DNL AWS S3] wilt verbinden met Workfront Fusion, moet u uw [!DNL AWS] -account aansluiten op Workfront Fusion. Hiervoor moet u eerst een API-gebruiker maken in [!DNL AWS] [!UICONTROL IAM] .

1. Meld u aan bij uw [!DNL AWS] [!UICONTROL IAM] -account.
1. Navigeer naar **[!UICONTROL Identity and Access Management]** > **[!UICONTROL Access Management]** > **[!UICONTROL Users]** .

1. Klik op **[!UICONTROL Add User]**.
1. Voer de naam van de nieuwe gebruiker in en selecteer de optie **[!UICONTROL Programmatic access]** in de sectie [!UICONTROL Access type] .
1. Klik op **[!UICONTROL Attach existing policies directly]** en zoek vervolgens naar **[!UICONTROL AmazonS3FullAccess]** in de zoekbalk. Klik op de knop wanneer deze wordt weergegeven en klik vervolgens op **[!UICONTROL Next]** .

1. Ga door de andere dialoogschermen te werk en klik vervolgens op **[!UICONTROL Create User]** .
1. Kopieer de opgegeven **[!UICONTROL Access key ID]** en **[!UICONTROL Secret access key]** .

1. Ga naar Workfront Fusion en open het dialoogvenster [!DNL AWS S3] van de module **[!UICONTROL Create a connection]** .
1. Voer [!UICONTROL Access key ID] en [!UICONTROL Secret access key] in van stap 7 naar de respectievelijke velden en klik **[!UICONTROL Continue]** om de verbinding tot stand te brengen.

De verbinding is tot stand gebracht. U kunt doorgaan met het instellen van de module.

## [!DNL AWS S3] modules en hun velden

Wanneer u [!DNL AWS S3] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL AWS S3] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Handelingen

* [[!UICONTROL Create Bucket]](#create-bucket)
* [[!UICONTROL Get File]](#get-file)
* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Upload File]](#upload-file)

#### [!UICONTROL Create Bucket]

Deze actiemodule maakt een emmer in AWS.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL AWS] rekening aan Workfront Fusion, zie <a href="#connect-aws-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL AWS] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer de naam van het nieuwe emmertje in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Selecteer uw regionale eindpunt. Voor meer informatie, zie <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints"> regionale eindpunten </a> in de documentatie van AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get File]

Deze actiemodule downloadt een bestand van een emmertje.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL AWS] rekening aan Workfront Fusion, zie <a href="#connect-aws-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL AWS] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Selecteer uw regionale eindpunt. Voor meer informatie, zie <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints"> regionale eindpunten </a> in de [!DNL AWS] documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Selecteer het emmertje waarvan u het bestand wilt downloaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Path]</p> </td> 
   <td> <p>Voer het pad naar het bestand in. Voorbeeld: <code>/photos/2019/February/image023.jpg</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Deze actiemodule maakt een aangepaste aanroep naar de AWS S3 API.

Zie [!DNL Amazon S3] API-introductie [[!DNL Amazon S3] [!UICONTROL REST] voor een gedetailleerde beschrijving van de &#x200B;](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html) API.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL AWS] rekening aan Workfront Fusion, zie <a href="#connect-aws-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL AWS] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Region] </td> 
   <td> <p>Selecteer uw regionale eindpunt. Voor meer informatie, zie <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints"> regionale eindpunten </a> in de [!DNL AWS] documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Voer een host-URL in. Het pad moet relatief zijn ten opzichte van <code> https://s3.&lt;selected-region>.amazonaws.com/</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Selecteer de aanvraagmethode [!UICONTROL HTTP] die u nodig hebt om de API-aanroep te configureren. Zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">[!UICONTROL HTTP] request methods in Adobe Workfront Fusion </a> voor meer informatie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Voeg een aanvraagkoptekst toe. Voor elke kopbal wilt u toevoegen, <b> toevoegen punt </b> en gaan de kopbal in. U kunt de volgende algemene aanvraagheaders gebruiken. Voor meer verzoekkopballen verwijs naar <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3] API Documentatie </a>.</p> <p>Workfront Fusion voegt automatisch machtigingsheaders toe.</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>Naam koptekst</th> 
       <th> <p> Beschrijving</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Length]</p> </td> 
       <td> <p>Lengte van het bericht (zonder de kopballen) volgens RFC 2616. Deze kopbal wordt vereist voor [!UICONTROL PUT] s en verrichtingen die XML, zoals registreren en ACLs laden.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Type]</p> </td> 
       <td> <p>Het inhoudstype van de bron, voor het geval dat de aanvraaginhoud zich in de hoofdtekst bevindt. Voorbeeld: <code>text/plain</code> .</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-MD5]</p> </td> 
       <td> <p>De base64 gecodeerde 128-bits MD5 samenvatting van het bericht (zonder de kopballen) volgens RFC 1864. Deze kopbal kan als controle van de berichtintegriteit worden gebruikt om te verifiëren dat de gegevens de zelfde gegevens zijn die oorspronkelijk werden verzonden. Hoewel dit optioneel is, raden we u aan het [!UICONTROL Content-MD5] -mechanisme te gebruiken als een integriteitscontrole van begin tot eind. Voor meer informatie over [!UICONTROL REST] verzoekauthentificatie, zie <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821"> Ondertekenend en voor authentiek REST verzoeken </a> in de documentatie van AWS.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Date]</p> </td> 
       <td> <p>De huidige datum en tijd volgens de aanvrager. Voorbeeld: <code>Wed, 01 Mar 2006 12:00:00 GMT</code> . Wanneer u de <code>Authorization </code> kopbal specificeert, moet u of <code>x-amz-date</code> of de <code>Date </code> kopbal specificeren.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Expect]</p> </td> 
       <td> <p>Wanneer uw toepassing [!UICONTROL 100-continue] gebruikt, verzendt het niet het verzoeklichaam tot het een erkenning ontvangt. Als het bericht wordt verworpen gebaseerd op de kopballen, wordt het lichaam van het bericht niet verzonden. Deze koptekst kan alleen worden gebruikt als u een hoofdtekst verzendt.</p> <p>Geldige waarden: [!UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
       <td> <p>Voor aanvragen in padstijl is de waarde <code>s3.amazonaws.com</code> . Voor aanvragen in de virtuele stijl is de waarde <code>BucketName.s3.amazonaws.com</code> . Voor meer informatie, zie <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html"> Virtueel Hosting </a> in de documentatie van AWS.</p> <p>Deze header is vereist voor HTTP 1.1 (de meeste toolkits voegen deze header automatisch toe); optioneel voor HTTP/1.0-aanvragen.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>Wanneer het gebruiken van handtekeningsversie 4 om het verzoek voor authentiek te verklaren, verstrekt deze kopbal een knoeiboel van de verzoeklading. Wanneer u een object in blokken uploadt, stelt u de waarde in op <code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code> om aan te geven dat de handtekening alleen op kopteksten van toepassing is en dat er geen lading is. Voor meer informatie, zie <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html"> Berekeningen van de Handtekening voor de Kopbal van de Vergunning </a> in de documentatie van AWS.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-date]</p> </td> 
       <td> <p>De huidige datum en tijd volgens de aanvrager. Voorbeeld: <code>Wed, 01 Mar 2006 12:00:00 GMT</code> . Wanneer u de <code>Authorization </code> kopbal specificeert, moet u of <code>x-amz-date</code> of de <code>Date </code> kopbal specificeren. Als u beide opgeeft, heeft de waarde die voor de <code>x-amz-date</code> -header is opgegeven voorrang.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>Deze kopbal kan in de volgende scenario's worden gebruikt:</p> 
        <ul> 
         <li>Beveiligingstokens opgeven voor [!DNL Amazon DevPay] -bewerkingen. Voor elke aanvraag die [!DNL Amazon DevPay] gebruikt, zijn twee <code>x-amz-security-token</code> -headers vereist: een voor de producttoken en een voor de gebruikerstoken. Wanneer [!DNL Amazon S3] een voor authentiek verklaard verzoek ontvangt, vergelijkt het de gegevens verwerkte handtekening met de verstrekte handtekening. Bij onjuist opgemaakte meerwaardekop voor het berekenen van een handtekening kunnen verificatieproblemen optreden.</li> 
         <li>Geef een beveiligingstoken op wanneer u tijdelijke beveiligingsreferenties gebruikt. Wanneer het maken van verzoeken gebruikend tijdelijke veiligheidsgeloofsbrieven u van IAM verwierf, moet u een veiligheidstoken verstrekken gebruikend deze kopbal. Ga voor meer informatie over tijdelijke beveiligingsreferenties naar Aanvragen indienen.</li> 
        </ul> <p>Deze header is vereist voor aanvragen die [!DNL Amazon DevPay] gebruiken en aanvragen die zijn ondertekend met tijdelijke beveiligingsreferenties.</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Voeg de gewenste querytekenreeksen toe, zoals parameters of formuliervelden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:   <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload File]

Deze actiemodule uploadt een bestand naar een AWS S3-emmertje.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL AWS] rekening aan Workfront Fusion, zie <a href="#connect-aws-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL AWS] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Selecteer uw regionale eindpunt. Voor meer informatie, zie <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints"> regionale eindpunten </a> in de [!DNL AWS] documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Folder] </p> </td> 
   <td> <p>Geef de doelmap op waarnaar u een bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers] (optioneel)</p> </td> 
   <td> <p> Voor elke kopbal wilt u toevoegen, <b> toevoegen punt </b> en ingaan de sleutel en de waarde van de kopbal.</p><p> Voor beschikbare kopballen, zie <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html"> PutObject </a> in de documentatie van AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

* [[!UICONTROL List Files]](#list-files)
* [[!UICONTROL List Folders]](#list-folders)

#### [!UICONTROL List Files]

Retourneert een lijst met bestanden van een opgegeven locatie.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL AWS] rekening aan Workfront Fusion, zie <a href="#connect-aws-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL AWS] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Selecteer uw regionale eindpunt. Voor meer informatie, zie <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints"> regionale eindpunten </a> in de [!DNL AWS] documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Selecteer het emmertje [!DNL Amazon S3] dat u naar bestanden wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix]</p> </td> 
   <td> <p> Voer een pad in naar een map waarin u bestanden wilt zoeken, zoals <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Folders]

Retourneert een lijst met mappen van een opgegeven locatie.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL AWS] rekening aan Workfront Fusion, zie <a href="#connect-aws-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL AWS] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Selecteer uw regionale eindpunt. Voor meer informatie, zie <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints"> regionale eindpunten </a> in de [!DNL AWS] documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Selecteer het emmertje [!DNL Amazon S3] dat u naar mappen wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (optioneel)</p> </td> 
   <td> <p> Pad naar een map om mappen in op te zoeken, zoals <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

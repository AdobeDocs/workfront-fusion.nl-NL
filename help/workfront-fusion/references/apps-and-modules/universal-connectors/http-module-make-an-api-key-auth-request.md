---
title: HTTP > Een aanvraag voor een API-sleutelautorisatie indienen
description: Deze  [!DNL Adobe Workfront Fusion]  actiemodule verzendt een HTTPS- verzoek naar gespecificeerde URL die een zeer belangrijke vergunning van de Auteur van API vereist, en de reactie verwerkt.
author: Becky
feature: Workfront Fusion
exl-id: 362b80b5-42f4-4b82-b06c-39c7c5a1eb1a
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 0%

---

# HTTP > [!UICONTROL Make an API Key Authorization request]

Deze [!DNL Adobe Workfront Fusion] actiemodule verzendt een HTTPS-aanvraag naar een opgegeven URL die een API-sleutelautorisatie vereist, en verwerkt de reactie.

>[!NOTE]
>
>Als u verbinding maakt met een Adobe-product dat momenteel geen speciale aansluiting heeft, raden we u aan de Adobe Authenticator-module te gebruiken.
>
>Voor meer informatie, zie [ module van Adobe Authenticator ](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

## [!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request] moduleconfiguratie

Wanneer u de module [!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request] configureert, geeft [!DNL Adobe Workfront Fusion] de onderstaande velden weer. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Credentials]</td> 
   <td> <p>Selecteer de sleutel die uw API-sleutelverificatiereferenties bevat. Als u een nieuwe sleutel wilt toevoegen, klikt u op <strong>[!UICONTROL Add]</strong> en configureert u de volgende gegevens:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key name]</strong></p> <p>Voer een naam in voor deze set API-referenties.</p> </li> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Voer de API-sleutel in.</p> </li> 
     <li> <p><strong>[!UICONTROL API Key placement]</strong> </p> <p>Selecteer of u de API-sleutel in de koptekst of in de query van de API-aanroep wilt plaatsen.</p> </li> 
     <li> <p><strong>[!UICONTROL API Key parameter name]</strong> </p> <p>Voer de naam in waarmee de API-aanroep de API-sleutel identificeert, zoals "apiKey" of "X-API-sleutel". U vindt deze informatie in de documentatie van de webservice waarmee de module verbinding maakt.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx)] </td> 
   <td> <p>Gebruik deze optie om foutafhandeling in te stellen.</p> <p>Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref"> de behandeling van de Fout </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Voer de URL in waarnaar u een aanvraag wilt verzenden, zoals een API-eindpunt, website, enzovoort.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object. Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Voer de gewenste sleutel-waardeparen voor de query in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>De hoofdtekst van HTTP is de gegevensbytes die in een HTTP- transactiebericht onmiddellijk na de kopballen worden overgebracht als er om het even welk zijn om worden gebruikt.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>Het type Raw-hoofdtekst is over het algemeen geschikt voor de meeste HTTP-hoofdtekstaanvragen, zelfs in situaties waarin in de documentatie van de ontwikkelaar geen gegevens zijn opgegeven die moeten worden verzonden.</p> <p>Geef een vorm voor het parseren van de gegevens op in het veld [!UICONTROL Content type] .</p> <p>Ondanks het geselecteerde inhoudstype, gaat de module gegevens in om het even welk formaat in dat door de ontwikkelaardocumentatie wordt bepaald of wordt vereist.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>Dit hoofdtype bestaat uit [!UICONTROL POST] data using <code>application/x-www-form-urlencoded</code> .</p> <p>Voor <code>[!UICONTROL application/x-www-form-urlencoded]</code> is de hoofdtekst van het HTTP-bericht dat naar de server wordt verzonden, in wezen één queryreeks. De sleutels en waarden worden gecodeerd in sleutel-waardeparen die door <code>&amp;</code> worden gescheiden en met een <code>=</code> tussen de sleutel en de waarde. </p> <p>Gebruik in plaats hiervan <code>[!UICONTROL multipart/form-data]</code> voor binaire gegevens.</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b> Voorbeeld: </b></span></span> 
       <p>Voorbeeld van de resulterende HTTP-aanvraagindeling:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data] is een multipart HTTP-aanvraag die wordt gebruikt om bestanden en gegevens te verzenden. Het wordt doorgaans gebruikt om bestanden naar de server te uploaden.</p> <p>Voeg velden toe die in de aanvraag moeten worden verzonden. Elk veld moet een sleutelwaardepaar bevatten.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>Voer de sleutel en waarde in die binnen de aanvraaginstantie moeten worden verzonden.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Voer de sleutel in en geef het bronbestand op dat u wilt verzenden in de hoofdtekst van de aanvraag.</p> <p>Wijs het dossier toe u van de vorige module (zoals [!UICONTROL HTTP] &gt; [!UICONTROL Get a File] of [!UICONTROL Google Drive] &gt; [!UICONTROL Download a File]) wilt uploaden, of ga de dossier - naam en gegevens manueel in.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Schakel deze optie in om reacties automatisch te parseren en JSON- en XML-reacties om te zetten, zodat u de modules [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON] of [!UICONTROL XML] &gt; [!UICONTROL Parse XML] niet hoeft te gebruiken.</p> <p>Voordat u geparseerde JSON- of XML-inhoud kunt gebruiken, voert u de module één keer handmatig uit, zodat de module de inhoud van de reactie herkent en deze in volgende modules kunt toewijzen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>Geef de time-out van het verzoek op in seconden (1-300). De standaardwaarde is 40 seconden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> Schakel deze optie in om cookies van de server te delen met alle HTTP-modules in uw scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p>Een zelfondertekend certificaat toevoegen:</p>
          <ol>
            <li value="1">
              <p>Klik op <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selecteer het type bestand dat u extraheert.</p>
            </li>
            <li value="3">
              <p>Selecteer het bestand dat het certificaat of certificaat bevat.</p>
            </li>
            <li value="4">
              <p>Voer het wachtwoord voor het bestand in.</p>
            </li>
            <li value="5">
              <p>Klik op <b>[!UICONTROL Save]</b> om het bestand uit te pakken en terug te keren naar de module-instelling.</p>
            </li>
          </ol>
</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>Schakel deze optie in om verbindingen die niet-geverifieerde TLS-certificaten gebruiken, te weigeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> Schakel deze optie in om de URL-omleidingen te volgen met 3xx-reacties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>Schakel deze optie in om de URL-omleidingen te volgen met alle antwoordcodes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>Standaard handelt [!DNL Workfront Fusion] meerdere waarden af voor dezelfde URL-querytekenreeks-parametersleutel als arrays. <code>www.test.com?foo=bar&amp;foo=baz</code> wordt bijvoorbeeld omgezet in <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code> . Activeer deze optie om deze functie uit te schakelen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> Schakel deze optie in om een gecomprimeerde versie van de website aan te vragen.</p> <p>Voegt een <code>[!UICONTROL Accept-Encoding]</code> -header toe om gecomprimeerde inhoud aan te vragen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>Schakel deze optie in om Wederzijdse TLS te gebruiken in de HTTP-aanvraag.</p> <p>Voor meer informatie over Wederzijdse TLS, zie <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref"> Gebruik Wederzijdse TLS in de modules van HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

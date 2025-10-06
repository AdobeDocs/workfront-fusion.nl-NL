---
title: SOAP-module
description: Met de SOAP-module kunt u verbinding maken met SOAP API's in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
source-git-commit: 29f9595d063e89e9cd393fecba07194d2e9008aa
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# [!UICONTROL SOAP] module

Met de module [!UICONTROL SOAP] kunt u verbinding maken met [!UICONTROL SOAP] API&#39;s in [!UICONTROL Adobe Workfront Fusion] .

## SOAP-module en de bijbehorende velden

De SOAP-connector bevat slechts één module, SOAP-actie uitvoeren

### SOAP uitvoeren, actie

Deze actiemodule voert de opgegeven SOAP-handeling uit.



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

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## SOAP-module en de bijbehorende velden

Wanneer u SOAP-modules configureert, geeft Workfront Fusion de onderstaande velden weer.  Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### SOAP uitvoeren, actie

Deze handelingsmodule voert een SOAP-actie uit op basis van WSDL die u opgeeft.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL WSDL]</td> 
   <td> Selecteer WSDL die u de module wilt gebruiken. Om een WSDL tot stand te brengen, <b> voeg </b> naast het gebied toe en vul de gebieden in. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTTP headers]</td> 
   <td> Voor elke kopbal van HTTP die u wilt toevoegen, klik <b> toevoegen punt </b> en ga de naam en de waarde van de kopbal in.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL SOAP headers]</td> 
   <td> Voor elke kopbal van SOAP die u wilt toevoegen, <b> toevoegen punt </b> en ga de naam van de kopbal, waarde, namespace, en XMLNS in.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Force SOAP headers]</td> 
   <td> Schakel deze optie in om kopteksten voor SOAP 1.2 te configureren. </td> 
  </tr> 
  </tbody> 
</table>

## Beperkingen van de module [!UICONTROL SOAP]

>[!NOTE]
>
>Omleidingen zijn uitgeschakeld tijdens het laden van WDSL. Dit is een veiligheidseigenschap, maar kan betekenen dat niet geverifieerde omleidingen worden geblokkeerd wanneer de module in werking wordt gesteld.

De module [!UICONTROL SOAP] is momenteel in bèta en biedt geen ondersteuning voor:

* Elementen opnieuw definiëren
* Beperkingen voor breukcijfers
* Totaal aantal getalbeperkingen
* Beperkingen voor witruimte
* Meerdere onderdelen in invoer- en uitvoerberichten. Er worden slechts enkelvoudige berichten ondersteund
* Aangepast XML-schema-elementen die zijn gedefinieerd met behulp van SOAP Encoding-schema&#39;s en -elementen.

>[!BEGINSHADEBOX]

**Voorbeeld:**

Het volgende wordt niet correct herkend door [!UICONTROL Workfront Fusion] :

```
<complexType name="ArrayOfFloat">
   <complexContent>
      <restriction base="soapenc:Array">
         <attribute ref="soapenc:arrayType"
            wsdl:arrayType="xsd:integer[]"/>
      </restriction>
   </complexContent>
</complexType>
```

Dit voorbeeld bevat de verwijzingen `soapenc:Array` , `soapenc:arrayType` en `wsdl:arrayType` , die nog niet worden ondersteund in [!UICONTROL Workfront Fusion] .

>[!ENDSHADEBOX]

## Workaround

Als de module [!UICONTROL SOAP] weigert het WSDL-bestand te verwerken of verschillende fouten in de configuratie van de module veroorzaakt, kunt u in plaats daarvan de module Universal **[!UICONTROL HTTP]>[!UICONTROL Make a request]** gebruiken:

1. Maak een nieuw scenario in Workfront Fusion.
1. Voeg de module **[!UICONTROL HTTP]>[!UICONTROL Make a request]** in het scenario in.
1. Open de configuratie van de module en vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method]</td> 
      <td> <p>[!UICONTROL POST]</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td role="rowheader">[!UICONTROL Body type]</td> 
      <td> <p>[!UICONTROL Raw]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content type]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Parse response]</td> 
      <td>[!UICONTROL Enabled]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![Workaround](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. Open een nieuw webbrowservenster of tabblad.
1. Plak de URL van WSDL in de adresbalk van de webbrowser en haal het XML-bestand op.

   De WSDL-URL eindigt gewoonlijk met `?wsdl` , maar niet noodzakelijkerwijs met bijvoorbeeld `http://voip.ms/api/v1/server.wsdl` .

1. Als het WSDL-bestand niet rechtstreeks in de webbrowser wordt weergegeven, opent u het gedownloade bestand in een teksteditor.
1. Zoek naar de tag `<service>` of `<wsdl:service>` :

   <!--![Service](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. Kopieer de URL van het kenmerk `location` wanneer u deze hebt gevonden.
1. In de Fusie van Workfront, kleef URL in het de inhoudsgebied van het Verzoek van de module van HTTP **** gebied.
1. Geef waarden op voor de geselecteerde parameters door de vraagtekens te vervangen door werkelijke waarden.

   >[!NOTE]
   >
   > Gebruik een online WSDL-viewer om specifieke waarden uit het WSDL-bestand op te halen.

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Sluit de configuratie van de module door op **[!UICONTROL OK]** te klikken.
1. Voer het scenario of de module uit.

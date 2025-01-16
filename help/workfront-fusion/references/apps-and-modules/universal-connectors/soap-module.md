---
title: SOAP
description: U kunt de SOAP module gebruiken om verbinding te maken met SOAP API's in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# [!UICONTROL SOAP] module

Met de module [!UICONTROL SOAP] kunt u verbinding maken met [!UICONTROL SOAP] API&#39;s in [!UICONTROL Adobe Workfront Fusion] .

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] [!DNL Adobe Workfront] -abonnement hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
* De elementen van het Schema van XML van douane die met hulp van [[!UICONTROL SOAP] worden bepaald Coderend ](https://schemas.xmlsoap.org) schema&#39;s en elementen.

>[!INFO]
>
>**Voorbeeld:**
>  
>Het volgende wordt niet correct herkend door [!UICONTROL Workfront Fusion] :
>
>```
><complexType name="ArrayOfFloat">
>     <complexContent>
>           <restriction base="soapenc:Array">
>                 <attribute ref="soapenc:arrayType"
>                       wsdl:arrayType="xsd:integer[]"/>
>           </restriction>
>     </complexContent>
></complexType>
>```
>
>Dit voorbeeld bevat de verwijzingen `soapenc:Array` , `soapenc:arrayType` en `wsdl:arrayType` , die nog niet worden ondersteund in [!UICONTROL Workfront Fusion] .

## Workaround

Als de module [!UICONTROL SOAP] weigert het WSDL-bestand te verwerken of verschillende fouten in de configuratie van de module veroorzaakt, kunt u in plaats daarvan de module Universal **[!UICONTROL HTTP]>[!UICONTROL Make a request]** gebruiken:

1. Maak in [!DNL Workfront Fusion] een nieuw scenario.
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
      <td> <p>[!UICONTROL Raw]</p> </td> [!UICONTROL ]
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

   <!--![](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. Open een nieuw webbrowservenster of tabblad.
1. Plak de URL van WSDL in de adresbalk van de webbrowser en haal het XML-bestand op.

   De WSDL-URL eindigt gewoonlijk met `?wsdl` , maar niet noodzakelijkerwijs met bijvoorbeeld `http://voip.ms/api/v1/server.wsdl` .

1. Als het WSDL-bestand niet rechtstreeks in de webbrowser wordt weergegeven, opent u het gedownloade bestand in een teksteditor.
1. Zoek naar de tag `<service>` of `<wsdl:service>` :

   <!--![](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. Kopieer de URL van het kenmerk `location` wanneer u deze hebt gevonden.
1. Plak in [!DNL Workfront Fusion] de URL in het veld URL van de module HTTP.
1. Open de [ Online [!UICONTROL SOAP] Cliënt ](https://wsdlbrowser.com/) in een nieuw venster/lusje van Webbrowser.
1. Plak de URL van WSDL in het veld WSDL URL.
1. Klik op **[!UICONTROL Browse]**.
1. Kies bijvoorbeeld uit de lijst met functies naar links `getLanguages` .
1. Kopieer de inhoud van het tekstgebied [!UICONTROL Request XML] .
1. Plak de gekopieerde inhoud in [!UICONTROL Workfront Fusion] in het URL-veld van de module.
1. Geef waarden op voor de geselecteerde parameters door de vraagtekens te vervangen door werkelijke waarden:

   <!--![](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Sluit de configuratie van de module door op **[!UICONTROL OK]** te klikken.
1. Voer het scenario of de module uit.

---
title: JWT-modules
description: De toepassing Adobe Workfront Fusion [!UICONTROL JWT] biedt een module die JWT-tokens maakt op basis van het opgegeven algoritme.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# [!UICONTROL JWT] module

De toepassing Adobe Workfront Fusion [!UICONTROL JWT] biedt een module die JWT-tokens maakt op basis van het opgegeven algoritme.

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
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Informatie over JWT API

De JWT-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
   <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.1.5</td> 
  </tr>
 </tbody> 
 </table>

## JWT-module en de bijbehorende velden

### JWT genereren

Deze module produceert JWT die op het geselecteerde algoritme wordt gebaseerd.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algorithm]</td> 
   <td> <p>Selecteer het algoritme waarmee u de JWT wilt genereren.</p> <ul>
   <li><b> HS256 </b>: HMAC die SHA-256 knoeiboelalgoritme gebruikt</li>
   <li><b> HS384 </b>: HMAC die SHA-384 knoeiboelalgoritme gebruikt</li>
   <li><b> HS512 </b>: HMAC die SHA-512 knoeiboelalgoritme gebruikt</li>
   <li><b> RS256 </b>: RSASSA-PKCS1-v1_5 gebruikend SHA-256 knoeiboelalgoritme</li>
   <li><b> RS384 </b>: RSASSA-PKCS1-v1_5 gebruikend SHA-384 knoeiboelalgoritme</li>
   <li><b> RS512 </b>: RSASSA-PKCS1-v1_5 gebruikend shash algoritme SHA-512</li>
   <li><b> PS256 </b>: RSASSA-PSS gebruikend sha-256 knoeiboelalgoritme (slechts Knoop ^6.12.0 OF &gt;=8.0.0)</li>
   <li><b> PS384 </b>: RSASSA-PSS gebruikend sha-384 knoeiboelalgoritme (slechts Knoop ^6.12.0 OF &gt;=8.0.0)</li>
   <li><b> PS512 </b>: RSASSA-PSS gebruikend sha-512 knoeiboelalgoritme (slechts Knoop ^6.12.0 OF &gt;=8.0.0)</li>
   <li><b> ES256 </b>: ECDSA die kromme P-256 en het hash algoritme SHA-256 gebruiken</li>
   <li><b> ES384 </b>: ECDSA die kromme P-384 en hash algoritme SHA-384 gebruiken</li>
   <li><b> ES512 </b>: ECDSA die kromme P-521 en sha-512 knoeiboelalgoritme gebruiken</li>
   </ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload] </td> 
   <td> <p>Voor elk ladingspunt wilt u toevoegen, <b> toevoegen punt </b> en ingaan de sleutel en de waarde van het punt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Options] </td> 
   <td> <p>Voor elk optie wilt u toevoegen punt, <b> toevoegen punt </b> klikken en de sleutel en de waarde van het punt ingaan.</p> <p>De volgende toetsen zijn beschikbaar:
   <ul>
   <li><b> algoritme </b>: (gebrek: RS256)</li>
   <li><b> validateIn </b>: Uitgedrukt in seconden of een koord beschrijvend een tijdspanwijdte (b.v., 2 dagen, 10h, 7d). Een numerieke waarde wordt geïnterpreteerd als een aantal seconden. Als u een tekenreeks gebruikt, moet u de tijdseenheden (dagen, uren, enz.) opgeven, anders wordt de eenheid voor milliseconden standaard gebruikt (120 is gelijk aan 120 ms).</li>
   <li><b> notBefore </b>: Uitgedrukt in seconden of een koord beschrijvend een tijdspanwijdte (b.v., 2 dagen, 10h, 7d). Een numerieke waarde wordt geïnterpreteerd als een aantal seconden. Als u een tekenreeks gebruikt, moet u de tijdseenheden (dagen, uren, enz.) opgeven, anders wordt de eenheid voor milliseconden standaard gebruikt (120 is gelijk aan 120 ms).
</li>
   <li><b>publiek</b></li>
   <li><b>uitgever</b></li>
   <li><b>jwtid</b></li>
   <li><b>onderwerp</b></li>
   <li><b>noTimestamp</b></li>
   <li><b>header</b></li>
   <li><b>sleutelid</b></li>
   <li><b> muatePayload </b>: Als <code>true</code>, zal de signaalfunctie het ladingsvoorwerp direct wijzigen. Dit is handig als u een ruwe verwijzing naar de lading nodig hebt nadat de eisen op het zijn toegepast maar alvorens het in een teken is gecodeerd.</li>
   <li><b> allowInsecureKeySizes </b>: Als <code>true</code>, privé sleutels met een modulus onder 2048 toestaat om voor RSA worden gebruikt.</li>
   <li><b> allowInvalidAsymmetricKeyTypes </b>: Als <code>true</code>, asymmetrische sleutels toestaat die niet het gespecificeerde algoritme aanpassen. Deze optie is alleen bedoeld voor achterwaartse compatibiliteit en moet worden vermeden.</li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

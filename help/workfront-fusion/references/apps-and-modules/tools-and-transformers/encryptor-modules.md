---
title: Versleuteling
description: Met Adobe Workfront Fusion Encryptor-modules kunt u alle tekstgegevens versleutelen. Ze ondersteunen momenteel berichtversleuteling via AES256 en PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---

# Versleuteling

Met Adobe Workfront Fusion [!UICONTROL Encryptor] -modules kunt u tekstgegevens versleutelen. Zij steunen momenteel berichtencryptie via AES256 en PGP ([!UICONTROL OpenPGP]).

Deze modules vereisen enige vertrouwdheid met encryptieprocessen.

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
   <p>Geen Workfront Fusion-licentievereiste</p>
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

## Berichtversleuteling en -ontsleuteling met PGP

Wanneer het coderen en het decrypteren via PGP, is het noodzakelijk om keychain te gebruiken en een privé of openbare sleutel (of allebei) tot stand te brengen.

Voor meer informatie over openbare en privé sleutels, zie [ Verklarende woordenlijst van de Fusie van Adobe Workfront ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).

Voor meer informatie over sleutels, zie [ Sleutels ](/help/workfront-fusion/references/modules/keys.md).

## [!UICONTROL Encryptor] modules en hun velden

Wanneer u [!UICONTROL Encryptor] modules configureert, worden de volgende velden weergegeven. Een bolde titel in een module wijst op een vereist gebied.

### AES Decrypt (geavanceerd)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Selecteer de sleutel die u de module wilt gebruiken. Om een sleutel tot stand te brengen, <b> voegt </b> toe en gaat de naam van de sleutel, de sleutel, en het coderen type in.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td>Selecteer of u de module 128-bits of 256-bits codering wilt gebruiken.</td>
    </tr>
    <tr>
        <td>Invoercodering</td>
        <td>Selecteer het type invoercodering dat u wilt gebruiken:
        <ul>
        <li>Binair</li>
        <li>Basis 64</li>
        <li>Hexadecimaal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Gegevens</td>
        <td>Voer de gegevens in of wijs deze toe die u wilt decoderen.</td>
    </tr>
    <tr>
        <td>Uitvoercodering</td>
        <td>Selecteer het type uitvoercodering dat u wilt gebruiken:
        <ul>
        <li>ASCII</li>
        <li>Binair</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Cipher-algoritme</td>
        <td>Selecteer het scriptalgoritme dat u wilt gebruiken:
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Vectorcodering initialiseren</td>
        <td>Selecteer de initialisatievectorcodering die u wilt gebruiken:
        <ul>
        <li>UTF-8</li>
        <li>Binair</li>
        <li>Basis 64</li>
        <li>Hexaadecimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codering verificatietag</td>
        <td>Selecteer de codering voor de verificatiemarkering die u wilt gebruiken:
        <ul>
        <li>UTF-8</li>
        <li>Binair</li>
        <li>Basis 64</li>
        <li>Hexaadecimal</li>
        </ul>
        </td>
    </tr>
</table>

### AES-decodering (eenvoudig)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Selecteer de sleutel die u de module wilt gebruiken. Om een sleutel tot stand te brengen, <b> voegt </b> toe en gaat de naam van de sleutel, de sleutel, en het coderen type in.</td>
    </tr>
   <tr>
        <td>Invoercodering</td>
        <td>Selecteer het type invoercodering dat u wilt gebruiken:
        <ul>
        <li>Binair</li>
        <li>Basis 64</li>
        <li>Hexadecimaal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Gegevens</td>
        <td>Voer de gegevens in of wijs deze toe die u wilt decoderen.</td>
    </tr>
    <tr>
        <td>Uitvoercodering</td>
        <td>Selecteer het type uitvoercodering dat u wilt gebruiken:
        <ul>
        <li>ASCII</li>
        <li>Binair</li>
        <li>UTF-8</li>
        </ul>
        </td>
     </tr>
    <tr>
        <td>Geheime sleutel</td>
        <td>Ga of kaart de geheime sleutel in die u wilt gebruiken.</td>
    </tr>
</table>

### AES Encrypt (geavanceerd)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Selecteer de sleutel die u de module wilt gebruiken. Om een sleutel tot stand te brengen, <b> voegt </b> toe en gaat de naam van de sleutel, de sleutel, en het coderen type in.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td>Selecteer of u de module 128-bits of 256-bits codering wilt gebruiken.</td>
    </tr>
    <tr>
        <td>Invoercodering</td>
        <td>Selecteer het type invoercodering dat u wilt gebruiken:
        <ul>
        <li>Binair</li>
        <li>ASCII</li>
        <li>Hexadecimaal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Gegevens</td>
        <td>Voer de gegevens in die u wilt coderen of wijs deze toe.</td>
    </tr>
    <tr>
        <td>Uitvoercodering</td>
        <td>Selecteer het type uitvoercodering dat u wilt gebruiken:
        <ul>
        <li>ASCII</li>
        <li>Binair</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Cipher-algoritme</td>
        <td>Selecteer het scriptalgoritme dat u wilt gebruiken:
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Vectorcodering initialiseren</td>
        <td>Selecteer de codering voor de verificatiemarkering die u wilt gebruiken:
        <ul>
        <li>UTF-8</li>
        <li>Binair</li>
        <li>Basis 64</li>
        <li>Hexaadecimal</li>
        </ul>
        </td>
    </tr>
</table>

### AES-codering (eenvoudig)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Selecteer de sleutel die u de module wilt gebruiken. Om een sleutel tot stand te brengen, <b> voegt </b> toe en gaat de naam van de sleutel, de sleutel, en het coderen type in.</td>
    </tr>
   <tr>
        <td>Invoercodering</td>
        <td>Selecteer het type invoercodering dat u wilt gebruiken:
        <ul>
        <li>Binair</li>
        <li>ASCII</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Gegevens</td>
        <td>Voer de gegevens in die u wilt coderen of wijs deze toe.</td>
    </tr>
    <tr>
        <td>Uitvoercodering</td>
        <td>Selecteer het type uitvoercodering dat u wilt gebruiken:
        <ul>
        <li>Basis 64</li>
        <li>Binair</li>
        <li>Hexadecimaal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Geheime sleutel</td>
        <td>Ga of kaart de geheime sleutel in die u wilt gebruiken.</td>
    </tr>
</table>


### Digitale handtekening maken

Deze module staat u toe om een bericht te decrypteren gebruikend openbare en privé sleutels.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Selecteer de persoonlijke sleutel die u voor deze handtekening wilt gebruiken. Om een privé sleutel toe te voegen, <b> voegt </b> toe en gaat de naam van de sleutel, de zeer belangrijke tekst, en passphrase in.</td>
    </tr>
    <tr>
        <td>Algorithm </td>
        <td>Selecteer of u RSA-SHA1 of RSA-SHA256 wilt gebruiken. </td>
    </tr>
   <tr>
        <td>Invoercodering</td>
        <td>Selecteer het type invoercodering dat u wilt gebruiken:
        <ul>
        <li>ASCII</li>
        <li>Binair</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Uitvoercodering</td>
        <td>Selecteer het type uitvoercodering dat u wilt gebruiken:
        <ul>
        <li>Basis 64</li>
        <li>Hexadecimaal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Gegevens</td>
        <td>Voer de gegevens in of wijs deze toe waaruit u de handtekening wilt maken.</td>
    </tr>
</table>

### Een PGP-bericht decoderen

Deze module staat u toe om een bericht te decrypteren gebruikend openbare en privé sleutels.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Selecteer de persoonlijke sleutel van de ontvanger die u voor dit bericht wilt gebruiken. Om een privé sleutel toe te voegen, <b> voegt </b> toe en gaat de naam van de sleutel, de zeer belangrijke tekst, en passphrase in.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Voer de openbare sleutel van de afzender in. Hierdoor kan de identiteit van de afzender worden geverifieerd.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Wijs het bericht toe dat u wilt decoderen.</td>
    </tr>
</table>

### Een PGP-bericht versleutelen

Met deze module kunt u een bericht versleutelen met openbare en persoonlijke sleutels.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Voer de persoonlijke sleutel van de afzender in. Hierdoor kan de identiteit van de afzender worden geverifieerd.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Voer de openbare sleutel van de ontvanger in.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Voer het bericht in dat u wilt versleutelen.</td>
    </tr>
    </table>

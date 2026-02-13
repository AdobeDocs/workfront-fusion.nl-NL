---
title: Gegevens toewijzen met behulp van aangepaste functies
description: Wanneer u items toewijst, kunt u functies gebruiken om eenvoudige of complexe formules te maken.
author: Becky
feature: Workfront Fusion
source-git-commit: 109ea8a6b3c37918110dc930a19ac85ef3e6d764
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---

# Gegevens toewijzen met behulp van aangepaste functies

U kunt aangepaste functies maken in het gedeelte Functies van Fusion. Vervolgens voegt u deze functies toe aan uw scenario&#39;s in de vorm van een Adobe App Builder-module.

Aangezien aangepaste functies werken via Adobe App Builder, moet uw organisatie over een Adobe App Builder-licentie beschikken om deze te kunnen gebruiken.

Aangepaste functies zijn, net als de meeste scenario-elementen, eigendom van teams.

Workfront Fusion bevat ook ingebouwde functies waarmee u eenvoudige of complexe formules kunt maken. Deze functies hebben betrekking op een groot aantal gebruiksgevallen, waaronder functies voor arrays, tekenreeksen, getallen en gegevens uit vorige modules.

Voor informatie en instructies op ingebouwde functies, zie [&#x200B; een punt in kaart brengen gebruikend ingebouwde functies &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

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
   <p><ul><li>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li><li>U moet een Adobe App Builder-licentie hebben om aangepaste functies te kunnen gebruiken.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Een aangepaste functie configureren

Aangepaste functies worden geconfigureerd in het gebied Functies van Workfront Fusion. Nadat een functie is geconfigureerd, kunt u deze aan een scenario toevoegen met behulp van de Adobe App Builder-connector.

### De runtimeomgeving initialiseren

Voordat u aangepaste functies kunt maken, moet u de runtimeomgeving initialiseren. Dit hoeft alleen te worden gedaan als uw team geen aangepaste functies heeft.

>[!IMPORTANT]
>
>De initialisatie kan slechts worden uitgevoerd een gebruiker met toegang tot Adobe App Builder, of een ontwikkelaar of een systeembeheerder binnen de organisatie IMS.
>
>Nadat de initialisatie is voltooid, kunnen alle gebruikers in het team waar de initialisatie is uitgevoerd functies maken en gebruiken.

1. Klik het **pictogram van Functies** ![&#x200B; &#x200B;](assets/functions-icon.png) lusje van Functies in het linkerpaneel.

   Als u nog niet uw runtime hebt gevormd, ziet u het bericht &quot;Runtime milieu niet gevormd.&quot;
1. Klik **initialiseren runtime**.

   Na enige tijd wordt een lijst Functies weergegeven met twee voorbeeldfuncties.

### Een aangepaste functie maken

Nadat de runtimeomgeving is geconfigureerd, kunt u beginnen met het maken van aangepaste functies.

>[!IMPORTANT]
>
>* Uw douanefunctie **moet** een functie van JavaScript zijn.
>* Uw douanefunctie **moet** een voorwerp terugkeren.
>* Nadat u een aangepaste functie hebt gemaakt, kunt u het volgende niet meer doen:
>
>   * Naam wijzigen
>   * De standaardparameterwaarden weergeven

1. Klik het **pictogram van Functies** ![&#x200B; &#x200B;](assets/functions-icon.png) lusje van Functies in het linkerpaneel.
1. Klik **toevoegen functie**.
1. Voer een naam in voor de aangepaste functie.

   U kunt deze naam later niet wijzigen.
1. Voer de code voor de functie in.
1. Voor elke standaardparameterwaarde wilt u toevoegen, **klikken voegt Parameter** toe en gaat de parameternaam en standaardwaarde in.

   U kunt standaardparameters met voeten treden wanneer het toevoegen van de functie aan een scenario.
1. Klik **sparen**

## Een aangepaste functie toevoegen aan een scenario

Als u een aangepaste functie aan een scenario wilt toevoegen, gebruikt u de Adobe App Builder-connector.

Voor instructies, zie {de module van App Builder van 0} Adobe [.](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md)


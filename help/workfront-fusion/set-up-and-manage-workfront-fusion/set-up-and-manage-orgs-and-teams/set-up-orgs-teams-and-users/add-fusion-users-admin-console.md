---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Gebruikers aan Adobe Workfront Fusion toevoegen via de Adobe Admin Console
description: U kunt een gebruiker toevoegen aan de Adobe Admin Console en deze toewijzen aan Adobe Workfront Fusion, of een bestaande gebruiker in de Adobe Admin Console toewijzen aan Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Gebruikers aan Adobe Workfront Fusion toevoegen via de Adobe Admin Console

U kunt een gebruiker aan [!DNL Adobe Admin Console] toevoegen en hen toewijzen aan Adobe Workfront Fusion, of een bestaande gebruiker in [!DNL Adobe Admin Console] toewijzen aan Workfront Fusion.

Voor een video die de Fusie van Workfront in [!DNL Adobe Admin Console] beschrijft, met inbegrip van hoe te om gebruikers toe te voegen, zie [[!DNL Fusion]  op Adobe IMS ](https://video.tv.adobe.com/v/3412464/){target=_blank}.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configuraties op toegangsniveau</td> 
   <td> 
     <p>U moet een Workfront Fusion-beheerder zijn voor uw organisatie.</p>
     <p>U moet een Workfront Fusion-beheerder zijn voor uw team.</p>
   </td> 
  </tr> 
  </tr>
   <tr> 
   <td role="rowheader">Configuraties op toegangsniveau</td> 
   <td>U moet een beheerder van de Configuratie van het Product van de producten van Adobe voor uw organisatie zijn.</td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Vereisten

Voordat u [!DNL Admin Console] for Workfront gebruikt, ontvangt u een e-mail met de uitnodiging aan de console.

1. Als u [!DNL Adobe] nog niet eerder hebt gebruikt en u een e-mail hebt ontvangen waarin u wordt gemeld dat u nu beheerrechten hebt voor [!DNL Adobe] -software en -services voor uw organisatie, klikt u op de knop in de e-mail om een [!DNL Adobe] -account te maken en opent u [!DNL Admin Console] .

   of

   Als u reeds een rekening van Adobe hebt, ga naar de [[!DNL Adobe Admin Console]  pagina ](https://adminconsole.adobe.com).


## Een nieuwe gebruiker toevoegen aan [!DNL Adobe Admin Console] en Workfront Fusion

1. Van de [[!DNL Adobe Admin Console]  pagina ](https://adminconsole.adobe.com/), selecteer het **[!UICONTROL Products]** lusje in de hoogste navigatiebar, en selecteer dan de **de Fusie van Workfront** producttegel.

   ![ Fusie in Admin Console ](assets/fusion-product-admin-console.png)

1. Selecteer in de lijst die wordt weergegeven de organisatie waaraan u een gebruiker wilt toevoegen.

   ![ instantie van de Fusie in Admin Console ](assets/fusion-instances-admin-console.png)

1. Klik in de lijst die wordt weergegeven met het tabblad **[!UICONTROL Product Profiles]** geselecteerd op de naam van de Workfront Fusion [!UICONTROL Product Profile] -koppeling.

   >[!IMPORTANT]
   >
   > Breng geen wijzigingen aan in de [!UICONTROL Product Profile] zelf.

1. Selecteer de tab **[!UICONTROL Users]** boven de lijst en klik op **[!UICONTROL Add User]** .

1. Voer in het vak **[!UICONTROL Add users to this product profile]** het e-mailadres of de naam in van de gebruiker die u wilt toevoegen en selecteer vervolgens de gebruiker in de lijst die wordt weergegeven.

1. Klik op **[!UICONTROL Save]**.

   De gebruiker wordt gemaakt in Workfront Fusion.

1. (Optioneel) Ga door met [ Toegangsniveau van een gebruiker wijzigen in Workfront Fusion ](#change-a-users-access-level-in-workfront-fusion)

## Het toegangsniveau van een gebruiker wijzigen in Workfront Fusion

* [De rol van een gebruiker wijzigen in Beheerder](#change-a-users-role-to-admin)
* [De rol van een gebruiker wijzigen in Lid, Accountant of App Developer](#change-a-users-role-to-member-accountant-or-app-developer)

### De rol van een gebruiker wijzigen in Beheerder

Het geven van een gebruiker een Admin rol moet in [!DNL Adobe Admin Console] worden gedaan.

1. Selecteer de tab [!UICONTROL Product Profile] op de Workfront Fusion **[!UICONTROL Admins]** -pagina waar u de gebruiker hebt toegevoegd.

1. Klik op **[!UICONTROL Add Admin]**.

1. Voer in het vak **[!UICONTROL Add product profile administrators]** het e-mailadres of de naam in van de gebruiker die u als beheerder wilt instellen en selecteer vervolgens de gebruiker in de lijst die wordt weergegeven.

1. Klik op **[!UICONTROL Save]**.

   De gebruiker is nu Beheerder in Workfront Fusion.

### De rol van een gebruiker wijzigen in Lid, Accountant of App Developer

De rollen Lid, Accountant, en App Developer worden behandeld binnen Workfront Fusion.

Voor instructies, zie [ Mening of geef gebruikersrollen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md) uit.

## Bestaande gebruikers in de [!DNL Adobe Admin Console] toewijzen aan Workfront Fusion

U kunt een bestaande gebruiker aan een team in Fusion toevoegen. Dit wordt afgehandeld in Fusion.

Voor instructies, zie [ een gebruiker aan een team ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md) toevoegen.

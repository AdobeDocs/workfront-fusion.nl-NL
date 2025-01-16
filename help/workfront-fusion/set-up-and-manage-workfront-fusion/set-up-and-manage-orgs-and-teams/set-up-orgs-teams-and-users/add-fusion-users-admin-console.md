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
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# Gebruikers aan Adobe Workfront Fusion toevoegen via de Adobe Admin Console

U kunt een gebruiker aan [!DNL Adobe Admin Console] toevoegen en hen toewijzen aan [!DNL Adobe Workfront Fusion], of een bestaande gebruiker in [!DNL Adobe Admin Console] toewijzen aan [!DNL Workfront Fusion].

Voor video beschrijvend [!DNL Workfront Fusion] in [!DNL Adobe Admin Console], met inbegrip van hoe te om gebruikers toe te voegen, zie [[!DNL Fusion]  op Adobe IMS ](https://video.tv.adobe.com/v/3412464/){target=_blank}.



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
   <p>Huidige productvereiste: als u het abonnement [!UICONTROL Select] of [!UICONTROL Prime] [!DNL Adobe Workfront] hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] beheerdersrechten</td> 
   <td>U moet een [!UICONTROL Product Configuration Administrator] van [!DNL Adobe] producten voor uw organisatie zijn.</td> 
  </tr>
  </tbody> 
</table>

&#42; om te weten te komen welk plan, vergunningstype, of toegang u hebt, contacteer uw [!DNL Workfront] beheerder.

&#42;&#42; voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie</td> 
   <td> <p>Nieuw: [!UICONTROL Standard]</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidig: Geen [!DNL Workfront Fusion] vereiste licentie.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] [!DNL Workfront] -abonnement: uw organisatie moet het abonnement aanschaffen [!DNL Adobe Workfront Fusion] .</li><li>[!UICONTROL Ultimate] [!DNL Workfront] abonnement: [!DNL Workfront Fusion] is opgenomen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet [!DNL Adobe Workfront Fusion] aanschaffen.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configuraties op toegangsniveau*</td> 
   <td> 
     <p>U moet een [!DNL Workfront Fusion] beheerder voor uw organisatie zijn.</p>
     <p>U moet een [!DNL Workfront Fusion] beheerder voor uw team zijn.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++


## Vereisten

Voordat u [!DNL Admin Console] for [!DNL Workfront] gebruikt, ontvangt u een e-mail waarin u wordt uitgenodigd naar de console.

1. Als u [!DNL Adobe] nog niet eerder hebt gebruikt en u een e-mail hebt ontvangen waarin u wordt gemeld dat u nu beheerrechten hebt voor [!DNL Adobe] -software en -services voor uw organisatie, klikt u op de knop in de e-mail om een [!DNL Adobe] -account te maken en opent u [!DNL Admin Console] .

   of

   Als u reeds een rekening van de Adobe hebt, ga naar de [[!DNL Adobe Admin Console]  pagina ](https://adminconsole.adobe.com).


## Een nieuwe gebruiker toevoegen aan de [!DNL Adobe Admin Console] en [!DNL Workfront Fusion]

1. Van de [[!DNL Adobe Admin Console]  pagina ](https://adminconsole.adobe.com/), selecteer het **[!UICONTROL Products]** lusje in de hoogste navigatiebar, en selecteer dan de **[!DNL Workfront Fusion]** producttegel.

   ![ Fusie in Admin Console ](assets/fusion-product-admin-console.png)

1. Selecteer in de lijst die wordt weergegeven de organisatie waaraan u een gebruiker wilt toevoegen.

   ![ instantie van de Fusie in Admin Console ](assets/fusion-instances-admin-console.png)

1. Klik in de lijst die wordt weergegeven met de tab **[!UICONTROL Product Profiles]** geselecteerd op de naam van de koppeling [!DNL Workfront Fusion] [!UICONTROL Product Profile] .

   >[!IMPORTANT]
   >
   > Breng geen wijzigingen aan in de [!UICONTROL Product Profile] zelf.

1. Selecteer de tab **[!UICONTROL Users]** boven de lijst en klik op **[!UICONTROL Add User]** .

1. Voer in het vak **[!UICONTROL Add users to this product profile]** het e-mailadres of de naam in van de gebruiker die u wilt toevoegen en selecteer vervolgens de gebruiker in de lijst die wordt weergegeven.

1. Klik op **[!UICONTROL Save]**.

   De gebruiker wordt gemaakt in [!DNL Workfront Fusion] .

1. (Optioneel) Ga door met [ Wijzig het toegangsniveau van een gebruiker in  [!DNL Workfront Fusion]](#change-a-users-access-level-in-workfront-fusion)

## Het toegangsniveau van een gebruiker wijzigen in Workfront Fusion

* [De rol van een gebruiker wijzigen in Beheerder](#change-a-users-role-to-admin)
* [De rol van een gebruiker wijzigen in Lid, Accountant of App Developer](#change-a-users-role-to-member-accountant-or-app-developer)

### De rol van een gebruiker wijzigen in Beheerder

Het geven van een gebruiker een Admin rol moet in [!DNL Adobe Admin Console] worden gedaan.

1. Selecteer de tab **[!UICONTROL Admins]** op de pagina [!DNL Workfront Fusion] [!UICONTROL Product Profile] waaraan u de gebruiker hebt toegevoegd.

1. Klik op **[!UICONTROL Add Admin]**.

1. Voer in het vak **[!UICONTROL Add product profile administrators]** het e-mailadres of de naam in van de gebruiker die u als beheerder wilt instellen en selecteer vervolgens de gebruiker in de lijst die wordt weergegeven.

1. Klik op **[!UICONTROL Save]**.

   De gebruiker is nu Beheerder in [!DNL Workfront Fusion].

### De rol van een gebruiker wijzigen in Lid, Accountant of App Developer

De rollen Lid, Accountant, en App Developer worden behandeld binnen Workfront Fusion.

Voor instructies, zie [ Mening of geef gebruikersrollen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md) uit.

## Bestaande gebruikers toewijzen in de [!DNL Adobe Admin Console] aan [!DNL Workfront Fusion]

U kunt een bestaande gebruiker aan een team in Fusion toevoegen. Dit wordt afgehandeld in Fusion.

Voor instructies, zie [ een gebruiker aan een team ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md) toevoegen.

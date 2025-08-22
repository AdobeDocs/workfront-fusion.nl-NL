---
title: Vorm IP Adressen voor Fusie in de lijst van gewenste personen van uw organisatie
description: Fusion gebruikt specifieke IP adressen en domeinen voor Webmededeling. Deze moeten aan de lijst van gewenste personen van uw organisatie worden toegevoegd alvorens u Workfront in uw organisatie kunt gebruiken.
author: Becky
feature: Workfront Fusion
exl-id: 406dd45c-0863-4270-a80e-c1c115e0b367
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Vorm IP Adressen voor Fusie in de lijst van gewenste personen van uw organisatie

Omdat Adobe Workfront Fusion communiceert met het netwerk van uw organisatie, moet de firewall van uw organisatie worden gevormd om die mededeling toe te staan. De firewalls zijn hoogst efficiënte veiligheidsmaatregelen die door het netwerk van een organisatie van Internet te scheiden functioneren. Zij zorgen ervoor dat slechts het geselecteerde gegevens en netwerkverkeer zich in of uit het netwerk van de organisatie kan bewegen. De firewall staat of blokkeert gegevens toe die op de plaats worden gebaseerd die de gegevens verzendt of ontvangt. Als beheerder van de Fusie, moet u ervoor zorgen dat de gegevens die naar of van Fusion worden verzonden door de firewall van uw organisatie kunnen overgaan.

Dit wordt verwezenlijkt door een lijst van gewenste personen, die hoofdzakelijk een &quot;lijst&quot;van plaatsen is die &quot;toegestaan&quot;zijn om gegevens door de firewall te verzenden of te ontvangen. De plaatsen kunnen op één van twee manieren worden geïdentificeerd:

* **IP adres**: een reeks aantallen zoals 52.31.132.175
* **Domein**: deel van een URL, zoals `thisdomain` in `www.thisdomain.com`

Fusion gebruikt specifieke IP adressen en domeinen voor Webmededeling. Deze moeten aan de lijst van gewenste personen van uw organisatie worden toegevoegd alvorens u Workfront in uw organisatie kunt gebruiken.

Gewoonlijk, wordt een lijst van gewenste personen gevormd door een netwerkbeheerder. Werk met de netwerkbeheerder van uw organisatie om ervoor te zorgen dat uw firewall deze IP adressen toestaat. Als u niet weet wie uw netwerkbeheerder is, kan de afdeling van IT van uw organisatie u in de juiste richting wijzen.

>[!IMPORTANT]
>
>Als beheerder van de Fusie, moet u ervoor zorgen dat deze IP adressen en domeinen aan de lijst van gewenste personen van uw organisatie worden toegevoegd. Dit geldt ook als u ze niet zelf toevoegt. De fusie kan niet de lijst van gewenste personen van uw organisatie vormen.

U kunt alle Fusion IP adressen en domeinen aan uw lijst van gewenste personen toevoegen, of u kunt van uw cluster de plaats bepalen en slechts de IP adressen en de domeinen voor die cluster toevoegen.

## Alle Fusion IP-adressen en -domeinen toevoegen

Voeg de volgende IP adressen aan uw lijst van gewenste personen toe:

* 52.30.133.50
* 54.220.93.204
* 34.254.76.122
* 54.244.142.219
* 52.39.217.230
* 44.241.82.96
* 100.20.126.137
* 34.223.32.4
* 52.39.176.220
* 20.36.133.48/28
* 20.81.156.240/28
* 172.172.84.48/28

Ook, als uw organisatie uitgaande netwerk het filtreren gebruikt, voeg het volgende domein aan uw lijst van gewenste personen toe om uw systeem toe te laten om tot Workfront Fusion toegang te hebben.

* hook.app.workfrontfusion.com
* hook.app-eu.workfrontfusion.com
* hook.app-az.workfrontfusion.com

## Voeg IP van de Fusie adressen en domeinen voor uw cluster slechts toe

### Identificeer uw datacenter

De IP adressen variëren gebaseerd op waar uw gegevens worden opgeslagen.

Als u via een URL toegang hebt tot Fusion, kunt u de URL onderzoeken om uw datacenter te zoeken.

| URL | Datacenter |
| --- | --- |
| `https://app.workfrontfusion.com` | VS-datacenter |
| `https://app-eu.workfrontfusion.com` | EU-datacenter |
| `https://app-az.workfrontfusion.com` | Azure-cluster |

Als u tot Fusion door `experience.adobe.com` toegang hebt, kunt u het netwerklusje in uw browser controleren om datacenter te identificeren.

| URL | Datacenter |
| --- | --- |
| Oproepen aan `https://fusion.adobe.com` | VS-datacenter |
| Oproepen aan `https://eu.fusion.adobe.com` | EU-datacenter |
| Oproepen aan `https://az.fusion.adobe.com` | Azure-cluster |

### IP-adressen en domeinen toevoegen voor uw datacenter

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront EU Datacenter</td> 
   <td> 
    <ul> 
     <li>52 30 133 50</li> 
     <li>54 220 93 204</li> 
     <li>34 254 76 122</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront US Datacenter</p> </td> 
   <td> 
    <ul> 
     <li>54 244 142 219</li> 
     <li>52 39 217 230</li> 
     <li>44 241 82 96</li>
     <li>10.20.126.137</li>
     <li>34 223 32,4</li>
     <li>52 39 176 220</li>
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion op de Microsoft Azure-cluster</td> 
   <td> 
    <ul> 
     <li>20.36.133.48/28</li> 
     <li>20.81.156.240/28</li> 
     <li>172.172.84.48/28</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Ook, als uw organisatie uitgaande netwerk het filtreren gebruikt, voeg het volgende domein aan uw lijst van gewenste personen toe om uw systeem toe te laten om tot Workfront Fusion toegang te hebben. Deze worden gebruikt voor webhaken

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront EU Datacenter</td> 
   <td> <p> hook.app-eu.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront US Datacenter</p> </td> 
   <td> <p>hook.app.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront Fusion op de Microsoft Azure-cluster</p> </td> 
   <td> <p>hook.app-az.workfrontfusion.com </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het uitgaande netwerk filtreren is ongewoon. Controleer met uw netwerkbeheerder om te zien of moet u uw lijst van gewenste personen bijwerken om voor het aan te passen.

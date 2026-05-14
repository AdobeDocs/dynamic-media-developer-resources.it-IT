---
description: Visualizzare gli indicatori della stampante. Specifica come visualizzare gli indicatori della stampante.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
TQID: 'https://experienceleague.adobe.com/tit-a3stXGj0fZoMgi15lPIk-MtZSvUDOqlcayfNlwk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 24%

---

# printerMark{#printermark}

Visualizzare gli indicatori della stampante. Specifica come visualizzare gli indicatori della stampante.

` printerMark= *`indicatori di taglio`*, *`indicatori di smarginatura`*, *`indicatori di registrazione`*, *`barre di colore`*, *`informazioni pagina`*, *`stile`*, *`spessore riga`*, *`incorporamento livello`*`

I diversi contrassegni possono essere disattivati o attivati. È inoltre possibile controllare lo stile degli indicatori della stampante.

Di seguito sono riportati i valori validi:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= indicatori di taglio </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>indicatori di pagina al vivo= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= marche di registrazione </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= barre colore </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= informazioni pagina </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Predefinito </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Impostazione predefinita </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>spessore riga= </p></td> 
  <td class="stentry"> <p>Qualsiasi valore compreso tra 0,125 e 2,0, compresi entrambi i valori. </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= incorporamento livello </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 1. </p></td> 
 </tr> 
</table>

## Esempio {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`

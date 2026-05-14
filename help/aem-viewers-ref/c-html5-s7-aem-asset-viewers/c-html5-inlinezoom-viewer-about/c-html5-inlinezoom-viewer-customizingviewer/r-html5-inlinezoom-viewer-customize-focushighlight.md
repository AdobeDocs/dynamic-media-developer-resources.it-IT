---
title: Evidenziazione focus
description: L’evidenziazione dello stato attivo dell’input visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore attivo è controllata con il selettore di classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 5849dc2f-d4df-40a2-82c9-454284308a04
TQID: 'https://experienceleague.adobe.com/MPYn1vtOd6HLAgZjKoXL-hm7glJDmAgymdVkmE738lQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 1%

---

# Evidenziazione focus{#focus-highlight}

L’evidenziazione dello stato attivo dell’input visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore attivo è controllata con il selettore di classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS**

L’aspetto viene controllato con il seguente selettore di classe CSS:

```
.s7flyoutviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> struttura </span> </p> </td> 
   <td colname="col2"> <p>Attiva lo stile di evidenziazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disattivare l’evidenziazione predefinita dello stato attivo del browser per tutti gli elementi dell’interfaccia utente del visualizzatore, aggiungi il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7flyoutviewer *:focus { 
 outline: none; 
}
```

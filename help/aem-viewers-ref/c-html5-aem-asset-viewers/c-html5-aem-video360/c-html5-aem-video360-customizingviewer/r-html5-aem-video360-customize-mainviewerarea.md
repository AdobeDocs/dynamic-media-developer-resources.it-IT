---
description: L'area di visualizzazione principale è l'area occupata dal video 360. In genere è impostata per adattarsi allo schermo del dispositivo disponibile quando non sono specificate dimensioni.
seo-description: L'area di visualizzazione principale è l'area occupata dal video 360. In genere è impostata per adattarsi allo schermo del dispositivo disponibile quando non sono specificate dimensioni.
seo-title: Area visualizzatore principale
solution: Experience Manager
title: Area visualizzatore principale
topic: Dynamic media
uuid: ec321901-f077-4f71-a48c-20cae11c41d1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Area visualizzatore principale{#main-viewer-area}

L&#39;area di visualizzazione principale è l&#39;area occupata dal video 360. In genere è impostata per adattarsi allo schermo del dispositivo disponibile quando non sono specificate dimensioni.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

```
.s7video360viewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-ee18025b182a42dc98052de5f133ddfe}

Per impostare un visualizzatore con uno sfondo bianco ( `#FFFFFF`) e impostarne le dimensioni di 512 x 288 pixel.

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```


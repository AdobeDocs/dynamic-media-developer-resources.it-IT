---
title: Visualizzazione pagina
description: La visualizzazione principale è costituita dall'immagine del catalogo. Può essere scorrevole per passare a un’altra pagina o ingrandito.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d3368115-15e7-4d9d-a417-a3c82c9a8a64
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 1%

---

# Visualizzazione pagina{#page-view}

La visualizzazione principale è costituita dall&#39;immagine del catalogo. Può essere scorrevole per passare a un’altra pagina o ingrandito.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato dal seguente selettore di classi CSS:

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della visualizzazione principale in formato esadecimale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursore </span> </p> </td> 
   <td colname="col2"> <p>Cursore visualizzato sopra la vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione principale.

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

Sui sistemi desktop, il componente supporta `cursortype` selettore di attributi che può essere applicato a `.s7pageview` e controlla il tipo di cursore in base allo stato del componente e all&#39;azione dell&#39;utente. I seguenti elementi `cursortype` sono supportati i seguenti valori:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> predefinito </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l'immagine non è ingrandita a causa di una risoluzione di immagine ridotta, impostazioni dei componenti o entrambi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoom </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzato quando è possibile ingrandire l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ripristina </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzata quando l'immagine è al massimo livello di zoom e può essere ripristinata allo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trascinare </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzato quando l’utente effettua una panoramica dell’immagine ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzato quando l’utente esegue uno scambio di immagini facendo un gesto rapido o un gesto rapido orizzontale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il divisore di pagina che separa visivamente le pagine a sinistra e a destra della pagina visualizzata nel catalogo è controllato dal seguente selettore di classe CSS:

`.s7ecatalogviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del divisore di pagina. Imposta su <span class="codeph"> 0 </span> px per nascondere completamente il divisore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine da utilizzare come divisore di pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per avere un divisore di pagina di 40 pixel con immagine semitrasparente.

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Quando `frametransition` il modificatore è impostato su `turn` o `auto` (sui sistemi desktop), l&#39;aspetto del divisore di pagina è controllato dal `pageturnstyle` e `.s7pagedivider` Classe CSS ignorata.

È possibile configurare la visualizzazione dei cursori personalizzati del mouse sull&#39;area del visualizzatore principale. Questa funzionalità è controllata con selettori di attributi aggiuntivi applicati a `.s7ecatalogviewer .s7pageview` Classe CSS:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> predefinito </span> </p> </td> 
   <td colname="col2"> <p> Normalmente viene visualizzata una freccia per un'immagine non ingrandibile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoom </span> </p> </td> 
   <td colname="col2"> <p> Mostra quando è possibile ingrandire un'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ripristina </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando un'immagine è al massimo zoom e può essere reimpostata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trascinare </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando l’utente esegue un’operazione di trascinamento su un’immagine ingrandita </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando l'utente esegue lo scambio di immagini utilizzando il movimento diapositiva </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: utilizzare cursori del mouse diversi per ogni tipo di stato del componente.

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```

---
description: La vista principale è costituita dall’immagine del catalogo. È possibile scorrere per passare a un’altra pagina o ingrandirla.
solution: Experience Manager
title: Vista a pagina
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---

# Vista a pagina{#page-view}

La vista principale è costituita dall’immagine del catalogo. È possibile scorrere per passare a un’altra pagina o ingrandirla.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della vista principale in formato esadecimale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursore  </span> </p> </td> 
   <td colname="col2"> <p>Cursore visualizzato sulla vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : per rendere trasparente la visualizzazione principale.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

Nei sistemi desktop il componente supporta il selettore di attributi `cursortype` che può essere applicato alla classe `.s7pageview` e controlla il tipo di cursore in base allo stato del componente e all’azione dell’utente. Sono supportati i seguenti valori `cursortype`:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l'immagine non è zoomabile a causa di una piccola risoluzione dell'immagine, impostazioni del componente o entrambe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l'immagine può essere ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzata quando l'immagine è al livello di zoom massimo e può essere ripristinata allo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trascinare  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l’utente fa scorrere l’immagine con lo stato di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l’utente esegue uno scambio di immagini facendo scorrere o scorrere in orizzontale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il divisore di pagina che separa visivamente le pagine sinistra e destra dello spread di catalogo è controllato con il seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

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
   <td colname="col2"> <p> Larghezza del divisore di pagina. Impostare su <span class="codeph"> 0 </span> px per nascondere completamente il divisore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine da usare come divisore di pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per avere un divisore di pagina largo 40 pixel con immagine semitrasparente.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Quando il modificatore `frametransition` è impostato su `turn` o `auto` (sui sistemi desktop), l’aspetto del divisore di pagina viene controllato con il modificatore `pageturnstyle` e la classe CSS `.s7pagedivider` viene ignorata.

È possibile configurare la visualizzazione dei cursori del mouse personalizzati sull&#39;area del visualizzatore principale. Questo è controllato con i selettori di attributi aggiuntivi applicati alla classe CSS `.s7ecatalogsearchviewer .s7pageview`:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default  </span> </p> </td> 
   <td colname="col2"> <p> Normalmente viene visualizzata una freccia per un'immagine non zoomabile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina  </span> </p> </td> 
   <td colname="col2"> <p> Mostra quando è possibile ingrandire un’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset  </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando un'immagine è con lo zoom massimo e può essere reimpostata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trascinare  </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando l’utente esegue un’operazione di trascinamento su un’immagine ingrandita </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva  </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando l'utente esegue lo scambio di immagini utilizzando il movimento di diapositiva </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : disporre di cursori del mouse diversi per ogni tipo di stato del componente.

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```

---
description: La vista principale è costituita dall’immagine del catalogo. È possibile passare il dito per passare a un’altra pagina o ingrandirla.
seo-description: La vista principale è costituita dall’immagine del catalogo. È possibile passare il dito per passare a un’altra pagina o ingrandirla.
seo-title: Visualizzazione pagina
solution: Experience Manager
title: Visualizzazione pagina
topic: Dynamic media
uuid: f585bf57-c66a-4213-a2af-d9625beb5bed
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Page view{#page-view}

La vista principale è costituita dall’immagine del catalogo. È possibile passare il dito per passare a un’altra pagina o ingrandirla.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della vista principale in formato esadecimale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursore visualizzato sulla vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la vista principale.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

Sui sistemi desktop il componente supporta il selettore `cursortype` di attributi che può essere applicato alla `.s7pageview` classe e controlla il tipo di cursore in base allo stato del componente e all&#39;azione dell&#39;utente. The following `cursortype` values are supported:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l’immagine non può essere ingrandita a causa di una risoluzione immagine ridotta, impostazioni del componente o entrambe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando è possibile ingrandire l’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Visualizzata quando l’immagine è al livello di zoom massimo e può essere reimpostata allo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> drag </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l’utente esegue il panning dell’immagine con lo stato di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l’utente esegue uno scambio di immagini eseguendo un passaggio del dito o un gesto di scorrimento orizzontale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il separatore di pagina che separa visivamente le pagine sinistra e destra del set di pagine affiancate del catalogo è controllato dal seguente selettore di classe CSS:

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
   <td colname="col2"> <p> Larghezza del separatore di pagina. Impostare su <span class="codeph"> 0 </span> px per nascondere completamente il separatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine da usare come separatore di pagina. </p> </td> 
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
>Quando il `frametransition` modificatore è impostato su `turn` o `auto` (su sistemi desktop), l’aspetto del separatore di pagina viene controllato con il `pageturnstyle` modificatore e la classe `.s7pagedivider` CSS viene ignorata.

È possibile configurare la visualizzazione dei cursori del mouse personalizzati sull&#39;area del visualizzatore principale. Questo è controllato con i selettori di attributi aggiuntivi applicati alla classe `.s7ecatalogsearchviewer .s7pageview` CSS:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p> Normalmente viene visualizzata una freccia per un’immagine non zoomabile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina </span> </p> </td> 
   <td colname="col2"> <p> Mostra quando è possibile ingrandire un’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando un’immagine è con lo zoom massimo e può essere reimpostata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> drag </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando l'utente esegue un'operazione di trascinamento sull'immagine ingrandita </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando l'utente esegue lo scambio di immagini utilizzando un gesto diapositiva </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: con diversi cursori del mouse per ogni tipo di stato del componente.

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


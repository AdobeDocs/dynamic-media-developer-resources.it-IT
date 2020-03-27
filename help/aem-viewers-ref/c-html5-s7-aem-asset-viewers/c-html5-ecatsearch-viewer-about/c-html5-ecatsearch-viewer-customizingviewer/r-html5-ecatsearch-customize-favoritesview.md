---
description: La visualizzazione Preferiti è composta da una colonna di miniature.
seo-description: La visualizzazione Preferiti è composta da una colonna di miniature.
seo-title: Visualizzazione Preferiti
solution: Experience Manager
title: Visualizzazione Preferiti
topic: Dynamic media
uuid: e9d0380e-3b08-45e4-8419-447df2e8de37
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Visualizzazione Preferiti{#favorites-view}

La visualizzazione Preferiti è composta da una colonna di miniature.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

L&#39;aspetto del contenitore di visualizzazione Preferiti è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview
```

La posizione e l&#39;altezza della visualizzazione Preferiti sono gestite dalla vista; in CSS è possibile definire solo la larghezza.

**Proprietà CSS della visualizzazione Preferiti**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della visualizzazione Preferiti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della vista. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una visualizzazione Preferiti larga 100 pixel con uno sfondo grigio semi-trasparente.

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

La spaziatura tra le miniature Preferiti è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**Proprietà CSS delle miniature Preferiti**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> La dimensione del margine verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature è uguale alla somma del margine superiore e inferiore impostato per la cella <span class="codeph"> .s7thumbnail </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una spaziatura di 10 pixel.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

L&#39;aspetto di una singola miniatura è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**Proprietà CSS delle miniature Preferiti**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Bordo della miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumbnail supporta il selettore `state` di attributi, che può essere usato per applicare interfacce diverse a stati di miniature diversi. In particolare, `state="selected"` corrisponde alla miniatura selezionata di recente dall’utente. `state="default"` corrisponde alle altre miniature. E `state="over"` viene usato al passaggio del mouse.

Esempio: per impostare le miniature da 75 x 75 pixel, avete un bordo grigio chiaro predefinito e un bordo grigio scuro selezionato.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

L&#39;aspetto dell&#39;etichetta della miniatura è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**Proprietà CSS dell&#39;etichetta Preferiti**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare etichette con un font Helvetica da 14 pixel.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```


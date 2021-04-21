---
description: La vista Preferiti è costituita da una colonna di miniature.
solution: Experience Manager
title: Vista Preferiti
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# Vista Preferiti{#favorites-view}

La vista Preferiti è costituita da una colonna di miniature.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

L’aspetto del contenitore di visualizzazione Preferiti è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview
```

La posizione e l&#39;altezza della vista Preferiti vengono gestite dalla vista. in CSS è possibile definire solo la larghezza.

**Proprietà CSS della vista Preferiti**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della vista Preferiti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della visualizzazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una visualizzazione Preferiti larga 100 pixel con sfondo grigio semitrasparente.

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
   <td colname="col1"> <p> <span class="codeph"> margine  </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del margine verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature è uguale alla somma del margine superiore e inferiore impostato per <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una spaziatura di 10 pixel.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

L’aspetto della singola miniatura è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**Proprietà CSS delle miniature Preferiti**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo della miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura supporta il selettore di attributi `state` , che può essere utilizzato per applicare skin diversi a diversi stati di miniatura. In particolare, `state="selected"` corrisponde alla miniatura selezionata di recente dall’utente. `state="default"` corrisponde al resto delle miniature. E `state="over"` viene utilizzato al passaggio del mouse.

Esempio : per impostare miniature con 75 x 75 pixel, sono disponibili un bordo grigio chiaro predefinito e un bordo grigio scuro selezionato.

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

L’aspetto dell’etichetta miniatura è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**Proprietà CSS dell’etichetta Preferiti**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del carattere. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare etichette con un carattere Helvetica da 14 pixel.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```


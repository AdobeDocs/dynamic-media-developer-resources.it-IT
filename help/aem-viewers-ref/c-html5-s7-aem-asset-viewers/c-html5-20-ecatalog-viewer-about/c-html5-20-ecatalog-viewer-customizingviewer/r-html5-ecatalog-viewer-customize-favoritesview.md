---
title: Visualizzazione Preferiti
description: La vista Preferiti è costituita da una colonna di miniature.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
TQID: 'https://experienceleague.adobe.com/jOrrq3rLoXwGWAKAcafCkv2twn-N-PE5jbEqQpZI9WQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 295
ht-degree: 0%

---

# Visualizzazione Preferiti{#favorites-view}

La vista Preferiti è costituita da una colonna di miniature.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

L&#39;aspetto del contenitore della visualizzazione Preferiti è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7favoritesview
```

La posizione e l&#39;altezza della vista Preferiti vengono gestite dalla vista; in CSS è possibile definire solo la larghezza.

**Proprietà CSS della visualizzazione Preferiti**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della visualizzazione Preferiti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della vista. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una visualizzazione Preferiti larga 100 pixel con uno sfondo grigio semitrasparente:

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

La spaziatura tra le miniature Preferiti è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**Proprietà CSS delle miniature Preferiti**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del margine verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature è uguale alla somma del margine superiore e inferiore impostato per <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - Per impostare una spaziatura di dieci pixel:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

L’aspetto di una singola miniatura viene controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**Proprietà CSS delle miniature Preferiti**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo della miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura supporta il selettore di attributi `state`, che può essere utilizzato per applicare skin diversi a stati di miniature diversi. In particolare, `state="selected"` corrisponde alla miniatura selezionata di recente dall&#39;utente. L&#39;attributo `state="default"` corrisponde alle altre miniature. L&#39;attributo `state="over"` viene utilizzato al passaggio del mouse.

Esempio: per impostare miniature da 75 x 75 pixel, usare un bordo predefinito grigio chiaro e un bordo selezionato grigio scuro:

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

L’aspetto dell’etichetta delle miniature è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**Proprietà CSS dell&#39;etichetta Preferiti**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Famiglia di caratteri <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - Per impostare etichette con un carattere Helvetica® da 14 pixel:

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

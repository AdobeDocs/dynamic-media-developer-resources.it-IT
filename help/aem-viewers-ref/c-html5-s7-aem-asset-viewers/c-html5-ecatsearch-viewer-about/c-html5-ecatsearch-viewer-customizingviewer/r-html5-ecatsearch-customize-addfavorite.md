---
title: Pulsante Aggiungi preferito
description: La posizione del pulsante Aggiungi preferiti è completamente gestita dal menu Preferiti.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 703b57c0-b764-44c0-a1c1-37f7dd8836f3
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Pulsante Aggiungi preferito{#add-favorite-button}

La posizione del pulsante Aggiungi preferiti è completamente gestita dal menu Preferiti.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L&#39;aspetto del pulsante Aggiungi preferito è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7addfavoritebutton
```

**Proprietà CSS del pulsante Aggiungi preferito**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia i selettori di attributi `state` che `selected`, che possono essere utilizzati per applicare interfacce diverse a stati di pulsante diversi. In particolare, `selected='true'` corrisponde allo stato in cui un utente può aggiungere una nuova icona Preferiti selezionando o toccando. Mentre `selected='false'` corrisponde alla normale modalità operativa in cui un utente può eseguire zoom, scorrimento e scambio di pagine.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: per impostare un pulsante Aggiungi preferito di 28 x 28 pixel e visualizzare un&#39;immagine diversa per ciascuno dei quattro stati del pulsante, se selezionato o non selezionato.

```
.s7ecatalogsearchviewer .s7addfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/AddFavoriteButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/AddFavoriteButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/AddFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/AddFavoriteButton_dark_disabled.png); 
}
```

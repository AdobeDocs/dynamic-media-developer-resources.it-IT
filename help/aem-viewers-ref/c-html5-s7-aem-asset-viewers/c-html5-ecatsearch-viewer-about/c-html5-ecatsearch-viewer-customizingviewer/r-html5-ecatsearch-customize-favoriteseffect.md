---
description: Il visualizzatore visualizza le icone Preferiti nella vista principale, in punti in cui è stato originariamente aggiunto dall’utente.
solution: Experience Manager
title: Effetto Preferiti
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# Effetto Preferiti{#favorites-effect}

Il visualizzatore visualizza le icone Preferiti nella vista principale, in punti in cui è stato originariamente aggiunto dall’utente.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto dell’icona Preferito è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**Proprietà CSS dell’icona Preferito**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per l’icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza dell’icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell’icona. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta un&#39;icona Preferiti da 36 x 36 pixel.

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Nei sistemi desktop, il componente supporta il selettore di attributi `cursortype` che è possibile applicare alla classe `.s7favoriteseffect` e controlla il tipo di cursore in base all&#39;azione utente selezionata. Sono supportati i seguenti valori `cursortype`:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>L'utente visualizzato sta aggiungendo una nuova icona Preferiti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>L'utente visualizzato sta rimuovendo un'icona Preferito esistente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzata in modalità normale quando la modifica dei Preferiti non è attiva. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : disporre di cursori del mouse diversi per ogni tipo di stato del componente.

```
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```


---
title: Effetto Preferiti
description: Il visualizzatore visualizza le icone Preferiti nella vista principale, in punti in cui è stato originariamente aggiunto dall’utente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---

# Effetto Preferiti{#favorites-effect}

Il visualizzatore visualizza le icone Preferiti nella vista principale, in punti in cui è stato originariamente aggiunto dall’utente.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto dell’icona Preferito è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**Proprietà CSS dell’icona Preferito**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per l’icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
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
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Sui sistemi desktop, il componente supporta il `cursortype` selettore di attributi che puoi applicare al `.s7favoriteseffect` e controlla il tipo di cursore in base all&#39;azione utente selezionata. I seguenti `cursortype` sono supportati:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>L'utente visualizzato sta aggiungendo una nuova icona Preferiti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>L'utente visualizzato sta rimuovendo un'icona Preferito esistente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>Visualizzata in modalità normale quando la modifica dei Preferiti non è attiva. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : per disporre di diversi cursori del mouse per ogni tipo di stato del componente.

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```

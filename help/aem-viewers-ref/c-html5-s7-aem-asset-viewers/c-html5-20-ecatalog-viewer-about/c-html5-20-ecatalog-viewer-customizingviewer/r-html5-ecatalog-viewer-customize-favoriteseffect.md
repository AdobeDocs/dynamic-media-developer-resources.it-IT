---
title: Effetto Preferiti
description: Il visualizzatore visualizza le icone Preferiti sopra la vista principale nei punti in cui è stato originariamente aggiunto dal utente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Effetto Preferiti{#favorites-effect}

Il visualizzatore visualizza le icone Preferiti sopra la vista principale nei punti in cui è stato originariamente aggiunto dal utente.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L&#39;aspetto dell&#39;icona Favorite è controllato con il seguente selettore della classe CSS:

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**Proprietà CSS dell&#39;icona Preferiti**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per l'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'icona. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare un&#39;icona Preferiti di 36x36 pixel.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Nei sistemi desktop, il componente supporta l&#39;attributo `cursortype` selettore cui è possibile applicare alla `.s7favoriteseffect` classe e controlla il tipo di cursore in base all&#39;azione utente selezionata. Sono supportati i seguenti `cursortype` valori:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzato utente viene aggiunta una nuova icona Preferiti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzato utente sta rimuovendo un'icona Preferiti esistente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato in modalità operativa normale quando la modifica dei preferiti non è attiva. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per avere cursori del mouse diversi per ogni tipo di stato del componente.

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

---
title: Effetto Preferiti
description: Il visualizzatore visualizza le icone Preferiti sopra la visualizzazione principale nelle posizioni in cui è stata originariamente aggiunta dall'utente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
TQID: 'https://experienceleague.adobe.com/lhaRhTyBr5F6S9erGG76x2rbZuRc4i9kFVtCgWo0xCE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Effetto Preferiti{#favorites-effect}

Il visualizzatore visualizza le icone Preferiti sopra la visualizzazione principale nelle posizioni in cui è stata originariamente aggiunta dall&#39;utente.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto dell’icona Preferiti è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'icona. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare un’icona Preferiti di 36 x 36 pixel.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Nei sistemi desktop il componente supporta il selettore di attributi `cursortype` che è possibile applicare alla classe `.s7favoriteseffect` e controlla il tipo di cursore in base all&#39;azione utente selezionata. Sono supportati i seguenti valori `cursortype`:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>L'utente visualizzato sta aggiungendo una nuova icona Preferiti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> modalità_rimozione </span> </p> </td> 
   <td colname="col2"> <p>L'utente visualizzato sta rimuovendo un'icona Preferiti esistente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> visualizzazione modalità </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato in modalità operativa normale quando la modifica Preferiti non è attiva. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disporre di cursori del mouse diversi per ogni tipo di stato del componente.

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

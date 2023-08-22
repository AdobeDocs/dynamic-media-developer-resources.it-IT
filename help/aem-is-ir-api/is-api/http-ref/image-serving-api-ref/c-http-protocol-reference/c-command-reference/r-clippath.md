---
title: clipPath
description: Tracciato clip livello. Specifica un tracciato di ritaglio per il livello corrente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 1%

---

# clipPath{#clippath}

Tracciato clip livello. Specifica un tracciato di ritaglio per il livello corrente.

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Dati percorso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nome del percorso incorporato nell'immagine sorgente del livello (solo ASCII). </p></td> 
 </tr> 
</table>

Qualsiasi parte del livello che non rientra nell&#39;area definita da `clipPath=` sono resi trasparenti.

`*`pathName`*` è il nome di un tracciato incorporato nell&#39;immagine sorgente del livello. Il percorso viene trasformato automaticamente per mantenere l&#39;allineamento relativo con il contenuto dell&#39;immagine. Se più di uno `*`pathName`*` è specificato, il server ritaglia l&#39;immagine all&#39;intersezione di questi percorsi. Qualsiasi `*`pathName`*` non trovato nell&#39;immagine di origine viene ignorato.

>[!NOTE]
>
>Sono supportate solo le stringhe ASCII per `*`pathName`*`.

`*`pathDefinition`*` consente di specificare dati di tracciato espliciti in coordinate pixel del livello.

Se `size=` è specificato e non 0,0, il livello viene ridimensionato. In questo caso, le coordinate del tracciato sono relative all&#39;angolo superiore sinistro del rettangolo del livello e il livello è posizionato in base a `origin=` o il suo valore predefinito. Qualsiasi area del tracciato all&#39;esterno del rettangolo di livello rimane trasparente.

Se `size=` non è specificato per un colore a tinta unita o per un livello di testo, il livello viene considerato di dimensionamento automatico con l&#39;estensione del percorso che ne determina la dimensione. Se `origin=` non è specificato, il valore predefinito è (0,0) dello spazio delle coordinate del tracciato. Ciò consente di specificare le coordinate del tracciato rispetto all&#39;origine del livello 0.

>[!NOTE]
>
>`scale=`, `rotate=`, e `anchor=` I comandi non sono consentiti per i livelli di colore a tinta unita con ridimensionamento automatico.

`*`pathDefinition`*` accetta una stringa simile al valore della proprietà `d=` attributo del SVG `<path>` , ad eccezione del fatto che vengono utilizzate virgole al posto degli spazi per separare i valori. `*`pathDefinition`*` può includere uno o più percorsi secondari a loop chiuso.

I seguenti comandi di percorso sono supportati in `*`pathDefinition`*`:

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Comando</b> </th> 
   <th class="entry"> <b> Nome</b> </th> 
   <th class="entry"> <b> Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> sposta in assoluto </p> </td> 
   <td> <p> Avvia un nuovo percorso secondario da x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> passa a relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto assoluto </p> </td> 
   <td> <p> Disegnare una linea dalla posizione corrente a x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> assoluto curvato </p> </td> 
   <td> <p> Disegnate una curva di Bezier dalla posizione corrente a x,y. x1,y1 è il punto di controllo all'inizio della curva e x2,y2 è il punto di controllo alla fine della curva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath (Chiudi tracciato) </p> </td> 
   <td> <p> Chiudete il sottotracciato corrente con una linea retta. </p> </td> 
  </tr> 
 </tbody> 
</table>

I comandi in maiuscolo indicano che i valori delle coordinate sono in posizioni pixel assolute (relative all&#39;angolo superiore sinistro del rettangolo del livello). Gli offset pixel seguono i comandi minuscoli relativi alla posizione corrente.

&#39;m&#39; o &#39;M&#39; avvia sempre un nuovo percorso secondario. I sottopercorsi vengono chiusi automaticamente (con una linea retta) se &#39;Z&#39; o &#39;z&#39; non è specificato alla fine.

Se un percorso secondario inizia con un movimento relativo (&quot;m&quot;), è relativo a uno dei seguenti elementi:

* Punto iniziale del percorso secondario precedente, se è stato chiuso con &#39;z&#39; o &#39;Z&#39;.
* Punto finale del percorso secondario precedente, se non è stato chiuso in modo esplicito.
* 0,0, se questo è il primo percorso secondario.

## Proprietà {#section-d4127db0dac54e3cbd44f7ea1e001960}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. I livelli degli effetti lo ignorano.

`clipPathE=` viene ignorato se nell&#39;immagine di origine del livello non viene trovato alcun percorso con il nome specificato o se l&#39;origine del livello non è un&#39;immagine.

## Predefinito {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Nessuno, per non ritagliare ulteriormente il livello.

## Consultate anche {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend= estensione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)

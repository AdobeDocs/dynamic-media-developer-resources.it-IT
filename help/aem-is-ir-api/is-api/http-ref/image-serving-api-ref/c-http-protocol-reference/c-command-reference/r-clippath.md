---
description: Tracciato Clip Livello. Specifica un percorso di clip per il livello corrente.
seo-description: Tracciato Clip Livello. Specifica un percorso di clip per il livello corrente.
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Scene7 Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipPath{#clippath}

Tracciato Clip Livello. Specifica un percorso di clip per il livello corrente.

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathNamepathName`*&#42;[, *``*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> pathDefinition <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>Dati percorso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nome del tracciato incorporato nell’immagine sorgente del livello (solo ASCII). </p></td> 
 </tr> 
</table>

Tutte le parti del livello che non rientrano nell’area definita da `clipPath=` vengono rese trasparenti.

` *`pathName`*` è il nome di un tracciato incorporato nell’immagine sorgente del livello. Il tracciato viene trasformato automaticamente per mantenere l’allineamento relativo con il contenuto dell’immagine. Se si specificano più ` *`pathName`*` , il server ritaglia l&#39;immagine all&#39;intersezione di tali percorsi. Eventuali ` *`pathName`*` non trovati nell&#39;immagine di origine vengono ignorati.

>[!NOTE]
>
>Solo le stringhe ASCII sono supportate per ` *`pathName`*`.

` *`pathDefinition`*` consente di specificare dati di percorso espliciti nelle coordinate pixel del livello.

Se `size=` è specificato e non è 0,0, il livello viene preimpostato. In questo caso, le coordinate del tracciato sono relative all’angolo superiore sinistro del rettangolo del livello e il livello è posizionato in base `origin=` o al suo valore predefinito. Eventuali aree del tracciato all’esterno del rettangolo del livello rimangono trasparenti.

Se non `size=` viene specificato per un colore in tinta unita o un livello di testo, il livello viene considerato ridimensionamento automatico con l’estensione del tracciato che ne determina le dimensioni. Se non `origin=` viene specificato, per impostazione predefinita viene impostato (0,0) dello spazio delle coordinate del percorso. Questo consente di specificare le coordinate del tracciato rispetto all’origine del livello 0.

>[!NOTE]
>
>`scale=`, `rotate=`e `anchor=` comandi non sono consentiti per i livelli di colore tinta unita di ridimensionamento automatico.

` *`pathDefinition`*` accetta una stringa simile al valore dell&#39; `d=` attributo dell&#39; `<path>` elemento SVG, con la differenza che le virgole vengono utilizzate invece degli spazi per separare i valori. ` *`pathDefinition`*` può includere uno o più percorsi secondari a ciclo chiuso.

I seguenti comandi di percorso sono supportati in ` *`pathDefinition`*`:

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
   <td> <p> assoluto di moveto </p> </td> 
   <td> <p> Inizia un nuovo sottopercorso in x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> relativo a moveto </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> assoluto di lineto </p> </td> 
   <td> <p> Disegna una linea dalla posizione corrente a x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>) </td> 
   <td> <p> assoluto di curveto </p> </td> 
   <td> <p> Disegnate una curva Bezier dalla posizione corrente a x,y. x1,y1 è il punto di controllo all'inizio della curva e x2,y2 è il punto di controllo alla fine della curva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath (Chiudi tracciato) </p> </td> 
   <td> <p> Chiude il sottotracciato corrente con una linea retta. </p> </td> 
  </tr> 
 </tbody> 
</table>

I comandi maiuscoli indicano che i valori delle coordinate sono in posizioni in pixel assolute (rispetto all’angolo superiore sinistro del rettangolo del livello). Gli offset dei pixel seguono i comandi minuscoli relativi alla posizione corrente.

&#39;m&#39; o &#39;M&#39; inizia sempre un nuovo sottopercorso. I sottotracciati vengono chiusi automaticamente (con una linea retta) se alla fine non è specificato &#39;Z&#39; o &#39;z&#39;.

Se un sottopercorso inizia con un moveto relativo (&#39;m&#39;), è relativo a uno dei seguenti elementi:

* Punto iniziale del sottopercorso precedente, se chiuso con &#39;z&#39; o &#39;Z&#39;.
* Punto finale del sottopercorso precedente, se non è stato chiuso in modo esplicito.
* 0,0, se si tratta del primo sottopercorso.

## Proprietà {#section-d4127db0dac54e3cbd44f7ea1e001960}

Attributo layer. Si applica al livello corrente o all’immagine composita, se `layer=comp`. I livelli degli effetti li ignorano.

`clipPathE=` viene ignorato se nell’immagine sorgente del livello non viene trovato alcun percorso con il nome specificato o se la sorgente del livello non è un’immagine.

## Predefinito {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Nessuno, per nessun ulteriore ritaglio del livello.

## Consultate anche {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)

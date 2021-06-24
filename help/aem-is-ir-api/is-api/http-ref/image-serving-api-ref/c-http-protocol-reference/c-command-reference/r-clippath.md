---
description: Percorso clip livello. Specifica un percorso di clip per il livello corrente.
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 1%

---

# clipPath{#clippath}

Percorso clip livello. Specifica un percorso di clip per il livello corrente.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Dati del percorso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nome del percorso incorporato nell’immagine sorgente del livello (solo ASCII). </p></td> 
 </tr> 
</table>

Tutte le parti del livello che non rientrano nell&#39;area definita da `clipPath=` vengono rese trasparenti.

`*``*` pathName è il nome di un tracciato incorporato nell&#39;immagine sorgente del livello. Il percorso viene automaticamente trasformato per mantenere l’allineamento relativo con il contenuto dell’immagine. Se sono specificati più `*`pathName`*`, il server ritaglia l&#39;immagine all&#39;intersezione di questi percorsi. Qualsiasi `*`nomePercorso`*` non trovato nell&#39;immagine di origine viene ignorato.

>[!NOTE]
>
>Sono supportate solo le stringhe ASCII per `*`pathName`*`.

`*``*` pathDefinition consente di specificare i dati espliciti del percorso nelle coordinate dei pixel del livello.

Se `size=` è specificato e non 0,0, il livello viene predimensionato. In questo caso, le coordinate del tracciato sono relative all&#39;angolo superiore sinistro del rettangolo di livello e il livello viene posizionato in base a `origin=` o al suo valore predefinito. Tutte le aree del tracciato all&#39;esterno del rettangolo del livello rimangono trasparenti.

Se `size=` non è specificato per un livello di colore o testo a tinta unita, il livello viene considerato auto-dimensionamento con l&#39;estensione del tracciato che ne determina le dimensioni. Se `origin=` non è specificato, viene impostato automaticamente su (0,0) dello spazio di coordinate del percorso. Ciò consente di specificare le coordinate del percorso rispetto all&#39;origine del livello 0.

>[!NOTE]
>
>`scale=`I  `rotate=`comandi ,  `anchor=`  e non sono consentiti per il ridimensionamento automatico dei livelli a colori solidi.

`*``*` pathDefinition accetta una stringa simile al valore dell&#39; `d=` attributo dell&#39; `<path>` elemento SVG, con la differenza che le virgole vengono utilizzate invece degli spazi per separare i valori. `*``*` pathDefinition può includere uno o più percorsi secondari a ciclo chiuso.

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
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> assoluto di moveto </p> </td> 
   <td> <p> Avvia un nuovo percorso secondario in x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
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
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> assoluto </p> </td> 
   <td> <p> Disegna una curva Bezier dalla posizione corrente a x,y. x1,y1 è il punto di controllo all'inizio della curva e x2,y2 è il punto di controllo alla fine della curva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> relativo al diritto di veto </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b>  |  <b>z</b> </td> 
   <td> <p> closepath (Chiudi tracciato) </p> </td> 
   <td> <p> Chiude il sottotracciato corrente con una linea retta. </p> </td> 
  </tr> 
 </tbody> 
</table>

I comandi in maiuscolo indicano che i valori delle coordinate sono in posizioni in pixel assolute (rispetto all&#39;angolo superiore sinistro del rettangolo di livello). Gli offset pixel seguono i comandi minuscoli relativi alla posizione corrente.

&#39;m&#39; o &#39;M&#39; inizia sempre un nuovo sottopercorso. I sottotracciati vengono chiusi automaticamente (con una linea retta) se alla fine non è specificato &quot;Z&quot; o &quot;z&quot;.

Se un sottopercorso inizia con un relativo moveto (&#39;m&#39;), è relativo a uno dei seguenti elementi:

* Punto iniziale del sottopercorso precedente, se chiuso con &#39;z&#39; o &#39;Z&#39;.
* Punto finale del sottopercorso precedente, se non è stato chiuso in modo esplicito.
* 0,0, se si tratta del primo sottopercorso.

## Proprietà {#section-d4127db0dac54e3cbd44f7ea1e001960}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Gli strati degli effetti li ignorano.

`clipPathE=` viene ignorato se nell&#39;immagine sorgente del livello non viene trovato alcun percorso con il nome specificato, o se la sorgente del livello non è un&#39;immagine.

## Predefinito {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Nessuno, per nessun ritaglio aggiuntivo del livello.

## Consultate anche {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)

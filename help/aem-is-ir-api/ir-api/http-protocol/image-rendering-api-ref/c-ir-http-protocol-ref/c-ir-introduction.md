---
description: Questo documento descrive il protocollo HTTP per Scene7 Image Rendering.
seo-description: Questo documento descrive il protocollo HTTP per Scene7 Image Rendering.
seo-title: Introduzione
solution: Experience Manager
title: Introduzione
topic: Scene7 Image Serving - Image Rendering API
uuid: d709f1d2-e7cc-4e9f-b039-aa333e517cbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---


# Introduzione{#introduction}

Questo documento descrive il protocollo HTTP per Scene7 Image Rendering.

Vengono descritti solo gli aspetti del protocollo disponibili al pubblico. Il server può supportare comandi aggiuntivi riservati all&#39;uso da parte del software client Scene7.

**Destinatari**

Questo documento è destinato a programmatori esperti e sviluppatori di siti Web che desiderano utilizzare Scene7 Image Rendering per un sito Web o un&#39;applicazione personalizzata.

Si presume che il lettore abbia familiarità con Scene7 Image Authoring e Image Rendering, con gli standard e le convenzioni generali del protocollo HTTP e con la terminologia di base dell’imaging.

**Convenzioni documento**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>letterale </p> </td> 
  <td class="stentry"> <p>Nelle sezioni di sintassi, il testo non corsivo è letterale; questo non si applica allo spazio vuoto e ai simboli [ ] { } | * </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>Nelle sezioni descrittive, il testo non in corsivo tra virgolette singole è letterale. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parameter  </span> </p> </td> 
  <td class="stentry"> <p>Il corsivo indica una variabile o un parametro da sostituire con un valore effettivo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso 'attribute::' fa riferimento a un attributo di catalogo immagini. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogo::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso 'catalog::' fa riferimento a un campo di dati del catalogo dei materiali. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso 'icc::' fa riferimento a un campo nella mappa del profilo colore ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro:Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso 'macro::' fa riferimento a un campo nella tabella di definizione della macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset:Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso 'ruleset::' si riferisce a un elemento in un set di regole di pre-elaborazione URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> predefinito:Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso 'default::' fa riferimento a un attributo del catalogo immagini predefinito. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignettatura:Item  </span> </td> 
  <td class="stentry"> <p>Un nome con il prefisso "vignettatura::" fa riferimento a un campo nella mappa di vignettatura. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> facoltativo </span> ] </p> </td> 
  <td class="stentry"> <p>Gli elementi di sintassi opzionali sono racchiusi tra parentesi quadre. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> facoltativo </span> ] </p> </td> 
  <td class="stentry"> <p>L'elemento di sintassi opzionale può essere ripetuto una o più volte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> articolo 2  </span> </p> </td> 
  <td class="stentry"> <p>Una barra verticale indica che è possibile utilizzare un singolo elemento di sintassi a sinistra o l'elemento a destra. È necessario selezionare esattamente un elemento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> gruppo </span> } </p> </td> 
  <td class="stentry"> <p>Le parentesi graffe sono utilizzate per raggruppare gli elementi di sintassi. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> gruppo </span> } </p> </td> 
  <td class="stentry"> <p>Gli elementi di sintassi all'interno del gruppo possono essere ripetuti una o più volte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>spazio vuoto </p> </td> 
  <td class="stentry"> <p>Lo spazio vuoto (spazi o schede) non è consentito nelle richieste HTTP. Questo documento utilizza occasionalmente lo spazio vuoto tra gli elementi sintattici solo per motivi di chiarezza. </p> </td> 
 </tr> 
</table>

**Termini comuni**

** *`MSS`* ** Segmento delle specifiche del materiale: un insieme di attributi di materiale tra due comandi di selezione nella richiesta.

** *`vignette`* ** Un&#39;immagine preparata in Scene7 Image Authoring per l&#39;utilizzo con il rendering delle immagini.

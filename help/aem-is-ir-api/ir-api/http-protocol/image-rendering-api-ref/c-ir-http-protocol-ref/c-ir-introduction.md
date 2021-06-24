---
description: Questo documento descrive il protocollo HTTP per il rendering delle immagini di Dynamic Media.
solution: Experience Manager
title: Introduzione
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Introduzione{#introduction}

Questo documento descrive il protocollo HTTP per il rendering delle immagini di Dynamic Media.

Vengono descritti solo gli aspetti del protocollo disponibili al pubblico. Il server può supportare comandi aggiuntivi riservati per l&#39;uso da parte del software client Dynamic Media.

**Pubblico previsto**

Questa documentazione è destinata a programmatori esperti e sviluppatori di siti web che desiderano sfruttare il rendering delle immagini Dynamic Media per un sito web o un&#39;applicazione personalizzata.

Si presume che il lettore abbia familiarità con Dynamic Media Image Authoring e Image Rendering, gli standard e le convenzioni generali del protocollo HTTP e la terminologia di base dell&#39;imaging.

**Convenzioni documento**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>letterale </p> </td> 
  <td class="stentry"> <p>Nelle sezioni di sintassi, il testo non corsivo è letterale; questo non si applica allo spazio vuoto e ai simboli [ ] { } | </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>"letterale" </p> </td> 
  <td class="stentry"> <p>Nelle sezioni descrittive, il testo non corsivo tra virgolette singole è letterale. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parameter  </span> </p> </td> 
  <td class="stentry"> <p>Il corsivo indica una variabile o un parametro da sostituire con un valore effettivo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attributo::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso "attribute::" fa riferimento a un attributo di catalogo di immagini. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogo::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso "catalog:::" fa riferimento a un campo dati del catalogo dei materiali. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso "icc::" fa riferimento a un campo nella mappa del profilo colore ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso "macro::" fa riferimento a un campo nella tabella di definizione della macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso 'ruleset::' fa riferimento a un elemento in un set di regole di pre-elaborazione URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> predefinito::Item  </span> </p> </td> 
  <td class="stentry"> <p>Un nome con il prefisso "default::" fa riferimento a un attributo del catalogo immagini predefinito. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignetta::Item  </span> </td> 
  <td class="stentry"> <p>Un nome con prefisso "vignette::" fa riferimento a un campo nella mappa della vignetta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> facoltativo </span> ] </p> </td> 
  <td class="stentry"> <p>Gli elementi di sintassi facoltativi sono racchiusi tra parentesi quadre. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> facoltativo </span> ] </p> </td> 
  <td class="stentry"> <p>L'elemento di sintassi opzionale può essere ripetuto una o più volte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> punto 2  </span> </p> </td> 
  <td class="stentry"> <p>Una barra verticale indica che è possibile utilizzare il singolo elemento di sintassi a sinistra o l'elemento a destra. È necessario selezionare esattamente un elemento. </p> </td> 
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
  <td class="stentry"> <p>Lo spazio vuoto (spazi o schede) non è consentito nelle richieste HTTP. Questo documento utilizza occasionalmente lo spazio vuoto tra gli elementi sintattici solo per chiarezza. </p> </td> 
 </tr> 
</table>

**Termini comuni**

** *`MSS`* ** Segmento di specifica del materiale: un insieme di attributi di materiale tra due comandi di selezione nella richiesta.

** *`vignette`* ** Un’immagine preparata in Dynamic Media Image Authoring per l’utilizzo con Image Rendering.

---
description: Questo documento descrive il catalogo dei materiali per Dynamic Medie Image Rendering.
solution: Experience Manager
title: Introduzione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1cdb9c45-329d-44df-92c3-8cba5b2b1339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Introduzione{#introduction}

Questo documento descrive il catalogo dei materiali per Dynamic Medie Image Rendering.

**Pubblico previsto**

Questo documento è destinato a programmatori esperti e sviluppatori di siti web che desiderano sfruttare il Rendering di immagini Dynamic Medie per un sito web o un’applicazione personalizzata.

Si presume che il lettore abbia familiarità con Dynamic Medie Image Authoring e Image Rendering, gli standard e le convenzioni generali del protocollo HTTP e la terminologia di base dell’imaging.

**Convenzioni documento**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Letterale </p> </td> 
  <td class="stentry"> <p>Nelle sezioni di sintassi, il testo non corsivo è letterale e non si applica allo spazio vuoto e ai simboli [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'letterale' </p> </td> 
  <td class="stentry"> <p>Nelle sezioni descrittive, il testo non corsivo tra virgolette singole è letterale. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parametro </span> </p> </td> 
  <td class="stentry"> <p>Il corsivo indica una variabile o un parametro da sostituire con un valore effettivo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> Attributo <span class="codeph">::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso "attribute::" fa riferimento a un attributo del catalogo delle immagini. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> Catalogo <span class="codeph">::Elemento </span> </td> 
  <td class="stentry"> <p>Un nome con prefisso "catalog::" fa riferimento a un campo dati di catalogo materiali. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso "icc::" fa riferimento a un campo nella mappa del profilo colore ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso "macro::" fa riferimento a un campo nella tabella di definizione della macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> set di regole::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso "ruleset::" fa riferimento a un elemento in un set di regole di pre-elaborazione URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> predefinito::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso "default::" fa riferimento a un attributo del catalogo immagini predefinito. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vignettatura::Elemento </span> </p> </td> 
  <td class="stentry"> <p>Un nome con prefisso "vignettatura::" fa riferimento a un campo nella mappa vignettatura. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> facoltativo </span> ] </p> </td> 
  <td class="stentry"> <p>Gli elementi di sintassi facoltativi sono racchiusi tra parentesi quadre. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> facoltativo </span> ] </p> </td> 
  <td class="stentry"> <p>L’elemento di sintassi facoltativo può essere ripetuto una o più volte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> elemento1 </span>| <span class="varname"> elemento2 </span> </p> </td> 
  <td class="stentry"> <p>Una barra verticale indica che è possibile utilizzare l'elemento con sintassi singola a sinistra o l'elemento a destra. Selezionare un solo elemento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> gruppo </span> } </p> </td> 
  <td class="stentry"> <p>Le parentesi graffe vengono utilizzate per raggruppare gli elementi di sintassi. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> gruppo </span> } </p> </td> 
  <td class="stentry"> <p>Gli elementi di sintassi all’interno del gruppo possono essere ripetuti una o più volte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Spazio vuoto. </p> </td> 
  <td class="stentry"> <p>Nelle richieste HTTP non sono consentiti spazi vuoti (spazi o tabulazioni). Questo documento utilizza occasionalmente uno spazio vuoto tra gli elementi sintattici solo a scopo di chiarezza. </p> </td> 
 </tr> 
</table>

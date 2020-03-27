---
description: Le funzioni e la sintassi dei cataloghi di immagini sono descritte in questa sezione.
seo-description: Le funzioni e la sintassi dei cataloghi di immagini sono descritte in questa sezione.
seo-title: Cataloghi delle immagini
solution: Experience Manager
title: Cataloghi delle immagini
topic: Scene7 Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Cataloghi delle immagini{#image-catalogs}

Le funzioni e la sintassi dei cataloghi di immagini sono descritte in questa sezione.

I cataloghi di immagini offrono le seguenti funzionalità:

* Consenti associazione permanente di immagini con alcuni metadati e comandi di modificatore.

   Alle voci nei cataloghi delle immagini viene fatto riferimento tramite una notazione rapida ` *`rootId/objId`*`, dove ` *`rootId`*` identifica il catalogo immagini e ` *`objId`*` identifica un record di dati nel catalogo.
* Specificate le impostazioni predefinite per alcuni attributi di richiesta, ad esempio la qualità JPEG o se applicare una filigrana.
* Gestione di font, profili ICC, definizioni di macro e modelli di richiesta

Anche se non sono definiti cataloghi di immagini specifici, tutte le funzioni dei cataloghi di immagini sono disponibili tramite il catalogo predefinito ( [!DNL default.ini]).

Se ` *`rootId`*` nel percorso URL della richiesta corrisponde a un catalogo `attribute::RootId` di immagini specifico, tale catalogo diventerà il catalogo principale per la richiesta. Il catalogo principale fornisce gli attributi e le impostazioni predefiniti per l’intera richiesta. Se non viene trovata alcuna corrispondenza, viene utilizzato il catalogo predefinito.

Un catalogo identificato in un `src=` comando o in un `mask=` comando fornisce i seguenti attributi e dati del catalogo al livello corrente:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attributo/Dati</b> </th> 
   <th class="entry"> <b> Note</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> l’estensione predefinita per tutti i percorsi dei file immagine nel livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::Scadenza</span> </p> </td> 
   <td> <p> predefinito per <span class="codeph"> catalogo::Scadenza</span> o scadenza del livello corrente se non è coinvolto alcun record catalogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> il profilo colore ICC di lavoro, l’intento di rendering e il flag di compensazione del punto nero per la richiesta e/o il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::RootPath</span> </p> </td> 
   <td> <p> utilizzato per tutti i percorsi di file sorgente del livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute:Resolution</span> </p> </td> 
   <td> <p> predefinito per <span class="codeph"> catalogo::Solo risoluzione</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::Ancoraggio</span> </p> </td> 
   <td> <p> predefinito per il valore <span class="codeph"> anchor=</span> del livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::Scadenza</span> </p> </td> 
   <td> <p> il valore di scadenza più piccolo di tutti i livelli viene utilizzato come valore time-to-live dell’immagine di risposta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::IccProfile</span> </p> </td> 
   <td> <p> profilo colore immagine sorgente per il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo:Mappa</span> </p> </td> 
   <td> <p> i dati della mappa immagine per il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::MaskPath</span> </p> </td> 
   <td> <p> impostazione predefinita per <span class="codeph"> mask=</span> per il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo:Modificatore</span> </p> </td> 
   <td> <p> i comandi di prefisso per il livello corrente (ogni comando nel <span class="codeph"> catalogo::Modificatore</span> può essere sostituito dallo stesso comando nell’URL, se specificato per lo stesso livello) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo:Percorso</span> </p> </td> 
   <td> <p> il file immagine sorgente per il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::PostModifier</span> </p> </td> 
   <td> <p> i comandi postfix per il livello corrente (simili a <span class="codeph"> catalog::Modifier</span>, ma <span class="codeph"> catalogo::PostModifier</span> ignorano gli stessi comandi specificati nell’URL o nel <span class="codeph"> catalogo::Modificatore</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo:Risoluzione</span> </p> </td> 
   <td> <p> la risoluzione oggetto del livello corrente </p> </td> 
  </tr> 
 </tbody> 
</table>

All’interno dello stesso livello, `src=` e `mask=` deve fare riferimento allo stesso catalogo immagini (se presente).

Un catalogo identificato in un `icc=` comando viene utilizzato solo per cercare una voce dalla tabella del profilo ICC del catalogo. Non sono coinvolti altri attributi o dati del catalogo.

Se ` *`rootId`*` viene risolto in un catalogo e ` *`objId`*` viene confrontato con un `catalog::Id` in questo catalogo, ` *`rootId/objId`*` viene effettivamente sostituito dalla voce del catalogo in modo simile al seguente:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Consultate anche {#section-00e4f6b39cd14244bcce537a3f831259}

[Riferimento](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)catalogo immagini, [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)

---
description: Le funzioni e la sintassi dei cataloghi di immagini sono descritte in questa sezione.
solution: Experience Manager
title: Cataloghi immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Cataloghi immagini{#image-catalogs}

Le funzioni e la sintassi dei cataloghi di immagini sono descritte in questa sezione.

I cataloghi di immagini offrono le seguenti funzionalità:

* Consenti associazione permanente di immagini con determinati metadati e comandi modificatori.

  Le voci nei cataloghi di immagini sono referenziate utilizzando una notazione di scelta rapida `*`rootId/objId`*`, dove `*`rootId`*` identifica il catalogo immagini e `*`objId`*` identifica un record di dati nel catalogo.
* Specifica le impostazioni predefinite per alcuni attributi di richiesta, ad esempio la qualità JPEG o se deve essere applicata una filigrana.
* Gestione di font, profili ICC, definizioni di macro e modelli di richiesta

Anche se non sono definiti cataloghi di immagini specifici, tutte le funzioni dei cataloghi di immagini sono disponibili tramite il catalogo predefinito ( [!DNL default.ini]).

Se `*`rootId`*` nelle corrispondenze del percorso URL della richiesta `attribute::RootId` di un catalogo immagini specifico, tale catalogo diventa il catalogo principale per questa richiesta. Il catalogo principale fornisce gli attributi e le impostazioni predefiniti per l’intera richiesta. Se non viene trovata alcuna corrispondenza, viene utilizzato il catalogo predefinito.

Un catalogo identificato in un `src=` o `mask=` Il comando fornisce i seguenti attributi e dati di catalogo al livello corrente:

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
   <td> <p> l'estensione predefinita per tutti i percorsi dei file di immagine nel livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Scadenza</span> </p> </td> 
   <td> <p> impostazione predefinita per <span class="codeph"> catalogo::scadenza</span> o scadenza del livello corrente se non è coinvolto alcun record catalogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> il profilo colore ICC, l'intento di rendering e il flag di compensazione del punto nero per la richiesta e/o il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> utilizzato per tutti i percorsi dei file di origine del livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Risoluzione</span> </p> </td> 
   <td> <p> impostazione predefinita per <span class="codeph"> catalogo::Risoluzione</span> solo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::ancoraggio</span> </p> </td> 
   <td> <p> impostazione predefinita per <span class="codeph"> ancoraggio=</span> valore del livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::scadenza</span> </p> </td> 
   <td> <p> il valore di scadenza più piccolo di tutti i livelli viene utilizzato come valore time-to-live dell’immagine di risposta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::IccProfile</span> </p> </td> 
   <td> <p> profilo colore immagine sorgente per il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::Mappa</span> </p> </td> 
   <td> <p> dati mappa immagine per il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> impostazione predefinita per <span class="codeph"> mask= maschera</span> per il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::Modificatore</span> </p> </td> 
   <td> <p> comandi di prefisso per il livello corrente (ogni comando in <span class="codeph"> catalogo::Modificatore</span> può essere sostituito dallo stesso comando nell’URL, se specificato per lo stesso livello) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> file di immagine di origine per il livello corrente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::PostModifier</span> </p> </td> 
   <td> <p> comandi di suffisso per il livello corrente (simili a <span class="codeph"> catalogo::Modificatore</span>, ma comandi in <span class="codeph"> catalogo::PostModifier</span> ignora gli stessi comandi specificati nell’URL o in <span class="codeph"> catalogo::Modificatore</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::Risoluzione</span> </p> </td> 
   <td> <p> risoluzione oggetto del livello corrente </p> </td> 
  </tr> 
 </tbody> 
</table>

All&#39;interno dello stesso livello `src=` e `mask=` deve fare riferimento allo stesso catalogo immagini (se presente).

Un catalogo identificato in un `icc=` viene utilizzato solo per cercare una voce dalla tabella dei profili ICC del catalogo. Non sono coinvolti altri attributi o dati di catalogo.

Se, `*`rootId`*` viene risolto in un catalogo e `*`objId`*` corrisponde a `catalog::Id` in questo catalogo, quindi `*`rootId/objId`*` viene effettivamente sostituito dalla voce di catalogo in un modo simile al seguente:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Consultate anche {#section-00e4f6b39cd14244bcce537a3f831259}

[Riferimento catalogo immagini](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask= maschera](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [ancoraggio=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)

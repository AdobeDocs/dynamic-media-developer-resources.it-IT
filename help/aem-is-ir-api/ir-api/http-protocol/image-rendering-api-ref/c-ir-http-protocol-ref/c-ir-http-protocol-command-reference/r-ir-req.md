---
title: req
description: Tipo di richiesta. Specifica il tipo di dati richiesti.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 3%

---

# req{#req}

Tipo di richiesta. Specifica il tipo di dati richiesti.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> debug </span> </p> </td> 
  <td class="stentry"> <p>Esegui comandi in modalità debug. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> contenuto </span> </p> </td> 
  <td class="stentry"> <p>Restituire informazioni sugli oggetti nella vignettatura. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Esegui i comandi e restituisce l’immagine di cui è stato eseguito il rendering. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> proprietà immagine </span> </p> </td> 
  <td class="stentry"> <p>Restituisce le proprietà della vignettatura specificata. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> mappa </span> </p> </td> 
  <td class="stentry"> <p>Restituisce i dati della mappa immagine incorporati nella vignettatura. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> oggetto </span> </p> </td> 
  <td class="stentry"> <p>Esegui i comandi e restituisce l'immagine di cui è stato eseguito il rendering mascherata alla selezione dell'oggetto corrente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> proprietà </span> </p> </td> 
  <td class="stentry"> <p>Esegui i comandi e restituisce le proprietà dell'immagine di risposta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> dati utente </span> </p> </td> 
  <td class="stentry"> <p>Restituisce il contenuto di <span class="codeph"> vignettatura::UserData </span>. </p> </td> 
 </tr> 
</table>

Se non diversamente indicato nelle descrizioni dettagliate, il server restituisce risposte di testo con tipo MIME &lt;text/plain>.

`debug`

Esegue i comandi specificati e restituisce l&#39;immagine di cui è stato eseguito il rendering. Se si verifica un errore, vengono restituite informazioni di debug e di errore anziché l&#39;immagine di errore ( `attribute::ErrorImagePath`).

`contents`

Restituisce una rappresentazione XML della gerarchia degli oggetti nella vignettatura, inclusi gli attributi degli oggetti selezionati. Altri comandi nella richiesta vengono ignorati.

`img`

Esegue i comandi specificati e restituisce l&#39;immagine di cui è stato eseguito il rendering. Il formato dei dati di risposta e il tipo di risposta sono determinati da `fmt=`.

`imageprops`

Restituisce le proprietà selezionate del file di vignettatura o della voce di catalogo specificata nel percorso URL. Per una descrizione della sintassi di risposta e del tipo MIME di risposta, vedere [Proprietà](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a). Altri comandi nella richiesta vengono ignorati. Vengono restituite le seguenti proprietà:

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Proprietà </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine.scadenza </span> </p> </td> 
   <td colname="col2"> <p>Doppio </p> </td> 
   <td colname="col3"> <p> Attributo <span class="codeph">::scadenza </span> o durata predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Intero </p> </td> 
   <td colname="col3"> <p>Altezza massima risoluzione in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>Stringa </p> </td> 
   <td colname="col3"> <p>nome/descrizione del profilo associato a questa vignettatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>Booleano </p> </td> 
   <td colname="col3"> <p>1 se il profilo associato è incorporato nella vignetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine.PhotoshopPaths incorporati </span> </p> </td> 
   <td colname="col2"> <p>Booleano </p> </td> 
   <td colname="col3"> <p>1 se la vignettatura incorpora i dati del percorso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine.modificatore </span> </p> </td> 
   <td colname="col2"> <p>Stringa </p> </td> 
   <td colname="col3"> <p> Attributo <span class="codeph">::Modificatore </span> o vuoto se non è una voce di catalogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Tipo di pixel dell’immagine di risposta; può essere "CMYK", "RGB" o "BW" (per immagini in scala di grigio). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Reale </p> </td> 
   <td colname="col3"> <p>Risoluzione di stampa predefinita in dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>Stringa </p> </td> 
   <td colname="col3"> <p>Data/ora di modifica (dal catalogo <span class="codeph">::TimeStamp </span> o il file di vignettatura). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Intero </p> </td> 
   <td colname="col3"> <p>Larghezza a risoluzione massima in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>Stringa </p> </td> 
   <td colname="col3"> <p>Nome vignettatura (stringa di nome dell'oggetto vignettatura principale). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignettatura.res </span> </p> </td> 
   <td colname="col2"> <p>Reale </p> </td> 
   <td colname="col3"> <p>Risoluzione massima dell'oggetto in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> risoluzione del materiale </a> unità (in genere pixel/pollice). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Reale </p> </td> 
   <td colname="col3"> <p>Risoluzione media oggetto in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> risoluzione materiale </a> unità (in genere pixel/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> risoluzione materiale </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Reale </p> </td> 
   <td colname="col3"> <p>Risoluzione minima dell'oggetto in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> risoluzione del materiale </a> unità (in genere pixel/pollice). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>Intero </p> </td> 
   <td colname="col3"> <p>Numero di versione del file di vignettatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Restituisce i dati della mappa immagine inclusi nella vignettatura. Per impostazione predefinita, vengono restituiti i dati di mappa per tutti i gruppi più esterni. I dati della mappa per tutti i gruppi più interni possono essere ottenuti con

`req=map&groupLevel=-1`

I dati della mappa non vengono ridimensionati a `wid=` o `hei=` o modificati in altro modo. Il tipo MIME di risposta è `<text/xml>`.

I dati di risposta sono costituiti da un elemento `<map>` contenente un set di elementi `<area>`, simile al tag `<AREA>` di HTML.

Ogni elemento `<area>` include gli attributi standard `type=` e `coord=` e un attributo `name=` che specifica il nome o il percorso del nome del gruppo di vignettatura. Se le maschere del gruppo di oggetti corrispondente presentano aree discontinue, sono presenti più elementi `<area>` con lo stesso nome.

Oltre agli attributi predefiniti, le vignettature possono definire attributi aggiuntivi, se così creati. Tali attributi personalizzati sono definiti come attributi del gruppo di oggetti. I nomi degli attributi personalizzati devono iniziare con `map` per essere inclusi negli elementi `<area>`. Ad esempio, se gli attributi del gruppo includono `map.href=http://www.scene7.com`, l&#39;elemento `<area>` corrispondente include `href="http://www.scene7.com"`.

Se la vignettatura non include i dati di mapping, viene restituito un documento XML con un elemento `<map>` vuoto.

`object`

Esegue i comandi specificati e restituisce l&#39;immagine di rendering mascherata dalla selezione dell&#39;oggetto residuo (il gruppo o l&#39;oggetto selezionato con l&#39;ultimo comando `sel=` o `obj=` nella richiesta). In genere viene utilizzato con un formato immagine che supporta alfa (vedere [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Se si utilizza un formato di immagine che non supporta l&#39;alfa, le aree esterne alla maschera sono nere.

`props`

Esegue i comandi specificati e restituisce le proprietà di vignettatura e le proprietà di gruppo o oggetto, anziché l&#39;immagine di cui è stato eseguito il rendering. Per una descrizione della sintassi di risposta e del tipo MIME di risposta, vedere [Proprietà](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a). La selezione predefinita viene applicata a meno che non sia specificato anche `obj=` o `sel=` (vedere [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

Le seguenti proprietà possono essere incluse nella risposta:

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Proprietà </p> </th> 
   <th class="entry"> <p> Tipo </p> </th> 
   <th class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Colore di sfondo immagine di risposta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Intero </p> </td> 
   <td> <p> Altezza immagine di risposta in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p>True se il profilo ICC è incorporato nell'immagine di risposta (vedere <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Nome del profilo associato all'immagine di risposta (vedere <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p> True se l'immagine di risposta include il formato alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p> True se l'immagine di risposta include i dati del percorso (vedere <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Tipo di immagine di risposta, che può essere "CMYK", "RGB" o "BW" (per immagini in scala di grigio) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Reale </p> </td> 
   <td> <p> Risoluzione di stampa (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine.qualità </span> </p> </td> 
   <td> <p>Intero, booleano </p> </td> 
   <td> <p> Flag qualità JPEG e chroma (vedere <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Tipo MIME per l'immagine di risposta (vedere <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Larghezza immagine di risposta in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selezione.attributi </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Stringa di attributi per la selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Numero di oggetti nella selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selezione.ident </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Valore del rientro della selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> seleziona <span class="codeph"> selezione.attributi </span>ion.name </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Percorso del nome completo della selezione oggetto corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selezione.sovrapposizione di </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> numero di oggetti sovrapposti nella selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selezione.renderable </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p>Numero di oggetti renderizzabili nella selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selezione.texturable </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Numero di oggetti texturable nella selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selezione.visibile </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Stato corrente per mostrare/nascondere la selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Valore ordine Z del primo oggetto di sovrapposizione nella selezione corrente. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Restituisce il contenuto di `vignette::UserData`. Il server sostituisce tutte le occorrenze di `'??'` in `vignette::UserData` con i terminatori di riga ( `<cr><lf>`). La risposta viene formattata come dati di testo con il tipo MIME di risposta impostato su &lt;text/plain>.

Se l&#39;oggetto specificato nel percorso URL non viene risolto in una voce di mappa di vignettatura valida o se `vignette::UserData` è vuoto, la risposta contiene solo un terminatore di riga ( `CR/LF`).

Qualsiasi altro comando nella stringa di richiesta viene ignorato.

## Proprietà {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Comando di richiesta. Può verificarsi ovunque nella stringa di richiesta.

## Predefinito {#section-00c593cbf1af4364b6b78812e6b93c64}

Se l’URL non include uno o più modificatori di immagine, effettua le seguenti operazioni:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

In caso contrario, `req=img`

## Consultate anche {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attributo::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignettatura::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Proprietà](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)

---
description: Tipo di richiesta. Specifica il tipo di dati richiesti.
solution: Experience Manager
title: req
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 3%

---

# req{#req}

Tipo di richiesta. Specifica il tipo di dati richiesti.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> debug  </span> </p> </td> 
  <td class="stentry"> <p>Esegui i comandi in modalità di debug. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> sommario  </span> </p> </td> 
  <td class="stentry"> <p>Restituisce informazioni sugli oggetti nella vignetta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img  </span> </p> </td> 
  <td class="stentry"> <p>Esegui i comandi e restituisce l'immagine renderizzata. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops  </span> </p> </td> 
  <td class="stentry"> <p>Restituisce le proprietà della vignetta specificata. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> map  </span> </p> </td> 
  <td class="stentry"> <p>Restituisce i dati della mappa immagine incorporati nella vignetta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> oggetto  </span> </p> </td> 
  <td class="stentry"> <p>Esegui i comandi e restituisce l'immagine di cui è stato eseguito il rendering mascherata alla selezione dell'oggetto corrente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> proprietà  </span> </p> </td> 
  <td class="stentry"> <p>Esegui i comandi e restituisce le proprietà dell'immagine di risposta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> dati utente  </span> </p> </td> 
  <td class="stentry"> <p>Restituisce il contenuto della vignetta <span class="codeph">::UserData </span>. </p> </td> 
 </tr> 
</table>

Se non diversamente indicato nelle descrizioni dettagliate, il server restituisce risposte testuali con tipo MIME &lt;text/plain>.

`debug`

Esegue i comandi specificati e restituisce l&#39;immagine renderizzata. Se si verifica un errore, vengono restituite informazioni di errore e debug invece dell&#39;immagine di errore ( `attribute::ErrorImagePath`).

`contents`

Restituisce una rappresentazione XML della gerarchia oggetto nella vignetta, inclusi gli attributi oggetto selezionati. Altri comandi nella richiesta vengono ignorati.

`img`

Esegue i comandi specificati e restituisce l&#39;immagine renderizzata. Il formato dei dati di risposta e il tipo di risposta sono determinati da `fmt=`.

`imageprops`

Restituisce le proprietà selezionate del file di vignetta o della voce di catalogo specificate nel percorso URL. Per una descrizione della sintassi di risposta e del tipo MIME di risposta, consulta [Proprietà](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) . Altri comandi nella richiesta vengono ignorati. Vengono restituite le seguenti proprietà:

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
   <td colname="col1"> <p> <span class="codeph"> image.expiration  </span> </p> </td> 
   <td colname="col2"> <p>Doppio </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attributo::Scadenza  </span> o il tempo predefinito per la durata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td colname="col2"> <p>Intero </p> </td> 
   <td colname="col3"> <p>Altezza a piena risoluzione in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Stringa </p> </td> 
   <td colname="col3"> <p>nome/descrizione del profilo associato a questa vignetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Booleano </p> </td> 
   <td colname="col3"> <p>1 se il profilo associato è incorporato nella vignetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths  </span> </p> </td> 
   <td colname="col2"> <p>Booleano </p> </td> 
   <td colname="col3"> <p>1 se la vignetta incorpora i dati del percorso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier  </span> </p> </td> 
   <td colname="col2"> <p>Stringa </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attributo::Modificatore  </span> o vuoto se non è presente una voce di catalogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Tipo di pixel dell'immagine di risposta; può essere "CMYK", "RGB" o "BW" (per immagini in scala di grigi). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td colname="col2"> <p>Reale </p> </td> 
   <td colname="col3"> <p>Risoluzione di stampa predefinita in dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Stringa </p> </td> 
   <td colname="col3"> <p>Data/ora di modifica (dal catalogo <span class="codeph">::TimeStamp </span> o dal file della vignetta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td colname="col2"> <p>Intero </p> </td> 
   <td colname="col3"> <p>Larghezza a piena risoluzione in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name  </span> </p> </td> 
   <td colname="col2"> <p>Stringa </p> </td> 
   <td colname="col3"> <p>Nome della vignetta (stringa del nome dell'oggetto vignetta principale). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignetta.res  </span> </p> </td> 
   <td colname="col2"> <p>Reale </p> </td> 
   <td colname="col3"> <p>Risoluzione massima dell'oggetto in unità <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> risoluzione del materiale </a> (in genere pixel/pollice). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg  </span> </p> </td> 
   <td colname="col2"> <p>Reale </p> </td> 
   <td colname="col3"> <p>Risoluzione media dell'oggetto in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unità di risoluzione del materiale </a> (in genere pixel/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> risoluzione del materiale </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min  </span> </p> </td> 
   <td colname="col2"> <p>Reale </p> </td> 
   <td colname="col3"> <p>Risoluzione minima dell'oggetto in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> unità di risoluzione del materiale </a> (in genere pixel/pollice). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version  </span> </p> </td> 
   <td colname="col2"> <p>Intero </p> </td> 
   <td colname="col3"> <p>Numero di versione del file di vignetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Restituisce i dati della mappa immagine inclusi nella vignetta. Per impostazione predefinita, vengono restituiti i dati mappa per tutti i gruppi più esterni. I dati mappa per tutti i gruppi più interni possono essere ottenuti con

`req=map&groupLevel=-1`

I dati della mappa non vengono ridimensionati in `wid=` o `hei=` o modificati in altro modo. Il tipo MIME della risposta è `<text/xml>`.

I dati di risposta sono costituiti da un elemento `<map>` contenente un set di elementi `<area>`, simile al tag HTML `<AREA>` .

Ogni elemento `<area>` include gli attributi standard `type=` e `coord=`, nonché un attributo `name=` che specifica il nome o il percorso del gruppo di vignette. Se le maschere del gruppo di oggetti corrispondente hanno aree discontinue, saranno presenti più elementi `<area>` con lo stesso nome.

Oltre agli attributi predefiniti, le vignette possono definire attributi aggiuntivi, se create. Tali attributi personalizzati sono definiti come attributi del gruppo di oggetti. I nomi degli attributi personalizzati devono iniziare con `map`. da includere negli elementi `<area>`. Ad esempio, se gli attributi del gruppo includono `map.href=http://www.scene7.com`, l&#39;elemento corrispondente `<area>` includerà `href="http://www.scene7.com"`.

Se la vignetta non include dati mappa, viene restituito un documento XML con un elemento `<map>` vuoto.

`object`

Esegue i comandi specificati e restituisce l&#39;immagine di cui è stato eseguito il rendering mascherata dalla selezione dell&#39;oggetto residuo (il gruppo o l&#39;oggetto selezionato con l&#39;ultimo comando `sel=` o `obj=` nella richiesta). Generalmente utilizzato insieme a un formato immagine che supporta l&#39;alfa (vedi [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Se si utilizza un formato immagine che non supporta l’alfa, le aree esterne alla maschera sono nere.

`props`

Esegue i comandi specificati e restituisce le proprietà della vignetta e le proprietà del gruppo o dell&#39;oggetto, anziché l&#39;immagine renderizzata. Per una descrizione della sintassi di risposta e del tipo MIME di risposta, consulta [Proprietà](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) . La selezione predefinita si applica a meno che non sia specificato anche `obj=` o `sel=` (vedere [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

Nella risposta è possibile includere le seguenti proprietà:

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
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Risposta colore di sfondo dell'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p>Intero </p> </td> 
   <td> <p> Reply image height in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p>True se il profilo ICC verrà incorporato nell'immagine di risposta (vedere <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Nome collegamento del profilo associato all’immagine di risposta (consulta <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p> True se l'immagine di risposta include l'alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> Booleano </p> </td> 
   <td> <p> True se l'immagine di risposta include i dati del percorso (vedere <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Reply image type (Tipo immagine di risposta), può essere 'CMYK', 'RGB' o 'BW' (per immagini in scala di grigi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> Reale </p> </td> 
   <td> <p> Risoluzione di stampa (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p>Intero, booleano </p> </td> 
   <td> <p> Flag di qualità JPEG e crominanza (vedi <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Tipo di MIME per l'immagine di risposta (vedere <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Rispondi alla larghezza dell'immagine in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes  </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Stringa Attributi per la selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count  </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Numero di oggetti nella selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident  </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Rientra il valore della selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> seleziona  <span class="codeph"> selection.attributes  </span>ion.name  </span> </p> </td> 
   <td> <p> Stringa </p> </td> 
   <td> <p> Percorso nome completo della selezione dell'oggetto corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.sovrapapping  </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> numero di oggetti di sovrapposizione nella selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.rendeable  </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p>Numero di oggetti renderizzabili nella selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable  </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Numero di oggetti testurizzabili nella selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible  </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Stato corrente visualizzazione/nascondi della selezione corrente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder  </span> </p> </td> 
   <td> <p> Intero </p> </td> 
   <td> <p> Valore dell'ordine Z del primo oggetto di sovrapposizione nella selezione corrente. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Restituisce il contenuto di `vignette::UserData`. Il server sostituirà tutte le occorrenze di `'??'` in `vignette::UserData` con terminatori di riga ( `<cr><lf>`). La risposta viene formattata come dati di testo con il tipo MIME della risposta impostato su &lt;text/plain>.

Se l&#39;oggetto specificato nel percorso URL non viene risolto in una voce di mappa di vignetta valida o se il valore `vignette::UserData` è vuoto, la risposta conterrà solo un terminatore di riga ( `CR/LF`).

Tutti gli altri comandi nella stringa di richiesta vengono ignorati.

## Proprietà {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Richiedi, comando. Può verificarsi in qualsiasi punto della stringa di richiesta.

## Predefinito {#section-00c593cbf1af4364b6b78812e6b93c64}

Se l&#39;URL non include un percorso immagine o modificatori, allora:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

In caso contrario, `req=img`

## Consultate anche {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ,  [attributo::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0),  [vignetta::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85),  [Proprietà](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)

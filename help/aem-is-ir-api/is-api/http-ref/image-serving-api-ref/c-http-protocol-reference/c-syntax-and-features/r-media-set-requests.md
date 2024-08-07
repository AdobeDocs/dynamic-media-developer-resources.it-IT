---
description: Image Server fornisce un meccanismo per recuperare una risposta di testo gerarchica (xml o json) che rappresenta tutte le risorse e i metadati associati al set di immagini catalogo per un determinato record.
solution: Experience Manager
title: Richieste di set di file multimediali
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Richieste di set di file multimediali{#media-set-requests}

Image Server fornisce un meccanismo per recuperare una risposta di testo gerarchica (xml o json) che rappresenta tutte le risorse e i metadati associati a catalog::ImageSet per un determinato record.

I visualizzatori possono utilizzare questo meccanismo per generare risposte che informano la presentazione di immagini semplici, video, set video, set di campioni, set 360 gradi, set di pagine (e-catalogs) e set di file multimediali.

## Sintassi della richiesta {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

È possibile recuperare la risposta impostata per un `catalog::ImageSet` utilizzando il modificatore `req=set` e facendo riferimento all&#39;ID del record del catalogo nel percorso di rete. In alternativa, è possibile specificare il set di immagini direttamente nell&#39;URL utilizzando il modificatore `imageset=`. Se il modificatore `imageset=` viene utilizzato per specificare il set di immagini, l&#39;intero valore deve essere racchiuso tra parentesi graffe per uscire dal valore del set di immagini e assicurarsi che tutti i modificatori inclusi non vengano interpretati come parte della stringa di query URL.

## Tipi di risposta impostata {#section-93eb0a1f70344da2a888e56372ad3896}

Il meccanismo di impostazione supporta i seguenti tipi di risposte:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>immagini semplici </p></td> 
  <td class="stentry"> <p>Record immagine senza catalogo <span class="codeph">::ImageSet</span> definito. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>video semplici </p></td> 
  <td class="stentry"> <p>Record video nel catalogo dei contenuti statici. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set di campioni </p></td> 
  <td class="stentry"> <p>Un insieme di elementi costituito da un riferimento a un record immagine e da un riferimento separato facoltativo a un record immagine utilizzato come campione. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set di campioni gerarchici </p></td> 
  <td class="stentry"> <p>Un insieme di elementi costituito da un elemento campione di base o da un riferimento a un record set di campioni. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set 360 gradi </p></td> 
  <td class="stentry"> <p>Un set di elementi costituito da un semplice elenco di ID immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set 360 gradi bidimensionali </p></td> 
  <td class="stentry"> <p>Un insieme di elementi costituito da un'immagine semplice o da un riferimento a un set 360 gradi di base. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set di pagine </p></td> 
  <td class="stentry"> <p>Un set di elementi costituito da un elenco di un massimo di tre immagini pagina </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>media set </p></td> 
  <td class="stentry"> <p>Un set di elementi costituito da immagini semplici, set video, set di campioni, set di campioni gerarchici, set 360 gradi, set 360 gradi bidimensionali, set di pagine e risorse video. Ogni elemento del set di file multimediali può contenere anche un campione opzionale. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set video </p></td> 
  <td class="stentry"> <p>Un set di elementi costituito da un elenco di video semplici. </p></td> 
 </tr> 
</table>

## Rilevamento del tipo di set esterno {#section-3dd6e453528d46898e559d31458a59ba}

Quando viene ricevuta una richiesta `req=set`, il tipo di risposta da generare è determinato dal valore di `catalog::AssetType`. Se `catalog::AssetType` non è definito, il tipo di risposta è determinato dalle regole seguenti:

* Se il record viene trovato nel catalogo immagini E `catalog::ImageSet` è definito

   * Si supponga di avere impostato un catalogo elettronico se almeno una voce nel campo Record Imageset contiene due punti
   * Supponiamo che il set di file multimediali sia impostato se almeno una voce nel campo Record Imageset contiene due punti e virgola.
   * Si supponga che il set di immagini sia impostato se almeno una voce nel campo Record Imageset contiene un punto e virgola.
   * Si supponga che il set 360 gradi non contenga due punti né punto e virgola, ma che almeno una voce contenga un set di riferimenti o un set in linea (set 360 gradi 2D).
   * Si supponga che il set sia sconosciuto se nessuna voce contiene due punti, un punto e virgola, un set di riferimento o un set in linea (ovvero un elenco di immagini separato da virgole).

* Se il record viene trovato sia nei cataloghi di contenuto statico che in quelli di immagini

   * Si supponga che l&#39;estensione file sia nel seguente set: mp3, mp4, flv, f4v, swf, xml
   * Ipotizza immagine in caso contrario

* Se il record viene trovato nel catalogo dei contenuti statici ma NON nel catalogo delle immagini

   * Si supponga che l&#39;estensione file sia nel seguente set: mp3, mp4, flv, f4v, swf, xml
   * Presupponiamo statico in caso contrario

* Se il record in è stato trovato nel catalogo immagini ma NON nel catalogo contenuti statici

   * Immagini

* Se il record NON viene trovato nel catalogo immagini e NON nel catalogo dei contenuti statici

   * Si supponga che l&#39;estensione file sia nel seguente set: mp3, mp4, flv, f4v, swf, xml
   * Supponiamo un’immagine basata su file in caso contrario

In tutti i casi, la risposta XML risultante è conforme al documento XML specificato con il nodo principale impostato corrispondente al tipo rilevato.

## Rilevamento tipo set interno {#section-8f46490e467247e69ce284704def06f3}

Quando il set esterno viene rilevato come tipo di set di file multimediali, la risposta contiene un set di elementi del set di file multimediali corrispondente a ogni voce del set di file multimediali in `catalog::ImageSet`. Se il parametro di tipo opzionale è specificato per una particolare voce di set di file multimediali, viene mappato a un tipo di output in base alla tabella seguente:

| Tipo di input | Tipo di output |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

Se il parametro di tipo opzionale per una particolare voce del set di file multimediali non è specificato o corrisponde a un tipo non supportato, il tipo di elemento del set di file multimediali viene rilevato automaticamente utilizzando le stesse regole applicate a livello di set esterno.

## Specifica XML {#section-c1bd60948ef545759a16885bb6fcc607}

La risposta xml restituita è conforme alle seguenti specifiche:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

Il modificatore `labelkey=` viene utilizzato insieme al campo `catalog::UserData` per generare etichette per immagini e campioni. Il campo `catalog:UserData` viene analizzato come un set di coppie chiave/valore e gli indici labelkey in questo set per recuperare il valore per la chiave specificata. Questo valore viene quindi restituito nell&#39;attributo *`l`* per *`s`* e *`i`*.

## Restrizioni applicate {#section-b9f042873bee45a5ae11b69fd42f2bca}

Per limitare le dimensioni della risposta ed evitare problemi autoreferenziali, la profondità massima di nidificazione è controllata dalla proprietà del server `PS::fvctx.nestingLimit`. Se questo limite viene superato, viene restituito un errore.

Per limitare le dimensioni delle risposte xml per i set di e-catalog di grandi dimensioni, i metadati privati vengono soppressi per gli elementi dei set di brochure in base alla proprietà del server `PS::fvctx.brochureLimit`. Tutti i metadati privati associati alla brochure vengono esportati fino al raggiungimento del limite della brochure. Una volta superato il limite, le mappe private e i dati utente vengono eliminati e viene impostato un flag corrispondente per indicare quale tipo di dati è stato eliminato.

I set di file multimediali nidificati non sono supportati. Un set di file multimediali nidificato è definito come un set di file multimediali contenente un elemento del set di file multimediali di tipo set di file multimediali. Se questa condizione viene rilevata, viene restituito un errore.

## Esempi {#section-588c9d33aa05482c86cd2b1936887228}

Per risposte XML di esempio per la richiesta `req=set`, fare riferimento alla pagina Proprietà nell&#39;intestazione Esempi di HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Consultate anche {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Riferimento catalogo immagini](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

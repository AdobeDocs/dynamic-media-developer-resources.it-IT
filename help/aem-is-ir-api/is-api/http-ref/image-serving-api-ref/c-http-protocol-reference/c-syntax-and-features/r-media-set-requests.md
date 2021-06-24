---
description: Image Serving fornisce un meccanismo per recuperare una risposta testuale gerarchica (xml o json) che rappresenta tutte le risorse e i metadati associati al catalogo ImageSet per un particolare record.
solution: Experience Manager
title: Richieste set di file multimediali
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Richieste set di file multimediali{#media-set-requests}

Image Serving fornisce un meccanismo per recuperare una risposta testuale gerarchica (xml o json) che rappresenta tutte le risorse e i metadati associati al catalogo::ImageSet per un particolare record.

I visualizzatori possono utilizzare questo meccanismo per generare risposte che informino la presentazione di immagini semplici, video, set di video, set di campioni, set 360 gradi, set di pagine (eCatalogs) e set di contenuti multimediali.

## Sintassi della richiesta {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

La risposta impostata per un `catalog::ImageSet` può essere recuperata utilizzando il modificatore `req=set` e facendo riferimento all&#39;ID del record del catalogo nel percorso di rete. In alternativa, il set di immagini può essere specificato direttamente nell’URL utilizzando il modificatore `imageset=` . Se il modificatore `imageset=` viene utilizzato per specificare il set di immagini, l’intero valore deve essere racchiuso tra parentesi graffe per evitare il valore del set di immagini e assicurarsi che eventuali modificatori inclusi non vengano interpretati come parte della stringa di query URL.

## Tipi di risposte impostate {#section-93eb0a1f70344da2a888e56372ad3896}

Il meccanismo set supporta i seguenti tipi di risposte:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>immagini semplici </p></td> 
  <td class="stentry"> <p>Un record immagine senza <span class="codeph"> catalogo::ImageSet</span> definito. </p></td> 
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
  <td class="stentry"> <p>set 360 </p></td> 
  <td class="stentry"> <p>Un set di elementi costituito da un semplice elenco di ID immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set 360 gradi bidimensionali </p></td> 
  <td class="stentry"> <p>Set di elementi costituito da un'immagine semplice o da un riferimento a un set 360 gradi di base. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set di pagine </p></td> 
  <td class="stentry"> <p>Un insieme di elementi costituito da un elenco di fino a tre immagini di pagina </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set di file multimediali </p></td> 
  <td class="stentry"> <p>Un set di elementi costituito da immagini semplici, set di video, set di campioni, set di campioni gerarchici, set 360 gradi, set 360 gradi bidimensionali, set di pagine e risorse video. Ogni elemento del set di file multimediali può anche contenere un campione opzionale. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>set video </p></td> 
  <td class="stentry"> <p>Un set di elementi costituito da un elenco di video semplici. </p></td> 
 </tr> 
</table>

## Rilevamento del tipo di set esterno {#section-3dd6e453528d46898e559d31458a59ba}

Quando viene ricevuta una richiesta `req=set`, il tipo di risposta da generare è determinato dal valore di `catalog::AssetType`. Se `catalog::AssetType` non è definito, il tipo di risposta è determinato dalle seguenti regole:

* Se il record si trova nel catalogo immagini E `catalog::ImageSet` è definito

   * Si supponga di aver impostato un catalogo elettronico se almeno una voce nel campo Immagine record contiene due punti
   * Si supponga di aver impostato un supporto se almeno una voce nel campo Imageset record contiene due punti e virgola.
   * Si supponga di aver impostato l&#39;immagine se almeno una voce nel campo Imageset record contiene un punto e virgola.
   * Supponiamo di usare un set 360 gradi se nessuna voce contiene due punti o un punto e almeno una voce contiene un set di riferimento o un set in-line (questo è un set 360 gradi 2D).
   * Si supponga di aver impostato un valore sconosciuto se nessuna voce contiene due punti o un punto e virgola, né un set di riferimento né un set in-line (ad esempio un elenco di immagini separato da virgole).

* Se il record si trova sia nei cataloghi di contenuti statici E immagine

   * Supponi video se l’estensione del file è nel seguente set: mp3, mp4, flv, f4v, swf, xml
   * Ipotizza immagine altrimenti

* Se il record si trova nel catalogo dei contenuti statici ma NON nel catalogo delle immagini

   * Supponi video se l’estensione del file è nel seguente set: mp3, mp4, flv, f4v, swf, xml
   * Supponiamo di essere statici in caso contrario

* Se il record si trova nel catalogo immagini ma NON nel catalogo dei contenuti statici

   * Ipotizza immagine

* Se il record NON viene trovato nel catalogo immagini e NON viene trovato nel catalogo dei contenuti statici

   * Supponi video basati su file se l&#39;estensione del file è nel seguente set: mp3, mp4, flv, f4v, swf, xml
   * Supponi immagini basate su file in caso contrario

In tutti i casi, la risposta xml risultante sarà conforme al documento XML specificato con il nodo principale impostato corrispondente al tipo rilevato.

## Rilevamento del tipo di set interno {#section-8f46490e467247e69ce284704def06f3}

Quando il set esterno viene rilevato come set di file multimediali di tipo , la risposta conterrà un set di elementi del set di file multimediali corrispondenti a ciascuna voce del set di file multimediali in `catalog::ImageSet`. Se per una particolare voce del set di file multimediali è specificato il parametro opzionale type, questo verrà mappato su un tipo di output in base alla tabella seguente:

| Tipo di ingresso | Tipo di uscita |
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

Se il parametro opzionale type per una particolare voce del set di file multimediali non è specificato o corrisponde a un tipo non supportato, il tipo di elemento del set di file multimediali viene rilevato automaticamente utilizzando le stesse regole applicate a livello del set esterno.

## Specifica XML {#section-c1bd60948ef545759a16885bb6fcc607}

La risposta xml restituita è conforme alla seguente specifica:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

Il modificatore `labelkey=` viene utilizzato insieme al campo `catalog::UserData`per generare etichette per immagini e campioni. Il campo `catalog:UserData` viene analizzato come un set di coppie chiave/valore e l’etichetta indicizza questo set per recuperare il valore per la chiave specificata. Questo valore viene quindi restituito nell&#39;attributo *`l`* per *`s`* e *`i`*.

## Restrizioni imposte {#section-b9f042873bee45a5ae11b69fd42f2bca}

Per limitare le dimensioni della risposta ed evitare problemi di autoreferenza, la profondità massima di nidificazione è controllata dalla proprietà server `PS::fvctx.nestingLimit`. Se questo limite viene superato, viene restituito un errore.

Al fine di limitare le dimensioni delle risposte xml per i set di catalogo elettronico di grandi dimensioni, i metadati privati vengono soppressi per gli elementi del set di brochure in base alla proprietà del server `PS::fvctx.brochureLimit`. Tutti i metadata privati associati all&#39;opuscolo saranno esportati fino al raggiungimento del limite della brochure. Una volta superato il limite, le mappe private e i dati utente verranno soppressi e verrà impostato un flag corrispondente per indicare quale tipo di dati è stato soppresso.

I set di file multimediali nidificati non sono supportati. Un set di file multimediali nidificati è definito come un set di file multimediali che contiene un elemento set di file multimediali di tipo set di file multimediali. Se viene rilevata questa condizione, viene restituito un errore.

## Esempi {#section-588c9d33aa05482c86cd2b1936887228}

Per le risposte XML di esempio per la richiesta `req=set`, fare riferimento alla pagina Proprietà nell&#39;intestazione Esempi HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Consultate anche {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3),  [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), Riferimento catalogo  [immagini](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

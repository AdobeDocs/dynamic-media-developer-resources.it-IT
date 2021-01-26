---
description: Selezionare Livello. Seleziona un livello e avvia un nuovo segmento di definizione del livello nella sequenza di comandi.
seo-description: Selezionare Livello. Seleziona un livello e avvia un nuovo segmento di definizione del livello nella sequenza di comandi.
seo-title: layer
solution: Experience Manager
title: layer
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# layer{#layer}

Selezionare Livello. Seleziona un livello e avvia un nuovo segmento di definizione del livello nella sequenza di comandi.

`layer= *``*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Numero del livello da selezionare (0 o numero maggiore di int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Selezionate l’immagine composita. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Nome del livello. </p></td> 
 </tr> 
</table>

Tutti i comandi all’interno del segmento del livello vengono applicati al livello specificato. Un segmento di livello viene terminato dal comando successivo `layer=` o `effect=` o dalla fine della richiesta.

Specificare `layer=comp` per selezionare l&#39;immagine composita (o la visualizzazione, per alcuni comandi).

Il numero del livello specifica l’ordine z del livello. I livelli con numero superiore vengono posizionati sopra a quelli con numero inferiore.

I numeri dei livelli non devono essere consecutivi. Il livello 0 è obbligatorio.

Un nome può essere assegnato a un livello con la variante di comando `layer= *`n`*, *`name`*`. Una volta definito un livello denominato, è possibile farvi riferimento con ` layer= *`name`*`, senza dover conoscere il numero del livello. Possono essere assegnati più nomi allo stesso livello, utilizzando più comandi `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>Il livello 0 determina la dimensione complessiva del quadro di composizione. Tutte le parti di livelli che si trovano al di fuori dei limiti del livello 0 vengono ritagliate quando il composito viene creato.

## Proprietà {#section-499963ee52c14f2898f0d0f90c1d01be}

Livello, comando. I riferimenti alle variabili di sostituzione non sono supportati in `layer=`.

`comp` non è consentito come  *`name`* stringa. Viene restituito un errore se lo stesso *`name`* è assegnato a più livelli, oppure se a un livello viene fatto riferimento da *`name`* che non è stato definito in precedenza.

## Predefinito {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Molti comandi e attributi si applicano al livello 0 se `layer=comp`.

## Casi speciali {#section-e087cb2e3562473e8d391abfa3b9489f}

* Se lo stesso nome è mappato a più livelli (ad esempio: `layer=1,image&layer=2,image`), si verifica un errore.
* Se lo stesso nome viene mappato più volte su un singolo livello (ad esempio: `layer=1,image&layer=1,image`), l&#39;ambito è impostato come al solito, senza errori.
* Sono supportati più nomi per lo stesso livello.

   Potete usare uno dei due nomi per fare riferimento al livello (ad esempio: `layer=1,image&layer=1,picture`).
* Se un nome di riferimento non viene mai mappato a un numero di livello (ad esempio: `layer=1,image&layer=picture`), si verifica un errore.
* Le variabili di sostituzione non sono supportate nei modificatori di livello (ad esempio: `layer=$image$`).

   Questo vale per tutte le permutazioni, non solo per i nomi dei livelli, ma anche per i modificatori di livello in generale.

* Tutte le regole di unione e sostituzione devono funzionare esattamente come quando lo stesso livello viene fatto riferimento in più origini (record di catalogo di richieste, pre o post modificatori, macro, ecc.).

## Esempio {#section-cc40de6a0a754178aa752601539c815b}

Vedere gli esempi in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

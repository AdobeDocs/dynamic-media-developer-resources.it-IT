---
description: Gli effetti ombra e bagliore in stile Photoshop vengono implementati utilizzando sottolivelli speciali (livelli di effetto) che possono essere collegati a qualsiasi livello (il livello principale), inclusi layer=0 e layer=comp.
seo-description: Gli effetti ombra e bagliore in stile Photoshop vengono implementati utilizzando sottolivelli speciali (livelli di effetto) che possono essere collegati a qualsiasi livello (il livello principale), inclusi layer=0 e layer=comp.
seo-title: Effetti livello
solution: Experience Manager
title: Effetti livello
topic: Scene7 Image Serving - Image Rendering API
uuid: 076e98de-cbbb-457b-984a-367a935b4356
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Effetti livello{#layer-effects}

Gli effetti ombra e bagliore in stile Photoshop vengono implementati utilizzando sottolivelli speciali (livelli di effetto) che possono essere collegati a qualsiasi livello (il livello principale), inclusi layer=0 e layer=comp.

I livelli degli effetti supportano una serie di attributi e comandi standard per immagini e livelli, ma non sono destinati a livelli per scopi generali e non supportano dati di immagine o testo indipendenti.

È possibile collegare un numero qualsiasi di effetti di livello a un singolo livello principale.

## Effetti interni ed esterni {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Gli effetti* interni vengono rappresentati sopra al livello principale e sono visibili solo nelle aree opache del livello principale. *Gli effetti* esterni vengono sottoposti a rendering dietro il livello principale (non saranno mai visibili all’interno delle aree opache del livello principale) e possono essere posizionati ovunque all’interno del quadro di composizione. Un effetto interno o esterno viene scelto assegnando un numero di livello positivo o negativo con il `effect=` comando. Il `effect=` comando controlla anche l’ordine z tra più livelli di effetto collegati allo stesso livello principale.

## Relazione con il livello padre {#section-eb8bfc4f754a42fc973b562821d6f2d3}

I livelli degli effetti vengono ridimensionati automaticamente e posizionati in modo da coincidere con il livello principale (ovvero il livello dell’effetto eredita i valori `size=` e `origin=` del livello principale). `pos=` può essere usato per spostare il livello dell’effetto dal livello principale, come generalmente richiesto per gli effetti ombra esterna e interna. Mentre per i livelli standard `pos=` specifica un offset tra le origini di questo livello e il livello 0, per i livelli degli effetti `pos=` specifica l’offset tra le origini del livello dell’effetto e il livello principale.

## Comandi e attributi supportati {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

I livelli degli effetti accettano i comandi e gli attributi seguenti:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Tutti gli altri comandi immagine e livello contenuti nei livelli degli effetti vengono ignorati.

## Macro degli effetti predefiniti {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Per facilitare l’utilizzo degli effetti livello, IS fornisce due macro con il catalogo immagini predefinito `$shadow$` e `$glow$`, che forniscono valori predefiniti per gli attributi del livello degli effetti simili agli effetti livello di Photoshop. Nella tabella seguente sono elencati i comandi di effetto e la macro da utilizzare per implementare gli effetti di livello predefiniti. Naturalmente, qualsiasi attributo specificato nelle macro può essere modificato nell&#39;URL, oppure è possibile creare macro alternative per implementare effetti livello personalizzati.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Effetto Desiderato</b> </th> 
   <th class="entry"> <b> Comando</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Ombra esterna </p> </td> 
   <td> <p> <span class="codeph"> effetto=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Ombra interna </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Bagliore esterno </p> </td> 
   <td> <p> <span class="codeph"> effetto=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Bagliore interno </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-4c449fdf707b43858917fb271fa1fe96}

Aggiungete un bordo rosso e largo tre pixel con opacità del 50% a un livello:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

Il bordo seguirà i contorni del canale alfa o della maschera dell’immagine. L&#39;impostazione `effect=1` posiziona invece il bordo sul bordo interno.

Aggiungete un’ombra esterna blu a un’immagine, utilizzando le impostazioni dell’effetto predefinito (eccetto il colore):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` aggiunge un piccolo margine ai bordi inferiore destro dell’immagine, per evitare che l’ombra esterna venga ritagliata ai limiti dell’immagine.

## Consultate anche {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Macro comandi%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)

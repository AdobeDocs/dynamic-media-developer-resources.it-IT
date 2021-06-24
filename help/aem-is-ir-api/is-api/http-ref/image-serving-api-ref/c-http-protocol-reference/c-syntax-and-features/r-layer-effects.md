---
description: Gli effetti di ombreggiatura e bagliore dei livelli in stile Photoshop vengono implementati utilizzando sottolivelli speciali (livelli di effetto) che possono essere collegati a qualsiasi livello (livello padre), inclusi layer=0 e layer=comp.
solution: Experience Manager
title: Effetti livello
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 2%

---

# Effetti livello{#layer-effects}

Gli effetti di ombreggiatura e bagliore dei livelli in stile Photoshop vengono implementati utilizzando sottolivelli speciali (livelli di effetto) che possono essere collegati a qualsiasi livello (livello padre), inclusi layer=0 e layer=comp.

Mentre i livelli di effetto supportano una serie di attributi e comandi standard di immagine e livello, non sono destinati a essere livelli generali e non supportano dati di immagine o testo indipendenti.

Un numero qualsiasi di effetti di livello può essere collegato a un singolo livello padre.

## Effetti interni ed esterni {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Gli* effetti interni vengono sottoposti a rendering sopra il livello padre e sono visibili solo nelle aree opache del livello padre. *Gli* effetti esterni vengono sottoposti a rendering dietro il livello padre (in modo che non saranno mai visibili all’interno di aree opache del livello padre) e possono essere posizionati ovunque all’interno del quadro di composizione. Un effetto interno o esterno viene scelto assegnando un numero di livello di effetto positivo o negativo con il comando `effect=`. Il comando `effect=` controlla anche l&#39;ordine z tra più livelli di effetto collegati allo stesso livello padre.

## Relazione con il livello padre {#section-eb8bfc4f754a42fc973b562821d6f2d3}

I livelli di effetto vengono dimensionati automaticamente e posizionati in modo da coincidere con il livello padre (ovvero il livello di effetto eredita i valori `size=` e `origin=` del livello padre). `pos=` può essere utilizzato per spostare il livello di effetto dal livello padre, come generalmente richiesto per gli effetti di ombreggiatura esterna e interna. Mentre per i livelli standard `pos=` specifica un offset tra le origini di questo livello e il livello 0, per i livelli di effetto `pos=` specifica l&#39;offset tra le origini del livello di effetto e il livello padre.

## Comandi e attributi supportati {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

I livelli di effetto accettano i comandi e gli attributi seguenti:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Tutti gli altri comandi immagine e livello contenuti nei livelli effetto vengono ignorati.

## Macro degli effetti predefiniti {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Per facilitare l’utilizzo degli effetti di livello, IS fornisce due macro con il catalogo immagini predefinito, `$shadow$` e `$glow$`, che forniscono valori predefiniti per gli attributi del livello di effetto simili agli effetti di livello Photoshop. Nella tabella seguente sono elencati i comandi di effetto e le macro da utilizzare per implementare gli effetti di livello predefiniti. Naturalmente, è possibile modificare nell&#39;URL qualsiasi attributo specificato nelle macro oppure creare macro alternative per implementare effetti di livello personalizzati.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Effetto desiderato</b> </th> 
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

Aggiungete un bordo rosso largo tre pixel con opacità del 50% a un livello:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

Il bordo seguirà i contorni del canale o della maschera alfa dell&#39;immagine. Se si imposta `effect=1`, il bordo viene posizionato sul bordo interno.

Aggiungi un’ombreggiatura bluastra a un’immagine, utilizzando le impostazioni dell’effetto predefinito (tranne che per il colore):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` aggiunge un piccolo margine ai bordi in basso a destra dell&#39;immagine, impedendo il ritaglio dell&#39;ombreggiatura ai limiti dell&#39;immagine.

## Consultate anche {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), macro  [di comando%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)

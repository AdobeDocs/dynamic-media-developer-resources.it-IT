---
title: Effetti livello
description: Gli effetti di ombreggiatura e bagliore del livello in stile Photoshop vengono implementati utilizzando speciali sottolivelli (livelli effetto) che possono essere attaccati a qualsiasi livello (il livello padre), inclusi layer=0 e layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 2%

---

# Effetti livello{#layer-effects}

Gli effetti di ombreggiatura e bagliore del livello in stile Photoshop vengono implementati utilizzando speciali sottolivelli (livelli effetto) che possono essere attaccati a qualsiasi livello (il livello padre), inclusi layer=0 e layer=comp.

Sebbene i livelli degli effetti supportino una serie di attributi e comandi standard per le immagini e i livelli, non sono destinati a essere livelli generici e non supportano dati di testo o immagini indipendenti.

Un numero qualsiasi di effetti di livello può essere associato a un singolo livello padre.

## Effetti interni ed esterni {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Effetti interni* vengono sottoposte a rendering sopra il livello padre e sono visibili solo nelle aree opache del livello padre. *Effetti esterni* vengono sottoposte a rendering dietro il livello principale (non saranno quindi mai visibili all&#39;interno di aree opache del livello principale) e possono essere posizionate ovunque all&#39;interno dell&#39;area di lavoro di composizione. Un effetto interno o esterno viene scelto assegnando un numero di livello di effetto positivo o negativo al `effect=` comando. Il `effect=` Questo comando controlla anche l&#39;ordinamento z tra più livelli di effetto collegati allo stesso livello padre.

## Relazione con il livello padre {#section-eb8bfc4f754a42fc973b562821d6f2d3}

I livelli degli effetti vengono automaticamente ridimensionati e posizionati in modo da coincidere con il livello padre (ad esempio, il livello degli effetti eredita il `size=` e `origin=` valori del livello padre). `pos=` può essere utilizzato per allontanare il livello dell&#39;effetto dal livello padre, come in genere è richiesto per gli effetti di ombreggiatura esterna e interna. Mentre per i livelli standard `pos=` specifica un offset tra le origini di questo livello e il livello 0, per i livelli di effetto `pos=` specifica l&#39;offset tra le origini del livello effetto e il livello padre.

## Comandi e attributi supportati {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

I livelli degli effetti accettano i seguenti comandi e attributi:

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

## Macro effetti predefinite {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Per facilitare l&#39;utilizzo degli effetti di livello, IS fornisce due macro con il catalogo immagini predefinito, `$shadow$` e `$glow$`, che forniscono i valori di default per gli attributi del livello di effetto simili agli effetti del livello Photoshop. Nella tabella seguente sono elencati i comandi e le macro da utilizzare per implementare gli effetti di livello predefiniti. Naturalmente, è possibile modificare nell&#39;URL qualsiasi attributo specificato nelle macro oppure creare macro alternative per implementare effetti di livello personalizzati.

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
   <td> <p> <span class="codeph"> effect=-1&amp;$ombra$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Ombra interna </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Bagliore esterno </p> </td> 
   <td> <p> <span class="codeph"> effetto=-1&amp;$bagliore$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Bagliore interno </p> </td> 
   <td> <p> <span class="codeph"> effetto=1&amp;$bagliore$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-4c449fdf707b43858917fb271fa1fe96}

Aggiungete a un livello un bordo rosso largo tre pixel con un&#39;opacità del 50%:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

Il bordo segue i contorni del canale o della maschera alfa dell&#39;immagine. Impostazione `effect=1` posizionerebbe invece il bordo sullo spigolo interno.

Aggiungete un&#39;ombra esterna di colore bluastro a un&#39;immagine, utilizzando le impostazioni degli effetti predefinite (ad eccezione del colore):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` aggiunge un piccolo margine ai bordi inferiori destro dell&#39;immagine, impedendo che l&#39;ombra esterna venga ritagliata ai limiti dell&#39;immagine.

## Consultate anche {#section-1acccccf534549aea23d4c008c17e7c0}

[effect= effetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Macro comandi%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)

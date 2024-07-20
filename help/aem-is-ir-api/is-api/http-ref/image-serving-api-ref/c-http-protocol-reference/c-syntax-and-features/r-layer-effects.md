---
title: Effetti livello
description: Gli effetti di ombreggiatura e bagliore del livello in stile Photoshop vengono implementati utilizzando speciali sottolivelli (livelli effetto) che possono essere attaccati a qualsiasi livello (il livello padre), inclusi layer=0 e layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---

# Effetti livello{#layer-effects}

Gli effetti di ombreggiatura e bagliore del livello in stile Photoshop vengono implementati utilizzando speciali sottolivelli (livelli effetto) che possono essere attaccati a qualsiasi livello (il livello padre), inclusi layer=0 e layer=comp.

Sebbene i livelli degli effetti supportino una serie di attributi e comandi standard per le immagini e i livelli, non sono destinati a essere livelli generici e non supportano dati di testo o immagini indipendenti.

Un numero qualsiasi di effetti di livello può essere associato a un singolo livello padre.

## Effetti interni ed esterni {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Gli effetti interni* vengono visualizzati sopra il livello principale e sono visibili solo nelle aree opache del livello principale. *Gli effetti esterni* vengono sottoposti a rendering dietro il livello principale (quindi non sono mai visibili all&#39;interno di aree opache del livello principale) e possono essere posizionati ovunque all&#39;interno dell&#39;area di lavoro di composizione. Un effetto interno o esterno viene scelto assegnando un numero di livello di effetto positivo o negativo con il comando `effect=`. Il comando `effect=` controlla inoltre l&#39;ordinamento z tra più livelli di effetti collegati allo stesso livello padre.

## Relazione con il livello padre {#section-eb8bfc4f754a42fc973b562821d6f2d3}

I livelli degli effetti vengono automaticamente ridimensionati e posizionati in modo da coincidere con il livello padre (ovvero, il livello effetto eredita i valori `size=` e `origin=` del livello padre). `pos=` può essere utilizzato per spostare il livello dell&#39;effetto dal livello padre, come in genere è necessario per gli effetti di ombreggiatura esterna e interna. Mentre per i livelli standard `pos=` specifica un offset tra le origini di questo livello e il livello 0, per i livelli effetto `pos=` specifica l&#39;offset tra le origini del livello effetto e il livello padre.

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

Per facilitare l&#39;utilizzo degli effetti di livello, IS fornisce due macro con il catalogo immagini predefinito, `$shadow$` e `$glow$`, che forniscono valori predefiniti per gli attributi di livello effetto simili agli effetti di livello Photoshop. Nella tabella seguente sono elencati i comandi e le macro da utilizzare per implementare gli effetti di livello predefiniti. Naturalmente, è possibile modificare nell&#39;URL qualsiasi attributo specificato nelle macro oppure creare macro alternative per implementare effetti di livello personalizzati.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> effetto desiderato</b> </th> 
   <th class="entry"> Comando <b></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Ombra esterna </p> </td> 
   <td> <p> <span class="codeph"> effetto=-1&amp;$ombra$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Ombra interna </p> </td> 
   <td> <p> <span class="codeph"> effetto=1&amp;$ombra$</span> </p> </td> 
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

Il bordo segue i contorni del canale o della maschera alfa dell&#39;immagine. Se si imposta `effect=1`, il bordo verrà posizionato sul bordo interno.

Aggiungete un&#39;ombra esterna di colore bluastro a un&#39;immagine, utilizzando le impostazioni degli effetti predefinite (ad eccezione del colore):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` aggiunge un piccolo margine ai bordi inferiori destro dell&#39;immagine, impedendo che l&#39;ombra esterna venga ritagliata ai limiti dell&#39;immagine.

## Consultate anche {#section-1acccccf534549aea23d4c008c17e7c0}

[effetto=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Macro comando%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)

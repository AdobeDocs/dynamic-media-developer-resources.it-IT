---
description: Selezionate Livello effetto. Seleziona un livello di effetto e avvia un nuovo segmento di livello nella stringa di richiesta, associato al livello corrente.
seo-description: Selezionate Livello effetto. Seleziona un livello di effetto e avvia un nuovo segmento di livello nella stringa di richiesta, associato al livello corrente.
seo-title: effetto
solution: Experience Manager
title: effetto
topic: Scene7 Image Serving - Image Rendering API
uuid: 622dc7ca-55b8-4a82-b9a7-65588aee87d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---


# effect{#effect}

Selezionate Livello effetto. Seleziona un livello di effetto e avvia un nuovo segmento di livello nella stringa di richiesta, associato al livello corrente.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Numero del livello dell’effetto (numero intero non uguale a 0). </p></td> 
 </tr> 
</table>

Tutti i comandi all’interno del nuovo segmento vengono applicati al livello dell’effetto specificato. Un segmento del livello di effetto viene terminato dal comando successivo `layer=` o `effect=` o dalla fine della richiesta.

*`n`* deve essere minore di 0 per gli effetti del livello esterno (ossia gli effetti dietro il livello principale) e maggiore di 0 per gli effetti del livello interno (ossia gli effetti all’interno del livello principale). I numeri del livello dell’effetto non devono essere consecutivi.

Il numero del livello dell’effetto specifica l’ordine z, nel caso di più livelli di effetto per lo stesso livello principale. I livelli con numero superiore vengono posizionati sopra a quelli con numero inferiore.

I livelli degli effetti possono essere collegati a `layer=comp`.

## Proprietà {#section-e11f795deff345779ce280a82cf221ca}

Livello effetto, comando. *`n`* non deve essere 0.

## Predefinito {#section-84bbe1cfe7a94040827c994323ac59d4}

Nessuno.

## Esempio {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Consultate anche {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`

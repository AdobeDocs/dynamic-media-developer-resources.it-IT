---
title: effetto
description: Selezionate Livello effetto. Seleziona un livello effetto e avvia un nuovo segmento di livello nella stringa di richiesta, associato al livello corrente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# effetto{#effect}

Selezionate Livello effetto. Seleziona un livello effetto e avvia un nuovo segmento di livello nella stringa di richiesta, associato al livello corrente.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Numero livello effetto (int non uguale a 0). </p></td> 
 </tr> 
</table>

Tutti i comandi all&#39;interno del nuovo segmento vengono applicati al livello di effetto specificato. Un segmento di livello effetto viene terminato dal comando `layer=` o `effect=` successivo o dalla fine della richiesta.

Il valore *`n`* deve essere minore di 0 per gli effetti di livello esterno (ovvero, effetti dietro il livello padre) e maggiore di 0 per gli effetti di livello interno (ovvero, effetti all&#39;interno del livello padre). I numeri dei livelli di effetto non devono essere consecutivi.

Il numero del livello dell&#39;effetto specifica l&#39;ordine z, se sono presenti più livelli dell&#39;effetto per lo stesso livello padre. I livelli con numero più alto vengono posizionati sopra i livelli con numero più basso.

I livelli degli effetti possono essere collegati a `layer=comp`.

## Proprietà {#section-e11f795deff345779ce280a82cf221ca}

Comando Livello effetto. Il valore *`n`* non deve essere 0.

## Predefinito {#section-84bbe1cfe7a94040827c994323ac59d4}

Nessuno.

## Esempio {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Consultate anche {#section-573273e9e0e64103a5764075f5e50180}

[layer= livello](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)

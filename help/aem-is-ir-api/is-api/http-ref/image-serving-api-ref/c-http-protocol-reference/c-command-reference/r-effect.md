---
title: effetto
description: Selezionare Livello effetto. Seleziona un livello di effetto e avvia un nuovo segmento di livello nella stringa di richiesta, associata al livello corrente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 3%

---

# effetto{#effect}

Selezionare Livello effetto. Seleziona un livello di effetto e avvia un nuovo segmento di livello nella stringa di richiesta, associata al livello corrente.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Numero del livello dell'effetto (in numero non uguale a 0). </p></td> 
 </tr> 
</table>

Tutti i comandi all’interno del nuovo segmento vengono applicati al livello di effetto specificato. Un segmento del livello di effetto viene terminato dal successivo `layer=` o `effect=` o alla fine della richiesta.

*`n`* deve essere minore di 0 per gli effetti del livello esterno (cioè gli effetti dietro il livello padre) e maggiore di 0 per gli effetti del livello interno (cioè gli effetti all&#39;interno del livello padre). I numeri dei livelli di effetto non devono essere consecutivi.

Il numero del livello di effetto specifica l&#39;ordine z, nel caso di più livelli di effetto per lo stesso livello padre. I livelli numerati più in alto vengono posizionati sopra i livelli numerati più in basso.

Gli strati degli effetti possono essere collegati a `layer=comp`.

## Proprietà {#section-e11f795deff345779ce280a82cf221ca}

Livello effetto, comando. *`n`* non deve essere 0.

## Predefinito {#section-84bbe1cfe7a94040827c994323ac59d4}

Nessuno.

## Esempio {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Consultate anche {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)

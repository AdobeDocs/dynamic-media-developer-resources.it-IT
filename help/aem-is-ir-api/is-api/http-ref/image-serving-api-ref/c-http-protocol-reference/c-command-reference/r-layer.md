---
title: layer
description: Selezionate Livello (Layer). Seleziona un livello e avvia un nuovo segmento di definizione del livello nella sequenza di comando.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# layer{#layer}

Selezionate Livello (Layer). Seleziona un livello e avvia un nuovo segmento di definizione del livello nella sequenza di comando.

`layer= *`n`*|comp[, *`nome`*]`

`layer= *`nome`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Numero di livelli da selezionare (0 o più int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Selezionare l'immagine composita. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nome</span></span> </p></td> 
  <td class="stentry"> <p>Nome livello. </p></td> 
 </tr> 
</table>

Tutti i comandi all&#39;interno del segmento di livello vengono applicati al livello specificato. Un segmento di livello viene terminato dal successivo `layer=` o `effect=` o alla fine della richiesta.

Specifica `layer=comp` per selezionare l&#39;immagine composita (o la vista, per alcuni comandi).

Il numero di livello specifica l&#39;ordine z per il livello. I livelli con numero più alto vengono posizionati sopra i livelli con numero più basso.

I numeri dei livelli non devono essere consecutivi. È richiesto il livello 0.

È possibile assegnare un nome a un livello con `layer= *`n`*, *`nome`*` variante del comando. Una volta definito un livello con nome, è possibile farvi riferimento con ` layer= *`nome`*`, senza dover conoscere il numero del livello. È possibile assegnare più nomi allo stesso livello utilizzando più `layer= *`n`*, *`nome`*` comandi.

>[!NOTE]
>
>Il livello 0 determina le dimensioni complessive dell&#39;area di lavoro di composizione. Tutte le parti dei livelli che ricadono al di fuori dei limiti del livello 0 vengono ritagliate al momento della costruzione del composito.

## Proprietà {#section-499963ee52c14f2898f0d0f90c1d01be}

Comando Livello. I riferimenti alle variabili di sostituzione non sono supportati in `layer=`.

`comp` non è consentito come *`name`* stringa. Viene restituito un errore se lo stesso *`name`* è assegnato a più di un livello o se un livello è referenziato da *`name`* che non è stato definito in precedenza.

## Predefinito {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Molti comandi e attributi vengono applicati al livello 0 se `layer=comp`.

## Casi speciali {#section-e087cb2e3562473e8d391abfa3b9489f}

* Se lo stesso nome è mappato su più livelli (ad esempio: `layer=1,image&layer=2,image`), si verifica un errore.
* Se lo stesso nome viene mappato più volte su un singolo livello (ad esempio: `layer=1,image&layer=1,image`), l’ambito viene impostato come di consueto, senza errori.
* Sono supportati più nomi per lo stesso livello.

   Entrambi i nomi possono essere utilizzati per fare riferimento al livello (ad esempio: `layer=1,image&layer=1,picture`).
* Se un nome a cui si fa riferimento non viene mai mappato a un numero di livello (ad esempio: `layer=1,image&layer=picture`), si verifica un errore.
* Le variabili di sostituzione non sono supportate nei modificatori di livello (ad esempio: `layer=$image$`).

   Questo vale per tutte le permutazioni, non solo per i nomi dei livelli ma anche per i modificatori di livello in generale.

* Tutte le regole di unione e sostituzione devono funzionare esattamente come quando si fa riferimento allo stesso livello in più origini (record di catalogo per richieste, pre o post modificatori, macro, ecc.).

## Esempio {#section-cc40de6a0a754178aa752601539c815b}

Vedi gli esempi in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

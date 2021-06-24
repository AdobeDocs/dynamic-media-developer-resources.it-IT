---
description: Selezionare Livello. Seleziona un livello e avvia un nuovo segmento di definizione del livello nella sequenza di comando.
solution: Experience Manager
title: strato
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---

# strato{#layer}

Selezionare Livello. Seleziona un livello e avvia un nuovo segmento di definizione del livello nella sequenza di comando.

`layer= *`Nome `*|comp[, *``*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Numero del livello da selezionare (0 o numero maggiore di int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Selezionare l'immagine composita. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Nome del livello. </p></td> 
 </tr> 
</table>

Tutti i comandi all’interno del segmento di livello vengono applicati al livello specificato. Un segmento di livello viene terminato dal comando successivo `layer=` o `effect=` o dalla fine della richiesta.

Specificare `layer=comp` per selezionare l&#39;immagine composita (o visualizzare, per alcuni comandi).

Il numero del livello specifica efficacemente l&#39;ordine z del livello. I livelli numerati più in alto vengono posizionati sopra i livelli numerati più in basso.

I numeri dei livelli non devono essere consecutivi. Il livello 0 è obbligatorio.

Un nome può essere assegnato a un livello con la variante di comando `layer= *`n`*, *`name`*`. Una volta definito un livello denominato, è possibile farvi riferimento con ` layer= *`name`*`, senza dover conoscere il numero del livello. È possibile assegnare più nomi allo stesso livello utilizzando più comandi `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>Il livello 0 determina la dimensione complessiva del quadro di composizione. Tutte le parti dei livelli che non rientrano nei limiti del livello 0 vengono ritagliate quando il composito è costruito.

## Proprietà {#section-499963ee52c14f2898f0d0f90c1d01be}

Livello, comando. I riferimenti alle variabili di sostituzione non sono supportati in `layer=`.

`comp` non è consentito come  *`name`* stringa. Viene restituito un errore se lo stesso *`name`* è assegnato a più di un livello, o se a un livello viene fatto riferimento da *`name`* che non è stato definito in precedenza.

## Predefinito {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Molti comandi e attributi si applicano al livello 0 se `layer=comp`.

## Casi speciali {#section-e087cb2e3562473e8d391abfa3b9489f}

* Se lo stesso nome è mappato su più livelli (ad esempio: `layer=1,image&layer=2,image`), si verifica un errore.
* Se lo stesso nome viene mappato più volte su un singolo livello (ad esempio: `layer=1,image&layer=1,image`), l&#39;ambito viene impostato come di consueto, senza errori.
* Sono supportati più nomi per lo stesso livello.

   Entrambi i nomi possono essere utilizzati per fare riferimento al livello (ad esempio: `layer=1,image&layer=1,picture`).
* Se un nome di riferimento non viene mai mappato su un numero di livello (ad esempio: `layer=1,image&layer=picture`), si verifica un errore.
* Le variabili di sostituzione non sono supportate nei modificatori di livello (ad esempio: `layer=$image$`).

   Questo vale per tutte le permutazioni, non solo per i nomi dei livelli, ma per i modificatori di livello in generale.

* Tutte le regole di unione e di override devono funzionare esattamente come quando lo stesso livello viene referenziato in più origini (richieste, record catalogo modificatori pre o post, macro, ecc.).

## Esempio {#section-cc40de6a0a754178aa752601539c815b}

Vedi gli esempi in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

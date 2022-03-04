---
description: Le variabili di sostituzione vengono utilizzate per trasferire i valori dall’URL della richiesta ai modelli di composizione memorizzati nei cataloghi di immagini. Le variabili possono anche essere utilizzate per trasmettere lo stesso valore in posizioni diverse in una richiesta complessa.
solution: Experience Manager
title: Variabili di sostituzione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Variabili di sostituzione{#substitution-variables}

Le variabili di sostituzione vengono utilizzate per trasferire i valori dall’URL della richiesta ai modelli di composizione memorizzati nei cataloghi di immagini. Le variabili possono anche essere utilizzate per trasmettere lo stesso valore in posizioni diverse in una richiesta complessa.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome della variabile. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore a cui deve essere impostata la variabile (stringa). </p> </td> 
 </tr> 
</table>

Le definizioni delle variabili e i riferimenti possono verificarsi nella parte query della richiesta, in `catalog::Modifier`e in `catalog::PostModifier`.

Le variabili sono definite come sopra, simili ad altri comandi IS; il comando &#39;$&#39; iniziale identifica il comando come definizione di variabile. Prima di fare riferimento alle variabili, è necessario definirle.

Nome della variabile *`var`* non distingue tra maiuscole e minuscole e può consistere in una combinazione di lettere ASCII, numeri, &quot;-&quot;, &quot;_&quot; e &quot;.&quot;.

>[!NOTE]
>
>*`value`* devono essere codificati in URL a passa singolo per una trasmissione HTTP sicura. La doppia codifica è necessaria se *`value`* viene ritrasmesso tramite HTTP. Questo è il caso quando *`value`* viene sostituito in una richiesta esterna nidificata o nell&#39;attributo href di un SVG `<image>` elemento.

I riferimenti di variabile sono costituiti dal nome della variabile delimitato da &#39;$&#39; iniziale e finale ($)*var*$). I riferimenti possono verificarsi in qualsiasi punto della porzione di valore di qualsiasi comando IS (cioè tra il &#39;=&#39; che segue il nome del comando e il successivo &#39;&amp;&#39; o la fine della richiesta). Le variabili personalizzate non possono essere applicate al `layer=` e `effect=` comandi. Più variabili sono consentite nello stesso valore di comando. Il server sostituisce ogni occorrenza di ` $ *`var`*$` con *`value`*.

I riferimenti alle variabili potrebbero non essere nidificati. Qualsiasi occorrenza di ` $ *`var`*$` entro *`value`* non sono sostituiti.

Ad esempio, il frammento di richiesta:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

risolve in:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; non è un carattere riservato; potrebbe verificarsi altrimenti nella richiesta. Ad esempio: `src=my$image$file.tif` è un comando valido (supponendo che una voce di catalogo o un file immagine denominato `my$image$file.tif` esiste), mentre `wid=$number$` non è perché `wid` richiede un argomento numerico.

## Elaborazione delle variabili nelle richieste nidificate {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` i riferimenti possono verificarsi ovunque all’interno delle parentesi graffe di una richiesta Image Server o Image Rendering nidificata, inclusa a sinistra di &#39;?&#39; separazione del percorso dalla query. Il server sostituisce questi riferimenti con i valori (dall&#39;url o da `catalog::Modifier` del catalogo immagini principale) prima di analizzare ed elaborare ulteriormente la richiesta nidificata.

Inoltre, tutti ` $ *`var`*=` definizioni dall&#39;url o `catalog::Modifier` vengono inoltrate a tutte le richieste di Image Server e Image Rendering nidificate. In questo modo tutte le definizioni di variabili sono disponibili per tutti i modelli, indipendentemente dal livello di nidificazione.

Indipendentemente dal livello di nidificazione, ai valori variabili che devono essere sostituiti in qualsiasi punto delle richieste di Image Rendering o Image Server nidificate o associate deve essere applicata solo la codifica HTTP a passo singolo `catalog::Modifier` stringhe.

## Elaborazione variabile nelle richieste esterne incorporate {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` i riferimenti che si verificano in qualsiasi punto delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti dai valori di definizione della variabile corrispondenti. Questo consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili che devono essere sostituiti in richieste esterne in genere devono essere codificati in doppia codifica, poiché non viene applicata alcuna nuova codifica prima che il server tenti di trasmettere l’URL esterno finale.

## Elaborazione delle variabili nei file SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` i riferimenti possono verificarsi nei file SVG nei valori attributo e in `<text>` stringhe. Image Serving sostituisce questi con il corrispondente ` $ *`var`*=` definizioni note al livello di nidificazione della richiesta in cui è specificato il file SVG.

>[!NOTE]
>
>Qualsiasi valore di variabile che deve essere sostituito in un `href` il valore dell&#39;attributo deve essere codificato in doppio URL; tutti gli altri devono essere codificati singolarmente.

## Variabile di percorso predefinita {#section-930d0dd12e8f49499becc9fe8df24092}

La *`object`* specificato nel percorso della richiesta viene assegnato alla variabile predefinita `*`$object`*`. &#39; ` $ *`oggetto`*$`&#39; può essere posizionato ovunque nella richiesta, nel modello a cui fa riferimento la richiesta, o in una richiesta nidificata/incorporata in cui tale oggetto è consentito, compreso il valore di `src=` e `mask=`e il percorso di una richiesta nidificata/incorporata.

Ad esempio, la seguente richiesta riutilizzerà l’immagine specificata nel percorso come origine di un livello in una richiesta nidificata:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Equivale a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

La definizione di `*`$object`*` può essere ignorato specificando esplicitamente ` $ *`oggetto`*=` con il valore desiderato.

La variabile di percorso predefinita viene comunemente utilizzata insieme a `template=`.

## Predefinito {#section-b02483d15529444586a2e9504805b155}

Nessuno. Solo le variabili definite vengono sostituite dal server (ad eccezione della variabile di percorso predefinita $object, che sarà sempre sostituita). Qualsiasi occorrenza di ` $ *`var`*$` rimanere letterale se `*`var`*`impossibile trovare una corrispondenza con una definizione di variabile esistente.

## Esempi {#section-fba9393df6984247b7e30b3f93992e86}

Vedi &quot;Esempio A&quot; in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)

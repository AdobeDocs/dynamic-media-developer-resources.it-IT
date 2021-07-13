---
description: Le variabili di sostituzione vengono utilizzate per trasferire i valori dall’URL della richiesta ai modelli di composizione memorizzati nei cataloghi di immagini. Le variabili possono anche essere utilizzate per trasmettere lo stesso valore in posizioni diverse in una richiesta complessa.
solution: Experience Manager
title: Variabili di sostituzione
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Variabili di sostituzione{#substitution-variables}

Le variabili di sostituzione vengono utilizzate per trasferire i valori dall’URL della richiesta ai modelli di composizione memorizzati nei cataloghi di immagini. Le variabili possono anche essere utilizzate per trasmettere lo stesso valore in posizioni diverse in una richiesta complessa.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome della variabile. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore a cui deve essere impostata la variabile (stringa). </p> </td> 
 </tr> 
</table>

Le definizioni e i riferimenti delle variabili possono verificarsi nella parte query della richiesta, in `catalog::Modifier` e in `catalog::PostModifier`.

Le variabili sono definite come sopra, simili ad altri comandi IS; il comando &#39;$&#39; iniziale identifica il comando come definizione di variabile. Prima di fare riferimento alle variabili, è necessario definirle.

Il nome della variabile *`var`* non fa distinzione tra maiuscole e minuscole e può essere costituito da qualsiasi combinazione di lettere ASCII, numeri, &#39;-&#39;, &#39;_&#39; e &#39;.&#39;.

>[!NOTE]
>
>*`value`* devono essere codificati in URL a passa singolo per una trasmissione HTTP sicura. La doppia codifica è necessaria se *`value`* viene ritrasmessa tramite HTTP. Ciò si verifica quando *`value`* viene sostituito in una richiesta straniera nidificata o nell&#39;attributo href di un elemento SVG `<image>`.

I riferimenti delle variabili sono costituiti dal nome della variabile delimitato da &#39;$&#39; iniziale e finale ($*var*$). I riferimenti possono verificarsi in qualsiasi punto della porzione di valore di qualsiasi comando IS (cioè tra il &#39;=&#39; che segue il nome del comando e il successivo &#39;&amp;&#39; o la fine della richiesta). Le variabili personalizzate non possono essere applicate ai comandi `layer=` e `effect=`. Più variabili sono consentite nello stesso valore di comando. Il server sostituisce ogni occorrenza di ` $ *`var`*$` con *`value`*.

I riferimenti alle variabili potrebbero non essere nidificati. Eventuali occorrenze di ` $ *`var`*$` all&#39;interno di *`value`* non vengono sostituite.

Ad esempio, il frammento di richiesta:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

risolve in:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; non è un carattere riservato; potrebbe verificarsi altrimenti nella richiesta. Ad esempio, `src=my$image$file.tif` è un comando valido (supponendo che esista una voce di catalogo o un file immagine denominato `my$image$file.tif`), mentre `wid=$number$` non lo è, perché `wid` richiede un argomento numerico.

## Elaborazione delle variabili nelle richieste nidificate {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *``*$` i riferimenti varici possono verificarsi ovunque all’interno delle parentesi graffe di una richiesta Image Server o Image Rendering nidificata, inclusa a sinistra di &#39;?&#39; separazione del percorso dalla query. Il server sostituisce questi riferimenti con i valori (dall’url o da `catalog::Modifier` del catalogo immagini principale) prima di analizzare ed elaborare ulteriormente la richiesta nidificata.

Inoltre, tutte le definizioni ` $ *`var`*=` dall&#39;url o `catalog::Modifier` vengono inoltrate a tutte le richieste nidificate di Image Serving e Image Rendering. In questo modo tutte le definizioni di variabili sono disponibili per tutti i modelli, indipendentemente dal livello di nidificazione.

Indipendentemente dal livello di nidificazione, solo la codifica HTTP a passo singolo deve essere applicata ai valori delle variabili che devono essere sostituiti in qualsiasi punto delle richieste Image Rendering nidificate o Image Serving o delle relative stringhe `catalog::Modifier` associate.

## Elaborazione variabile nelle richieste esterne incorporate {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *``*$` i riferimenti che si verificano in qualsiasi punto delle parentesi graffe di una richiesta esterna incorporata sono sostituiti dai valori di definizione della variabile corrispondenti. Questo consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili che devono essere sostituiti in richieste esterne in genere devono essere codificati in doppia codifica, poiché non viene applicata alcuna nuova codifica prima che il server tenti di trasmettere l’URL esterno finale.

## Elaborazione variabile in file SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *``*$` i riferimenti varici possono verificarsi nei file SVG nei valori di attributo e nelle  `<text>` stringhe. Image Server le sostituisce con le definizioni ` $ *`var`*=` corrispondenti note al livello di nidificazione della richiesta in cui è specificato il file SVG.

>[!NOTE]
>
>Qualsiasi valore di variabile che deve essere sostituito in un valore di attributo `href` deve essere codificato in doppio URL; tutti gli altri devono essere codificati singolarmente.

## Variabile di percorso predefinita {#section-930d0dd12e8f49499becc9fe8df24092}

Il *`object`* specificato nel percorso della richiesta viene assegnato alla variabile predefinita `*`$object`*`. &#39; ` $ *`object`*$`&#39; può essere posizionato in qualsiasi punto della richiesta, nel modello a cui fa riferimento la richiesta o in una richiesta nidificata/incorporata in cui tale oggetto è consentito, compreso il valore di `src=` e `mask=` e il percorso di una richiesta nidificata/incorporata.

Ad esempio, la seguente richiesta riutilizzerà l’immagine specificata nel percorso come origine di un livello in una richiesta nidificata:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Equivale a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

È possibile ignorare la definizione di `*`$object`*` specificando esplicitamente ` $ *`object`*=` con il valore desiderato.

La variabile di percorso predefinita viene comunemente utilizzata insieme a `template=`.

## Predefinito {#section-b02483d15529444586a2e9504805b155}

Nessuno. Solo le variabili definite verranno sostituite dal server (ad eccezione della variabile di percorso predefinita $object, che sarà sempre sostituita). Qualsiasi occorrenza di ` $ *`var`*$` rimane letterale se `*`var`*`non può essere abbinata a una definizione di variabile esistente.

## Esempi {#section-fba9393df6984247b7e30b3f93992e86}

Vedere &quot;Esempio A&quot; in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)

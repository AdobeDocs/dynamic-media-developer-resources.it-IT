---
description: Le variabili di sostituzione vengono utilizzate per trasferire i valori dall’URL della richiesta ai modelli di composizione memorizzati nei cataloghi di immagini. Le variabili possono anche essere utilizzate per trasmettere lo stesso valore in posizioni diverse in una richiesta complessa.
solution: Experience Manager
title: Variabili di sostituzione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '736'
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
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valore </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore al quale deve essere impostata la variabile (stringa). </p> </td> 
 </tr> 
</table>

Definizioni di variabili e riferimenti possono verificarsi nella parte query della richiesta, in `catalog::Modifier` e in `catalog::PostModifier`.

Le variabili sono definite come sopra, in modo simile ad altri comandi IS; l&#39;iniziale &#39;$&#39; identifica il comando come definizione di variabile. Le variabili devono essere definite prima di essere referenziate.

Il nome della variabile *`var`* non fa distinzione tra maiuscole e minuscole e può essere costituito da qualsiasi combinazione di lettere ASCII, numeri, &quot;-&quot;, &quot;_&quot; e &quot;.&quot;.

>[!NOTE]
>
>*`value`* deve avere un URL con codifica single-pass per una trasmissione HTTP sicura. La doppia codifica è necessaria se *`value`* viene ritrasmesso tramite HTTP. Ciò si verifica quando *`value`* viene sostituito in una richiesta esterna nidificata o nell&#39;attributo href di un elemento SVG `<image>`.

I riferimenti di variabile sono costituiti dal nome della variabile delimitato da &#39;$&#39; iniziale e finale ($*var*$). I riferimenti possono verificarsi in qualsiasi punto della porzione di valore di qualsiasi comando IS, ovvero tra &#39;=&#39; dopo il nome del comando e il successivo &#39;&amp;&#39; o la fine della richiesta. Impossibile applicare variabili personalizzate ai comandi `layer=` e `effect=`. Più variabili sono consentite nello stesso valore di comando. Il server sostituisce ogni occorrenza di ` $ *`var`*$` con *`value`*.

I riferimenti di variabile non possono essere nidificati. Eventuali occorrenze di ` $ *`var`*$` in *`value`* non vengono sostituite.

Ad esempio, il frammento di richiesta:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

si risolve in:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; non è un carattere riservato. È possibile che la richiesta non contenga alcun carattere riservato. `src=my$image$file.tif`, ad esempio, è un comando valido (supponendo che esista una voce di catalogo o un file di immagine denominato `my$image$file.tif`), mentre `wid=$number$` non lo è, perché `wid` richiede un argomento numerico.

## Elaborazione delle variabili nelle richieste nidificate {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` i riferimenti possono verificarsi ovunque all&#39;interno delle parentesi graffe di una richiesta di Image Server o Image Rendering nidificata, anche a sinistra di &#39;?&#39; separazione del percorso dalla query. Il server sostituisce questi riferimenti con valori (provenienti dall&#39;URL o da `catalog::Modifier` del catalogo principale delle immagini) prima di analizzare ed elaborare ulteriormente la richiesta nidificata.

Inoltre, tutte le definizioni di ` $ *`var`*=` dall&#39;URL o `catalog::Modifier` vengono inoltrate a tutte le richieste nidificate di Image Server e Image Rendering. In questo modo tutte le definizioni di variabili sono disponibili per tutti i modelli, indipendentemente dal livello di nidificazione.

Indipendentemente dal livello di nidificazione, solo la codifica HTTP a passata singola deve essere applicata ai valori delle variabili che devono essere sostituiti in qualsiasi punto delle richieste di Image Rendering o Image Server nidificate o delle relative stringhe `catalog::Modifier` associate.

## Elaborazione delle variabili nelle richieste esterne incorporate {#section-314e39a9aefb46faa737fd137897d1b0}

I riferimenti ` $ *`var`*$` che si verificano in qualsiasi punto all&#39;interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti con valori di definizione della variabile corrispondenti. Questo consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili da sostituire in richieste esterne in genere devono avere una doppia codifica, poiché non viene applicata alcuna nuova codifica prima che il server tenti di trasmettere l’URL esterno finale.

## Elaborazione variabile in file SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` riferimenti possono verificarsi nei file SVG nei valori degli attributi e nelle stringhe `<text>`. Image Server sostituisce questi elementi con le definizioni ` $ *`var`*=` corrispondenti note al livello di nidificazione della richiesta in cui è specificato il file SVG.

>[!NOTE]
>
>Qualsiasi valore di variabile da sostituire in un valore di attributo `href` deve avere una doppia codifica URL; tutti gli altri devono avere una codifica singola.

## Variabile di percorso predefinita {#section-930d0dd12e8f49499becc9fe8df24092}

Il *`object`* specificato nel percorso della richiesta è assegnato alla variabile predefinita `*`$object`*`. &#39; ` $ *`object`*$`&#39; può trovarsi in qualsiasi punto della richiesta, nel modello a cui fa riferimento la richiesta o in una richiesta nidificata/incorporata in cui tale oggetto è consentito, inclusi il valore di `src=` e `mask=` e il percorso di una richiesta nidificata/incorporata.

Ad esempio, la seguente richiesta riutilizza l’immagine specificata nel percorso come origine di un livello in una richiesta nidificata:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Equivale a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

È possibile sovrascrivere la definizione di `*`$object`*` specificando esplicitamente ` $ *`object`*=` con il valore desiderato.

La variabile di percorso predefinita viene comunemente utilizzata insieme a `template=`.

## Predefinito {#section-b02483d15529444586a2e9504805b155}

Nessuno. Solo le variabili definite vengono sostituite dal server, ad eccezione della variabile di percorso predefinita $object, che viene sempre sostituita. Eventuali occorrenze di ` $ *`var`*$` rimangono letterali se `*`var`*`non corrispondono a una definizione di variabile esistente.

## Esempi {#section-fba9393df6984247b7e30b3f93992e86}

Vedi &quot;Esempio A&quot; in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [modello=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)

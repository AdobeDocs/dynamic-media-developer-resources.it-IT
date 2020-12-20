---
description: Image Rendering supporta un semplice meccanismo di pre-elaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.
seo-description: Image Rendering supporta un semplice meccanismo di pre-elaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.
seo-title: Riferimento set di regole
solution: Experience Manager
title: Riferimento set di regole
topic: Scene7 Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---


# Riferimento set di regole{#rule-set-reference}

Image Rendering supporta un semplice meccanismo di pre-elaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Le raccolte di regole di pre-elaborazione (*set di regole*) possono essere collegate ai cataloghi dei materiali o al catalogo predefinito. Le regole nel catalogo predefinito si applicano solo se la richiesta non allega un catalogo materiale specifico.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dall&#39;analizzatore delle richieste del server, compresa la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono essere utilizzate anche per configurare e ignorare alcuni attributi del catalogo, nonché per limitare il servizio a specifici indirizzi IP client.

I set di regole sono memorizzati come file di documento XML. Il percorso relativo o assoluto del file del set di regole deve essere specificato in `attribute::RuleSetFile`.

## Struttura generale {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
<ruleset>
   <rule>
      <expression>
<varname>
  expression
</varname></expression>
      <substitution>
<varname>
  substitution
</varname></substitution>
      <addressfilter>
<varname>
  addressFilter
</varname></addressfilter>
   </rule>
</ruleset>
```

Gli elementi `<?xml>`, `<!DOCTYPE>` e `<ruleset>` sono sempre richiesti in un file XML di set di regole valido, anche se non sono definite regole effettive.

È consentito un elemento `<ruleset>` contenente un numero qualsiasi di elementi `<rule>`.

I contenuti dei file delle regole di pre-elaborazione sono con distinzione tra maiuscole e minuscole.

## Pre-elaborazione URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Prima di qualsiasi altra elaborazione, una richiesta HTTP in entrata viene analizzata in parte per determinare quale catalogo di materiali applicare. Una volta identificato il catalogo, viene applicato il set di regole per il catalogo selezionato (o per il catalogo predefinito, se non è stato identificato alcun catalogo specifico).

La ricerca degli elementi `<rule>` avviene nell&#39;ordine specificato per trovare una corrispondenza con il contenuto dell&#39;elemento `<expression>` ( *`expression`*).

Se viene rilevata una corrispondenza tra `<rule>`, viene applicata l&#39;opzione *`substitution`* e la stringa di richiesta modificata viene passata al parser di richieste del server per una normale elaborazione.

Se non viene eseguita alcuna corrispondenza valida quando viene raggiunta la fine del `<ruleset>`, la richiesta viene trasmessa al parser senza modifiche.

## L&#39;attributo OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Il comportamento predefinito può essere modificato con l&#39;attributo `OnMatch` degli elementi `<rule>`. `OnMatch` può essere impostato su  `break` (predefinito),  `continue`oppure  `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elemento e attributo </p> </th> 
   <th colname="col2" class="entry"> <p>Comportamento quando si verifica una corrispondenza </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>L'elaborazione della regola viene terminata immediatamente dopo l'applicazione della sostituzione per questa regola. Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>La sostituzione viene applicata e l'elaborazione continua con la regola successiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>L'elaborazione della regola viene terminata immediatamente e lo stato di risposta della richiesta rifiutata viene restituito al client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sostituzione degli attributi del catalogo {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` gli elementi possono anche definire attributi che ignorano gli attributi del catalogo corrispondenti quando la regola viene rilevata e  `OnMatch="break"` impostata correttamente. Non vengono applicati attributi se è impostato `OnMatch="continue"`. Fare riferimento alla descrizione di `<rule>` per un elenco di attributi che possono essere controllati con le regole.

## Espressioni regolari {#section-4d326507b52544b0960a9a5f303e3fe6}

La semplice corrispondenza delle stringhe funziona per applicazioni molto semplici, ma nella maggior parte dei casi sono necessarie espressioni regolari. Sebbene le espressioni regolari siano standard di settore, l&#39;implementazione specifica varia da un&#39;istanza all&#39;altra.

[package java.util.](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) regexdescrive l’implementazione specifica delle espressioni regolari utilizzate da Image Server.

## Sottostringhe acquisite {#section-8057cd65d48949ffb6a50e929bd3688b}

Per semplificare complesse modifiche agli URL, nell&#39;espressione possono essere acquisite delle sottostringhe racchiudendo la sottostringa con parentesi (...). Le sottostringhe acquisite vengono numerate in sequenza a partire da 1 in base alla posizione delle parentesi iniziali. Le sottostringhe acquisite possono essere inserite nella sostituzione utilizzando *`$n`*, dove *`n`* è il numero di sequenza della sottostringa acquisita.

## Gestione dei file di set di regole {#section-e8ce976b56404c009496426fd334d23d}

È possibile allegare un file set di regole a ciascun catalogo di materiali con l&#39;attributo di catalogo `attribute::RuleSetFile`. Anche se potete modificare il file del set di regole in qualsiasi momento, il server immagini riconosce le modifiche solo quando il catalogo materiale associato viene ricaricato. Ciò si verifica quando il server della piattaforma viene avviato o riavviato e ogni volta che il file del catalogo principale (con un suffisso di file [!DNL .ini]) viene modificato o toccato (per modificare la data del file).

## Esempi {#section-c4142a41f5cd4ff799a72fbc130c3700}

Gli esempi di set di regole sono forniti nella sezione corrispondente del Riferimento per il catalogo immagini nella documentazione di Image Server.

## Consultate anche {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

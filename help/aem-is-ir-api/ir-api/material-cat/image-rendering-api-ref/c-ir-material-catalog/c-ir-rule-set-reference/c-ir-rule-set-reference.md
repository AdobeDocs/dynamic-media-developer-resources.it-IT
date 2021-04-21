---
description: Image Rendering supporta un semplice meccanismo di pre-elaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.
solution: Experience Manager
title: Riferimento set di regole
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 0%

---


# Riferimento set di regole{#rule-set-reference}

Image Rendering supporta un semplice meccanismo di pre-elaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Le raccolte di regole di pre-elaborazione (*set di regole*) possono essere collegate ai cataloghi di materiali o al catalogo predefinito. Le regole nel catalogo predefinito si applicano solo se la richiesta non allega un catalogo di materiali specifico.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser di richieste del server, inclusa la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. È inoltre possibile utilizzare le regole per configurare e sostituire alcuni attributi del catalogo, nonché per limitare il servizio a specifici indirizzi IP del client.

I set di regole vengono memorizzati come file di documento XML. Il percorso relativo o assoluto del file del set di regole deve essere specificato in `attribute::RuleSetFile`.

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

Gli elementi `<?xml>`, `<!DOCTYPE>` e `<ruleset>` sono sempre necessari in un file XML di set di regole valido, anche se non sono definite regole effettive.

È consentito un elemento `<ruleset>` contenente un numero qualsiasi di elementi `<rule>`.

I contenuti dei file delle regole di preelaborazione sono sensibili all’uso di maiuscole e minuscole.

## Pre-elaborazione URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Prima di qualsiasi altra elaborazione, una richiesta HTTP in arrivo viene analizzata in parte per determinare quale catalogo di materiali applicare. Una volta identificato il catalogo, viene applicato il set di regole per il catalogo selezionato (o per il catalogo predefinito, se non è stato identificato alcun catalogo specifico).

Gli elementi `<rule>` vengono ricercati nell’ordine specificato per trovare una corrispondenza con il contenuto dell’elemento `<expression>` ( *`expression`*).

Se viene rilevata una corrispondenza a `<rule>`, viene applicato l&#39;facoltativo *`substitution`* e la stringa di richiesta modificata viene passata al parser di richiesta del server per una normale elaborazione.

Se non viene effettuata alcuna corrispondenza corretta quando viene raggiunta la fine del `<ruleset>`, la richiesta viene trasmessa al parser senza modifiche.

## Attributo OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Il comportamento predefinito può essere modificato con l’attributo `OnMatch` degli elementi `<rule>` . `OnMatch` può essere impostato su  `break` (predefinito),  `continue`, oppure  `error.`

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
   <td colname="col2"> <p>L'elaborazione delle regole viene terminata immediatamente dopo l'applicazione della sostituzione di questa regola. Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>La sostituzione viene applicata e l'elaborazione continua con la regola successiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>L'elaborazione delle regole viene terminata immediatamente e lo stato di risposta "richiesta rifiutata" viene restituito al client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sovrascrittura degli attributi del catalogo {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` facoltativamente, gli elementi possono definire attributi che sovrascrivono gli attributi del catalogo corrispondenti quando la regola viene confrontata correttamente e  `OnMatch="break"` impostata. Se è impostato `OnMatch="continue"`, non vengono applicati attributi. Fai riferimento alla descrizione di `<rule>` per un elenco di attributi che possono essere controllati con le regole.

## Espressioni regolari {#section-4d326507b52544b0960a9a5f303e3fe6}

La corrispondenza semplice delle stringhe funziona per applicazioni molto semplici, ma nella maggior parte delle istanze sono necessarie espressioni regolari. Anche se le espressioni regolari sono standard di settore, l&#39;implementazione specifica varia da un&#39;istanza all&#39;altra.

[package java.util.](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) regexdescrive l&#39;implementazione specifica delle espressioni regolari utilizzata da Image Server.

## Sottostringhe acquisite {#section-8057cd65d48949ffb6a50e929bd3688b}

Per facilitare modifiche complesse all’URL, le sottostringhe possono essere acquisite nell’espressione racchiudendo la sottostringa con parentesi (...). Le sottostringhe acquisite vengono numerate in sequenza a partire da 1 in base alla posizione della parentesi iniziale. Le sottostringhe acquisite possono essere inserite nella sostituzione utilizzando *`$n`*, dove *`n`* è il numero di sequenza della sottostringa acquisita.

## Gestione dei file dei set di regole {#section-e8ce976b56404c009496426fd334d23d}

Un file set di regole può essere allegato a ciascun catalogo di materiali con l&#39;attributo di catalogo `attribute::RuleSetFile`. Mentre è possibile modificare il file del set di regole in qualsiasi momento, il server di immagini riconosce le modifiche solo quando il catalogo del materiale associato viene ricaricato. Questo accade quando Platform Server viene avviato o riavviato e ogni volta che il file di catalogo principale (con un suffisso di file [!DNL .ini]) viene modificato o &quot;toccato&quot; (per modificare la data del file).

## Esempi {#section-c4142a41f5cd4ff799a72fbc130c3700}

Gli esempi di set di regole sono forniti nella sezione corrispondente del Riferimento al catalogo immagini nella documentazione Image Serving .

## Consultate anche {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[pacchetto java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

---
description: Image Rendering supporta un meccanismo di pre-elaborazione delle richieste semplice basato su regole di corrispondenza e sostituzione delle espressioni regolari.
solution: Experience Manager
title: Riferimento set di regole
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# Riferimento set di regole{#rule-set-reference}

Image Rendering supporta un meccanismo di pre-elaborazione delle richieste semplice basato su regole di corrispondenza e sostituzione delle espressioni regolari.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Raccolte di regole di pre-elaborazione (*set di regole*) può essere allegato ai cataloghi di materiale o al catalogo predefinito. Le regole del catalogo predefinito vengono applicate solo se la richiesta non allega un catalogo dei materiali specifico.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser di richieste del server, ad esempio la modifica del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono essere utilizzate anche per configurare ed eseguire l’override di alcuni attributi di catalogo, nonché per limitare il servizio a indirizzi IP client specifici.

I set di regole vengono memorizzati come file di documenti XML. Il percorso relativo o assoluto del file del set di regole deve essere specificato in `attribute::RuleSetFile`.

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

Il `<?xml>`, `<!DOCTYPE>` e `<ruleset>` Gli elementi sono sempre necessari in un file XML di set di regole valido, anche se non sono definite regole effettive.

Uno `<ruleset>` elemento contenente un numero qualsiasi di `<rule>` sono consentiti.

Il contenuto dei file delle regole di pre-elaborazione fa distinzione tra maiuscole e minuscole.

## Pre-elaborazione URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Prima di qualsiasi altra elaborazione, viene parzialmente analizzata una richiesta HTTP in ingresso per determinare quale catalogo dei materiali applicare. Una volta identificato il catalogo, viene applicato il set di regole per il catalogo selezionato (o il catalogo predefinito, se non è stato identificato alcun catalogo specifico).

Il `<rule>` Gli elementi vengono cercati nell&#39;ordine specificato per una corrispondenza con il contenuto del `<expression>` elemento ( *`expression`*).

Se un `<rule>` corrisponde, l&#39;opzione *`substitution`* viene applicata e la stringa di richiesta modificata viene passata al parser di richieste del server per la normale elaborazione.

Se non viene trovata alcuna corrispondenza corretta quando la fine del `<ruleset>` viene raggiunto, la richiesta viene passata al parser senza modifiche.

## Attributo OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Il comportamento predefinito può essere modificato con `OnMatch` attributo del `<rule>` elementi. `OnMatch` può essere impostato su `break` (impostazione predefinita), `continue`, o `error.`

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
   <td colname="col2"> <p>L'elaborazione delle regole viene terminata immediatamente dopo l'applicazione della sostituzione per questa regola. Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>La sostituzione viene applicata e l’elaborazione continua con la regola successiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>L’elaborazione delle regole viene interrotta immediatamente e al client viene restituito lo stato di risposta "richiesta rifiutata". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ignorare gli attributi del catalogo {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` Gli elementi possono facoltativamente definire attributi che sostituiscono gli attributi di catalogo corrispondenti quando la regola viene trovata correttamente e `OnMatch="break"` è impostato. Non vengono applicati attributi se `OnMatch="continue"` è impostato. Fai riferimento alla descrizione di `<rule>` per un elenco di attributi che possono essere controllati tramite regole.

## Espressioni regolari {#section-4d326507b52544b0960a9a5f303e3fe6}

La corrispondenza delle stringhe semplice funziona per applicazioni molto semplici, ma nella maggior parte dei casi sono necessarie espressioni regolari. Anche se le espressioni regolari sono standard di settore, l’implementazione specifica varia da un’istanza all’altra.

[pacchetto java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) descrive l’implementazione specifica di espressioni regolari utilizzata da Image Server.

## Sottostringhe acquisite {#section-8057cd65d48949ffb6a50e929bd3688b}

Per facilitare modifiche URL complesse, è possibile acquisire sottostringhe nell’espressione racchiudendo la sottostringa tra parentesi (...). Le sottostringhe acquisite vengono numerate in sequenza iniziando da 1 in base alla posizione delle parentesi iniziali. Le sottostringhe acquisite possono essere inserite nella sostituzione utilizzando *`$n`*, dove *`n`* è il numero di sequenza della sottostringa acquisita.

## Gestione dei file del set di regole {#section-e8ce976b56404c009496426fd334d23d}

È possibile allegare un file di set di regole a ciascun catalogo di materiali con l&#39;attributo catalogo `attribute::RuleSetFile`. Sebbene sia possibile modificare il file del set di regole in qualsiasi momento, il server immagini riconosce le modifiche solo quando il catalogo dei materiali associato viene ricaricato. Ciò si verifica quando [!DNL Platform Server] viene avviato o riavviato e ogni volta che il file di catalogo principale (che [!DNL .ini] suffisso del file) è stato modificato o &quot;toccato&quot; (per modificare la data del file).

## Esempi {#section-c4142a41f5cd4ff799a72fbc130c3700}

Gli esempi di set di regole sono forniti nella sezione corrispondente della documentazione Image Server della documentazione di Image Catalog.

## Consultate anche {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[pacchetto java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

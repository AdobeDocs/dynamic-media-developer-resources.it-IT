---
description: Image Serving supporta un semplice meccanismo di preelaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.
solution: Experience Manager
title: Riferimento set di regole
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# Riferimento set di regole{#rule-set-reference}

Image Serving supporta un semplice meccanismo di preelaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.

Le raccolte di regole di pre-elaborazione (*set di regole*) possono essere collegate ai cataloghi di immagini o al catalogo predefinito. Le regole nel catalogo predefinito si applicano solo se la richiesta non identifica un catalogo di immagini principale specifico.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser di Platform Server, inclusa la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. È inoltre possibile utilizzare le regole per configurare e sostituire determinate funzioni di sicurezza che sono normalmente controllate solo con attributi di catalogo, come l’offuscamento della richiesta, il watermarking e la limitazione del servizio a specifici indirizzi IP del client.

I set di regole vengono memorizzati come file di documento XML. Il percorso relativo o assoluto del file del set di regole deve essere specificato in `attribute::RuleSetFile`.

## Struttura generale {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
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
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

Gli elementi `<?xml>` e `<ruleset>` sono sempre necessari in un file XML di set di regole valido, anche se non sono definite regole effettive.

È consentito un elemento `<ruleset>` contenente un numero qualsiasi di elementi `<rule>`.

I contenuti dei file delle regole di preelaborazione sono sensibili all’uso di maiuscole e minuscole.

## Convalida set di regole {#section-d8d101a0b4d74580835e37d128d05567}

Una copia di [!DNL RuleSet.xsd] viene fornita nella cartella del catalogo e deve essere utilizzata per convalidare un file ruleset prima di registrarlo nel file [!DNL catalog.ini]. Image Server utilizza una copia interna di [!DNL RuleSet.xsd] per la convalida.

## Pre-elaborazione URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Prima di qualsiasi altra elaborazione, una richiesta HTTP in arrivo viene analizzata in parte per determinare quale catalogo immagini applicare. Una volta identificato il catalogo, viene applicato il set di regole per il catalogo selezionato (o per il catalogo predefinito, se non è stato identificato alcun catalogo specifico).

Gli elementi `<rule>` vengono ricercati nell’ordine specificato per trovare una corrispondenza con il contenuto dell’elemento `<expression>` ( *`expression`*).

Se viene rilevata una corrispondenza a `<rule>`, viene applicato l&#39;facoltativo *`substitution`* e la stringa di richiesta modificata viene passata al parser di richiesta del server per una normale elaborazione.

Se non viene effettuata alcuna corrispondenza corretta quando viene raggiunta la fine del `<ruleset>`, la richiesta viene trasmessa al parser senza modifiche.

## Attributo OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Il comportamento predefinito può essere modificato con l’attributo `OnMatch` dell’elemento `<rule>` . `OnMatch` può essere impostato su  `break` (predefinito),  `continue`, o  `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Elemento e attributo</b> </th> 
   <th class="entry"> <b>Comportamento quando si verifica una corrispondenza</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>L'elaborazione delle regole viene terminata immediatamente dopo l'applicazione della sostituzione di questa regola. Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>La sostituzione viene applicata e l'elaborazione continua con la regola successiva. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>L'elaborazione delle regole viene terminata immediatamente e lo stato di risposta "richiesta rifiutata" viene restituito al client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sovrascrittura degli attributi del catalogo {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` facoltativamente, gli elementi possono definire attributi che sovrascrivono gli attributi del catalogo corrispondenti quando la regola viene confrontata correttamente. Se più regole di corrispondenza impostano lo stesso attributo, l&#39;ultimo prevale. Fai riferimento alla descrizione dell’elemento ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` per un elenco di attributi che possono essere controllati con le regole.

## Espressioni regolari {#section-3f77bb9a265147b38c645f63ab1bad8b}

La corrispondenza semplice delle stringhe funziona per applicazioni molto semplici, ma nella maggior parte delle istanze sono necessarie espressioni regolari. Anche se le espressioni regolari sono standard di settore, l&#39;implementazione specifica varia da un&#39;istanza all&#39;altra.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) descrive l&#39;implementazione specifica delle espressioni regolari utilizzate da Image Serving.

## Sottostringhe acquisite {#section-066e659406d5403599cd26ae35e80d68}

Per facilitare modifiche complesse all’URL, le sottostringhe possono essere acquisite nell’espressione racchiudendo la sottostringa con parentesi (...). Le sottostringhe acquisite vengono numerate in sequenza a partire da 1 in base alla posizione della parentesi iniziale. Le sottostringhe acquisite possono essere inserite nella sostituzione utilizzando ` $ *`n`*`, dove *`n`* è il numero di sequenza della sottostringa acquisita.

## Gestione dei file dei set di regole {#section-0598a608e4044bb4805fe93ceebe10a9}

È possibile allegare un file set di regole a ciascun catalogo di immagini con l&#39;attributo di catalogo `attribute::RuleSetFile`. Anche se è possibile modificare il file del set di regole in qualsiasi momento, il server di immagini riconosce le modifiche solo quando il catalogo di immagini associato viene ricaricato. Questo ricaricamento avviene quando il server della piattaforma viene avviato o riavviato e ogni volta che il file del catalogo principale, che ha un suffisso di file [!DNL .ini], viene modificato o &quot;toccato&quot; per modificare la data del file.

## Esempi {#section-aa769437d967459299b83a4bf34fe924}

**Esempio A.** Definisci una regola che aumenti le impostazioni di qualità dell&#39;immagine se il nome dell&#39;immagine ha il suffisso &quot;  [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

L&#39;espressione della regola specifica una corrispondenza senza distinzione tra maiuscole e minuscole di &quot; [!DNL _hg]&quot; alla fine della stringa URL. Il suffisso viene sostituito dalla stringa di query specificata che modifica le impostazioni di qualità dell&#39;immagine. Il carattere `?` nella stringa di sostituzione è preceduto da un carattere speciale nelle espressioni regolari.

>[!NOTE]
>
>Codifica necessaria per il carattere e commerciale. In alternativa, la stringa di sostituzione può essere racchiusa in un blocco CDATA:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Esempio B.** Una particolare applicazione web non consente stringhe di query. Definire una regola che traduca l&#39;elemento del percorso finale `small`, `medium` o `large` in un modello, utilizzando il resto del percorso come nome dell&#39;immagine. Ad esempio, `myCat/myImage/small` viene convertito in `myCat/smallTemplate?src=myCat/myImage`.

È possibile utilizzare le sottostringhe per ristrutturare la richiesta:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Consultate anche {#section-9b748e7c5cff4759a70f96657bd43352}

[pacchetto java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

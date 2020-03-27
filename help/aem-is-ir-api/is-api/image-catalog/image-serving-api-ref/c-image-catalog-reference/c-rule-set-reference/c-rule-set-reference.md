---
description: Image Serving supporta un semplice meccanismo di preelaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.
seo-description: Image Serving supporta un semplice meccanismo di preelaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.
seo-title: Riferimento set di regole
solution: Experience Manager
title: Riferimento set di regole
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Riferimento set di regole{#rule-set-reference}

Image Serving supporta un semplice meccanismo di preelaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.

Le raccolte di regole di pre-elaborazione (set *di* regole) possono essere collegate ai cataloghi di immagini o al catalogo predefinito. Le regole nel catalogo predefinito si applicano solo se la richiesta non identifica uno specifico catalogo immagini principale.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima di essere elaborate dal parser del server della piattaforma, compresa la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono essere utilizzate anche per configurare e ignorare alcune funzioni di sicurezza che normalmente sono controllate solo con gli attributi del catalogo, come l&#39;offuscamento della richiesta, l&#39;indicazione dell&#39;acqua, nonché per limitare il servizio a specifici indirizzi IP del client.

I set di regole sono memorizzati come file di documento XML. Il percorso relativo o assoluto del file set di regole deve essere specificato in `attribute::RuleSetFile`.

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

Gli elementi `<?xml>` e `<ruleset>` sono sempre richiesti in un file XML con set di regole valido, anche se non sono definite regole effettive.

È consentito un `<ruleset>` elemento contenente un numero qualsiasi di `<rule>` elementi.

I contenuti dei file delle regole di pre-elaborazione sono con distinzione tra maiuscole e minuscole.

## Convalida del set di regole {#section-d8d101a0b4d74580835e37d128d05567}

Una copia di [!DNL RuleSet.xsd] viene fornita nella cartella del catalogo e deve essere utilizzata per convalidare un file ruleset prima di registrarlo nel [!DNL catalog.ini] file. Image Server utilizza una copia interna di [!DNL RuleSet.xsd] per la convalida.

## Pre-elaborazione URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Prima di qualsiasi altra elaborazione, una richiesta HTTP in entrata viene analizzata in parte per determinare quale catalogo immagini applicare. Una volta identificato il catalogo, viene applicato il set di regole per il catalogo selezionato (o per il catalogo predefinito, se non è stato identificato alcun catalogo specifico).

La ricerca `<rule>` degli elementi viene eseguita nell&#39;ordine specificato per trovare una corrispondenza con il contenuto dell&#39; `<expression>` elemento ( *`expression`*).

Se `<rule>` viene rilevata una corrispondenza, *`substitution`* viene applicata l&#39;opzione facoltativa e la stringa di richiesta modificata viene passata al parser di richieste del server per una normale elaborazione.

Se non viene trovata alcuna corrispondenza valida al raggiungimento della fine del `<ruleset>` test, la richiesta viene trasmessa al parser senza modifiche.

## L’attributo OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Il comportamento predefinito può essere modificato con l&#39; `OnMatch` attributo dell&#39; `<rule>` elemento. `OnMatch` può essere impostato su `break` (predefinito), `continue`o `error`.

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
   <td> <p>L'elaborazione della regola viene terminata immediatamente dopo l'applicazione della sostituzione per questa regola. Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>La sostituzione viene applicata e l'elaborazione continua con la regola successiva. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>L'elaborazione della regola viene terminata immediatamente e lo stato di risposta della richiesta rifiutata viene restituito al client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sostituzione degli attributi del catalogo {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` facoltativamente, gli elementi possono definire attributi che ignorano gli attributi del catalogo corrispondenti quando la regola viene rilevata correttamente. Se più regole associate impostano lo stesso attributo, prevale l&#39;ultimo. Fare riferimento alla descrizione dell&#39; ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` elemento per un elenco di attributi che possono essere controllati con le regole.

## Espressioni regolari {#section-3f77bb9a265147b38c645f63ab1bad8b}

La semplice corrispondenza delle stringhe funziona per applicazioni molto semplici, ma nella maggior parte dei casi sono necessarie espressioni regolari. Sebbene le espressioni regolari siano standard di settore, l&#39;implementazione specifica varia da un&#39;istanza all&#39;altra.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) descrive l&#39;implementazione specifica dell&#39;espressione regolare utilizzata da Image Server.

## Sottostringhe acquisite {#section-066e659406d5403599cd26ae35e80d68}

Per semplificare complesse modifiche agli URL, nell&#39;espressione possono essere acquisite delle sottostringhe racchiudendo la sottostringa con parentesi (...). Le sottostringhe acquisite vengono numerate in sequenza a partire da 1 in base alla posizione delle parentesi iniziali. Le sottostringhe acquisite possono essere inserite nella sostituzione utilizzando ` $ *`n`*`, dove *`n`* è il numero di sequenza della sottostringa acquisita.

## Gestione dei file set di regole {#section-0598a608e4044bb4805fe93ceebe10a9}

È possibile allegare un file set di regole a ciascun catalogo di immagini con l’attributo catalogo `attribute::RuleSetFile`. Anche se potete modificare il file del set di regole in qualsiasi momento, il server immagini riconosce le modifiche solo quando il catalogo immagini associato viene ricaricato. Questo ricaricamento avviene quando il server della piattaforma viene avviato o riavviato e ogni volta che il file del catalogo primario, con un suffisso di [!DNL .ini] file, viene modificato o &quot;toccato&quot; per modificare la data del file.

## Esempi {#section-aa769437d967459299b83a4bf34fe924}

**Esempio A.** Definite una regola che aumenta le impostazioni di qualità dell’immagine se il nome dell’immagine ha il suffisso &quot; [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

L&#39;espressione regola specifica una corrispondenza senza distinzione tra maiuscole e minuscole di &quot; [!DNL _hg]&quot; alla fine della stringa URL. Il suffisso viene sostituito con la stringa di query specificata che modifica le impostazioni di qualità dell&#39;immagine. Tenere presente che il `?` carattere nella stringa di sostituzione è preceduto da un carattere speciale nelle espressioni regolari.

>[!NOTE]
>
>Codifica richiesta per il carattere e commerciale. In alternativa, è possibile racchiudere la stringa di sostituzione in un blocco CDATA:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Esempio B.** Una particolare applicazione Web non consente le stringhe di query. Definite una regola che traduca l’elemento del percorso finale `small`, `medium`o `large` in un modello, utilizzando il resto del percorso come nome dell’immagine. Ad esempio, `myCat/myImage/small` si tradurrebbe in `myCat/smallTemplate?src=myCat/myImage`.

È possibile utilizzare le sottostringhe per ristrutturare la richiesta:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Consultate anche {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

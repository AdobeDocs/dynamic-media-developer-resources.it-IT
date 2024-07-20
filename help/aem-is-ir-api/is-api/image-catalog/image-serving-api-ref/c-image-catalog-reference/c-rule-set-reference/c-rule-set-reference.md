---
description: Image Server supporta un semplice meccanismo di preelaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.
solution: Experience Manager
title: Riferimento set di regole
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Riferimento set di regole{#rule-set-reference}

Image Server supporta un semplice meccanismo di preelaborazione delle richieste basato su regole di corrispondenza e sostituzione delle espressioni regolari.

Raccolte di regole di pre-elaborazione (*set di regole*) possono essere collegate ai cataloghi di immagini o al catalogo predefinito. Le regole del catalogo predefinito si applicano solo se la richiesta non identifica un catalogo principale di immagini specifico.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e eseguire query su parti delle richieste prima che vengano elaborate dal parser di [!DNL Platform Server], inclusa la modifica del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono essere utilizzate anche per configurare e ignorare alcune funzioni di sicurezza che di solito sono controllate solo con attributi di catalogo, come offuscamento delle richieste, watermark, nonché per limitare il servizio a specifici indirizzi IP client.

I set di regole vengono memorizzati come file di documenti XML. Il percorso relativo o assoluto del file del set di regole deve essere specificato in `attribute::RuleSetFile`.

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

Il contenuto dei file delle regole di preelaborazione distingue tra maiuscole e minuscole.

## Convalida set di regole {#section-d8d101a0b4d74580835e37d128d05567}

Una copia di [!DNL RuleSet.xsd] è fornita nella cartella del catalogo e deve essere utilizzata per convalidare un file del set di regole prima di registrarlo nel file [!DNL catalog.ini]. Image Server utilizza una copia interna di [!DNL RuleSet.xsd] per la convalida.

## Pre-elaborazione URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Prima di qualsiasi altra elaborazione, viene parzialmente analizzata una richiesta HTTP in ingresso per determinare quale catalogo immagini applicare. Una volta identificato il catalogo, viene applicato il set di regole per il catalogo selezionato (o il catalogo predefinito, se non è stato identificato alcun catalogo specifico).

Gli elementi `<rule>` vengono cercati nell&#39;ordine specificato per trovare una corrispondenza con il contenuto dell&#39;elemento `<expression>` ( *`expression`*).

Se viene trovata una corrispondenza per `<rule>`, viene applicato l&#39;elemento facoltativo *`substitution`* e la stringa di richiesta modificata viene passata al parser di richieste del server per la normale elaborazione.

Se non viene stabilita una corrispondenza corretta quando viene raggiunta la fine di `<ruleset>`, la richiesta viene passata al parser senza modifiche.

## Attributo OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

È possibile modificare il comportamento predefinito con l&#39;attributo `OnMatch` dell&#39;elemento `<rule>`. `OnMatch` può essere impostato su `break` (impostazione predefinita), `continue` o `error`.

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
   <td> <p>L'elaborazione delle regole viene terminata immediatamente dopo l'applicazione della sostituzione per questa regola. Impostazione predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;regola OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>La sostituzione viene applicata e l’elaborazione continua con la regola successiva. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;regola OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>L’elaborazione delle regole viene interrotta immediatamente e al client viene restituito lo stato di risposta "richiesta rifiutata". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ignorare gli attributi del catalogo {#section-3f1e33a65c5346d1b4a69958c61432f3}

L&#39;elemento `rule` può facoltativamente definire attributi che sostituiscono gli attributi di catalogo corrispondenti quando la regola viene trovata correttamente corrispondente. Se più regole corrispondenti impostano lo stesso attributo, prevale l’ultimo. Per un elenco di attributi controllabili tramite regole, vedere l&#39;elemento [rule](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md).

## Espressioni regolari {#section-3f77bb9a265147b38c645f63ab1bad8b}

La corrispondenza delle stringhe semplice funziona per applicazioni molto semplici, ma nella maggior parte dei casi sono necessarie espressioni regolari. Anche se le espressioni regolari sono standard di settore, l’implementazione specifica varia da un’istanza all’altra.

[[!DNL package java.util.regex]](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) descrive l&#39;implementazione specifica delle espressioni regolari utilizzata da Image Server.

## Sottostringhe acquisite {#section-066e659406d5403599cd26ae35e80d68}

Per facilitare modifiche URL complesse, è possibile acquisire sottostringhe nell’espressione racchiudendo la sottostringa tra parentesi (...). Le sottostringhe acquisite vengono numerate in sequenza iniziando da 1 in base alla posizione delle parentesi iniziali. Le sottostringhe acquisite possono essere inserite nella sostituzione utilizzando ` $ *`n`*`, dove *`n`* è il numero di sequenza della sottostringa acquisita.

## Gestione dei file del set di regole {#section-0598a608e4044bb4805fe93ceebe10a9}

È possibile allegare un file di set di regole a ogni catalogo immagini con l&#39;attributo di catalogo `attribute::RuleSetFile`. Anche se è possibile modificare il file del set di regole in qualsiasi momento, il server immagini riconosce le modifiche solo quando il catalogo immagini associato viene ricaricato. Questo ricaricamento si verifica all&#39;avvio o al riavvio del server Platform e ogni volta che il file di catalogo primario, con suffisso di file [!DNL .ini], viene modificato o &quot;toccato&quot; per modificare la data del file.

## Esempi {#section-aa769437d967459299b83a4bf34fe924}

**Esempio A.** Definisci una regola che aumenti le impostazioni di qualità dell&#39;immagine se il nome dell&#39;immagine ha il suffisso &quot; [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

L&#39;espressione della regola specifica una corrispondenza senza distinzione tra maiuscole e minuscole di &quot; [!DNL _hg]&quot; alla fine della stringa URL. Il suffisso viene sostituito con la stringa di query specificata che modifica le impostazioni di qualità dell&#39;immagine. Si noti che il carattere `?` nella stringa di sostituzione ha escape, in quanto si tratta di un carattere speciale nelle espressioni regolari.

>[!NOTE]
>
>La codifica richiesta per il carattere e commerciale. In alternativa, la stringa di sostituzione potrebbe essere racchiusa in un blocco CDATA:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Esempio B.** Una particolare applicazione Web non consente stringhe di query. Definire una regola che converta l&#39;elemento del percorso finale `small`, `medium` o `large` in un modello, utilizzando il resto del percorso come nome dell&#39;immagine. `myCat/myImage/small`, ad esempio, tradurrebbe in `myCat/smallTemplate?src=myCat/myImage`.

È possibile utilizzare le sottostringhe per ristrutturare la richiesta:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Consultate anche {#section-9b748e7c5cff4759a70f96657bd43352}

[pacchetto java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

---
description: Elemento pattern con espressione regolare. Facoltativo negli elementi <rule>.
seo-description: Elemento pattern con espressione regolare. Facoltativo negli elementi <rule>.
seo-title: expression
solution: Experience Manager
title: expression
topic: Scene7 Image Serving - Image Rendering API
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# espressione{#expression}

Elemento pattern con espressione regolare. Facoltativo negli elementi `<rule>`.

## Attributi {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Nessuno.

## Dati {#section-e2601008d71243109af1a8c55b58416d}

Stringa di pattern con espressione regolare.

## Descrizione {#section-759bfb738ddb45dba1f0807aba8c1113}

L&#39;elemento `<expression>` può essere vuoto o contenere una semplice stringa di ricerca o un pattern di espressione regolare. Il pattern viene applicato all&#39;intera stringa di richiesta.

Una corrispondenza si verifica sempre quando `<expression>` è vuoto o non è specificato; equivale a specificare `<expression>.*</expression>`.

L&#39;implementazione è basata sul pacchetto Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), che fornisce una sintassi di espressione regolare simile a quella di Perl.

## Note {#section-10b472a902674893b49ca49a7052c366}

La stringa di espressione non deve contenere caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<`, oppure l&#39;intera stringa può essere racchiusa in una sezione XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Tutti i caratteri compresi tra i tag `<expression>` e `</expression>` vengono passati al parser di espressioni regolari, inclusi i caratteri al di fuori della sezione opzionale `CDATA`. Fare attenzione a evitare spazi bianchi aggiuntivi.

## Consultate anche {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

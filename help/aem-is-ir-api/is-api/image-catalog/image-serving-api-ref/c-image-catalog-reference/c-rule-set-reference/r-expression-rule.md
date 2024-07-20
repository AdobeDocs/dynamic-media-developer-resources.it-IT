---
description: Elemento pattern espressione regolare. Facoltativo negli elementi <rule>.
solution: Experience Manager
title: espressione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# espressione{#expression}

Elemento pattern espressione regolare. Facoltativo negli elementi `<rule>`.

## Attributi {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Nessuno.

## Dati {#section-e2601008d71243109af1a8c55b58416d}

Stringa di pattern con espressione regolare.

## Descrizione {#section-759bfb738ddb45dba1f0807aba8c1113}

L&#39;elemento `<expression>` può essere vuoto o contenere una stringa di ricerca semplice o un pattern di espressione regolare. Il pattern viene applicato all’intera stringa di richiesta.

Una corrispondenza si verifica sempre quando `<expression>` è vuoto o non è specificato; ciò equivale a specificare `<expression>.*</expression>`.

L&#39;implementazione si basa sul pacchetto Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), che fornisce una sintassi di espressione regolare simile a quella di Perl.

## Note {#section-10b472a902674893b49ca49a7052c366}

La stringa di espressione non deve contenere i caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<` oppure l&#39;intera stringa può essere racchiusa in una sezione XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Tutti i caratteri compresi tra i tag `<expression>` e `</expression>` vengono passati al parser di espressioni regolari, inclusi i caratteri all&#39;esterno della sezione facoltativa `CDATA`. Prestare attenzione per evitare spazi vuoti aggiuntivi.

## Consultate anche {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

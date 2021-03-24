---
description: I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso di file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.
solution: Experience Manager
title: File di attributi del catalogo
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# File di attributi del catalogo{#catalog-attribute-files}

I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso di file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.

I file di attributi del catalogo sono costituiti da un set di record di testo, separati da una singola `<CR>` (codice ASCII 0xD), un singolo `<LF>` (codice ASCII 0xA) o una coppia `<CR><LF>`. Ogni record è costituito da un nome di attributo e da uno o più valori di attributo separati da virgole:

`*``*= *``*&#42;[, *`nome del valore`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome dell'attributo; può essere costituito da una o più lettere, numero, '-' e '_'; senza distinzione tra maiuscole e minuscole. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore dell'attributo; non devono includere caratteri <span class="codeph"> &lt;CR&gt; </span> o <span class="codeph"> &lt;LF&gt; </span>, a meno che non siano preceduti da una barra rovesciata singola immediatamente prima del carattere di nuova riga. </p> </td> 
 </tr> 
</table>

* Lo spazio vuoto tra i token è facoltativo.
* I record con nomi di attributi sconosciuti vengono ignorati dal server Platform.
* I nomi degli attributi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot;, &quot;_&quot; e &quot;.&quot;
* Se lo stesso nome attributo si verifica più di una volta nello stesso file di attributi, prevale l&#39;ultimo rilevato.
* Utilizzare &#39;#&#39; come primo carattere per contrassegnare qualsiasi record come commento ignorato dal parser.


---
description: I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.
seo-description: I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.
seo-title: File di attributi del catalogo
solution: Experience Manager
title: File di attributi del catalogo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# File di attributi del catalogo{#catalog-attribute-files}

I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.

I file di attributi del catalogo sono composti da un set di record di testo, separati da una singola `<CR>` (codice ASCII 0xD), una singola `<LF>` (codice ASCII 0xA) o una coppia `<CR><LF>`. Ogni record è costituito da un nome di attributo e da uno o più valori di attributo separati da virgola:

`*`Nome `*= *``*&#42;[, *`valore`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome attributo; può essere costituito da una o più lettere, numero, '-' e '_'; senza distinzione tra maiuscole e minuscole. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore attributo; non devono includere caratteri <span class="codeph"> &lt;CR&gt; </span> o <span class="codeph"> &lt;LF&gt; </span>, a meno che non siano preceduti da una barra rovesciata, immediatamente prima del carattere della nuova riga. </p> </td> 
 </tr> 
</table>

* Lo spazio vuoto tra i token è facoltativo.
* I record con nomi di attributi sconosciuti vengono ignorati dal server piattaforma.
* I nomi degli attributi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot;, &quot;_&quot; e &quot;.&quot;
* Se lo stesso nome di attributo si verifica più volte nello stesso file di attributo, prevale l&#39;ultimo.
* Utilizzare &#39;#&#39; come primo carattere per contrassegnare qualsiasi record come commento ignorato dal parser.


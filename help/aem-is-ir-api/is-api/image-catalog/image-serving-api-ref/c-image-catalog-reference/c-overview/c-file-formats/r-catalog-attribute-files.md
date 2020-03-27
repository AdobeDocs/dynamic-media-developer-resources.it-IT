---
description: I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.
seo-description: I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.
seo-title: File di attributi del catalogo
solution: Experience Manager
title: File di attributi del catalogo
topic: Scene7 Image Serving - Image Rendering API
uuid: 63985780-f032-4542-8d84-b8b608ceea4b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# File di attributi del catalogo{#catalog-attribute-files}

I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.

I file di attributi del catalogo sono composti da un set di record di testo, separati da un singolo `<CR>` (codice ASCII `0xD`), un singolo `<LF>` (codice ASCII `0xA`) o una `<CR><LF>` coppia. Ogni record è costituito da un nome di attributo e da uno o più valori di attributo separati da virgola:

` *``*= *`namevalues`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valori</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Nome attributo. Può essere costituito da una o più lettere, numero, - e _. Senza distinzione tra maiuscole e minuscole. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valore attributo. Non devono includere caratteri <span class="codeph"> &lt;CR&gt;</span> o <span class="codeph"> &lt;LF&gt;</span> , a meno che non siano preceduti da una barra rovesciata singola. </p></td> 
 </tr> 
</table>

Lo spazio vuoto tra i token è facoltativo.

I record con nomi di attributi sconosciuti vengono ignorati dal server piattaforma.

I nomi degli attributi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot;, &quot;_&quot; e &quot;.&quot;.

Se lo stesso nome di attributo si verifica più volte nello stesso file di attributo, prevale l&#39;ultimo.

Utilizzate # come primo carattere per contrassegnare qualsiasi record come commento, che il parser ignora.

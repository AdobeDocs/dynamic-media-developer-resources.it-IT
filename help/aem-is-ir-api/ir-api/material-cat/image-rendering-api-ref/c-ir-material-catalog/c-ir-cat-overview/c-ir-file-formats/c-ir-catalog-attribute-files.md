---
title: File di attributi del catalogo
description: I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso di file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# File di attributi del catalogo{#catalog-attribute-files}

I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un `.ini` suffisso file. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.

I file di attributi del catalogo sono costituiti da un set di record di testo, separati da un singolo `<CR>` (codice ASCII 0xD), un singolo `<LF>` (codice ASCII 0xA), oppure `<CR><LF>` coppia. Ogni record è costituito da un nome di attributo e da uno o più valori di attributo separati da virgole:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome dell'attributo; può essere costituito da una o più lettere, numero, '-' e '_'; senza distinzione tra maiuscole e minuscole. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore dell'attributo; non deve includere <span class="codeph"> &lt;cr&gt; </span>oppure <span class="codeph"> &lt;lf&gt; </span> caratteri, a meno che non siano preceduti da una singola barra rovesciata immediatamente prima del carattere della nuova riga. </p> </td> 
 </tr> 
</table>

* Lo spazio vuoto tra i token è facoltativo.
* I record con nomi di attributi sconosciuti vengono ignorati dal server Platform.
* I nomi degli attributi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri e &quot;-&quot;, &quot;_&quot; e &quot;.&quot;
* Se lo stesso nome attributo si verifica più di una volta nello stesso file di attributi, prevale l&#39;ultimo rilevato.
* Utilizzare &#39;#&#39; come primo carattere per contrassegnare qualsiasi record come commento ignorato dal parser.

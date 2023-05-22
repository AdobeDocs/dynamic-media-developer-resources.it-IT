---
title: File di attributi catalogo
description: I file degli attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso di file INI. Possono essere gestiti facilmente con qualsiasi editor di testo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# File di attributi catalogo{#catalog-attribute-files}

I file degli attributi del catalogo possono avere qualsiasi nome, ma devono avere un `.ini` suffisso file. Possono essere gestiti facilmente con qualsiasi editor di testo.

I file di attributi del catalogo sono costituiti da un set di record di testo, separati da un singolo `<CR>` (codice ASCII 0xD), un singolo `<LF>` (codice ASCII 0xA) o un `<CR><LF>` coppia. Ogni record è costituito da un nome di attributo e da uno o più valori di attributo separati da virgola:

`*`nome`*= *`valore`*&#42;[, *`valore`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> nome </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome attributo; può essere costituito da una o più lettere, numeri, "-" e "_"; senza distinzione tra maiuscole e minuscole. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valore </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore attributo; non deve includere <span class="codeph"> &lt;cr&gt; </span>, o <span class="codeph"> &lt;lf&gt; </span> caratteri, a meno che non siano preceduti da una singola barra rovesciata. </p> </td> 
 </tr> 
</table>

* Lo spazio vuoto tra i token è facoltativo.
* I record con nomi di attributi sconosciuti vengono ignorati dal [!DNL Platform Server].
* I nomi degli attributi possono essere costituiti da qualsiasi combinazione di lettere ASCII, numeri e &quot;-&quot;, &quot;_&quot; e &quot;.&quot;
* Se lo stesso nome di attributo si trova più di una volta nello stesso file di attributi, prevale l’ultimo.
* Utilizza &#39;#&#39; come primo carattere per contrassegnare qualsiasi record come commento ignorato dal parser.

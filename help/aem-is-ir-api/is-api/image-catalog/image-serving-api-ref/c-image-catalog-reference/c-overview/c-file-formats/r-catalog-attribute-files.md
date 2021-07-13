---
description: I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso di file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.
solution: Experience Manager
title: File di attributi del catalogo
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# File di attributi del catalogo{#catalog-attribute-files}

I file di attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso di file .ini. Possono essere facilmente mantenuti utilizzando qualsiasi editor di testo.

I file di attributi del catalogo sono costituiti da un set di record di testo separati da una singola `<CR>` (codice ASCII `0xD`), un singolo `<LF>` (codice ASCII `0xA`) o da una coppia `<CR><LF>`. Ogni record è costituito da un nome di attributo e da uno o più valori di attributo separati da virgole:

`*``*= *`valori dei nomi`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Nome dell'attributo. Può essere costituito da una o più lettere, numero, - e _. Senza distinzione tra maiuscole e minuscole. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valore dell'attributo. Non devono includere caratteri <span class="codeph"> &lt;CR&gt;</span> o <span class="codeph"> &lt;LF&gt;</span>, a meno che non siano preceduti da una singola barra rovesciata immediatamente prima del carattere di nuova riga. </p></td> 
 </tr> 
</table>

Lo spazio vuoto tra i token è facoltativo.

I record con nomi di attributi sconosciuti vengono ignorati dal server Platform.

I nomi degli attributi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot;, &quot;_&quot; e &quot;.&quot;.

Se lo stesso nome attributo si verifica più di una volta nello stesso file di attributi, prevale l&#39;ultimo rilevato.

Usa # come primo carattere per contrassegnare qualsiasi record come commento, che il parser ignora.

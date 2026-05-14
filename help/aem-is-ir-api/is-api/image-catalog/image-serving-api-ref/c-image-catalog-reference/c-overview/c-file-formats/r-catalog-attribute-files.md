---
description: I file degli attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso di file INI. Possono essere gestiti facilmente con qualsiasi editor di testo.
solution: Experience Manager
title: File di attributi catalogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
TQID: 'https://experienceleague.adobe.com/RCxeXg3wb10jo37biAs1puqmEo8bAL-i-oZBwGHuloA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# File di attributi catalogo{#catalog-attribute-files}

I file degli attributi del catalogo possono avere qualsiasi nome, ma devono avere un suffisso di file INI. Possono essere gestiti facilmente con qualsiasi editor di testo.

I file degli attributi del catalogo sono costituiti da un set di record di testo separati da un singolo `<CR>` (codice ASCII `0xD`), un singolo `<LF>` (codice ASCII `0xA`) o una coppia `<CR><LF>`. Ogni record è costituito da un nome di attributo e da uno o più valori di attributo separati da virgola:

`*`nome`*= *`valori`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> valori</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valori</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Nome <span class="varname"></span> </p> </td> 
  <td class="stentry"> <p>Nome attributo. Può essere costituito da una o più lettere, numero, - e _. Senza distinzione tra maiuscole e minuscole. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Valore <span class="varname"></span> </p></td> 
  <td class="stentry"> <p>Valore attributo. Non deve includere <span class="codeph"> &lt;CR&gt;</span> o <span class="codeph"> &lt;LF&gt;</span> caratteri, a meno che non sia preceduto da una barra rovesciata prima del carattere di nuova riga. </p></td> 
 </tr> 
</table>

Lo spazio vuoto tra i token è facoltativo.

I record con nomi di attributi sconosciuti vengono ignorati da [!DNL Platform Server].

I nomi degli attributi possono essere costituiti da qualsiasi combinazione di lettere ASCII, numeri, nonché da &quot;-&quot;, &quot;_&quot; e &quot;.&quot;.

Se lo stesso nome di attributo si trova più di una volta nello stesso file di attributi, prevale l’ultimo.

Utilizzare # come primo carattere per contrassegnare qualsiasi record come commento, che verrà ignorato dal parser.

---
description: Informazioni immagine Digimarc. Abilita l’incorporamento Digimarc e specifica il tipo di filigrana ed eventuali dati specifici dell’immagine associati.
solution: Experience Manager
title: DigimarcInfo
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 12%

---


# DigimarcInfo{#digimarcinfo}

Informazioni immagine Digimarc. Abilita l’incorporamento Digimarc e specifica il tipo di filigrana ed eventuali dati specifici dell’immagine associati.

## Proprietà {#section-62af219e8bac422b8541841221c9ce4f}

Quattro valori interi, separati da virgole.

`*``*, *``*, *`typeflagsval1`*, *`val2`*`

`*``*` typeenable Digimarc embedding e specifica il tipo di filigrana:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>Tipo di filigrana</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Base. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>ID immagine. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>ID transazione. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>anni di copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*``*` flagsis a bit field con tre valori. Impostare il bit 0 per indicare il contenuto protetto da copia, il bit 1 per indicare il contenuto limitato e il bit 2 per indicare il contenuto per adulti:

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> flag</span> </span> </p> </th> 
   <th class="entry"> <p><b>Descrizione</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protetto da copia. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Limitata. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protetto da copia, limitato. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Contenuto maturo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Copia contenuto protetto per adulti. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Contenuto limitato per adulti. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Contenuti protetti da copia, limitati e maturi. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;interpretazione di `*`val1`*` e `*`val2`*` dipende da `*`type`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Non utilizzato. </p> </td> 
   <td> <p>Non utilizzato. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Non utilizzato. </p> </td> 
   <td> <p>Non utilizzato. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>ID immagine. </p> </td> 
   <td> <p>Non utilizzato. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>ID transazione. </p> </td> 
   <td> <p>Non utilizzato. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Primo anno di copyright. </p> </td> 
   <td> <p>Secondo anno di copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Predefinito {#section-4bb97e5f79074be89cc691e73449eb43}

Ereditato dall&#39;attributo::DigimarcInfo se il campo non è presente o se è vuoto.

## Esempi {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot; disabilita il watermarking Digimarc per questa immagine.

&quot;1,5,0,0&quot; specifica una filigrana di base con il flag di contenuto protetto da copia impostato.

&quot;2,0,4567,0&quot; specifica una filigrana con un ID immagine.

&quot;3,2,56483,0&quot; specifica una filigrana con un ID transazione e il flag di contenuto limitato impostato.

&quot;4,0,1998,2001&quot; specifica una filigrana con anni di copyright.

## Consultate anche {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attributo::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ,  [attributo::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)

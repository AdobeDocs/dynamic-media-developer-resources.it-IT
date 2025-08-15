---
title: Comandi di richiesta
description: Questi comandi vengono applicati indipendentemente dalla posizione nella richiesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3f794f46-e7f0-4899-90fa-898a698dd629
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Comandi di richiesta{#request-commands}

Questi comandi vengono applicati indipendentemente dalla posizione nella richiesta.

<table id="simpletable_3F7C17FB9E374EFDAD01EB24F57EC367"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache</a> </p></td> 
  <td class="stentry"> <p>Sostituisce il comportamento predefinito del caching delle risposte. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2" type="reference" format="dita" scope="local"> defaultImage</a> </p></td> 
  <td class="stentry"> <p>Specifica l'immagine da utilizzare al posto di un file di immagine mancante. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt</a> </p></td> 
  <td class="stentry"> <p>Specifica il formato immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517" type="reference" format="dita" scope="local"> icc</a> </p></td> 
  <td class="stentry"> <p>Imposta il profilo colore di output. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> iccEmbed</a> </p> </td> 
  <td class="stentry"> <p>Incorpora il profilo colore nell’immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed</a> </p></td> 
  <td class="stentry"> <p>Incorpora i dati del percorso Photoshop nell’immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed</a> </p></td> 
  <td class="stentry"> <p>Incorpora i metadati di XMP nell’immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-printres.md#reference-84f52afff4704c4b9d58e4bbbaea1491" type="reference" format="dita" scope="local"> printRes</a> </p> </td> 
  <td class="stentry"> <p>Specifica il valore di risoluzione di stampa incorporato nell'immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt</a> </p></td> 
  <td class="stentry"> <p>Specifica gli attributi di codifica JPEG. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> Quantize <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38" type="reference" format="dita" scope="local"></a> </p> </td> 
  <td class="stentry"> <p>Specifica gli attributi di quantizzazione colore per l'output GIF. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> richiesta</a> </p></td> 
  <td class="stentry"> <p>Seleziona il tipo di richiesta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md#reference-29a398cc59dc4caf9acd5f69c9ba9715" type="reference" format="dita" scope="local"> resMode</a> </p></td> 
  <td class="stentry"> <p>Specifica la modalità di ricampionamento o interpolazione dell'immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14" type="reference" format="dita" scope="local"> modello</a> </p> </td> 
  <td class="stentry"> <p>Specifica un modello di composizione. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb" type="reference" format="dita" scope="local"> impostazioni locali</a> </p></td> 
  <td class="stentry"> <p>Specifica un modello di composizione. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> ID <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"></a> </p> </td> 
  <td class="stentry"> <p>ID versione immagine/metadati. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3" type="reference" format="dita" scope="local"> set di immagini</a> </p> </td> 
  <td class="stentry"> <p>Specifica il set di immagini da utilizzare per questa richiesta. </p></td> 
 </tr> 
</table>

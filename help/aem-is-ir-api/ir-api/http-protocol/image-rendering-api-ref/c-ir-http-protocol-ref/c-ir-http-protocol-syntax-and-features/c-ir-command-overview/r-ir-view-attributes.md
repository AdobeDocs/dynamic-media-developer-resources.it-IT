---
title: Visualizza attributi
description: Questi comandi sono indipendenti dalla posizione e possono essere eseguiti in qualsiasi punto di una richiesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 18e1ee40-fe34-435a-be97-849b08618d48
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Visualizza attributi{#view-attributes}

Questi comandi sono indipendenti dalla posizione e possono essere eseguiti in qualsiasi punto di una richiesta.

<table id="simpletable_D30C7420AECD44ADBD7B0728594FF5FA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt</a> </span> </p></td> 
  <td class="stentry"> <p>Formato immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt</a> </span> </p></td> 
  <td class="stentry"> <p>Qualità JPEG. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-printres.md#reference-ff897ad013fb410b96edaa2c79edfddd" type="reference" format="dita" scope="local"> printRes</a> </span> </p></td> 
  <td class="stentry"> <p>Valore di risoluzione di stampa incorporato nell'immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478" type="reference" format="dita" scope="local"> hei</a></span> </p></td> 
  <td class="stentry"> <p>Ridimensiona l’immagine di cui è stato eseguito il rendering all’altezza specificata. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec" type="reference" format="dita" scope="local"> wid</a></span> </p></td> 
  <td class="stentry"> <p>Ridimensiona l’immagine di cui è stato eseguito il rendering alla larghezza specificata. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29" type="reference" format="dita" scope="local"> scl</a></span> </p></td> 
  <td class="stentry"> <p>Ridimensiona l’immagine di cui è stato eseguito il rendering rispetto alle dimensioni della vignettatura a risoluzione massima. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3" type="reference" format="dita" scope="local"> resMode</a></span> </p></td> 
  <td class="stentry"> <p>Modalità di ricampionamento per il ridimensionamento dell'immagine finale. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e" type="reference" format="dita" scope="local"> nitidezza</a></span> </p></td> 
  <td class="stentry"> <p>Contrasto immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc</a></span> </p></td> 
  <td class="stentry"> <p>Profilo colore di output. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed</a></span> </p></td> 
  <td class="stentry"> <p>Incorpora il profilo colore nell’immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed</a></span> </p></td> 
  <td class="stentry"> <p>Incorpora i percorsi Photoshop nell’immagine di risposta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-vignette.md#reference-eb3f458733294f988483b024348bc778" type="reference" format="dita" scope="local"> vignettatura</a></span> </p></td> 
  <td class="stentry"> <p>Vignettatura. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-cache.md#reference-a83329ce7c914ee4b518b0bda71f0438" type="reference" format="dita" scope="local"> cache</a></span> </p> </td> 
  <td class="stentry"> <p>Ignora il comportamento predefinito di caching delle risposte. </p></td> 
 </tr> 
</table>

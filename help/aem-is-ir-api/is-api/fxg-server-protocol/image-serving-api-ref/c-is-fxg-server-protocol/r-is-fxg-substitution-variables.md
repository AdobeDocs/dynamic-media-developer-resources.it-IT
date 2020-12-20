---
description: La variabile di sostituzione viene utilizzata per trasferire i valori dall’URL della richiesta ai modelli FXG memorizzati sul server.
seo-description: La variabile di sostituzione viene utilizzata per trasferire i valori dall’URL della richiesta ai modelli FXG memorizzati sul server.
seo-title: Variabili di sostituzione
solution: Experience Manager
title: Variabili di sostituzione
topic: Scene7 Image Serving - Image Rendering API
uuid: 87cd9594-ba3b-429d-aa57-399902ef3abe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Variabili di sostituzione{#substitution-variables}

La variabile di sostituzione viene utilizzata per trasferire i valori dall’URL della richiesta ai modelli FXG memorizzati sul server.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome della variabile. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore a cui impostare la variabile (stringa). </p> </td> 
 </tr> 
</table>

* Le definizioni delle variabili e i riferimenti possono verificarsi nella parte query dell’URL della richiesta.
* Le variabili sono definite come sopra, simili ad altri comandi IS; l&#39;interlinea &#39;$&#39; identifica il comando come definizione di variabile.
* Il nome della variabile ` *`var`*` fa distinzione tra maiuscole e minuscole e può essere costituito da una combinazione di lettere, numeri, &#39;-&#39; e &#39;_&#39;.
* Per una trasmissione HTTP sicura, il valore importante deve essere codificato nell’URL con una sola passata.


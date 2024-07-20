---
description: La variabile di sostituzione viene utilizzata per trasferire i valori dall’URL della richiesta ai modelli FXG memorizzati sul server.
solution: Experience Manager
title: Variabili di sostituzione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# Variabili di sostituzione{#substitution-variables}

La variabile di sostituzione viene utilizzata per trasferire i valori dall’URL della richiesta ai modelli FXG memorizzati sul server.

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome della variabile. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valore </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore al quale deve essere impostata la variabile (stringa). </p> </td> 
 </tr> 
</table>

* Definizioni di variabili e riferimenti possono verificarsi nella parte query dell’URL della richiesta.
* Le variabili sono definite come sopra, in modo simile ad altri comandi IS; l&#39;iniziale &#39;$&#39; identifica il comando come definizione di variabile.
* Il nome della variabile `*`var`*` fa distinzione tra maiuscole e minuscole e può essere costituito da qualsiasi combinazione di lettere, numeri, &quot;-&quot; e &quot;_&quot;.
* Per una trasmissione HTTP sicura, il valore importante deve essere codificato in URL a passaggio singolo.

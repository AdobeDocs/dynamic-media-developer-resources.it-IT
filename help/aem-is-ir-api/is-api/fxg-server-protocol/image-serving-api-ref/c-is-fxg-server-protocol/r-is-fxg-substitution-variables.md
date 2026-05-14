---
description: La variabile di sostituzione viene utilizzata per trasferire i valori dall’URL della richiesta ai modelli FXG memorizzati sul server.
solution: Experience Manager
title: Variabili di sostituzione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
TQID: 'https://experienceleague.adobe.com/-IHIbaXxoDEGqbV2inp4RlmWpH-8js7Dn9b-CK1paxg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
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

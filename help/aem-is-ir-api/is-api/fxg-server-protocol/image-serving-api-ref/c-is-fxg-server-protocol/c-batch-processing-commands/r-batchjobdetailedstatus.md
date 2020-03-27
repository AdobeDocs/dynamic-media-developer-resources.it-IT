---
description: Recuperare lo stato dettagliato di un processo inviato.
seo-description: Recuperare lo stato dettagliato di un processo inviato.
seo-title: batchjobdetailedstatus
solution: Experience Manager
title: batchjobdetailedstatus
topic: Scene7 Image Serving - Image Rendering API
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobdetailedstatus{#batchjobdetailedstatus}

Recuperare lo stato dettagliato di un processo inviato.

Questo parametro:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>ID processo ottenuto al momento dell’invio. </p> </td> 
 </tr> 
</table>

Restituisce:

stato dettagliato del processo in formato XML; se `jobid` non è valido o il processo è stato eliminato.

## Esempio {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`

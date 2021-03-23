---
description: Recupera lo stato dettagliato di un processo inviato.
seo-description: Recupera lo stato dettagliato di un processo inviato.
seo-title: batchjobdetailedstatus
solution: Experience Manager
title: batchjobdetailedstatus
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---


# batchjobdetailedstatus{#batchjobdetailedstatus}

Recupera lo stato dettagliato di un processo inviato.

Questo parametro:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID processo ottenuto al momento dell’invio. </p> </td> 
 </tr> 
</table>

Restituisce:

stato dettagliato del processo in formato XML; errore se `jobid` non è valido o il processo è stato eliminato.

## Esempio {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`

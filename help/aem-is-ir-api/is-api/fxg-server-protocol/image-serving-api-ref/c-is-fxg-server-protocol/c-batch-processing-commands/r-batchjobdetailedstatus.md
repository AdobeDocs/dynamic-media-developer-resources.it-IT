---
description: Recupera lo stato dettagliato di un processo inviato.
solution: Experience Manager
title: batchjobdetailedstatus
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fd385327-29af-448c-9a25-75098b578272
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '52'
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

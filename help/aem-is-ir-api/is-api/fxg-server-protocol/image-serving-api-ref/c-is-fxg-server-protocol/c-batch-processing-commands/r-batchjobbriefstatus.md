---
description: Recupera lo stato riepilogato di un processo inviato.
solution: Experience Manager
title: batchjobbriefstatus
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# batchjobbriefstatus{#batchjobbriefstatus}

Recupera lo stato riepilogato di un processo inviato.

Questo parametro:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID processo ottenuto al momento dell’invio. </p> </td> 
 </tr> 
</table>

Restituisce:

Breve stato del processo in formato XML; errore se il jobID non è valido o il job è stato eliminato.

## Esempio {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]

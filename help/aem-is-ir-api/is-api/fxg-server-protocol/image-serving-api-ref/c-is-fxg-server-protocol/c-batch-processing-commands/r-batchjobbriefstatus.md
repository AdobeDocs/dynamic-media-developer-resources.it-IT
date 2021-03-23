---
description: Recupera lo stato riepilogato di un processo inviato.
seo-description: Recupera lo stato riepilogato di un processo inviato.
seo-title: batchjobbriefstatus
solution: Experience Manager
title: batchjobbriefstatus
uuid: 601e8395-8a77-4324-9cd7-5fe321bc91e3
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '64'
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

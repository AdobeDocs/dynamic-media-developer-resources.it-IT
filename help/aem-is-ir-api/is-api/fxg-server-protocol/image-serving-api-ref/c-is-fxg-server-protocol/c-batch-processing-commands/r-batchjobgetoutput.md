---
description: Recupera l'output di un processo inviato.
solution: Experience Manager
title: batchjobgetoutput
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 3fb48c39-b15a-45b7-9aca-ed33f9c46c93
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# batchjobgetoutput{#batchjobgetoutput}

Recupera l&#39;output di un processo inviato.

Questo parametro:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID processo ottenuto al momento dell’invio. </p> </td> 
 </tr> 
</table>

Restituisce:

L&#39;output PDF del processo viene inviato in streaming; errore se `jobid` non è valido o il processo è stato eliminato.

## Esempio {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]

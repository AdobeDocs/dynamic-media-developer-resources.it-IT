---
description: Elimina l'output di un processo.
solution: Experience Manager
title: batchjobdelete
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

Elimina l&#39;output di un processo.

Se un processo è attualmente in esecuzione, viene interrotto immediatamente e tutte le relative informazioni di elaborazione vengono eliminate. Se il processo è stato completato correttamente, il relativo file di output viene eliminato.

Questo parametro:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>ID processo ottenuto al momento dell’invio. </p></td> 
 </tr> 
</table>

Restituisce:

Stato del processo al momento della ricezione della richiesta di eliminazione, errore se `jobid` non è valido o il processo è già stato eliminato.

## Esempio {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]

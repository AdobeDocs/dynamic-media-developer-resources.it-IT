---
description: Eliminate l’output di un processo.
seo-description: Eliminate l’output di un processo.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Scene7 Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobdelete{#batchjobdelete}

Eliminate l’output di un processo.

Se un processo è in esecuzione, viene interrotto immediatamente e tutte le relative informazioni di elaborazione vengono eliminate. Se il processo è stato completato correttamente, il relativo file di output viene eliminato.

Questo parametro:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>ID processo ottenuto al momento dell’invio. </p></td> 
 </tr> 
</table>

Restituisce:

Stato del processo al momento della ricezione della richiesta di eliminazione. Errore se `jobid` non è valido o il processo è già stato eliminato.

## Esempio {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]

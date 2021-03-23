---
description: Invia un nuovo processo batch.
seo-description: Invia un nuovo processo batch.
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 1%

---


# batchjobsubmit{#batchjobsubmit}

Invia un nuovo processo batch.

Questo parametro:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata  </span> </p> </td> 
  <td class="stentry"> <p>Frammento XML dei dati di processo completi. </p> </td> 
 </tr> 
</table>

Restituisce:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Stato del lavoro </p> </td> 
  <td class="stentry"> <p>Se la presentazione è riuscita o meno; in caso di esito positivo, ID processo in formato XML. </p> </td> 
 </tr> 
</table>

## Esempio {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`

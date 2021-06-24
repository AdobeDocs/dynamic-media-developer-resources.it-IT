---
description: Contiene le impostazioni per il sistema di monitoraggio/avviso.
solution: Experience Manager
title: monitor.conf
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 09c30680-dd9f-4744-b5ec-105721058883
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# monitor.conf{#monitor-conf}

Contiene le impostazioni per il sistema di monitoraggio/avviso.

Questo file è un file di proprietà JAVA. Si deve fare attenzione a seguire le convenzioni appropriate; in caso contrario, l&#39;avvio del server Platform potrebbe non riuscire. In particolare, è necessario utilizzare una barra rovesciata doppia &#39;\\&#39; o una singola barra rovesciata &#39;/&#39; invece di una barra rovesciata &#39;\&#39; nei percorsi dei file Windows, poiché la barra rovesciata viene utilizzata come carattere di escape in questo tipo di file.

Le modifiche a questo file hanno effetto poco dopo il salvataggio del file.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Generali </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false  </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1  </span> </p> <p> <span class="codeph"> mailSender.port=25  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Soglie avvisi </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>

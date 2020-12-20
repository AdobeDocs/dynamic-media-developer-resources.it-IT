---
description: Contiene le impostazioni per il sistema di monitoraggio/allarme.
seo-description: Contiene le impostazioni per il sistema di monitoraggio/allarme.
seo-title: monitor.conf
solution: Experience Manager
title: monitor.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 31949797-df2c-4b7c-841b-4c623299a228
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# monitor.conf{#monitor-conf}

Contiene le impostazioni per il sistema di monitoraggio/allarme.

Questo file è un file di proprietà JAVA. Occorre fare attenzione a seguire le convenzioni appropriate; in caso contrario, il server della piattaforma potrebbe non avviarsi. In particolare, nei percorsi dei file Windows deve essere utilizzata una doppia barra rovesciata &#39;\\&#39; o una singola barra rovesciata &#39;/&#39;, invece di una barra rovesciata &#39;\&#39;, poiché la barra rovesciata viene utilizzata come carattere di escape in questo tipo di file.

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


---
description: Tutti i file di configurazione si trovano in install_folder/conf e sono modificabili con la maggior parte degli editor di testo. Potrebbe essere necessario riavviare il server per rendere effettive le modifiche.
solution: Experience Manager
title: File di configurazione del server
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# File di configurazione del server{#server-configuration-files}

Tutti i file di configurazione si trovano in install_folder/conf e sono modificabili con la maggior parte degli editor di testo. Potrebbe essere necessario riavviare il server per rendere effettive le modifiche.

>[!NOTE]
>
>La maggior parte dei file di configurazione del server contiene proprietà e valori aggiuntivi non descritti in questo documento. Tali proprietà sono per uso interno del server e non devono essere modificate a meno che non sia specificamente indicato dal supporto tecnico Dynamic Media.

Questo documento illustra le impostazioni per i seguenti file di configurazione:

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>File di configurazione</b> </th> 
   <th class="entry"> <b>Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisoreRegistry.xml</span> </p> </td> 
   <td> <p>Configurazione di Server Supervisore. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Configurazione Tomcat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>Configurazione del server della piattaforma. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>Configurazione del servizio catalogo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>Configurazione del monitoraggio server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>Configurazione del server di immagini. </p> </td> 
  </tr> 
 </tbody> 
</table>

I file di configurazione vengono discussi più dettagliatamente più avanti in questo documento.

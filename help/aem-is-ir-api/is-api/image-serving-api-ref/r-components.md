---
title: Componenti Image Server
description: Dynamic Medie Image Server è costituito dai seguenti componenti.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# Componenti Image Server{#image-serving-components}

Dynamic Medie Image Server è costituito dai seguenti componenti:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Componente </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Supervisore server </p> </td> 
   <td colname="col2"> <p>Eseguibile autonomo responsabile dell'avvio, dell'arresto e della verifica dell'integrità degli altri componenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Fornisce l’ambiente per la maggior parte dei componenti basati su Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servizio di monitoraggio/avvisi </p> </td> 
   <td colname="col2"> <p>applicazione J2EE. Fornisce monitoraggio del server e avvisi e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>applicazione J2EE. Gestisce le connessioni client, la registrazione e le comunicazioni con altri componenti. Accesso HTTP in <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servizio di caching </p> </td> 
   <td colname="col2"> <p>applicazione J2EE. Gestisce le cache dei dati di [!DNL Platform Server]. Accesso HTTP in /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Esegue tutte le operazioni di elaborazione delle immagini e I/O dei file di immagine. I file eseguibili a 32 bit e a 64 bit sono disponibili per Linux® (solo a 32 bit per Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente rendering testo ATE </p> </td> 
   <td colname="col2"> <p>Una o più istanze del servizio di rendering del testo potrebbero essere attive quando vengono eseguite <span class="codeph"> operazioni textPs=</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente rendering SVG </p> </td> 
   <td colname="col2"> <p>Applicazione Java™ autonoma (non ospitata da Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendering immagini Dynamic Medie (alias Server di rendering) </p> </td> 
   <td colname="col2"> <p>Per l’attivazione è necessaria una licenza separata. Accesso HTTP in <span class="filepath"> /ir/render</span>. Tutte le funzionalità di Image Rendering sono integrate in [!DNL Platform Server] e nel server immagini, senza componenti eseguibili separati. </p> </td> 
  </tr> 
 </tbody> 
</table>

Impostazioni di configurazione aggiuntive vengono fornite dal catalogo predefinito ( [!DNL default.ini]) o da cataloghi di immagini specifici (per ulteriori informazioni, vedere [Cataloghi di immagini](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)).

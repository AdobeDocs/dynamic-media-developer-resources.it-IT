---
description: 'Scene 7 Image Serving è costituito dai seguenti componenti '
solution: Experience Manager
title: Componenti Image Serving
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Componenti Image Server{#image-serving-components}

Scene 7 Image Serving è costituito dai seguenti componenti:

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
   <td colname="col2"> <p>Eseguibile autonomo responsabile dell'avvio, dell'arresto e della garanzia dello stato degli altri componenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Fornisce l’ambiente per la maggior parte dei componenti basati su Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servizio di monitoraggio/avviso </p> </td> 
   <td colname="col2"> <p>Applicazione J2EE. Fornisce avvisi e-mail e monitoraggio del server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Server della piattaforma </p> </td> 
   <td colname="col2"> <p>Applicazione J2EE. Gestisce le connessioni client, la registrazione e le comunicazioni con altri componenti. Accesso HTTP all'indirizzo <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servizio di caching </p> </td> 
   <td colname="col2"> <p>Applicazione J2EE. Gestisce le cache di dati del server Platform. Accesso HTTP a /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Esegue tutte le operazioni di elaborazione delle immagini e I/O dei file di immagine. Per Linux sono disponibili eseguibili sia a 32 bit che a 64 bit (solo a 32 bit per Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente Rendering testo ATE </p> </td> 
   <td colname="col2"> <p>Una o più istanze del servizio di rendering del testo possono essere attive quando vengono eseguite le operazioni <span class="codeph"> textPs=</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente di rendering SVG </p> </td> 
   <td colname="col2"> <p>Applicazione Java indipendente (non ospitata da Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendering delle immagini di Dynamic Media (aka. Render Server) </p> </td> 
   <td colname="col2"> <p>Richiede una licenza separata per l'attivazione. Accesso HTTP su <span class="filepath"> /ir/render</span>. Tutte le funzionalità di rendering delle immagini sono integrate nel server Platform e nel server di immagini, senza componenti eseguibili separati. </p> </td> 
  </tr> 
 </tbody> 
</table>

Altre impostazioni di configurazione sono fornite dal catalogo predefinito ( [!DNL default.ini]) o da cataloghi di immagini specifici (per ulteriori informazioni, consulta [Cataloghi di immagini](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) ).

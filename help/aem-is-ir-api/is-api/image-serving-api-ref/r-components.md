---
description: Scene 7 Image Serving è costituito dai seguenti componenti
solution: Experience Manager
title: Componenti Image Serving
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# Componenti Image Serving{#image-serving-components}

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
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>Applicazione J2EE. Gestisce le connessioni client, la registrazione e le comunicazioni con altri componenti. accesso HTTP a <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servizio di caching </p> </td> 
   <td colname="col2"> <p>Applicazione J2EE. Gestisce i [!DNL Platform Server]I dati di sono memorizzati nella cache. Accesso HTTP a /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Esegue tutte le operazioni di elaborazione delle immagini e I/O dei file di immagine. Per Linux sono disponibili eseguibili sia a 32 bit che a 64 bit (solo a 32 bit per Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente rendering testo AEM </p> </td> 
   <td colname="col2"> <p>È possibile che una o più istanze del servizio di rendering del testo siano attive quando <span class="codeph"> textPs=</span> le operazioni vengono eseguite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente SVG Render </p> </td> 
   <td colname="col2"> <p>Applicazione Java indipendente (non ospitata da Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendering delle immagini di Dynamic Media (aka. Render Server) </p> </td> 
   <td colname="col2"> <p>Richiede una licenza separata per l'attivazione. accesso HTTP a <span class="filepath"> /ir/render</span>. Tutte le funzionalità di rendering delle immagini sono integrate nel [!DNL Platform Server] e Image Server, senza componenti eseguibili separati. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le impostazioni di configurazione aggiuntive vengono fornite dal catalogo predefinito ( [!DNL default.ini]) o cataloghi di immagini specifici (vedi [Cataloghi di immagini](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) per ulteriori informazioni).

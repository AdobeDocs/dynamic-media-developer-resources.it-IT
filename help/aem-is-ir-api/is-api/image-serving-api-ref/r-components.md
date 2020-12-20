---
description: 'Scene7 Image Serving è costituito dai seguenti componenti '
seo-description: 'Scene7 Image Serving è costituito dai seguenti componenti '
seo-title: Componenti per Image Server
solution: Experience Manager
title: Componenti per Image Server
topic: Scene7 Image Serving - Image Rendering API
uuid: 84e04972-32ce-4aca-aae6-d5b8bbe761e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Componenti Image Server{#image-serving-components}

Scene7 Image Serving è costituito dai seguenti componenti:

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
   <td colname="col2"> <p>Esecuzione autonoma responsabile dell'avvio, dell'arresto e della sicurezza dello stato degli altri componenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Fornisce l'ambiente per la maggior parte dei componenti basati su Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servizio di monitoraggio/allarme </p> </td> 
   <td colname="col2"> <p>Applicazione J2EE. Fornisce monitoraggio del server e avvisi e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Server piattaforma </p> </td> 
   <td colname="col2"> <p>Applicazione J2EE. Gestisce le connessioni client, la registrazione e le comunicazioni con altri componenti. Accesso HTTP all'indirizzo <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Memorizzazione nella cache </p> </td> 
   <td colname="col2"> <p>Applicazione J2EE. Gestisce le cache dei dati del server piattaforma. Accesso HTTP a /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Esegue tutte le operazioni I/O relative all'elaborazione delle immagini e ai file di immagine. Per Linux sono disponibili file eseguibili a 32 bit e a 64 bit (solo a 32 bit per Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente rendering testo AEM </p> </td> 
   <td colname="col2"> <p>Una o più istanze del servizio di rendering del testo potrebbero essere attive quando vengono eseguite le operazioni <span class="codeph"> textPs=</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente di rendering SVG </p> </td> 
   <td colname="col2"> <p>Applicazione Java autonoma (non ospitata da Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendering delle immagini Scene7 (alias Render Server) </p> </td> 
   <td colname="col2"> <p>Richiede una licenza separata per l'attivazione. Accesso HTTP all'indirizzo <span class="filepath"> /ir/rendering</span>. Tutte le funzionalità di rendering delle immagini sono integrate nel server piattaforma e nel server immagini, senza componenti eseguibili separati. </p> </td> 
  </tr> 
 </tbody> 
</table>

Impostazioni di configurazione aggiuntive sono fornite dal catalogo predefinito ( [!DNL default.ini]) o da specifici cataloghi di immagini (per ulteriori informazioni, consultate [Image Catalogs](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)).

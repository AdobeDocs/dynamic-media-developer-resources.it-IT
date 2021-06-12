---
description: La libreria di immagini reattive è un modulo JavaScript che regola dinamicamente la qualità delle immagini servite da Dynamic Media e incorporate in pagine web reattive. Inoltre, offre una migliore qualità delle immagini sui dispositivi con schermi ad alta densità. La libreria può anche eseguire il rendering dinamico dei risultati da Smart Crop e Smart Swatch.
solution: Experience Manager
title: Informazioni sulla libreria di immagini reattive
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Informazioni sulla libreria di immagini reattive{#about-responsive-image-library}

La libreria di immagini reattive è un modulo JavaScript che regola dinamicamente la qualità delle immagini servite da Dynamic Media e incorporate in pagine web reattive. Inoltre, offre una migliore qualità delle immagini sui dispositivi con schermi ad alta densità. La libreria può anche eseguire il rendering dinamico dei risultati da Smart Crop e Smart Swatch.

## URL demo {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Il caso d’uso più semplice della libreria di immagini reattive è quello di definire un elenco di valori dei punti di interruzione per la larghezza dell’immagine. Questo elenco assicura che il rendering appropriato venga caricato e visualizzato quando un&#39;immagine viene ridimensionata a causa di modifiche nel layout di una pagina web derivanti dal ridimensionamento della finestra del browser da parte dell&#39;utente o dalla modifica dell&#39;orientamento del dispositivo. La libreria controlla continuamente le dimensioni dell&#39;immagine sullo schermo e ogni volta che viene raggiunta una nuova larghezza del punto di interruzione recupera una nuova rappresentazione dell&#39;immagine da Dynamic Media.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>URL demo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Di seguito è riportato un esempio semplice in cui l’immagine reattiva si trova all’interno di un contenitore che occupa il 50% della larghezza della pagina web. Ogni volta che la finestra del browser viene ridimensionata, la larghezza del contenitore cambia. Quando la larghezza dell’immagine raggiunge uno dei punti di interruzione configurati, impostati a 200, 400, 600 e 800 pixel a scopo illustrativo, viene scaricato e visualizzato un nuovo rendering. L'obiettivo è quello di evitare il caricamento di immagini di grandi dimensioni non necessarie e di risparmiare la larghezza di banda della rete. </p> <p>Fai clic sull’URL per aprire la pagina web, ridimensionare la finestra del browser e monitorare il traffico di rete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>L’esempio di Bootstrap seguente illustra lo stesso caso d’uso in una pagina web. In base a Bootstrap CSS, la cella di layout a cui viene aggiunta l’immagine reattiva può avere una delle seguenti larghezze: 360, 720 e 940 pixel. Questi valori sono esattamente ciò che viene passato come punti di interruzione alla libreria di immagini reattive. Dynamic Media garantisce l'utilizzo efficiente della larghezza di banda di rete del cliente. Inoltre, assicura che l'immagine venga visualizzata nelle dimensioni richieste, dato il layout della pagina web corrente, senza artefatti visivi derivanti dal ridimensionamento del browser lato client. </p> <p>Fai clic sull’URL per aprire la pagina web, ridimensionare la finestra del browser in modo da raggiungere diversi punti di interruzione del layout e monitorare il traffico di rete. </p> <p>I casi d’uso più avanzati includono l’associazione di diversi predefiniti immagine, comandi Image Server o entrambi con valori di punti di interruzione diversi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>In questo esempio vengono utilizzati predefiniti per immagini di diversa qualità e formato per diverse dimensioni dei punti di interruzione. Per un piccolo punto di interruzione, viene applicato un predefinito di bassa qualità che forza Image Serving a restituire l'immagine GIF compressa solo a sei colori. Un punto di interruzione medio utilizza un predefinito per immagini configurato per JPEG con compressione elevata. Il punto di interruzione più grande è associato a un predefinito per immagini di alta qualità che utilizza PNG senza perdita di dati. Questo metodo garantisce la trasmissione di immagini di alta qualità a tali dispositivi, partendo dal presupposto che i dispositivi con schermi più grandi abbiano una larghezza di banda e una potenza di elaborazione maggiori. </p> <p>Fai clic sull’URL per aprire la pagina web, ridimensionare la finestra del browser Web da più grande a più piccola e notare il degrado della qualità dell’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Oltre ai predefiniti per immagini, è possibile associare comandi Image Serving specifici a punti di interruzione. L’esempio seguente mostra come è possibile ritagliare gradualmente l’immagine del banner nell’area di interesse quando le dimensioni dell’immagine sullo schermo diventano più piccole. In questo caso, il punto di interruzione più grande non dispone di alcun comando Image Serving, quindi l’immagine del banner è completamente visibile. Al punto di interruzione medio si applica un ritaglio moderato, rendendo visibile solo il corridore con testo "In esecuzione". Al punto di interruzione piccolo viene applicato un maggior numero di ritaglio in modo che venga mostrato solo il prodotto. </p> <p>Fai clic sull’URL per aprire la pagina web e ridimensionare la finestra del browser. Osserva come l’immagine si ritaglia gradualmente passando da una dimensione più grande a una più piccola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>È inoltre possibile utilizzare i comandi Image Serving con Image Serving Templates per controllare alcuni parametri del modello in base alle dimensioni dell'immagine. In questo esempio successivo, viene utilizzato un modello Image Serving in cui la dimensione del font della sovrapposizione di testo è parametrizzata utilizzando il parametro <span class="codeph"> $fontsize </span> . L’immagine reattiva è configurata per utilizzare un font di dimensioni maggiori per immagini di dimensioni più piccole, in modo che il testo rimanga sempre leggibile: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisiti di sistema {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Hardware e software del server**

* Dynamic Media Image Serving 6.0.1 o versione successiva.

**Requisiti minimi del browser client**

* Microsoft® Windows® 7 o versione successiva; macOS X 10.8 o versione successiva
* Firefox 23, Safari 6, Chrome 29, IE 9 o versione successiva.
* iOS 6 o versione successiva
* Certificato su iPhone3GS o versioni successive e iPad2 o versioni successive (solo browser nativi).
* Android™ OS 2.3 o successivo.
* Internet Explorer su dispositivi mobili non è attualmente supportato.

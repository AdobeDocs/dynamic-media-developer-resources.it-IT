---
description: Libreria immagini reattiva è un modulo JavaScript che regola in modo dinamico la qualità delle immagini trasmesse da Scene7 e incorporate in pagine Web reattive. Offre inoltre una migliore qualità delle immagini sui dispositivi con schermi ad alta densità. La libreria può anche eseguire il rendering reattivo dei risultati da SmartCrop e Smart Swatch.
seo-description: Libreria immagini reattiva è un modulo JavaScript che regola in modo dinamico la qualità delle immagini trasmesse da Scene7 e incorporate in pagine Web reattive. Offre inoltre una migliore qualità delle immagini sui dispositivi con schermi ad alta densità. La libreria può anche eseguire il rendering reattivo dei risultati da SmartCrop e Smart Swatch.
seo-title: Informazioni sulla libreria di immagini reattive
solution: Experience Manager
title: Informazioni sulla libreria di immagini reattive
topic: Scene7 Image Serving - Image Rendering API
uuid: 0906a940-59ff-45b0-b509-57bd02f2da57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---


# Informazioni sulla libreria di immagini reattive{#about-responsive-image-library}

Libreria immagini reattiva è un modulo JavaScript che regola in modo dinamico la qualità delle immagini trasmesse da Scene7 e incorporate in pagine Web reattive. Offre inoltre una migliore qualità delle immagini sui dispositivi con schermi ad alta densità. La libreria può anche eseguire il rendering reattivo dei risultati da SmartCrop e Smart Swatch.

## URL demo {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Il caso d’uso più semplice della libreria di immagini reattive è definire un elenco di valori dei punti di interruzione per la larghezza dell’immagine. Questo elenco assicura che la rappresentazione appropriata venga caricata e visualizzata quando un&#39;immagine viene ridimensionata a causa delle modifiche apportate al layout della pagina Web da un utente che ridimensiona la finestra del browser o modifica l&#39;orientamento del dispositivo. La libreria effettua un monitoraggio continuo delle dimensioni dell’immagine sullo schermo e ogni volta che viene raggiunta una nuova larghezza, ottiene una nuova rappresentazione immagine da Scene7.

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
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Di seguito è riportato un semplice esempio in cui l’immagine reattiva si trova all’interno di un contenitore che occupa il 50% della larghezza della pagina Web. Ogni volta che la finestra del browser viene ridimensionata, la larghezza del contenitore cambia. Quando la larghezza dell’immagine raggiunge uno dei punti di interruzione configurati, impostati su 200, 400, 600 e 800 pixel a scopo illustrativo, viene scaricata e visualizzata una nuova rappresentazione. L'obiettivo è evitare di caricare immagini di grandi dimensioni e di risparmiare sulla larghezza di banda della rete. </p> <p>Fate clic sull’URL per aprire la pagina Web, ridimensionare la finestra del browser e monitorare il traffico di rete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>L’esempio di Bootstrap seguente illustra lo stesso caso di utilizzo in una pagina Web. In base a Bootstrap CSS, la cella di layout a cui viene aggiunta l'immagine reattiva può avere una delle seguenti larghezze: 360, 720 e 940 pixel. Questi sono i valori esatti che vengono passati come punti di interruzione alla libreria di immagini reattive. Scene7 garantisce l'utilizzo efficiente della larghezza di banda di rete del cliente. Inoltre, garantisce che l'immagine venga visualizzata nella dimensione esatta necessaria, dato il layout della pagina Web corrente, senza artefatti visivi che ne impediscano il ridimensionamento del browser lato client. </p> <p>Fate clic sull’URL per aprire la pagina Web, ridimensionare la finestra del browser per individuare diversi punti di interruzione del layout e monitorare il traffico di rete. </p> <p>Casi di utilizzo più avanzati includono l’associazione di diversi predefiniti per immagini, comandi Image Server o entrambi con valori di punti di interruzione diversi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>In questo esempio vengono utilizzati predefiniti per immagini di qualità e formato diversi per diverse dimensioni di punti di interruzione. Per un piccolo punto di interruzione, viene applicato un predefinito di bassa qualità che fa sì che Image Serving restituisca l’immagine GIF compressa solo a sei colori. Un punto di interruzione medio utilizza un predefinito per immagini configurato per JPEG con compressione elevata. Il punto di interruzione più grande è associato a un predefinito per immagini di alta qualità che utilizza il formato PNG senza perdita di dati. Questo metodo garantisce la distribuzione di immagini di alta qualità a tali dispositivi, partendo dal presupposto che i dispositivi con schermi più grandi abbiano una larghezza di banda e una potenza di elaborazione maggiori. </p> <p>Fate clic sull’URL per aprire la pagina Web, ridimensionate la finestra del browser Web da più grande a più piccola e notate come la qualità dell’immagine si riduce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Oltre ai predefiniti per immagini, è possibile associare specifici comandi Image Server ai punti di interruzione. L'esempio seguente mostra come sia possibile ritagliare gradualmente l'immagine del banner fino all'area di interesse, man mano che le dimensioni dell'immagine sullo schermo diventano più piccole. In questo caso, il punto di interruzione più grande non dispone di alcun comando Image Serving, pertanto l'immagine del banner è completamente visibile. Con un punto di interruzione medio viene applicato un ritaglio moderato, rendendo visibile solo il corridore con testo "In esecuzione". A un punto di interruzione piccolo, viene applicato un maggior ritaglio in modo che venga mostrato solo il prodotto. </p> <p>Fate clic sull’URL per aprire la pagina Web e ridimensionare la finestra del browser. L’immagine viene ritagliata gradualmente passando da una dimensione più grande a una più piccola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Potete anche usare i comandi Image Server con Image Server Templates per controllare alcuni parametri di modello in base alle dimensioni dell’immagine. In questo esempio successivo, viene utilizzato un modello Image Server in cui la dimensione del font della sovrapposizione di testo è parametrizzata utilizzando il parametro <span class="codeph"> $fontsize </span>. L’immagine reattiva è configurata per utilizzare un font di dimensioni maggiori per immagini di dimensioni ridotte, in modo da garantire che il testo rimanga sempre leggibile: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisiti di sistema {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Software e hardware per server**

* Scene7 Image Serving 6.0.1 o versione successiva.

**Requisiti minimi del browser client**

* Microsoft® Windows® 7 o versione successiva; Mac OS X 10.8 o versione successiva.
* Firefox 23, Safari 6, Chrome 29, IE 9 o versione successiva.
* iOS 6 o versione successiva.
* Certificato su iPhone3GS o versioni successive e iPad2 o versioni successive (solo browser nativi).
* Android OS 2.3 o successivo.
* Internet Explorer sui dispositivi mobili non è attualmente supportato.


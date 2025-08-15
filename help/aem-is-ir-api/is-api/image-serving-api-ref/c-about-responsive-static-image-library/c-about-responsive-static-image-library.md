---
description: La Libreria di immagini reattive è un modulo di JavaScript che regola dinamicamente la qualità delle immagini distribuite da Dynamic Media e incorporate nelle pagine web reattive. Inoltre, offre una migliore qualità delle immagini su dispositivi con schermi ad alta densità. La libreria può anche eseguire il rendering responsive dei risultati da Ritaglio avanzato e Campione avanzato.
solution: Experience Manager
title: Informazioni sulla libreria Immagine reattiva
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Informazioni sulla libreria Immagine reattiva{#about-responsive-image-library}

La Libreria di immagini reattive è un modulo di JavaScript che regola dinamicamente la qualità delle immagini distribuite da Dynamic Media e incorporate nelle pagine web reattive. Inoltre, offre una migliore qualità delle immagini su dispositivi con schermi ad alta densità. La libreria può anche eseguire il rendering responsive dei risultati da Ritaglio avanzato e Campione avanzato.

## URL demo {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Il caso d’uso più semplice della Libreria di immagini reattive è quello di definire un elenco di valori dei punti di interruzione per la larghezza dell’immagine. Questo elenco assicura che venga caricata e visualizzata la rappresentazione appropriata quando un’immagine viene ridimensionata a causa di modifiche nel layout della pagina web apportate da un utente che ridimensiona la finestra del browser o modifica l’orientamento del dispositivo. La libreria monitora continuamente le dimensioni delle immagini sullo schermo e ogni volta che viene raggiunta una nuova larghezza del punto di interruzione recupera una nuova rappresentazione dell’immagine da Dynamic Media.

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
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=it" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=it </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Di seguito è riportato un semplice esempio in cui l’immagine reattiva si trova all’interno di un contenitore che occupa il 50% della larghezza della pagina web. Ogni volta che la finestra del browser viene ridimensionata, la larghezza del contenitore cambia. Quando la larghezza dell’immagine raggiunge uno dei punti di interruzione configurati, impostati a 200, 400, 600 e 800 pixel a scopo illustrativo, viene scaricata e visualizzata una nuova rappresentazione. L'obiettivo è quello di evitare il caricamento di inutili immagini di grandi dimensioni e di risparmiare larghezza di banda. </p> <p>Fai clic sull’URL per aprire la pagina web, ridimensionare la finestra del browser e monitorare il traffico di rete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=it" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=it </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>L’esempio di Bootstrap seguente illustra lo stesso caso d’uso in una pagina web. Secondo il CSS Bootstrap, la cella layout alla quale viene aggiunta l’immagine responsive può avere una delle seguenti larghezze: 360, 720 e 940 pixel. Questi valori sono esattamente ciò che viene passato come punti di interruzione alla Libreria di immagini reattive. Dynamic Media garantisce un utilizzo efficace della larghezza di banda del client. Inoltre, garantisce che l’immagine venga visualizzata nelle dimensioni esatte necessarie-dato il layout della pagina web corrente-senza artefatti visivi dovuti al ridimensionamento del browser lato client. </p> <p>Fai clic sull’URL per aprire la pagina web, ridimensionare la finestra del browser per raggiungere diversi punti di interruzione del layout e monitorare il traffico di rete. </p> <p>Casi d’uso più avanzati includono l’associazione di diversi predefiniti immagine o comandi Image Server, o entrambi, con valori di punto di interruzione diversi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=it" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=it</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>In questo esempio vengono utilizzati predefiniti immagine con qualità e formato diversi per punti di interruzione di dimensioni diverse. Per un punto di interruzione ridotto, viene applicato un predefinito di bassa qualità che forza Image Server a restituire l'immagine GIF compressa solo a sei colori. Un punto di interruzione medio utilizza un predefinito immagine configurato per JPEG con compressione elevata. Il punto di interruzione più grande è associato a un predefinito immagine di alta qualità utilizzando PNG senza perdita di dati. Questo metodo garantisce che immagini di alta qualità vengano distribuite a tali dispositivi, partendo dal presupposto che i dispositivi con schermi più grandi abbiano una maggiore larghezza di banda e una maggiore potenza di elaborazione. </p> <p>Fai clic sull’URL per aprire la pagina web, ridimensionare la finestra del browser web dalle dimensioni maggiori a quelle più piccole e notare il deterioramento della qualità dell’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=it" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=it </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Oltre ai predefiniti per immagini, è possibile associare specifici comandi Image Server ai punti di interruzione. L'esempio seguente mostra come è possibile ritagliare gradualmente l'immagine del banner nell'area di interesse man mano che le dimensioni dell'immagine sullo schermo si riducono. In questo caso, il punto di interruzione più grande non dispone di alcun comando Image Server, pertanto l'immagine del banner è completamente visibile. Al punto di interruzione medio applica un ritaglio moderato, rendendo visibile solo l’esecutore con il testo "In esecuzione". In un punto di interruzione di piccole dimensioni, viene applicato un numero maggiore di ritagli in modo da visualizzare solo il prodotto. </p> <p>Fare clic sull'URL per aprire la pagina Web e ridimensionare la finestra del browser. Osserva come l’immagine viene ritagliata gradualmente quando passi da una dimensione più grande a una più piccola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=it" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=it </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>È inoltre possibile utilizzare i comandi Image Server con i modelli Image Server per controllare alcuni parametri di modello in base alle dimensioni dell'immagine. In questo esempio viene utilizzato un modello Image Server in cui la dimensione del font della sovrapposizione di testo è parametrizzata utilizzando il parametro <span class="codeph"> $fontsize </span>. L’immagine reattiva è configurata per utilizzare un font di dimensioni maggiori per le immagini di dimensioni inferiori, in modo che il testo rimanga sempre leggibile: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisiti di sistema {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Hardware e software per server**

* Dynamic Media Image Server 6.0.1 o versione successiva.

**Requisiti minimi browser client**

* Microsoft® Windows® 7 o versione successiva; macOS X 10.8 o versione successiva.
* Firefox 23, Safari 6, Chrome 29, IE 9 o versione successiva.
* iOS 6 o versione successiva.
* Certificato su iPhone3GS o versione successiva e iPad2 o versione successiva (solo browser nativi).
* Android™ OS 2.3 o versione successiva
* Internet Explorer su dispositivi mobili non è attualmente supportato.

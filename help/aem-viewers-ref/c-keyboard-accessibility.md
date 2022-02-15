---
title: Accesso facilitato alla tastiera e navigazione
description: Tutte le funzioni esposte nell’interfaccia del visualizzatore Basic Zoom, eCatalog, Ricerca eCatalog, A comparsa, Zoom in linea, File multimediali diversi, Spin, Video, Zoom, Dimensionale (3D), Carosello, Immagine interattiva, Video interattivo e Video360 sono accessibili da tastiera.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Accesso facilitato alla tastiera e navigazione{#keyboard-accessibility-and-navigation}

Tutte le funzioni esposte nell’interfaccia del visualizzatore Basic Zoom, eCatalog, Ricerca eCatalog, A comparsa, Zoom in linea, File multimediali diversi, Spin, Video, Zoom, Carosello, Dimensionale (3D), Immagine interattiva, Video interattivo e Video360 sono accessibili da tastiera.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Accesso facilitato alla tastiera e navigazione {#topic-f5650e9493404e55a3627c8d1366b861}

Tutte le funzioni esposte nell’interfaccia del visualizzatore Basic Zoom, eCatalog, Ricerca eCatalog, A comparsa, Zoom in linea, File multimediali diversi, Spin, Video, Zoom, Carosello, Dimensionale (3D), Immagine interattiva, Video interattivo e Video360 sono accessibili da tastiera.

L’utente finale può navigare tra gli elementi dell’interfaccia utente del visualizzatore utilizzando **[!UICONTROL Scheda]** e **[!UICONTROL Maiusc+Tab]** colpi di tasti. Utilizzo **[!UICONTROL Scheda]** sposta lo stato attivo al successivo elemento dell’interfaccia utente nell’ordine di tabulazione; utilizzo **[!UICONTROL Maiusc+Tab]** ripristina lo stato attivo dell’interfaccia utente precedente. L&#39;attraversamento della messa a fuoco segue la posizione naturale dell&#39;elemento dell&#39;interfaccia utente sullo schermo e si sposta in ordine da sinistra a destra, quindi dall&#39;alto verso il basso.

A seconda del sistema operativo e delle impostazioni del browser Web, l’elemento dell’interfaccia utente attivo riceve un’indicazione visiva di focus. Ad esempio, l’indicatore visivo può essere un bordo sottile intorno all’elemento dell’interfaccia utente.

È possibile disabilitare o personalizzare tale messa a fuoco evidenziata nel CSS del visualizzatore. Nel sommario di questo sistema della Guida, sotto un nome di visualizzatore specifico (ad esempio, Zoom di base o Video interattivo), fare clic su **Personalizzazione *nome del visualizzatore*** >** Evidenziazione **.

Le sequenze di tasti supportate dai singoli elementi dell’interfaccia utente dei visualizzatori sono, nella maggior parte dei casi, ovvie e facili da scoprire.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Azione </p> </th> 
   <th colname="col2" class="entry"> <p>Tastiera </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Attiva componenti pulsante </p> </td> 
   <td colname="col2"> <p>Spazio o tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoom avanti o indietro </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> o <span class="uicontrol"> - </span>, rispettivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ripristino dello zoom </p> </td> 
   <td colname="col2"> <p>Chiave Esc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Panning </p> </td> 
   <td colname="col2"> <p>Freccia su, giù, sinistra o destra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fissare un'immagine a 360 gradi </p> </td> 
   <td colname="col2"> <p>Utilizza i tasti freccia quando l'immagine è in uno stato di reset. </p> <p>Utilizza il tasto freccia su o giù quando lavori con set 360 gradi multidimensionali. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Selezione di campioni di prodotto </p> </td> 
   <td colname="col2"> <p>Freccia su, giù, sinistra o destra; Chiave iniziale o finale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attivazione dei campioni di prodotto </p> </td> 
   <td colname="col2"> <p>Spazio o tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivi, riavvolgimento graduale </p> </td> 
   <td colname="col2"> <p>Freccia sinistra o freccia su. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivi, avanti rapido </p> </td> 
   <td colname="col2"> <p>Freccia destra o freccia giù. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivi, inizio o fine </p> </td> 
   <td colname="col2"> <p>Chiave iniziale o finale, rispettivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivo, controllo del livello del volume quando la messa a fuoco è sul dispositivo di scorrimento </p> </td> 
   <td colname="col2"> <p>Freccia su, giù, sinistra o destra; Chiave iniziale o finale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivi, volume variabile </p> </td> 
   <td colname="col2"> <p>Tasti freccia, Home e Fine per controllare il livello del volume quando la messa a fuoco è sulla parte del dispositivo di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video, quando viene visualizzata la finestra di dialogo modale, l'attraversamento dello stato attivo diventa limitato solo ai controlli della finestra di dialogo. </p> </td> 
   <td colname="col2"> <p>Tasto ESC per chiudere la finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carosello, modifica immagine banner nella visualizzazione principale </p> </td> 
   <td colname="col2"> <p>Tasto freccia sinistra o destra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carosello, selezione dei punti attivi e attivazione dei punti attivi </p> </td> 
   <td colname="col2"> <p>Selezione punti attivi: Freccia su, giù, sinistra o destra </p> <p>Attivazione punto attivo: Spazio o tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, modifica l’immagine della pagina nella vista principale </p> </td> 
   <td colname="col2"> <p> Tasti freccia sinistra o destra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, selezione miniature </p> </td> 
   <td colname="col2"> <p>tasti freccia; Chiave iniziale e finale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, attivazione campioni </p> </td> 
   <td colname="col2"> <p>Spazio o tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, selezione di punti caldi </p> </td> 
   <td colname="col2"> <p>Tasti freccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, attivazione </p> </td> 
   <td colname="col2"> <p>Spazio o tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, attivazione dei componenti a discesa </p> </td> 
   <td colname="col2"> <p> Freccia giù; Spazio o tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, quando lo stato attivo è nel pannello a discesa </p> </td> 
   <td colname="col2"> <p>Utilizza i tasti freccia per selezionare un elemento specifico nel pannello prima di attivarlo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, quando viene visualizzata una finestra di dialogo modale, l’attraversamento dello stato attivo diventa limitato solo ai controlli della finestra di dialogo. </p> </td> 
   <td colname="col2"> <p>Tasto ESC per chiudere la finestra di dialogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

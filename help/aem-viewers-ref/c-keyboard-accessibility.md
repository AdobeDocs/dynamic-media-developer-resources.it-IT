---
title: Accessibilità della tastiera e navigazione
description: Tutte le funzioni esposte nell'interfaccia di visualizzazione Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Dimensional (3D), Carosello, Immagine interattiva, Video interattivo e Video360 sono accessibili da tastiera.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Accessibilità della tastiera e navigazione{#keyboard-accessibility-and-navigation}

Tutte le funzioni esposte nell&#39;interfaccia di visualizzazione Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Carosello, Dimensional (3D), Interactive Image, Interactive Video e Video360 sono accessibili da tastiera.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Accessibilità della tastiera e navigazione {#topic-f5650e9493404e55a3627c8d1366b861}

Tutte le funzioni esposte nell&#39;interfaccia di visualizzazione Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Carosello, Dimensional (3D), Interactive Image, Interactive Video e Video360 sono accessibili da tastiera.

Un utente finale può spostarsi tra gli elementi dell&#39;interfaccia utente del visualizzatore utilizzando **[!UICONTROL Tab]** e **[!UICONTROL Maiusc+Tab]**. Se si utilizza **[!UICONTROL Tab]**, lo stato attivo dell&#39;input viene spostato sull&#39;elemento successivo dell&#39;interfaccia utente nell&#39;ordine di tabulazione. Se si utilizza **[!UICONTROL Maiusc+Tab]**, lo stato attivo dell&#39;input viene riportato sull&#39;elemento precedente dell&#39;interfaccia utente. L&#39;attraversamento della messa a fuoco segue la posizione naturale degli elementi dell&#39;interfaccia sullo schermo e si sposta da sinistra a destra e quindi dall&#39;alto al basso.

A seconda del sistema operativo e delle impostazioni del browser Web, l&#39;elemento dell&#39;interfaccia utente che dispone di input focus riceve un&#39;indicazione di focus visivo. Ad esempio, l’indicatore visivo può essere un bordo sottile rappresentato intorno all’elemento dell’interfaccia utente.

È possibile disabilitare o personalizzare tale evidenziazione dello stato attivo nel CSS del visualizzatore. Nel sommario di questa Guida in linea, sotto un nome di visualizzatore specifico (ad esempio, Zoom di base o Video interattivo), fare clic su **Personalizzazione del *nome del visualizzatore*** >** Evidenziazione elemento attivo **.

Le sequenze di tasti supportate dai singoli elementi dell’interfaccia utente del visualizzatore sono, nella maggior parte dei casi, ovvie e facili da individuare.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Azione </p> </th> 
   <th colname="col2" class="entry"> <p>Tasto </p> </th> 
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
   <td colname="col1"> <p>Ripristino zoom </p> </td> 
   <td colname="col2"> <p>Chiave ESC. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Panoramica </p> </td> 
   <td colname="col2"> <p>Freccia su, giù, sinistra o destra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rotazione di un'immagine a 360 gradi </p> </td> 
   <td colname="col2"> <p>Utilizzare i tasti freccia quando l'immagine è in stato di ripristino. </p> <p>Utilizzare i tasti freccia su o giù quando si lavora con set 360 gradi multidimensionali. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Selezione del campione di prodotto </p> </td> 
   <td colname="col2"> <p>Freccia Su, Giù, Sinistra o Destra; tasto Home o Fine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attivazione campione prodotto </p> </td> 
   <td colname="col2"> <p>Spazio o tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivi, riavvolgimento graduale </p> </td> 
   <td colname="col2"> <p>Freccia sinistra o freccia su. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivi, avanzamento rapido </p> </td> 
   <td colname="col2"> <p>Freccia destra o freccia giù. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivo, vai all’inizio o alla fine </p> </td> 
   <td colname="col2"> <p>Chiave Home o Fine, rispettivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivi, controlla il livello del volume quando la messa a fuoco è sul cursore </p> </td> 
   <td colname="col2"> <p>Freccia Su, Giù, Sinistra o Destra; tasto Home o Fine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video e video interattivi, volume mutabile </p> </td> 
   <td colname="col2"> <p>Tasti freccia, Home e End per controllare il livello del volume quando lo stato attivo si trova sulla parte del dispositivo di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video: quando viene visualizzata la finestra di dialogo modale, l'attraversamento dello stato attivo è limitato solo ai controlli della finestra di dialogo. </p> </td> 
   <td colname="col2"> <p>Tasto ESC per chiudere la finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carosello, cambia l'immagine del banner nella vista principale </p> </td> 
   <td colname="col2"> <p>Freccia sinistra o destra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carosello, selezione di punti attivi e attivazione di punti attivi </p> </td> 
   <td colname="col2"> <p>Selezione di punti attivi: freccia su, freccia giù, freccia sinistra o freccia destra </p> <p>Attivazione punto di attivazione: Spazio o Tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, modifica l'immagine della pagina nella visualizzazione principale </p> </td> 
   <td colname="col2"> <p> Tasti freccia sinistra o destra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, selezione miniature </p> </td> 
   <td colname="col2"> <p>Tasti freccia; tasto Home e tasto Fine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, attivazione campioni </p> </td> 
   <td colname="col2"> <p>Spazio o tasto Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, selezione hot spot </p> </td> 
   <td colname="col2"> <p>Tasti di direzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, attivazione </p> </td> 
   <td colname="col2"> <p>Spazio o tasti Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, attivazione dei componenti del menu a discesa </p> </td> 
   <td colname="col2"> <p> Freccia giù; Spazio o Invio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, quando lo stato attivo si trova nel pannello a tendina </p> </td> 
   <td colname="col2"> <p>Utilizza i tasti freccia per selezionare un elemento specifico nel pannello prima di attivarlo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, quando viene visualizzata una finestra di dialogo modale, l'attraversamento dello stato attivo è limitato solo ai controlli della finestra di dialogo. </p> </td> 
   <td colname="col2"> <p>Tasto ESC per chiudere la finestra di dialogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

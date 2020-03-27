---
description: Utilizzate i seguenti comandi per la formattazione avanzata del testo.
seo-description: Utilizzate i seguenti comandi per la formattazione avanzata del testo.
seo-title: Formattazione avanzata del testo
solution: Experience Manager
title: Formattazione avanzata del testo
topic: Scene7 Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Formattazione avanzata del testo{#advanced-text-formatting}

Utilizzate i seguenti comandi per la formattazione avanzata del testo.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descrizione </th> 
   <th class="entry"> Note </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn <span class="varname"> N </span></span> </td> 
   <td> <p>Pedice senza modifica della dimensione del font. </p> </td> 
   <td> <p>posizione in punti intermedi; il valore predefinito è 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span></span> </td> 
   <td> <p>Apice senza modifica della dimensione del font. </p> </td> 
   <td> <p>posizione in punti intermedi; il valore predefinito è 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span></span> </td> 
   <td> <p>Disabilita/abilita in base alla dimensione font specificata. </p> </td> 
   <td> <p>Dimensione del carattere in mezzo punto, sopra il quale applicare la crenatura; 0 per disabilitare la crenatura; il valore predefinito è 1 per la crenatura di tutte le dimensioni di font su ½ punto. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningottico </span> </td> 
   <td> <p>Selezionate la crenatura ottica. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernmetrica </span> </td> 
   <td> <p>Selezionate la crenatura metrica. </p> </td> 
   <td> <p>Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span></span> </td> 
   <td> <p>Modificare la spaziatura dei caratteri. </p> </td> 
   <td> <p>punti del trimestre positivi o negativi; il valore predefinito è 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span></span> </td> 
   <td> <p>Modificare la spaziatura dei caratteri. </p> </td> 
   <td> <p>Twip positivi o negativi. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span></span> </td> 
   <td> <p>Ridimensionamento orizzontale dei caratteri. </p> </td> 
   <td> <p>percentuale positiva o negativa; il valore predefinito è 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscale <span class="varname"> N </span></span> </td> 
   <td> <p>Ridimensionamento verticale dei caratteri. </p> </td> 
   <td> <p>percentuale positiva o negativa; il valore predefinito è 100; Estensione Scene7. </p> <p> <span class="codeph"> \charscaley ridimensiona </span> anche l’interlinea se applicata con <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> mantiene sempre l'interlinea indipendentemente dalla quantità di ridimensionamento verticale dei caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Selezionare il flusso di caratteri da sinistra a destra. </p> </td> 
   <td> <p>Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Selezionare il flusso di caratteri da destra a sinistra. </p> </td> 
   <td> <p> <span class="codeph"> text= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span></span> </td> 
   <td> <p>Abilita adattamento alla copia e imposta la dimensione font massima consentita. </p> </td> 
   <td> <p>Dimensione del font in mezzo punto; solo <span class="codeph"> textPs= </span> ; Estensione Scene7. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span></span> </td> 
   <td> <p>Numero massimo di righe di adattamento alla copia (limitazione morbida). </p> </td> 
   <td> <p>0 per nessuna limitazione di linea; solo <span class="codeph"> textPs= </span> ; Estensione Scene7. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span></span> </td> 
   <td> <p>Numero massimo di righe di testo da copiare (troncamento). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; Estensione Scene7. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span></span> </td> 
   <td> <p>Orientamento del carattere. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignorati per i font non romani; ignorato quando <span class="codeph"> \stextflow1 non </span> è attivo. </p> <p>0 vertical (predefinito). </p> <p>1 ruotato di 90 gradi in senso orario. </p> </td> 
  </tr> 
 </tbody> 
</table>


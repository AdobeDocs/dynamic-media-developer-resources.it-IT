---
description: Utilizzare i seguenti comandi per la formattazione avanzata del testo.
solution: Experience Manager
title: Formattazione testo avanzata
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 1%

---


# Formattazione testo avanzata{#advanced-text-formatting}

Utilizzare i seguenti comandi per la formattazione avanzata del testo.

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
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Pedice senza modifica della dimensione del font. </p> </td> 
   <td> <p>posizione in mezzo punto; Il valore predefinito è 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Apice senza modifica della dimensione del font. </p> </td> 
   <td> <p>posizione in mezzo punto; Il valore predefinito è 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Disabilita/abilita in base alle dimensioni del carattere specificate. </p> </td> 
   <td> <p>Dimensione del carattere in mezzo punto, al di sopra del quale applicare la crenatura; 0 per disabilitare la crenatura; Il valore predefinito è 1 per la crenatura di tutte le dimensioni di font oltre ½ punto. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningottico  </span> </td> 
   <td> <p>Selezionare la crenatura ottica. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernmetrico  </span> </td> 
   <td> <p>Seleziona la crenatura metrica. </p> </td> 
   <td> <p>Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Modificare la spaziatura dei caratteri. </p> </td> 
   <td> <p>punti di trimestre positivi o negativi; Il valore predefinito è 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Modificare la spaziatura dei caratteri. </p> </td> 
   <td> <p>Twip positivi o negativi. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Scala orizzontale dei caratteri. </p> </td> 
   <td> <p>percentuale positiva o negativa; Il valore predefinito è 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Ridimensionamento verticale dei caratteri. </p> </td> 
   <td> <p>percentuale positiva o negativa; il valore predefinito è 100; Estensione Dynamic Media. </p> <p> <span class="codeph"> \charscaley ridimensiona  </span> anche l’interlinea quando viene applicata con  <span class="codeph"> text=  </span>. <span class="codeph"> textPs= conserva  </span> sempre l'interlinea indipendentemente dalla quantità di ridimensionamento verticale dei caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>Selezionare il flusso di caratteri da sinistra a destra. </p> </td> 
   <td> <p>Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>Selezionare il flusso di caratteri da destra a sinistra. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Abilita l'adattamento alla copia e imposta la dimensione massima consentita del font. </p> </td> 
   <td> <p>Dimensione del carattere in mezzo punto; Solo <span class="codeph"> textPs= </span>; Estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Numero massimo di righe di adattamento (limite morbido). </p> </td> 
   <td> <p>0 per nessuna limitazione della linea; Solo <span class="codeph"> textPs= </span>; Estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Numero massimo di righe di adattamento (troncamento). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; Estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Orientamento del carattere. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorati per i caratteri non romani; ignorato quando  <span class="codeph"> \stextflow1 non  </span> è attivo. </p> <p>0 verticale (predefinito). </p> <p>1 ruotato di 90 gradi in senso orario. </p> </td> 
  </tr> 
 </tbody> 
</table>


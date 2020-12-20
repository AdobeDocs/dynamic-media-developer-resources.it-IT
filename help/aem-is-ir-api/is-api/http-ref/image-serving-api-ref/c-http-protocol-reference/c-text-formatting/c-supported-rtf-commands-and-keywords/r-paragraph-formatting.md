---
description: Sono supportati i seguenti comandi di formattazione dei paragrafi.
seo-description: Sono supportati i seguenti comandi di formattazione dei paragrafi.
seo-title: Formattazione paragrafo
solution: Experience Manager
title: Formattazione paragrafo
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Formattazione paragrafo{#paragraph-formatting}

Sono supportati i seguenti comandi di formattazione dei paragrafi.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Comando </p> </th> 
   <th class="entry"> <p>Descrizione </p> </th> 
   <th class="entry"> <p>Note </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>Ripristina la formattazione predefinita del paragrafo. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>Allinea a sinistra il testo. </p> </td> 
   <td> <p>Predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>Allinea a destra il testo. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>Centra il testo in orizzontale. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>Giustifica il testo in orizzontale. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>Allinea a sinistra l’ultima riga di un paragrafo. </p> </td> 
   <td> <p>Default; Solo <span class="codeph"> textPs= </span>; ignorato se <span class="codeph"> \qj </span>non è attivo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>Allineare a destra l’ultima riga di un paragrafo giustificato. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorato se  <span class="codeph"> \qj non  </span> è attivo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>Centra l’ultima riga di un paragrafo giustificato. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorato se  <span class="codeph"> \qj non  </span>è attivo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>Sostenete (estendete) l’ultima riga di un paragrafo giustificato. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorato se  <span class="codeph"> \qj non  </span>è attivo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Rientro prima riga. </p> </td> 
   <td> <p>Twip; Solo <span class="codeph"> textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Rientro sinistro. </p> </td> 
   <td> <p>Twip; Solo <span class="codeph"> textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Rientro destro. </p> </td> 
   <td> <p>Twip; Solo <span class="codeph"> textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Spazio tra le righe. </p> </td> 
   <td> <p>0 (impostazione predefinita) per l'interlinea automatica; valori positivi per utilizzare il valore solo se maggiore della spaziatura predefinita tra le righe; valore negativo per forzare la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Flag multiplo per l'interlinea. </p> </td> 
   <td> <p>Impostato su 0 (predefinito) se <span class="codeph"> \sl </span> è in twip, su 1 se <span class="codeph"> \sl </span> è in multipli della spaziatura predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Spazio aggiuntivo prima del paragrafo. </p> </td> 
   <td> <p>Twip; <span class="codeph"> text= </span>applica <span class="codeph"> \sb </span> al primo paragrafo della casella di testo, <span class="codeph"> textPs= </span> no. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Spazio aggiuntivo dopo il paragrafo. </p> </td> 
   <td> <p>Twip; <span class="codeph"> text= </span> applica <span class="codeph"> \sa </span> all'ultimo paragrafo della casella di testo, mentre <span class="codeph"> textPs= </span> non lo è. </p> </td> 
  </tr> 
 </tbody> 
</table>


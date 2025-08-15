---
description: Sono supportati i seguenti comandi di formattazione dei paragrafi.
solution: Experience Manager
title: Formattazione dei paragrafi
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Formattazione dei paragrafi{#paragraph-formatting}

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
   <td> <span class="codeph"> \Pard </span> </td> 
   <td> <p>Reimposta predefinita la formattazione del paragrafo. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>Allineamento a sinistra del testo. </p> </td> 
   <td> <p>Impostazione predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>Allineare il testo a destra. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>Centra il testo orizzontalmente. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Giustifica il testo orizzontalmente. </p> </td> 
   <td> <p> <span class="codeph"> textPs= Solo </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>Allineare a sinistra l'ultima riga di un paragrafo. </p> </td> 
   <td> <p>Default; <span class="codeph"> textPs= </span> only; ignorato se <span class="codeph"> \qj </span>non è attivo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>Allineare a destra l'ultima riga di un paragrafo giustificato. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignorato se <span class="codeph"> \qj </span> non è attivo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>Centra l'ultima riga di un paragrafo giustificato. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignorato se <span class="codeph"> \qj </span>non è attivo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>Sustificare (allungare) l'ultima riga di un paragrafo giustificato. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignorato se <span class="codeph"> \qj </span>non è attivo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>Rientro della prima riga. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= solo </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>Rientro sinistro. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>Rientro destro. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= solo </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>Spazio tra le righe. </p> </td> 
   <td> <p>0 (predefinito) per l'interlinea automatico; valori positivi per utilizzare il valore solo se maggiore dell'interlinea predefinita; Valore negativo per forzare la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>Interlinea per più contrassegno. </p> </td> 
   <td> <p>Imposta su 0 (valore predefinito) se <span class="codeph"> \sl </span> è in twips, su 1 se <span class="codeph"> \sl </span> è in multipli della spaziatura predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>Spazio extra prima del paragrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> testo= </span>applica <span class="codeph"> \sb </span> al primo paragrafo della casella di testo, <span class="codeph"> textPs= </span> no. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>Spazio aggiuntivo dopo il paragrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> applica <span class="codeph"> \sa </span> all'ultimo paragrafo della casella di testo, <span class="codeph"> textPs= </span> no. </p> </td> 
  </tr> 
 </tbody> 
</table>

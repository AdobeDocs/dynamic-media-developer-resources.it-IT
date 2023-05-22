---
description: Utilizzare i seguenti comandi per la codifica dei caratteri.
solution: Experience Manager
title: Codifica caratteri
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# Codifica caratteri{#character-encoding}

Utilizzare i seguenti comandi per la codifica dei caratteri.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descrizione </th> 
   <th class="entry"> Note </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>Singolo carattere a 8 bit. </p> </td> 
   <td> <p><span class="varname"> HH</span> deve essere un valore esadecimale a 2 cifre. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Singolo carattere Unicode. </p> </td> 
   <td> <p><span class="varname"> N</span> è un numero intero a 2 byte con segno, pertanto un valore Unicode maggiore di 32767 deve essere espresso come numero negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Dimensione caratteri Unicode. </p> </td> 
   <td> <p>Numero di byte corrispondenti al carattere Unicode specificato. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Seguono caratteri da area ANSI bassa. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \che </span> </td> 
   <td> <p>Seguono caratteri da area ANSI elevata. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Seguono caratteri a doppio byte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

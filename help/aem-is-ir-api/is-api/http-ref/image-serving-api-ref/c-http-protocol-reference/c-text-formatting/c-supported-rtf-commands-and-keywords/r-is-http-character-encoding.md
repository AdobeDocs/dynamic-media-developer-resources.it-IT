---
title: Codifica caratteri
description: Utilizzare i seguenti comandi per la codifica dei caratteri.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
TQID: 'https://experienceleague.adobe.com/rptRmm7xxUUF2l5WTYXjvbaifW2z5XKeCQIqa5XLFh4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
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
   <td> <p><span class="varname"> N</span> è un numero intero a 2 byte con segno e pertanto un valore Unicode maggiore di 32767 deve essere espresso come numero negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Dimensione caratteri Unicode. </p> </td> 
   <td> <p>Numero di byte corrispondenti a un determinato carattere Unicode. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Caratteri dell'area ANSI bassa. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Caratteri dell'area ANSI alta. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Seguono caratteri a doppio byte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

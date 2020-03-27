---
description: Utilizzare i comandi seguenti per la codifica dei caratteri.
seo-description: Utilizzare i comandi seguenti per la codifica dei caratteri.
seo-title: Codifica dei caratteri
solution: Experience Manager
title: Codifica dei caratteri
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Codifica dei caratteri{#character-encoding}

Utilizzare i comandi seguenti per la codifica dei caratteri.

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
   <td> <p><span class="varname"> Deve</span> essere un valore esadecimale di 2 cifre. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Singolo carattere Unicode. </p> </td> 
   <td> <p><span class="varname"> N</span> è un numero intero a 2 byte con segno, pertanto un valore Unicode maggiore di 32767 deve essere espresso come numero negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Dimensione dei caratteri Unicode. </p> </td> 
   <td> <p>Numero di byte corrispondenti a un carattere Unicode specificato. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Seguono i caratteri provenienti da un’area bassa ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Seguono caratteri provenienti da un'area ANSI elevata. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Seguono i caratteri a doppio byte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>


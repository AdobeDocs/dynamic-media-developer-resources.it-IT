---
description: Utilizzare i seguenti comandi per la formattazione avanzata del testo.
solution: Experience Manager
title: Formattazione testo avanzata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
TQID: 'https://experienceleague.adobe.com/ZTUWB5N6T-I3DnokCqX--dj9g-807-D9Fv8l20opVkg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 0%

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>Pedice senza modifica della dimensione del carattere. </p> </td> 
   <td> <p>Posizione in punti intermedi; il valore predefinito è 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>Apice senza modifica della dimensione del carattere. </p> </td> 
   <td> <p>Posizione in punti intermedi; il valore predefinito è 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \crenatura di <span class="varname"> N </span> </span> </td> 
   <td> <p>Disabilita/abilita alla dimensione font specificata. </p> </td> 
   <td> <p>Dimensione font in punti dimezzati, sopra la quale applicare la crenatura; 0 per disattivare la crenatura; il valore predefinito è 1 per crenatura di tutte le dimensioni font superiori a ½ punto. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>Selezionare crenatura ottica. </p> </td> 
   <td> <p> <span class="codeph"> textPs= solo </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>Selezionate la crenatura metrica. </p> </td> 
   <td> <p>Impostazione predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>Modificare la spaziatura dei caratteri. </p> </td> 
   <td> <p>Quarti positivi o negativi; il valore predefinito è 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>Modificare la spaziatura dei caratteri. </p> </td> 
   <td> <p>Twip positivi o negativi. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Ridimensionamento orizzontale dei caratteri. </p> </td> 
   <td> <p>Percentuale positiva o negativa; il valore predefinito è 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>Ridimensionamento verticale dei caratteri. </p> </td> 
   <td> <p>Percentuale positiva o negativa; il valore predefinito è 100; estensione Dynamic Media. </p> <p> <span class="codeph"> \charscaley </span> ridimensiona anche l'interlinea se applicata con <span class="codeph"> testo= </span>. <span class="codeph"> textPs= </span> mantiene sempre l'interlinea indipendentemente dal ridimensionamento verticale dei caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Seleziona il flusso di caratteri da sinistra a destra. </p> </td> 
   <td> <p>Impostazione predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Seleziona il flusso di caratteri da destra a sinistra. </p> </td> 
   <td> <p> <span class="codeph"> testo= solo </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>Attivate l'adattamento per la copia e impostate le dimensioni massime consentite per il carattere. </p> </td> 
   <td> <p>Dimensione font in punti dimezzati; <span class="codeph"> solo textPs= </span>; estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Numero massimo di righe di adattamento della copia (limitazione soft). </p> </td> 
   <td> <p>0 senza limite di riga; <span class="codeph"> solo textPs= </span>; estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Numero massimo di righe di adattamento alla copia (troncamento). </p> </td> 
   <td> <p> <span class="codeph"> solo textPs= </span>; estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientamento carattere. </p> </td> 
   <td> <p> <span class="codeph"> solo textPs= </span>; ignorato per i font non romani; ignorato quando <span class="codeph"> \stextflow1 </span> non è attivo. </p> <p>0 verticale (impostazione predefinita). </p> <p>1 ruotato di 90 gradi in senso orario. </p> </td> 
  </tr> 
 </tbody> 
</table>

---
description: Le seguenti proprietà del documento sono supportate nelle caselle di testo.
solution: Experience Manager
title: Proprietà documento (casella di testo)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
TQID: 'https://experienceleague.adobe.com/U8T6F0KmGyopf6rXM0-zssY-hpfKPVUHWt-vO8aA7xM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Proprietà documento (casella di testo){#document-text-box-properties}

Le seguenti proprietà del documento sono supportate nelle caselle di testo.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Comando</b> </th> 
   <th class="entry"> <b>Descrizione</b> </th> 
   <th class="entry"> <b>Note</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>Tabella caratteri. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>Set di caratteri per il carattere <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>Tavola colori RGB. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>Tavola colori CMYK. </p> </td> 
   <td> <p>Estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>Tavola colori per i colori Image Server. </p> </td> 
   <td> <p>Estensione Dynamic Media; <span class="codeph"> solo textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente colore rosso. </p> </td> 
   <td> <p>Può essere visualizzato solo in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \verde <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente colore verde. </p> </td> 
   <td> <p>Può essere visualizzato solo in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blu <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente colore blu. </p> </td> 
   <td> <p>Può essere visualizzato solo in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ciano <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente colore ciano. </p> </td> 
   <td> <p>Estensione Dynamic Media; può essere visualizzata solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente colore magenta. </p> </td> 
   <td> <p>Estensione Dynamic Media; può essere visualizzata solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \giallo <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente colore giallo. </p> </td> 
   <td> <p>Estensione Dynamic Media; può essere visualizzata solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \nero <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente colore nero. </p> </td> 
   <td> <p>Estensione Dynamic Media; può essere visualizzata solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>Margine sinistro. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= Solo </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>Margine destro. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= Solo </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>Margine superiore. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= Solo </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>Margine inferiore. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= Solo </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>Allinea in alto il testo nella casella di testo. </p> </td> 
   <td> <p>Predefinito </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>Allinea in basso il testo nella casella di testo. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>Centrare il testo nella casella di testo. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientamento del testo. </p> </td> 
   <td> <p>Flusso di testo specifico per la lingua; <span class="codeph"> textPs= </span> solo 0 (impostazione predefinita) a sinistra-destra, in alto-basso (europeo) 1 in alto-in basso, a destra-a sinistra (estremo oriente) </p> </td> 
  </tr> 
 </tbody> 
</table>

---
description: 'Visualizza cornici di testo sovrapposte con segno più. Un indicatore di testo in eccesso mostra quando il testo eccede lo spazio allocato al testo in una cornice di testo (o nell’ultima cornice di testo nel caso di testo in più cornici concatenate). Questo indicatori è una casella rossa contenente un segno più (+). '
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 60%

---

# markOverflowingTextFrames{#markoverflowingtextframes}

Visualizza cornici di testo sovrapposte con segno più. Un indicatore di testo in eccesso mostra quando il testo eccede lo spazio allocato al testo in una cornice di testo (o nell’ultima cornice di testo nel caso di testo in più cornici concatenate). Questo indicatori è una casella rossa contenente un segno più (+). 

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverflowingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

L’impostazione del modificatore `markOverflowingTextFrames=1` tramite una chiamata URL contrassegna tutte le cornici di testo in cui il testo viene sovraimpostato con un segno più. Inoltre, nell’anteprima di Dynamic Media Classic, l’indicatore di testo non inserito è impostato su &quot; `TRUE`&quot; per impostazione predefinita.

Il valore predefinito è 0.

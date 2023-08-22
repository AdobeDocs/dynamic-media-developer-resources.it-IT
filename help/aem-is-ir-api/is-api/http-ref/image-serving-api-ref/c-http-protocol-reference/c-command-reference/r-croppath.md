---
title: cropPathE
description: Consente di ritagliare fino al riquadro di delimitazione di un percorso denominato incorporato. Il ritaglio, a sua volta, cambia le dimensioni dell’immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# cropPathE{#croppathe}

Consente di ritagliare fino al riquadro di delimitazione di un percorso denominato incorporato. Il ritaglio, a sua volta, cambia le dimensioni dell’immagine.

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nome del percorso incorporato nell'immagine sorgente del livello (solo ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> è il nome di un tracciato incorporato nell'immagine sorgente del livello. Il percorso viene trasformato automaticamente in base alle necessità per mantenere l'allineamento relativo con il contenuto dell'immagine. Se più di uno <span class="codeph"><span class="varname"> pathName</span></span> , il server ritaglia il riquadro di delimitazione di ciascun percorso, uno alla volta. Qualsiasi <span class="codeph"><span class="varname"> pathName</span></span> non trovato nell'immagine di origine viene ignorato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti.

`cropPathE=` viene ignorato se nell&#39;immagine di origine del livello non viene trovato alcun percorso con il nome specificato o se l&#39;origine del livello non è un&#39;immagine.

## Predefinito {#section-d1986aa31af14767aeb1b4a57add67f4}

Nessuno, senza ritaglio aggiuntivo del livello.

## Consultate anche {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[ritagliare](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

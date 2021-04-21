---
description: Consente di ritagliare il riquadro di delimitazione di un percorso incorporato denominato. Questo ritaglio, a sua volta, modifica le dimensioni dell'immagine.
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# cropPathE{#croppathe}

Consente di ritagliare il riquadro di delimitazione di un percorso incorporato denominato. Questo ritaglio, a sua volta, modifica le dimensioni dell&#39;immagine.

`cropPathE= *``*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nome del percorso incorporato nell’immagine sorgente del livello (solo ASCII). </p> <p> <span class="codeph"><span class="varname"> </span></span> pathName è il nome di un tracciato incorporato nell'immagine sorgente del livello. Il percorso viene automaticamente trasformato in base alle esigenze per mantenere l’allineamento relativo con il contenuto dell’immagine. Se sono specificati più <span class="codeph"><span class="varname"> pathName</span></span>, il server ritaglia il riquadro di delimitazione di ciascun percorso, uno alla volta. Qualsiasi <span class="codeph"><span class="varname"> pathName</span></span> non trovato nell'immagine di origine viene ignorato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli di effetto.

`cropPathE=` viene ignorato se nell&#39;immagine sorgente del livello non viene trovato alcun percorso con il nome specificato, o se la sorgente del livello non è un&#39;immagine.

## Predefinito {#section-d1986aa31af14767aeb1b4a57add67f4}

Nessuno, senza ritaglio aggiuntivo del livello.

## Consultate anche {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[ritaglio](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

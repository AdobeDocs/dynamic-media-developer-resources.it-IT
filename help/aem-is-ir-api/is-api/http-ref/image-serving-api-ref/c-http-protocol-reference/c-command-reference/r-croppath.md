---
description: Consente di ritagliare il rettangolo di selezione di un tracciato con nome incorporato. Questo ritaglio, a sua volta, modifica le dimensioni dell’immagine.
seo-description: Consente di ritagliare il rettangolo di selezione di un tracciato con nome incorporato. Questo ritaglio, a sua volta, modifica le dimensioni dell’immagine.
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
topic: Scene7 Image Serving - Image Rendering API
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cropPathE{#croppathe}

Consente di ritagliare il rettangolo di selezione di un tracciato con nome incorporato. Questo ritaglio, a sua volta, modifica le dimensioni dell’immagine.

`cropPathE= *`pathNamepathName`*&#42;[, *``*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nome del tracciato incorporato nell’immagine sorgente del livello (solo ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> è il nome di un tracciato incorporato nell’immagine sorgente del livello. Il tracciato viene automaticamente trasformato in base alle esigenze per mantenere l’allineamento relativo con il contenuto dell’immagine. Se è specificato più <span class="codeph"><span class="varname"> pathName</span></span> , il server ritaglia il rettangolo di selezione di ciascun percorso, uno alla volta. Eventuali <span class="codeph"><span class="varname"> nome</span></span> percorso non trovati nell’immagine di origine vengono ignorati. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attributo layer. Si applica al livello corrente o all’immagine composita, se `layer=comp`. Ignorato dai livelli degli effetti.

`cropPathE=` viene ignorato se nell’immagine sorgente del livello non viene trovato alcun percorso con il nome specificato o se la sorgente del livello non è un’immagine.

## Predefinito {#section-d1986aa31af14767aeb1b4a57add67f4}

Nessuno, per nessun ritaglio aggiuntivo del livello.

## Consultate anche {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[ritaglio](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

---
description: Capovolgi livello. Riflette il livello orizzontalmente, verticalmente o entrambi dopo l’applicazione di ritaglia= e prima di ruotare= e estendere=.
seo-description: Capovolgi livello. Riflette il livello orizzontalmente, verticalmente o entrambi dopo l’applicazione di ritaglia= e prima di ruotare= e estendere=.
seo-title: riflettere
solution: Experience Manager
title: riflettere
topic: Scene7 Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# flip{#flip}

Capovolgi livello. Riflette il livello orizzontalmente, verticalmente o entrambi dopo l’applicazione di ritaglia= e prima di ruotare= e estendere=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Rifletti il livello in orizzontale (sinistra-destra). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Rifletti il livello in verticale (verso l’alto). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Rifletti sia in orizzontale che in verticale. </p> </td> 
 </tr> 
</table>

Può essere applicato anche ai livelli di testo.

Alcuni comandi, inclusi `extend=`, si applicano implicitamente al livello 0 invece del livello composito quando `layer=comp` è selezionato. In tali scenari, tutti i comandi assegnati automaticamente al livello 0 verranno applicati prima dei comandi a cui si applicano `layer=comp`. Quindi, quando `layer=comp`, `extend=` viene applicato prima `flip=`.

>[!NOTE]
>
>Il livello capovolto è posizionato in base all’ancoraggio del livello; valori flip= diversi determinano posizioni diverse del livello quando l’ancoraggio non si trova al centro del livello.

## Proprietà {#section-294da2af7be746b5adfc35e29ee68217}

Livello, comando. Si applica al livello corrente o all’immagine composita, se `layer=comp`. Ignorato dai livelli degli effetti.

## Predefinito {#section-502044f81a89492198d5f12a738459ea}

Nessuno.

## Consultate anche {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)

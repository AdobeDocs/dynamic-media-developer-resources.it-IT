---
description: Capovolgi livello. Inverte il livello orizzontalmente, verticalmente o entrambi dopo aver applicato crop= e prima di rotate= ed estendi=.
solution: Experience Manager
title: capovolgere
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# flip{#flip}

Capovolgi livello. Inverte il livello orizzontalmente, verticalmente o entrambi dopo aver applicato crop= e prima di rotate= ed estendi=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>Capovolgi il livello orizzontalmente (sinistra-destra). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> fango  </span> </p> </td> 
  <td class="stentry"> <p>Capovolgi lo strato verticalmente (verso l'alto). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lurido  </span> </p> </td> 
  <td class="stentry"> <p>Capovolgi sia orizzontalmente che verticalmente. </p> </td> 
 </tr> 
</table>

Può essere applicato anche ai livelli di testo.

Alcuni comandi, tra cui `extend=`, si applicano implicitamente al livello 0 invece del livello composito quando è selezionato `layer=comp`. In tali scenari, tutti i comandi assegnati automaticamente al livello 0 verranno applicati prima dei comandi che si applicano a `layer=comp`. Pertanto, quando `layer=comp`, `extend=` viene applicato prima di `flip=`.

>[!NOTE]
>
>Il livello capovolto viene posizionato in base all&#39;ancoraggio del livello; diversi valori flip= generano posizioni di livello diverse quando l’ancoraggio non si trova al centro del livello.

## Proprietà {#section-294da2af7be746b5adfc35e29ee68217}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli di effetto.

## Predefinito {#section-502044f81a89492198d5f12a738459ea}

Nessuno.

## Consultate anche {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)

---
description: Capovolgi livello. Capovolge il livello orizzontalmente, verticalmente o entrambi dopo aver applicato crop= e prima di rotate= ed extend=.
solution: Experience Manager
title: capovolgere
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# capovolgere{#flip}

Capovolgi livello. Capovolge il livello orizzontalmente, verticalmente o entrambi dopo aver applicato crop= e prima di rotate= ed extend=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Rifletti il livello orizzontalmente (da sinistra a destra). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Capovolgere il livello verticalmente (verso l'alto). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Capovolgi orizzontalmente e verticalmente. </p> </td> 
 </tr> 
</table>

Può essere applicato anche ai livelli di testo.

Alcuni comandi, tra cui `extend=`, si applica implicitamente al livello 0 invece del livello composito quando `layer=comp` è selezionato. In tali scenari, tutti i comandi assegnati automaticamente al livello 0 vengono applicati prima dei comandi che si applicano a `layer=comp`. Così, quando `layer=comp`, `extend=` viene applicato prima di `flip=`.

>[!NOTE]
>
>Il livello capovolto viene posizionato in base all&#39;ancoraggio del livello; diversi valori flip= determineranno posizioni di livello diverse quando l&#39;ancoraggio non si trova al centro del livello.

## Proprietà {#section-294da2af7be746b5adfc35e29ee68217}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti.

## Predefinito {#section-502044f81a89492198d5f12a738459ea}

Nessuno.

## Consultate anche {#section-47f6484deccd420983df15ec163b4a83}

[rotate= ruota](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [ancoraggio=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)

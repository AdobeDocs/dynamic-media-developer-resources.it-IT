---
title: RootUrl
description: URL principale per gli URL immagine relativi. Specifica l'URL principale per gli URL immagine relativi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# RootUrl{#rooturl}

URL principale per gli URL immagine relativi. Specifica l&#39;URL principale per gli URL immagine relativi. Viene utilizzato `attribute::RootUrl` invece di `attribute::RootPath` quando un valore `src=` è racchiuso tra { parentesi graffe }.

## Proprietà {#section-69cd0f71ea614770a8778c745d23197a}

Valore stringa di testo. Percorso directory principale URL assoluto, incluso l’identificatore del protocollo principale. Sono supportati i seguenti protocolli: HTTP, HTTPS e FTP.

## Predefinito {#section-7a81569728474725a70f3a2cc4d48e85}

Ereditato da `default::RootUrl` se non definito. Se definiti ma vuoti, gli URL relativi non sono supportati da questo catalogo dei materiali.

## Consultate anche {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

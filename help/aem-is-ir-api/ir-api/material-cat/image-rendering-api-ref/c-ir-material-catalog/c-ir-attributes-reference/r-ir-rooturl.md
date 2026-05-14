---
title: RootUrl
description: URL principale per gli URL immagine relativi. Specifica l'URL principale per gli URL immagine relativi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
TQID: 'https://experienceleague.adobe.com/1wKgvbd1t4HyDlz-CTDkp2gQuryBJYfMyDG7SmVgNwE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# RootUrl{#rooturl}

URL principale per gli URL immagine relativi. Specifica l&#39;URL principale per gli URL immagine relativi. Viene utilizzato `attribute::RootUrl` invece di `attribute::RootPath` quando un valore `src=` è racchiuso da {curly braces}.

## Proprietà {#section-69cd0f71ea614770a8778c745d23197a}

Valore stringa di testo. Percorso directory principale URL assoluto, incluso l’identificatore del protocollo principale. Sono supportati i seguenti protocolli: HTTP, HTTPS e FTP.

## Predefinito {#section-7a81569728474725a70f3a2cc4d48e85}

Ereditato da `default::RootUrl` se non definito. Se definiti ma vuoti, gli URL relativi non sono supportati da questo catalogo dei materiali.

## Consultate anche {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attributo:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

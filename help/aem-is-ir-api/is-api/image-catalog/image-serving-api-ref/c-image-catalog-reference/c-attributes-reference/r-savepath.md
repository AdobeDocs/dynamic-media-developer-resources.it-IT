---
description: Percorso principale per saveToFile=. Percorso relativo per la cartella principale in cui devono essere scritte le immagini generate con req=saveToFile.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# SavePath{#savepath}

Percorso principale per saveToFile=. Percorso relativo per la cartella principale in cui devono essere scritte le immagini generate con req=saveToFile.

`SavePath` è un valore di stringa di testo.

## Proprietà {#section-343d1371e966491c92854a8df14c3c50}

Stringa di testo. Deve essere vuoto o un percorso di cartella relativo valido. Sempre combinato con il percorso radice assoluto configurato con `ImageServer::SaveDirectory`.

## Predefinito {#section-ae751eea97654f399c6aaee3f3252cbb}

Ereditato da `default::SavePath` se non definito. Il salvataggio in file viene disattivato se il valore risolto è vuoto.

## Consultate anche {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)

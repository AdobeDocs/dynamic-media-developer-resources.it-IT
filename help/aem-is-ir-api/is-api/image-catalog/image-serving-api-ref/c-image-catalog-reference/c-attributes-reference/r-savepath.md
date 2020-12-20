---
description: Percorso principale per saveToFile=. Percorso relativo per la cartella principale in cui devono essere scritte le immagini generate con req=saveToFile.
seo-description: Percorso principale per saveToFile=. Percorso relativo per la cartella principale in cui devono essere scritte le immagini generate con req=saveToFile.
seo-title: SavePath
solution: Experience Manager
title: SavePath
topic: Scene7 Image Serving - Image Rendering API
uuid: 02b88e83-7fee-40d4-95ea-daba9a608e8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# SavePath{#savepath}

Percorso principale per saveToFile=. Percorso relativo per la cartella principale in cui devono essere scritte le immagini generate con req=saveToFile.

`SavePath` è un valore di stringa di testo.

## Proprietà {#section-343d1371e966491c92854a8df14c3c50}

Stringa di testo. Deve essere vuoto o un percorso di cartella relativo valido. Sempre combinato con il percorso radice assoluto configurato con `ImageServer::SaveDirectory`.

## Predefinito {#section-ae751eea97654f399c6aaee3f3252cbb}

Ereditato da `default::SavePath` se non definito. Il salvataggio in file è disattivato se il valore risolto è vuoto.

## Consultate anche {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)

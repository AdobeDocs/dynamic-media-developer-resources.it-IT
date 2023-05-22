---
title: Origini immagine esterne
description: Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Origini immagine esterne{#foreign-image-sources}

Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.

Per specificare un URL esterno per un `src=` o un `mask=` ; delimita semplicemente l’intero URL incorporato con parentesi graffe:

` …&src={ *[!DNL foreignUrl]*}&…`

URL assoluti completi (se `attribute::AllowDirectUrls` è impostato) e gli URL relativi a `attribute::RootUrl` sono consentite. Si verifica un errore se è incorporato un URL assoluto e si verifica un attributo: `AllowDirectUrls` è 0, o se è specificato un URL relativo e `attribute::RootUrl` è vuoto.

Le immagini esterne vengono memorizzate nella cache dal server in base alle intestazioni di memorizzazione in cache incluse nella risposta HTTP.

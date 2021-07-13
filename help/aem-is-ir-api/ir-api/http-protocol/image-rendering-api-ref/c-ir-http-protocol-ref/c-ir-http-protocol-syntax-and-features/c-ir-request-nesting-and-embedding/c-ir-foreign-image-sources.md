---
description: Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.
solution: Experience Manager
title: Origini immagine straniere
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Origini immagine straniere{#foreign-image-sources}

Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.

Per specificare un URL esterno per un comando `src=` o `mask=`; delimita semplicemente l’intero URL incorporato con parentesi graffe:

` …&src={ *[!DNL foreignUrl]*}&…`

Sono consentiti gli URL assoluti completi (se è impostato `attribute::AllowDirectUrls`) e gli URL relativi a `attribute::RootUrl` . Si verifica un errore se un URL assoluto è incorporato e attributo: `AllowDirectUrls` è 0 oppure se è specificato un URL relativo e `attribute::RootUrl` è vuoto.

Le immagini esterne vengono memorizzate nella cache dal server in base alle intestazioni di memorizzazione nella cache incluse nella risposta HTTP.

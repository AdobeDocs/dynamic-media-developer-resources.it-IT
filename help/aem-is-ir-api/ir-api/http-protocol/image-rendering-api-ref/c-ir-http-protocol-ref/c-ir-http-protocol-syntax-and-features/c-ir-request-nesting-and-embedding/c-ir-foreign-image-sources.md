---
description: Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.
solution: Experience Manager
title: Origini immagine straniere
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Origini immagine esterne{#foreign-image-sources}

Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.

Per specificare un URL esterno per un comando `src=` o `mask=`; delimita semplicemente l’intero URL incorporato con parentesi graffe:

` …&src={ *[!DNL foreignUrl]*}&…`

Sono consentiti gli URL assoluti completi (se è impostato `attribute::AllowDirectUrls`) e gli URL relativi a `attribute::RootUrl` . Si verifica un errore se un URL assoluto è incorporato e attributo: `AllowDirectUrls` è 0 oppure se è specificato un URL relativo e `attribute::RootUrl` è vuoto.

Le immagini esterne vengono memorizzate nella cache dal server in base alle intestazioni di memorizzazione nella cache incluse nella risposta HTTP.

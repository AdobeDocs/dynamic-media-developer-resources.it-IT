---
description: Impostazioni generali del server
solution: Experience Manager
title: Generali
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# Generali{#general}

Impostazioni generali del server

## TC::PsPort - Porta di ascolto principale {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Specifica la porta di ascolto principale per Platform Server. Questa porta viene utilizzata anche per accedere alla documentazione e alle pagine di esempio per Image Serving, Image Rendering e i visualizzatori Dynamic Media (se installati).

## IS::CacheServerUrl - Url radice del servizio di caching {#section-bcca227a1f91453b834db4ea050968e2}

Specifica il percorso principale HTTP per consentire l&#39;accesso al servizio di caching da parte del server di immagini. Deve essere impostato su [!DNL http://localhost:TC::PsPort /is/cache/secondary], con il numero di porta corrispondente a `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL predefinito Image Source remoto {#section-e4c31228b459492cacd2f482d9575f71}

TTL per le immagini memorizzate nella cache ottenute tramite HTTP da un&#39;origine remota utilizzando il costrutto `src={…}`. Utilizzato solo quando il server remoto non include un&#39;intestazione Expiration nella risposta HTTP. Valore intero in secondi.

## IS::RemoteUrlTimeout - Timeout Image Source remoto {#section-437646c479cc4bea81dae42100a3c50a}

Il momento in cui Image Server attenderà che un server remoto distribuisca il file immagine richiesto tramite HTTP prima di restituire un errore. Valore intero in secondi.

## PS::allowDefaultCatalogRequests - Attiva/disattiva le richieste di catalogo predefinite {#section-484e442a115a49b4ac269d1718b351e1}

Imposta su false per disabilitare le richieste che non includono un ID catalogo valido nel percorso. Il valore predefinito è `true`. Se è impostato su `false`, viene restituito un errore per le richieste senza un ID catalogo.

>[!NOTE]
>
>`req=catalogprops` non è soggetto a questa impostazione.

## PS::saveToFile.saveTimeout - Timeout salvataggio file {#section-d22afd8ad86144b28684ed95a59db40e}

Valore di timeout predefinito per `req=saveToFile` quando `timeout=`non è specificato. `msec`. Se l’operazione di salvataggio non viene completata entro il periodo di tempo specificato, viene restituito un errore.

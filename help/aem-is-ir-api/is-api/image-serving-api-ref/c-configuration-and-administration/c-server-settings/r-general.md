---
description: Impostazioni server generali
seo-description: Impostazioni server generali
seo-title: Generali
solution: Experience Manager
title: Generali
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 2%

---


# Generali{#general}

Impostazioni server generali

## TC::PsPort - Porta di ascolto principale {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Specifica la porta di ascolto principale per Platform Server. Questa porta viene utilizzata anche per accedere alla documentazione e alle pagine di esempio per Image Server, Image Rendering e i visualizzatori Scene7 (se installati).

## IS::CacheServerUrl - Url radice del servizio di memorizzazione nella cache {#section-bcca227a1f91453b834db4ea050968e2}

Specifica il percorso principale HTTP per consentire al server immagini di accedere al servizio di caching. Deve essere impostato su [!DNL http://localhost:TC::PsPort /is/cache/secondary], con il numero di porta corrispondente a `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Remote Image Source Default TTL {#section-e4c31228b459492cacd2f482d9575f71}

TTL per le immagini memorizzate nella cache ottenute tramite HTTP da un&#39;origine remota utilizzando il costrutto `src={…}`. Utilizzato solo quando il server remoto non include un&#39;intestazione di scadenza nella risposta HTTP. Valore intero in secondi.

## IS::RemoteUrlTimeout - Timeout origine immagine remota {#section-437646c479cc4bea81dae42100a3c50a}

Quando il server immagini attende che un server remoto distribuisca il file immagine richiesto via HTTP prima di restituire un errore. Valore intero in secondi.

## PS::allowDefaultCatalogRequests - Abilita/Disattiva richieste catalogo predefinite {#section-484e442a115a49b4ac269d1718b351e1}

Impostato su false per non consentire le richieste che non includono un ID catalogo valido nel percorso. Il valore predefinito è `true`. Se è impostata su `false`, viene restituito un errore per le richieste senza un ID catalogo.

>[!NOTE]
>
>`req=catalogprops` non è soggetto a questa impostazione.

## PS::saveToFile.saveTimeout - Timeout salvataggio file {#section-d22afd8ad86144b28684ed95a59db40e}

Valore di timeout predefinito per `req=saveToFile` quando `timeout=`non è specificato. `msec`. Se l&#39;operazione di salvataggio non viene completata entro il periodo di tempo specificato, verrà restituito un errore.

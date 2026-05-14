---
description: Impostazioni generali del server
solution: Experience Manager
title: Generali
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
TQID: 'https://experienceleague.adobe.com/hjww7EYpf4xNxpUFQ1fudMOqNtokgykthwhonn78ZFE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# Generali{#general}

Impostazioni generali del server

## TC::PsPort - Porta di ascolto principale {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Specifica la porta di ascolto principale per [!DNL Platform Server]. Questa porta viene utilizzata anche per accedere alla documentazione e alle pagine di esempio per Image Server, Image Rendering e visualizzatori Dynamic Media (se installati).

## IS::CacheServerUrl - Url radice del servizio di caching {#section-bcca227a1f91453b834db4ea050968e2}

Specifica il percorso root HTTP per consentire al server immagini di accedere al servizio di caching. Deve essere impostato su [!DNL http://localhost:TC::PsPort /is/cache/secondary], con il numero di porta corrispondente a `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL predefinito Image Source remoto {#section-e4c31228b459492cacd2f482d9575f71}

TTL per le immagini memorizzate nella cache ottenute tramite HTTP da un&#39;origine remota utilizzando il costrutto `src={…}`. Utilizzato solo quando il server remoto non include un’intestazione Scadenza nella risposta HTTP. Valore intero in secondi.

## IS::RemoteUrlTimeout - Timeout Image Source remoto {#section-437646c479cc4bea81dae42100a3c50a}

Tempo di attesa del server immagini per la consegna del file immagine richiesto tramite HTTP da parte di un server remoto prima che venga restituito un errore. Valore intero in secondi.

## PS::allowDefaultCatalogRequests - Abilita/Disabilita richieste catalogo predefinite {#section-484e442a115a49b4ac269d1718b351e1}

Imposta su false per non consentire le richieste che non includono un ID catalogo valido nel percorso. Il valore predefinito è `true`. Se è impostato su `false`, viene restituito un errore per le richieste senza un ID catalogo.

>[!NOTE]
>
>`req=catalogprops` non è soggetto a questa impostazione.

## PS::saveToFile.saveTimeout - Timeout salvataggio file {#section-d22afd8ad86144b28684ed95a59db40e}

Valore di timeout predefinito per `req=saveToFile` quando `timeout=` non è specificato. `msec`. Se l&#39;operazione di salvataggio non viene completata entro il periodo di tempo specificato, viene restituito un errore.

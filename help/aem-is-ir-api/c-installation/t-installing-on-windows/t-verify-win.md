---
description: Dopo aver installato Dynamic Media Image Serving, è necessario verificare l'installazione.
solution: Experience Manager
title: Verifica dell'installazione
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Verifica dell&#39;installazione{#verifying-the-installation}

Dopo aver installato Dynamic Media Image Serving, è necessario verificare l&#39;installazione.

Image Server è installato come servizio Windows.

1. Apri il Pannello di controllo Campaign Servizi e verifica che &quot;Dynamic Media Image Serving&quot; sia presente con lo stato &quot;Started&quot;.
1. Apri un browser Internet sullo stesso host o su un altro e controlla le risposte del server predefinito:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Verifica la presenza di &quot; `imageServer.`&quot; elementi nella risposta, che indicano che Image Server è in ascolto.
>Puoi eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.

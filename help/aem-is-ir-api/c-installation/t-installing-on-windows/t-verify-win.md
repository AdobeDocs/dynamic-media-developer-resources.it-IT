---
description: Dopo aver installato Dynamic Media Image Serving, è necessario verificare l'installazione.
seo-description: Dopo aver installato Dynamic Media Image Serving, è necessario verificare l'installazione.
seo-title: Verifica dell'installazione
solution: Experience Manager
title: Verifica dell'installazione
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
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


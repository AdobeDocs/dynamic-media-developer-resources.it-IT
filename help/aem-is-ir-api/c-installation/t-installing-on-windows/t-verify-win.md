---
title: Verifica dell'installazione
description: Dopo aver installato Dynamic Media Image Server, è necessario verificare l’installazione.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Verifica dell&#39;installazione {#verifying-the-installation}

Dopo aver installato Dynamic Media Image Server, è necessario verificare l’installazione.

Il server immagini viene installato come servizio Windows.

1. Aprire il Pannello di controllo Campaign Servizi e verificare che `Dynamic Media Image Serving` sia presente con uno stato di `Started`.
1. Aprire un browser Internet sullo stesso host o su un host diverso e verificare le risposte predefinite del server:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Verificare la presenza di &quot;`imageServer.`&quot; elementi nella risposta, che indicano che il server immagini è in ascolto.
>Puoi eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.

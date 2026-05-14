---
title: Verifica dell'installazione
description: Dopo aver installato Dynamic Media Image Server, è necessario verificare l’installazione.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Verifica dell&#39;installazione {#verifying-the-installation}

Dopo aver installato Dynamic Media Image Server, è necessario verificare l’installazione.

Il server immagini viene installato come servizio Windows.

1. Aprire il Pannello di controllo Campaign Servizi e verificare che `Dynamic Media Image Serving` sia presente con uno stato di `Started`.
1. Aprire un browser Internet sullo stesso host o su un host diverso e verificare le risposte predefinite del server:

   `http:// server:port /is/image`

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Verificare la presenza di &quot;`imageServer.`&quot; elementi nella risposta, che indicano che il server immagini è in ascolto.

>Puoi eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.

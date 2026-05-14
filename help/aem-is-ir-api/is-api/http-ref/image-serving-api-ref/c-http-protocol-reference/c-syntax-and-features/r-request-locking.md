---
description: Per ridurre le opportunità di manomissione delle richieste, è disponibile una semplice funzione di blocco.
solution: Experience Manager
title: Richiedi blocco
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
TQID: 'https://experienceleague.adobe.com/9icGIK7meNSVUzYnsFBFM-GwG7KLe90bMDuqN89xmMk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 0%

---

# Richiedi blocco{#request-locking}

Per ridurre le opportunità di manomissione delle richieste, è disponibile una semplice funzione di blocco.

Se è impostato l&#39;attributo::RequestLock, è necessario aggiungere un valore di blocco alla richiesta, in formato `&xxxx`, con xxxx come valore esadecimale a quattro cifre. Questo valore esadecimale viene generato utilizzando un semplice algoritmo di hashing applicato alla porzione *modificatori* della richiesta (dopo &#39;?&#39; che separa il percorso URL dai *modificatori*). Questa operazione deve essere eseguita dopo che la richiesta è completamente codificata http, ma prima che sia (facoltativamente) offuscata. Dopo aver deoffuscato la richiesta, il server utilizza lo stesso algoritmo di hashing nella stringa del modificatore (esclusi gli ultimi 5 caratteri, che contengono il valore di blocco). Se la chiave generata non corrisponde al blocco, la richiesta viene rifiutata.

>[!IMPORTANT]
>
>Se abiliti questa funzione, tieni presente che esistono alcune limitazioni al suo utilizzo che includono quanto segue:<br>- L&#39;interfaccia utente di Dynamic Media potrebbe non mostrare i dettagli corretti per il campo **[!UICONTROL Ultima pubblicazione]**. Tuttavia, questo effetto non influisce sulla pubblicazione.<br>- Attualmente, il flusso video HLS non funziona quando **[!UICONTROL Offuscamento richiesta]** e **[!UICONTROL Blocco richiesta]** sono abilitati.<br>- Attualmente, alcuni visualizzatori Dynamic Media non funzionano quando **[!UICONTROL Offuscamento richiesta]** e **[!UICONTROL Blocco richiesta]** sono abilitati.

Codice di esempio C++ per generare il valore di blocco della richiesta:

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## Consultate anche {#section-a6d45406c0354669ac581793e4fa8436}

[Codifica HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Offuscamento richiesta](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attributo::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)

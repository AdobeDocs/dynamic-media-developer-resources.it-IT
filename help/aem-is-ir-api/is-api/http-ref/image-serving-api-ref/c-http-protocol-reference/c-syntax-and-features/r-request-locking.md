---
description: Per ridurre le possibilità di manomissione delle richieste, è disponibile un semplice impianto di bloccaggio.
seo-description: Per ridurre le possibilità di manomissione delle richieste, è disponibile un semplice impianto di bloccaggio.
seo-title: Richiedi blocco
solution: Experience Manager
title: Richiedi blocco
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 6b51248cdc6a6b9d36893545640dbbeb11a0c414
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Richiedi blocco{#request-locking}

Per ridurre le possibilità di manomissione delle richieste, è disponibile un semplice impianto di bloccaggio.

Se attribute::RequestLock è impostato, alla richiesta deve essere aggiunto un valore di blocco sotto forma di `&xxxx`, con xxxx come valore esadecimale a quattro cifre. Questo valore esadecimale viene generato utilizzando un algoritmo di hash semplice applicato alla parte *modificatori* della richiesta (dopo il simbolo &#39;?&#39; che separa il percorso dell’URL dai *modificatori*). Questa operazione deve essere eseguita dopo che la richiesta è completamente http-encoded, ma prima che sia (facoltativamente) offuscata. Dopo aver decompresso la richiesta, il server utilizzerà lo stesso algoritmo di hash sulla stringa del modificatore (ad eccezione degli ultimi 5 caratteri, che contengono il valore lock). Se la chiave generata non corrisponde al blocco, la richiesta viene rifiutata.

>[!IMPORTANT]
>
>Se attivate questa funzione, tenete presente che l’utilizzo di questa funzione presenta alcune limitazioni:<br>- L’interfaccia utente per i file multimediali dinamici potrebbe non mostrare i dettagli corretti per il campo **[!UICONTROL Ultima pubblicazione]** . Tuttavia, questo effetto non influisce sulla pubblicazione.<br>- Al momento, lo streaming video HLS non funziona quando **[!UICONTROL Request Obfuscation]** e **[!UICONTROL Request Locking]** sono abilitati.

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

[Codifica](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)HTTP, [Richiesta offuscamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attributo::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)

---
description: Per ridurre le opportunità di manomissione delle richieste, è disponibile una semplice funzione di blocco.
solution: Experience Manager
title: Richiedi blocco
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Richiedi blocco{#request-locking}

Per ridurre le opportunità di manomissione delle richieste, è disponibile una semplice funzione di blocco.

Se è impostato l&#39;attributo::RequestLock, è necessario aggiungere un valore di blocco alla richiesta, sotto forma di `&xxxx`, dove xxxx è un valore esadecimale a quattro cifre. Questo valore esadecimale viene generato utilizzando un semplice algoritmo di hashing applicato al *modificatori* parte della richiesta (dopo &quot;?&quot; che separa il percorso URL dal *modificatori*). Questa operazione deve essere eseguita dopo che la richiesta è completamente codificata http, ma prima che sia (facoltativamente) offuscata. Dopo aver deoffuscato la richiesta, il server utilizzerà lo stesso algoritmo di hashing nella stringa del modificatore (esclusi gli ultimi 5 caratteri, che contengono il valore di blocco). Se la chiave generata non corrisponde al blocco, la richiesta viene rifiutata.

>[!IMPORTANT]
>
>Se abiliti questa funzione, tieni presente che l’utilizzo di essa è soggetto a determinate limitazioni, tra cui:<br>- L&#39;interfaccia utente di Dynamic Media potrebbe non mostrare i dettagli corretti per **[!UICONTROL Ultima pubblicazione]** campo. Tuttavia, questo effetto non influisce sulla pubblicazione.<br>- Attualmente, lo streaming video HLS non funziona quando **[!UICONTROL Richiedi offuscamento]** e **[!UICONTROL Richiedi blocco]** sono attivati.<br>- Attualmente, alcuni visualizzatori Dynamic Media non funzionano quando **[!UICONTROL Richiedi offuscamento]** e **[!UICONTROL Richiedi blocco]** sono attivati.

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

[Codifica HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Richiedi offuscamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::BloccoRichiesta](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)

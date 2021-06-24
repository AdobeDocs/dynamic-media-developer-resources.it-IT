---
description: Per ridurre le possibilità di manomissione delle richieste, viene fornito un semplice impianto di blocco.
solution: Experience Manager
title: Blocco della richiesta
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Blocco della richiesta{#request-locking}

Per ridurre le possibilità di manomissione delle richieste, viene fornito un semplice impianto di blocco.

Se attribute::RequestLock è impostato, alla richiesta deve essere aggiunto un valore di blocco, sotto forma di `&xxxx`, con xxxx come valore esadecimale a quattro cifre. Questo valore esadecimale viene generato utilizzando un semplice algoritmo di hash applicato alla porzione *modificatori* della richiesta (dopo &#39;?&#39; che separa il percorso URL dai *modificatori*). Questo deve essere fatto dopo che la richiesta è completamente codificata in http, ma prima che sia (facoltativamente) offuscata. Dopo aver de-offuscato la richiesta, il server utilizzerà lo stesso algoritmo di hash sulla stringa del modificatore (esclusi gli ultimi 5 caratteri, che contengono il valore di blocco). Se la chiave generata non corrisponde al blocco, la richiesta viene rifiutata.

>[!IMPORTANT]
>
>Se abiliti questa funzione, tieni presente che sono presenti alcune limitazioni all’utilizzo della funzionalità che includono:<br>- L’interfaccia utente di Dynamic Media potrebbe non mostrare i dettagli corretti per il campo **[!UICONTROL Ultimo pubblicazione]**. Tuttavia, questo effetto non interessa la pubblicazione.<br>- Attualmente, lo streaming video HLS non funziona quando **[!UICONTROL l&#39;offuscamento della richiesta]** e il  **[!UICONTROL blocco della richiesta]** sono abilitati.<br>- Al momento, alcuni visualizzatori Dynamic Media non funzionano quando  **[!UICONTROL l’offuscamento della richiesta]** e il  **[!UICONTROL blocco della]** richiesta sono attivati.

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

[Codifica](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP,  [Offuscamento richiesta](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d),  [attributo::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)

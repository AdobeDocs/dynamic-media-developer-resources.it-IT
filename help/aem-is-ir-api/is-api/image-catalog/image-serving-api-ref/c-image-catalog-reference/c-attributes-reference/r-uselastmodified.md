---
description: Abilita le intestazioni di risposta dell’ultima modifica. Abilita o disabilita l'inclusione dell'intestazione Last-Modified nelle risposte HTTP memorizzabili in cache emesse da Image Server.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
TQID: 'https://experienceleague.adobe.com/jmwz9jThBnFtTZBRoI0kbKwoxf1MU7rn1CpKrSU4f04'
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
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Abilita le intestazioni di risposta dell’ultima modifica. Abilita o disabilita l&#39;inclusione dell&#39;intestazione Last-Modified nelle risposte HTTP memorizzabili in cache emesse da Image Server.

Il server utilizza il valore `catalog::TimeStamp` più recente di tutti i cataloghi/record di catalogo coinvolti in una risposta come valore di intestazione Ultima modifica.

Deve essere abilitato solo se si utilizza una rete di caching distribuito o un altro sistema di caching che non supporta le intestazioni etag.

>[!NOTE]
>
>Presta attenzione quando utilizzi le intestazioni Last-Modified in un ambiente con carico bilanciato che coinvolge più host Image Server. La memorizzazione nella cache del client può essere annullata e il carico del server può aumentare se per qualche motivo i server hanno marche temporali diverse per le stesse voci di catalogo. Tale situazione può verificarsi nel modo seguente:
>
>* Né `catalog::TimeStamp` né `attribute::TimeStamp`, pertanto l&#39;ora di modifica del file [!DNL catalog.ini] viene utilizzata come predefinita per `catalog::TimeStamp`.
>
>* Anziché condividere i file di catalogo delle immagini tramite un mount di rete, ogni server dispone di una propria istanza dei file di catalogo in un file system locale.
>* Due o più istanze dello stesso file [!DNL catalog.ini] hanno date di modifica del file diverse, probabilmente causate da una copia non corretta dei file.
>

## Proprietà {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Bandiera. 0 per disabilitare, 1 per abilitare le intestazioni HTTP Last-Modified.

## Predefinito {#section-4eb47aadab8b41609bef296a4115f9f4}

Ereditato da `default::UseLastModified` se non definito o se vuoto.

## Consultate anche {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalogo::Timestamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)

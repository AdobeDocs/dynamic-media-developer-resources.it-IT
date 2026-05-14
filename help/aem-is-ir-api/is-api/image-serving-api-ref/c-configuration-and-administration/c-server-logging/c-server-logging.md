---
description: Tutti i file di log vengono scritti nella stessa cartella di log specificata con la directory TC.
solution: Experience Manager
title: Registrazione server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
TQID: 'https://experienceleague.adobe.com/9I1gAXWb1Rpuml9WCCVPVC7FrpVazWN79Sk0-bb-tDc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 1%

---

# Registrazione server{#server-logging}

Tutti i file di log vengono scritti nella stessa cartella di log specificata con TC::directory.

I file di registro vengono generalmente creati e ruotati su base giornaliera. I file di log meno recenti nella cartella di log vengono eliminati automaticamente dopo un numero specificato di giorni ( `TC::maxDays`).

Importante È necessario riservare una quantità sufficiente di spazio su disco ai file di registro per evitare di esaurire lo spazio su disco. Per un server molto utilizzato e le impostazioni di registro predefinite potrebbero essere necessari 1-2 GB/die.

[!DNL Platform Server] e Image Server creano i tre tipi di file di registro descritti di seguito.

Anche altri componenti Image Server e alcuni altri pacchetti Dynamic Media, come i visualizzatori Dynamic Media, possono creare file di registro nella stessa cartella. Questi file di registro sono per uso interno di Dynamic Media e possono essere richiesti dal supporto tecnico di Dynamic Media per la risoluzione dei problemi.

* [Registro di accesso](c-access-log.md)
* [Registro traccia](c-trace-log.md)
* [Registro server immagini](c-image-server-log.md)

## Consultate anche {#section-5ff5e46031b1461c92de24e632610d6d}

[Registrazione accesso](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Registrazione debug/traccia](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)

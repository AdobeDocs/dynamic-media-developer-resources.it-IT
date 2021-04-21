---
description: Usa queste impostazioni del server per reindirizzare gli errori.
solution: Experience Manager
title: Reindirizzamento degli errori
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Reindirizzamento errore{#error-redirection}

Usa queste impostazioni del server per reindirizzare gli errori.

>[!NOTE]
>
>I caratteri di tubazione (|) nel percorso di rete non sono supportati per il reindirizzamento degli errori.

## PS::errorRedirect.rootUrl - Server di reindirizzamento {#section-85f22e48d68842a490b0e1191543b558}

L’URL principale ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) per la distribuzione secondaria Image Server a cui devono essere reindirizzate le richieste con errore locale. Il reindirizzamento degli errori è disattivato (impostazione predefinita) quando questa impostazione è vuota o non definita.

## PS::errorRedirect.connectTimeout - Timeout della connessione di reindirizzamento {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo massimo (in msec) in cui il server attenderà che venga stabilita una connessione con il server secondario prima di restituire un errore al client.

## PS::errorRedirect.socketTimeout - Timeout risposta di reindirizzamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo massimo (in msec) in cui il server secondario attenderà la restituzione dei dati prima di abbandonare la richiesta di reindirizzamento e restituire un errore al client.

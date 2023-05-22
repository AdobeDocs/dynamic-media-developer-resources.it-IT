---
description: Utilizzare queste impostazioni del server per reindirizzare gli errori.
solution: Experience Manager
title: Reindirizzamento errori
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Reindirizzamento errori{#error-redirection}

Utilizzare queste impostazioni del server per reindirizzare gli errori.

>[!NOTE]
>
>I caratteri di tubazione (|) nel percorso di rete non sono supportati per il reindirizzamento degli errori.

## PS::errorRedirect.rootUrl - Server di reindirizzamento {#section-85f22e48d68842a490b0e1191543b558}

URL principale ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) per la distribuzione secondaria Image Server alla quale devono essere reindirizzate le richieste che hanno esito negativo a livello locale. Errore di reindirizzamento disabilitato (impostazione predefinita) quando questa impostazione è vuota o non definita.

## PS::errorRedirect.connectTimeout - Timeout connessione reindirizzamento {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo massimo (in millisecondi) di attesa del server per l&#39;impostazione di una connessione con il server secondario prima della restituzione di un errore al client.

## PS::errorRedirect.socketTimeout - Timeout risposta reindirizzamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo massimo (in millisecondi) per il server secondario di restituire i dati prima di abbandonare la richiesta di reindirizzamento e restituire un errore al client.

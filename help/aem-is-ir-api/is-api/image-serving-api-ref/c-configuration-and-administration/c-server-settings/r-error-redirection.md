---
description: Utilizzare queste impostazioni del server per reindirizzare gli errori.
solution: Experience Manager
title: Reindirizzamento errori
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Reindirizzamento errori{#error-redirection}

Utilizzare queste impostazioni del server per reindirizzare gli errori.

>[!NOTE]
>
>I caratteri di tubazione (|) nel percorso di rete non sono supportati per il reindirizzamento degli errori.

## PS::errorRedirect.rootUrl - Server di reindirizzamento {#section-85f22e48d68842a490b0e1191543b558}

L&#39;URL radice ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) per la distribuzione secondaria di Image Server a cui devono essere reindirizzate le richieste che hanno esito negativo localmente. Errore di reindirizzamento disabilitato (impostazione predefinita) quando questa impostazione è vuota o non definita.

## PS::errorRedirect.connectTimeout - Timeout connessione reindirizzamento {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo massimo (in millisecondi) per cui il server attende che venga stabilita una connessione con il server secondario prima di restituire un errore al client.

## PS::errorRedirect.socketTimeout - Timeout risposta reindirizzamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo massimo (in millisecondi) di attesa del server secondario per la restituzione dei dati prima di abbandonare la richiesta di reindirizzamento e di restituire un errore al client.

---
description: Utilizzate queste impostazioni del server per reindirizzare gli errori.
seo-description: Utilizzate queste impostazioni del server per reindirizzare gli errori.
seo-title: Reindirizzamento errore
solution: Experience Manager
title: Reindirizzamento errore
topic: Scene7 Image Serving - Image Rendering API
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Reindirizzamento errore{#error-redirection}

Utilizzate queste impostazioni del server per reindirizzare gli errori.

>[!NOTE]
>
>I caratteri pipeline (|) nel percorso di rete non sono supportati per il reindirizzamento degli errori.

## PS::errorRedirect.rootUrl - Server di reindirizzamento {#section-85f22e48d68842a490b0e1191543b558}

L&#39;URL principale ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) per la distribuzione secondaria Image Server a cui reindirizzare le richieste che non vanno a buon fine localmente. Il reindirizzamento degli errori è disattivato (impostazione predefinita) quando questa impostazione è vuota o non definita.

## PS::errorRedirect.connectTimeout - Timeout connessione di reindirizzamento {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo massimo (in msec) per stabilire una connessione con il server secondario prima di restituire un errore al client.

## PS::errorRedirect.socketTimeout - Timeout risposta di reindirizzamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo massimo (in msec) in cui il server secondario deve restituire i dati prima di abbandonare la richiesta di reindirizzamento e restituire un errore al client.

---
description: I server IS possono essere configurati per il failover su server alternativi per le richieste che coinvolgono un’immagine sorgente che non può essere aperta o letta correttamente.
solution: Experience Manager
title: Reindirizza in caso di errore
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# Reindirizza in caso di errore{#redirect-on-error}

I server IS possono essere configurati per il failover su server alternativi per le richieste che coinvolgono un’immagine sorgente che non può essere aperta o letta correttamente.

Vengono reindirizzati i seguenti tipi di richieste:

* Immagini IS presenti nel catalogo, ma non su disco.

   Se un’immagine non si trova in un catalogo, il reindirizzamento per errori non dovrebbe verificarsi quando l’immagine non può essere trovata.

* Immagini, profili colore o font danneggiati.
* Impossibile trovare il contenuto statico sul disco.

   Le richieste di contenuto statico vengono reindirizzate quando non è possibile trovarlo sul disco, anche se il contenuto statico di riferimento non ha un record catalogo.

Il reindirizzamento per errori non si verifica in nessun altro caso.

Quando è abilitata e si verifica un errore durante l’elaborazione della richiesta, il server principale invia la richiesta al server secondario per l’elaborazione. La risposta, indipendentemente dal fatto che indichi esito positivo o negativo, viene quindi inoltrata direttamente al client. Il server principale contrassegna le voci di registro di tali richieste inoltrate con l’utilizzo della cache `REMOTE`. I dati di risposta non vengono memorizzati nella cache locale dal server primario.

Errore di reindirizzamento attivato dall&#39;impostazione `PS::errorRedirect.rootUrl` al nome di dominio HTTP e al numero di porta del server secondario. Inoltre, il timeout della connessione è configurato con `PS::errorRedirect.connectTimeout` e il tempo massimo di attesa del server primario per una risposta dal server secondario prima che venga restituito un errore al client è configurato con `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Se non è possibile contattare il server secondario, viene restituita al client una risposta di errore testuale, anche se è configurata un&#39;immagine predefinita o un&#39;immagine di errore.

>[!NOTE]
>
>I caratteri di tubazione (|) nel percorso di rete non sono supportati per il reindirizzamento degli errori.

## Consultate anche {#section-2e8bfc128b944baf8108279d16492f3f}

[Reindirizzamento errori](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)

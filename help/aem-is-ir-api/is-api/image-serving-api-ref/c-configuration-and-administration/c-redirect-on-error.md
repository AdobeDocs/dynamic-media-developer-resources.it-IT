---
description: I server IS possono essere configurati per il failover su server alternativi per le richieste che coinvolgono un'immagine sorgente che non può essere aperta o letta correttamente.
solution: Experience Manager
title: Reindirizza all’errore
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# Reindirizza all’errore{#redirect-on-error}

I server IS possono essere configurati per il failover su server alternativi per le richieste che coinvolgono un&#39;immagine sorgente che non può essere aperta o letta correttamente.

I seguenti tipi di richieste vengono reindirizzati:

* Immagini IS presenti nel catalogo, ma non sul disco.

   Se un&#39;immagine non si trova in un catalogo, non dovrebbe verificarsi un reindirizzamento quando l&#39;immagine non è trovata.

* Immagini corrotte, profili di colore o font.
* Impossibile trovare il contenuto statico su disco.

   Le richieste di contenuto statico vengono reindirizzate quando non è possibile trovarlo su disco, anche se il contenuto statico a cui si fa riferimento non dispone di un record di catalogo.

Il reindirizzamento degli errori non si verifica in nessun altro caso.

Quando è attivato e si verifica un tale errore durante l’elaborazione della richiesta, il server primario invia la richiesta al server secondario per l’elaborazione. La risposta, indipendentemente dal fatto che indichi il successo o l’errore, viene quindi inoltrata direttamente al client. Il server primario contrassegna le voci di registro di tali richieste inoltrate con l&#39;uso della cache `REMOTE`. I dati di risposta non vengono memorizzati nella cache locale dal server primario.

Reindirizzamento degli errori abilitato tramite impostazione `PS::errorRedirect.rootUrl` al nome di dominio HTTP e al numero di porta del server secondario. Inoltre, il timeout di connessione è configurato con `PS::errorRedirect.connectTimeout` e il tempo massimo in cui il server primario attende una risposta dal server secondario prima che venga restituito un errore al client con `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Se non è possibile contattare il server secondario, viene restituita al client una risposta di errore di testo, anche se è configurata un&#39;immagine o un&#39;immagine di errore predefinita.

>[!NOTE]
>
>I caratteri di tubazione (|) nel percorso di rete non sono supportati per il reindirizzamento degli errori.

## Consultate anche {#section-2e8bfc128b944baf8108279d16492f3f}

[Reindirizzamento degli errori](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)

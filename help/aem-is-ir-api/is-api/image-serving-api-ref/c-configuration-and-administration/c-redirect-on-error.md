---
description: I server IS possono essere configurati per il failover su server alternativi per le richieste che richiedono un'immagine sorgente che non può essere aperta o letta correttamente.
seo-description: I server IS possono essere configurati per il failover su server alternativi per le richieste che richiedono un'immagine sorgente che non può essere aperta o letta correttamente.
seo-title: Reindirizza a errore
solution: Experience Manager
title: Reindirizza a errore
topic: Scene7 Image Serving - Image Rendering API
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---


# Reindirizza a errore{#redirect-on-error}

I server IS possono essere configurati per il failover su server alternativi per le richieste che richiedono un&#39;immagine sorgente che non può essere aperta o letta correttamente.

I seguenti tipi di richieste vengono reindirizzati:

* Immagini IS presenti nel catalogo, ma non su disco.

   Se un’immagine non è presente in un catalogo, il reindirizzamento non dovrebbe essere eseguito quando l’immagine non è disponibile.

* Immagini, profili colore o font danneggiati.
* Impossibile trovare il contenuto statico su disco.

   Le richieste di contenuto statico vengono reindirizzate quando non è possibile trovarle su disco, anche se il contenuto statico a cui si fa riferimento non dispone di un record catalogo.

Il reindirizzamento degli errori non si verificherà in nessun altro caso.

Quando attivato e quando si verifica un errore di questo tipo durante l&#39;elaborazione della richiesta, il server primario invia la richiesta al server secondario per l&#39;elaborazione. La risposta, indipendentemente dal fatto che indichi un esito positivo o negativo, viene quindi inoltrata direttamente al client. Il server principale contrassegna le voci di registro di tali richieste inoltrate con l&#39;utilizzo della cache `REMOTE`. I dati di risposta non vengono memorizzati nella cache locale dal server primario.

Il reindirizzamento degli errori è abilitato impostando `PS::errorRedirect.rootUrl` il nome di dominio HTTP e il numero di porta del server secondario. Inoltre, il timeout di connessione è configurato con `PS::errorRedirect.connectTimeout` e il tempo massimo entro il quale il server primario attende una risposta dal server secondario prima che venga restituito un errore al client con `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Se il server secondario non può essere contattato, al client verrà restituita una risposta di errore di testo, anche se è configurata un&#39;immagine o un&#39;immagine di errore predefinita.

>[!NOTE]
>
>I caratteri pipeline (|) nel percorso di rete non sono supportati per il reindirizzamento degli errori.

## Consultate anche {#section-2e8bfc128b944baf8108279d16492f3f}

[Reindirizzamento errore](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)

---
description: Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.
solution: Experience Manager
title: Funzione di stampa
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Funzione di stampa{#print-feature}

Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.

La funzione di stampa viene attivata da un pulsante dedicato nella barra degli strumenti. Facendo clic sul pulsante l&#39;utente può scegliere un intervallo di stampa e il numero di pagine per foglio.

La qualità della stampa può essere regolata utilizzando il parametro di configurazione `printquality`. Si sconsiglia di impostare `printquality` su valori significativamente superiori a quelli predefiniti. Il motivo è che porta a un consumo di memoria molto elevato da parte del browser web sul sistema del cliente. Inoltre, assicurati che la dimensione massima di risposta dell’immagine impostata per la tua azienda Dynamic Media Classic sia maggiore del valore `printquality` configurato.

>[!NOTE]
>
>La funzione Stampa è disponibile solo sui sistemi desktop, ad eccezione di Internet Explorer 9.


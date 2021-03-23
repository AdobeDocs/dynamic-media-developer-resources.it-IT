---
description: Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.
seo-description: Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.
seo-title: Funzione di stampa
solution: Experience Manager
title: Funzione di stampa
uuid: 4ff170a3-ce37-454f-b4b0-b323de3dc9c9
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---


# Funzione di stampa{#print-feature}

Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.

La funzione di stampa viene attivata da un pulsante dedicato nella barra degli strumenti. Facendo clic sul pulsante l&#39;utente può scegliere un intervallo di stampa e il numero di pagine per foglio.

La qualità della stampa può essere regolata utilizzando il parametro di configurazione `printquality`. Si sconsiglia di impostare `printquality` su valori significativamente superiori a quelli predefiniti. Il motivo è che porta a un consumo di memoria molto elevato da parte del browser web sul sistema del cliente. Inoltre, assicurati che la dimensione massima di risposta dell’immagine impostata per la tua azienda Dynamic Media Classic sia maggiore del valore `printquality` configurato.

>[!NOTE]
>
>La funzione Stampa è disponibile solo sui sistemi desktop, ad eccezione di Internet Explorer 9.


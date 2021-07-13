---
description: Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.
solution: Experience Manager
title: Funzione di stampa
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Funzione di stampa{#print-feature}

Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.

La funzione di stampa viene attivata da un pulsante dedicato nella barra degli strumenti. Facendo clic sul pulsante l&#39;utente può scegliere un intervallo di stampa e il numero di pagine per foglio.

La qualità della stampa può essere regolata utilizzando il parametro di configurazione `printquality`. Si sconsiglia di impostare `printquality` su valori significativamente superiori a quelli predefiniti. Il motivo è che porta a un consumo di memoria molto elevato da parte del browser web sul sistema del cliente. Inoltre, assicurati che la dimensione massima di risposta dell’immagine impostata per la tua azienda Dynamic Media Classic sia maggiore del valore `printquality` configurato.

>[!NOTE]
>
>La funzione Stampa è disponibile solo sui sistemi desktop, ad eccezione di Internet Explorer 9.

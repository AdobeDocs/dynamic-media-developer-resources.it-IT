---
description: Il visualizzatore consente di stampare il contenuto del catalogo.
solution: Experience Manager
title: Funzione di stampa
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Funzione di stampa{#print-feature}

Il visualizzatore consente di stampare il contenuto del catalogo.

La funzione di stampa viene attivata da un pulsante dedicato nella barra degli strumenti. Facendo clic sul pulsante è possibile scegliere un intervallo di stampa e il numero di pagine per foglio.

È possibile regolare la qualità di stampa utilizzando il parametro di configurazione `printquality`. Si noti che non è consigliabile impostare `printquality` su valori significativamente superiori a quelli predefiniti. Il motivo è che porta a un consumo di memoria molto elevato da parte del browser web sul sistema del client. Inoltre, assicurati che la dimensione massima di risposta dell&#39;immagine impostata per la tua società Dynamic Media Classic sia maggiore del valore `printquality` configurato.

>[!NOTE]
>
>La funzione di stampa è disponibile solo sui sistemi desktop, ad eccezione di Internet Explorer 9.

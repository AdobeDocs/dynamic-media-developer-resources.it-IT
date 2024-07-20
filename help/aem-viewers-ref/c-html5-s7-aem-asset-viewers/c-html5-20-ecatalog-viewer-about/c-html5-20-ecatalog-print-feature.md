---
title: Funzione di stampa
description: Il visualizzatore consente di stampare il contenuto del catalogo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Funzione di stampa{#print-feature}

Il visualizzatore consente di stampare il contenuto del catalogo.

La funzione di stampa viene attivata da un pulsante dedicato nella barra degli strumenti. Facendo clic sul pulsante è possibile scegliere un intervallo di stampa e il numero di pagine per foglio.

È possibile regolare la qualità di stampa utilizzando il parametro di configurazione `printquality`. Non è consigliabile impostare `printquality` su valori superiori a quelli predefiniti. Il motivo è che porta ad un elevato consumo di memoria da parte del browser web sul sistema del client. Inoltre, assicurati che la dimensione massima di risposta dell&#39;immagine impostata per la tua società Dynamic Media Classic sia maggiore del valore `printquality` configurato.

>[!NOTE]
>
>La funzione di stampa è disponibile solo sui sistemi desktop, ad eccezione di Internet Explorer 9.

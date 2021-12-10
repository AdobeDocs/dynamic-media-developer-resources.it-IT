---
title: Funzione di stampa
description: Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Funzione di stampa{#print-feature}

Il visualizzatore consente di inviare il contenuto del catalogo a una stampante.

La funzione di stampa viene attivata da un pulsante dedicato nella barra degli strumenti. Facendo clic sul pulsante l&#39;utente può scegliere un intervallo di stampa e il numero di pagine per foglio.

La qualità della stampa può essere regolata utilizzando `printquality` parametro di configurazione. Impostazione `printquality` non si consiglia di impostare valori superiori a quelli predefiniti. Il motivo è che porta ad un elevato consumo di memoria da parte del browser web sul sistema del cliente. Inoltre, assicurati che la dimensione massima di risposta dell’immagine impostata per la tua azienda Dynamic Media Classic sia maggiore della dimensione configurata `printquality` valore.

>[!NOTE]
>
>La funzione Stampa è disponibile solo sui sistemi desktop, ad eccezione di Internet Explorer 9.

---
description: Il visualizzatore consente di stampare il contenuto del catalogo.
solution: Experience Manager
title: Funzione di stampa
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
TQID: 'https://experienceleague.adobe.com/mbsxiwsrZch87oSFFhXUNp892iQSmfyAFaY7bzDn2MM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 0%

---

# Funzione di stampa{#print-feature}

Il visualizzatore consente di stampare il contenuto del catalogo.

La funzione di stampa viene attivata da un pulsante dedicato nella barra degli strumenti. Facendo clic sul pulsante è possibile scegliere un intervallo di stampa e il numero di pagine per foglio.

È possibile regolare la qualità di stampa utilizzando il parametro di configurazione `printquality`. Si noti che non è consigliabile impostare `printquality` su valori significativamente superiori a quelli predefiniti. Il motivo è che porta a un consumo di memoria molto elevato da parte del browser web sul sistema del client. Inoltre, assicurati che la dimensione massima di risposta dell&#39;immagine impostata per la tua società Dynamic Media Classic sia maggiore del valore `printquality` configurato.

>[!NOTE]
>
>La funzione di stampa è disponibile solo sui sistemi desktop, ad eccezione di Internet Explorer 9.

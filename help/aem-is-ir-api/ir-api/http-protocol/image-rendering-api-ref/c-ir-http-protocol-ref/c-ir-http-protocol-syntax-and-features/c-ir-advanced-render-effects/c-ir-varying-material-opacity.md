---
title: Opacità materiale variabile
description: L'opacità variabile è supportata per i colori in tinta unita e le texture ripetibili applicate agli oggetti sovrapposti, nonché per le decalcomanie e i materiali di rivestimento delle finestre.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: 'https://experienceleague.adobe.com/i4d6vy62vn9BfFrS2W0srO671N9Ad4hCUXR7J4cajJA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# Opacità materiale variabile{#varying-material-opacity}

L&#39;opacità variabile è supportata per i colori in tinta unita e le texture ripetibili applicate agli oggetti sovrapposti, nonché per le decalcomanie e i materiali di rivestimento delle finestre.

Le informazioni sull&#39;opacità possono essere fornite semplicemente utilizzando un&#39;immagine RGB con un canale alfa. Inoltre, l&#39;opacità complessiva può essere variata con il comando `opacity=` (sia per le immagini RGB che RGBA).

I bordi delle pareti supportano anche le immagini RGBA, principalmente per i bordi con taglio automatico.

I file [!DNL vnw] che definiscono le coperture delle finestre possono includere un canale di opacità. Viene combinato dal renderer con il canale alfa della texture ripetibile e il valore `opacity=` per fornire una gamma completa di effetti di opacità per i trattamenti di finestre trasparenti e trasparenti.

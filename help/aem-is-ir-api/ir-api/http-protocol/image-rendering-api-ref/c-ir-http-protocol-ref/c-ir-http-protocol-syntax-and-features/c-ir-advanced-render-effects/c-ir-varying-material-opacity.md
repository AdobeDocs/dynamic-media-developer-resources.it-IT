---
title: Opacità materiale variabile
description: L'opacità variabile è supportata per i colori in tinta unita e le texture ripetibili applicate agli oggetti sovrapposti, nonché per le decalcomanie e i materiali di rivestimento delle finestre.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Opacità materiale variabile{#varying-material-opacity}

L&#39;opacità variabile è supportata per i colori in tinta unita e le texture ripetibili applicate agli oggetti sovrapposti, nonché per le decalcomanie e i materiali di rivestimento delle finestre.

Le informazioni sull&#39;opacità possono essere fornite semplicemente utilizzando un&#39;immagine RGB con un canale alfa. Inoltre, l&#39;opacità complessiva può essere variata con il comando `opacity=` (sia per le immagini RGB che RGBA).

I bordi delle pareti supportano anche le immagini RGBA, principalmente per i bordi con taglio automatico.

I file [!DNL vnw] che definiscono le coperture delle finestre possono includere un canale di opacità. Viene combinato dal renderer con il canale alfa della texture ripetibile e il valore `opacity=` per fornire una gamma completa di effetti di opacità per i trattamenti di finestre trasparenti e trasparenti.

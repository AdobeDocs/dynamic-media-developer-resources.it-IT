---
description: L'opacità variabile è supportata per il colore in tinta unita e le texture ripetibili applicate agli oggetti sovrapposti, nonché per le decorazioni e i materiali di rivestimento delle finestre.
seo-description: L'opacità variabile è supportata per il colore in tinta unita e le texture ripetibili applicate agli oggetti sovrapposti, nonché per le decorazioni e i materiali di rivestimento delle finestre.
seo-title: Opacità materiale variabile
solution: Experience Manager
title: Opacità materiale variabile
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Opacità materiale variabile{#varying-material-opacity}

L&#39;opacità variabile è supportata per il colore in tinta unita e le texture ripetibili applicate agli oggetti sovrapposti, nonché per le decorazioni e i materiali di rivestimento delle finestre.

Le informazioni sull&#39;opacità possono essere fornite semplicemente utilizzando un&#39;immagine RGB con un canale alfa. Inoltre, l&#39;opacità complessiva può essere variata con il comando `opacity=` (sia per le immagini RGB che per le immagini RGBA).

I bordi delle pareti supportano anche le immagini RGBA, principalmente per supportare i bordi di taglio dinamico.

I file [!DNL vnw] che definiscono i rivestimenti delle finestre possono includere un canale di opacità, che viene combinato dal renderer con il canale alfa della texture ripetibile e il valore `opacity=` per fornire una gamma completa di effetti di opacità per i trattamenti di finestre semplici e traslucidi.

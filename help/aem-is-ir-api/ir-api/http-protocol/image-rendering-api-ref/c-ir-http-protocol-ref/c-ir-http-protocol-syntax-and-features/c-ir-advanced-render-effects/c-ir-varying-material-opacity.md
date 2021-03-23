---
description: L'opacità variabile è supportata per i colori solidi e le texture ripetibili applicate agli oggetti sovrapposti, nonché per i decali e i materiali di rivestimento per finestre.
seo-description: L'opacità variabile è supportata per i colori solidi e le texture ripetibili applicate agli oggetti sovrapposti, nonché per i decali e i materiali di rivestimento per finestre.
seo-title: Opacità materiale variabile
solution: Experience Manager
title: Opacità materiale variabile
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# Opacità materiale variabile{#varying-material-opacity}

L&#39;opacità variabile è supportata per i colori solidi e le texture ripetibili applicate agli oggetti sovrapposti, nonché per i decali e i materiali di rivestimento per finestre.

Le informazioni sull&#39;opacità possono essere fornite semplicemente utilizzando un&#39;immagine RGB con un canale alfa. Inoltre, l&#39;opacità complessiva può essere variata con il comando `opacity=` (sia per le immagini RGB che RGBA).

I bordi a parete supportano anche le immagini RGBA, principalmente per supportare i bordi di stampa.

I file [!DNL vnw] che definiscono i rivestimenti per finestre possono includere un canale di opacità, che viene combinato dal renderer con il canale alfa della texture ripetibile e il valore `opacity=` per fornire un&#39;intera gamma di effetti di opacità per trattamenti di finestre semplici e traslucide.

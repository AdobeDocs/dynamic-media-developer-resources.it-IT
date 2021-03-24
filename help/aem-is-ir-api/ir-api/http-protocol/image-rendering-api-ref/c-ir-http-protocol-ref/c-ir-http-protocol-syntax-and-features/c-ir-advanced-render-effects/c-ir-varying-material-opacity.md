---
description: L'opacità variabile è supportata per i colori solidi e le texture ripetibili applicate agli oggetti sovrapposti, nonché per i decali e i materiali di rivestimento per finestre.
solution: Experience Manager
title: Opacità materiale variabile
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Opacità materiale variabile{#varying-material-opacity}

L&#39;opacità variabile è supportata per i colori solidi e le texture ripetibili applicate agli oggetti sovrapposti, nonché per i decali e i materiali di rivestimento per finestre.

Le informazioni sull&#39;opacità possono essere fornite semplicemente utilizzando un&#39;immagine RGB con un canale alfa. Inoltre, l&#39;opacità complessiva può essere variata con il comando `opacity=` (sia per le immagini RGB che RGBA).

I bordi a parete supportano anche le immagini RGBA, principalmente per supportare i bordi di stampa.

I file [!DNL vnw] che definiscono i rivestimenti per finestre possono includere un canale di opacità, che viene combinato dal renderer con il canale alfa della texture ripetibile e il valore `opacity=` per fornire un&#39;intera gamma di effetti di opacità per trattamenti di finestre semplici e traslucide.

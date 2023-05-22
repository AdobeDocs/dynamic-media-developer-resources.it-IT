---
title: Protocollo server FXG
description: Per manipolare un elemento grafico, potete usare punti di riferimento simili ai punti cardinali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 69%

---

# Protocollo server FXG{#fxg-server-protocol}

Per manipolare un elemento grafico, potete usare punti di riferimento simili ai punti cardinali.

Questi consentono di ruotare o ridimensionare un elemento grafico rispetto a un particolare punto di riferimento. I punti di riferimento sono `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south`, e `southeast`. Ad esempio, utilizzando il punto di riferimento centrale, potete ruotare un&#39;immagine di 45° rispetto al centro. L&#39;immagine seguente mostra la posizione dei punti di riferimento, un elemento grafico ruotato di 20° rispetto al relativo `northWest` punto di riferimento e la grafica ruotata di 20° rispetto al punto `east` punto di riferimento.

![Immagine dei punti di riferimento](assets/wp_ref_points.png)

* A. Posizioni dei punti di riferimento
* B. Un&#39;immagine
* C. La grafica ruotava di 20° rispetto alla `northWest` punto di riferimento
* D. L&#39;immagine è ruotata di 20° rispetto alla `east` punto di riferimento

È richiesta la seguente sintassi:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Il valore predefinito è none. Il valore `inherit` passa il valore `s7:referencePoint`, purché sia diverso da `none`, dall’inizio della pagina o dal livello gruppo a tutti gli elementi figlio. L’impostazione `none` significa che non c’è alcun punto di riferimento per l’oggetto e viene usato il sistema di coordinate FXG.

>[!NOTE]
>
>per usare un punto di riferimento ma non produrre alcuno spostamento nell’oggetto dopo che è stato manipolato, aggiornare i valori x e y dell’oggetto dopo averlo manipolato.

Quando si usa un valore`s7:referencePoint`   con dei gruppi (o tracciati, elementi linea o altri elementi che non hanno definizioni specifiche di larghezza e altezza), il valore è applicabile al rettangolo di selezione cumulativo del gruppo. Ad esempio, il punto superiore sinistro del rettangolo di selezione di tutti gli oggetti del gruppo agisce da punto di riferimento `northWest` (nord ovest) per il gruppo; il punto inferiore destro agisce invece da punto di riferimento `southEast` (sud est).

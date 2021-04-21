---
description: Per manipolare un elemento grafico, potete usare punti di riferimento simili ai punti cardinali.
solution: Experience Manager
title: Protocollo server FXG
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 84%

---


# Protocollo del server FXG{#fxg-server-protocol}

Per manipolare un elemento grafico, potete usare punti di riferimento simili ai punti cardinali.

Questi consentono di ruotare o ridimensionare un elemento grafico rispetto a un particolare punto di riferimento. I punti di riferimento sono `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` e `southeast`. Ad esempio, con il punto di riferimento center potete ruotare un elemento grafico di 45 gradi attorno al suo centro. Questa illustrazione mostra dove si trovano i punti di riferimento, un elemento grafico, tale elemento ruotato di 20 gradi rispetto al punto di riferimento `northWest` (nord ovest) e ruotato di 20 gradi rispetto al punto di riferimento `east` (est).

![](assets/wp_ref_points.png)

* A. Posizioni dei punti di riferimento
* B. Grafico A
* C. L&#39;immagine ha ruotato di 20 gradi dal suo punto di riferimento `northWest`
* D. L&#39;immagine ha ruotato di 20 gradi dal suo punto di riferimento `east`

È richiesta la seguente sintassi:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Il valore predefinito è none. Il valore `inherit` passa il valore `s7:referencePoint`, purché sia diverso da `none`, dall’inizio della pagina o dal livello gruppo a tutti gli elementi figlio. L’impostazione `none` significa che non c’è alcun punto di riferimento per l’oggetto e viene usato il sistema di coordinate FXG.

>[!NOTE]
>
>per usare un punto di riferimento ma non produrre alcuno spostamento nell’oggetto dopo che è stato manipolato, aggiornare i valori x e y dell’oggetto dopo averlo manipolato.

Quando si usa un valore`s7:referencePoint`   con dei gruppi (o tracciati, elementi linea o altri elementi che non hanno definizioni specifiche di larghezza e altezza), il valore è applicabile al rettangolo di selezione cumulativo del gruppo. Ad esempio, il punto superiore sinistro del rettangolo di selezione di tutti gli oggetti del gruppo agisce da punto di riferimento `northWest` (nord ovest) per il gruppo; il punto inferiore destro agisce invece da punto di riferimento `southEast` (sud est).


---
title: Protocollo server FXG
description: Per manipolare un elemento grafico, potete utilizzare punti di riferimento simili ai punti di bussola.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 18%

---

# Protocollo server FXG{#fxg-server-protocol}

Per manipolare un elemento grafico, potete utilizzare punti di riferimento simili ai punti di bussola.

Questi consentono di ruotare o ridimensionare un elemento grafico rispetto a un particolare punto di riferimento. I punti di riferimento sono `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` e `southeast`. Ad esempio, utilizzando il punto di riferimento centrale, potete ruotare un&#39;immagine di 45° rispetto al centro. L&#39;immagine seguente mostra la posizione dei punti di riferimento, un elemento grafico, l&#39;elemento grafico ruotato di 20° dal punto di riferimento `northWest` e l&#39;elemento grafico ruotato di 20° dal punto di riferimento `east`.

![Immagine punti di riferimento](assets/wp_ref_points.png)

* A. Posizioni dei punti di riferimento
* B. Un&#39;immagine
* C. L&#39;immagine è ruotata di 20° rispetto al punto di riferimento `northWest`
* D. L&#39;immagine è ruotata di 20° rispetto al punto di riferimento `east`

È richiesta la seguente sintassi:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Il valore predefinito è none. Il valore `inherit` passa il valore `s7:referencePoint`, purché non sia `none`, dalla parte superiore della pagina o del livello del gruppo a tutti gli elementi figlio. L&#39;impostazione `none` indica che non esiste alcun punto di riferimento per l&#39;oggetto e che viene utilizzato il sistema di coordinate FXG.

>[!NOTE]
>
>per usare un punto di riferimento ma non produrre alcuno spostamento nell’oggetto dopo che è stato manipolato, aggiornare i valori x e y dell’oggetto dopo averlo manipolato.

Quando un valore di `s7:referencePoint` viene utilizzato con gruppi (o percorsi, elementi di linea o qualsiasi elemento che non dispone di definizioni esplicite di larghezza e altezza), il valore viene applicato al riquadro limite cumulativo del gruppo. Ad esempio, il punto in alto a sinistra del rettangolo di selezione di tutti gli oggetti del gruppo funge da punto di riferimento `northWest` per il gruppo; il punto in basso a destra funge da punto di riferimento `southEast`.

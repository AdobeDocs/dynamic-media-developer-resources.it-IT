---
description: Image Serving implementa una semplice funzione di filigrana visiva.
solution: Experience Manager
title: Filigrane
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---


# Filigrane{#watermarks}

Image Serving implementa una semplice funzione di filigrana visiva.

Una filigrana è in genere un’immagine semitrasparente, ma può essere testo o un’immagine composita a più livelli. Il server sovrapporrà la filigrana sull&#39;immagine di risposta dopo l&#39;applicazione di tutti gli attributi di visualizzazione ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`).

La filigrana è abilitata impostando `attribute::Watermark` su una voce di catalogo valida che contenga l&#39;immagine o il modello della filigrana. Se `attribute::Watermark` è impostato in un catalogo denominato, il server aggiungerà la filigrana a tutte le richieste di immagini che fanno riferimento all&#39;ID del catalogo nell&#39;URL della richiesta. Se `default::Watermark` è impostata (nel catalogo predefinito, [!DNL default.ini]), la filigrana viene applicata a tutte le richieste di immagini, indipendentemente dal fatto che facciano riferimento o meno a un catalogo.

Le filigrane non vengono applicate alle immagini restituite in risposta alle richieste di miniature ( `req=tmb`) e a determinate richieste dei visualizzatori Dynamic Media.

## Ridimensionamento e allineamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando viene specificata una filigrana, il server genererà innanzitutto l&#39;immagine composita (l&#39; *immagine di destinazione*) a cui deve essere applicata la filigrana (prima di applicare le trasformazioni di visualizzazione). Il server genera quindi l&#39;immagine composita per la filigrana come qualsiasi altra immagine (l&#39; *immagine della filigrana*).

A differenza delle immagini standard, è possibile specificare `sizeN=` per layer=0 o layer=comp dell’immagine della filigrana. Questo consente di ridimensionare l&#39;immagine della filigrana rispetto all&#39;immagine di destinazione. Se `sizeN=` non è specificato, l&#39;immagine della filigrana viene mantenuta nella dimensione in pixel quando viene unita all&#39;immagine di destinazione.

I comandi di richiesta (come `fmt=`) e di visualizzazione (come `wid=`) vengono ignorati nei record delle filigrane, ad eccezione di `align=`. `align=` può essere utilizzata per posizionare l&#39;immagine della filigrana rispetto all&#39;immagine della filigrana relativa all&#39;immagine di destinazione. Questo consente di posizionare la filigrana rispetto a un angolo o a un bordo dell’immagine di destinazione.

Dopo il ridimensionamento e l&#39;allineamento, il server sovrapporrà l&#39;immagine della filigrana all&#39;immagine di destinazione utilizzando i valori `blendMode=` e `opac=` specificati per `layer=0` o `layer=comp` dell&#39;immagine della filigrana. Infine, i comandi di richiesta e visualizzazione specificati per l&#39;immagine di destinazione vengono applicati per creare l&#39;immagine di risposta.

L&#39;immagine della filigrana non si estenderà mai su alcuno spazio vuoto aggiunto all&#39;immagine di risposta dai comandi `wid=` e `hei=`.

## Esempio {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una tipica filigrana può essere costituita da una semplice immagine RGBA contenente un logo o un avviso di copyright. Create un record nel catalogo immagini (o nel catalogo predefinito) con `catalog::Id` impostato su `watermark` e specificate il file immagine della filigrana in `catalog::Path`. Desideriamo estendere la filigrana in modo da adattarla all&#39;immagine della vista (senza distorcere la filigrana) lasciando un margine aggiuntivo e ridurre l&#39;opacità al 20% della filigrana originale, quindi impostiamo `catalog::Modifier` su `sizeN=0.9,0.9&opac=20`. Per attivare la filigrana, impostare `attribute::Watermark` sull&#39;ID della voce del catalogo della filigrana, &quot;filigrana&quot; in questo esempio. Potremo sperimentare diverse scelte `blendMode=` per ottenere diversi effetti di filigrana.

## Consultate anche {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attributo::Filigrana](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)

---
description: Image Serving implementa una semplice funzione di filigrana visiva.
solution: Experience Manager
title: Filigrane
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Filigrane{#watermarks}

Image Serving implementa una semplice funzione di filigrana visiva.

Una filigrana è in genere un&#39;immagine semitrasparente, ma può essere costituita da testo o da un&#39;immagine composita a livelli più complessa. Il server applica la filigrana sull&#39;immagine di risposta dopo l&#39;applicazione di tutti gli attributi di visualizzazione ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`).

La filigrana è abilitata impostando `attribute::Watermark` su una voce di catalogo valida contenente l&#39;immagine o il modello della filigrana. Se `attribute::Watermark` è impostato in un catalogo denominato, il server aggiunge la filigrana a tutte le richieste di immagini che fanno riferimento all&#39;ID catalogo nell&#39;URL della richiesta. Se è impostato `default::Watermark` (nel catalogo predefinito, [!DNL default.ini]), la filigrana viene applicata a tutte le richieste di immagini, indipendentemente dal fatto che facciano riferimento o meno a un catalogo.

Le filigrane non vengono applicate alle immagini restituite in risposta a richieste di miniature ( `req=tmb`) e ad alcune richieste dei visualizzatori Dynamic Media.

## Ridimensionamento e allineamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando viene specificata una filigrana, il server genera innanzitutto l&#39;immagine composita *immagine di destinazione* a cui deve essere applicata la filigrana (prima di applicare le trasformazioni di visualizzazione). Il server genera quindi l&#39;immagine composita per la filigrana come qualsiasi altra immagine (*immagine filigrana*).

A differenza delle immagini standard, è possibile specificare `sizeN=` per layer=0 o layer=comp dell&#39;immagine della filigrana. Ciò consente di ridimensionare l’immagine della filigrana rispetto all’immagine di destinazione. Se `sizeN=` non è specificato, l&#39;immagine della filigrana mantiene le dimensioni in pixel quando viene unita all&#39;immagine di destinazione.

I comandi di richiesta (come `fmt=`) e i comandi di visualizzazione (come `wid=`) vengono ignorati nei record delle filigrane, ad eccezione di `align=`. `align=` può essere utilizzato per posizionare l&#39;immagine della filigrana rispetto all&#39;immagine della filigrana rispetto all&#39;immagine di destinazione. Ciò consente di posizionare la filigrana rispetto a un angolo o a un bordo dell’immagine di destinazione.

Dopo il ridimensionamento e l&#39;allineamento, il server posiziona l&#39;immagine della filigrana sull&#39;immagine di destinazione utilizzando i valori `blendMode=` e `opac=` specificati per `layer=0` o `layer=comp` dell&#39;immagine della filigrana. Infine, i comandi di richiesta e di visualizzazione specificati per l’immagine di destinazione vengono applicati per costruire l’immagine di risposta.

Si noti che l&#39;immagine della filigrana non si estende mai oltre gli spazi vuoti aggiunti all&#39;immagine di risposta dai comandi `wid=` e `hei=`.

## Esempio {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una filigrana tipica può essere costituita da una semplice immagine RGBA contenente un logo o un avviso di copyright. Si crea un record nel catalogo immagini (o nel catalogo predefinito) con `catalog::Id` impostato su `watermark` e si specifica il file di immagine della filigrana in `catalog::Path`. Desideriamo estendere la filigrana per adattarla all&#39;immagine di visualizzazione (senza distorcere la filigrana) lasciando un po&#39; di margine in più e ridurre l&#39;opacità al 20% della filigrana originale, quindi impostiamo `catalog::Modifier` su `sizeN=0.9,0.9&opac=20`. Per attivare la filigrana, impostare `attribute::Watermark` sull&#39;ID della voce di catalogo della filigrana, &quot;filigrana&quot; in questo esempio. È possibile sperimentare diverse `blendMode=` scelte per ottenere diversi effetti di filigrana.

## Consultate anche {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attributo::filigrana](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)

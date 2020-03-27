---
description: Image Serving implementa una semplice funzione di filigrana visiva.
seo-description: Image Serving implementa una semplice funzione di filigrana visiva.
seo-title: Filigrane
solution: Experience Manager
title: Filigrane
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Filigrane{#watermarks}

Image Serving implementa una semplice funzione di filigrana visiva.

Una filigrana è in genere un’immagine semitrasparente, ma può essere testo o un’immagine composita a più livelli. Il server sovrapporrà la filigrana sull&#39;immagine di risposta dopo che tutti gli attributi di visualizzazione ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) saranno stati applicati.

La filigrana è abilitata impostando `attribute::Watermark` una voce di catalogo valida che contenga l’immagine o il modello della filigrana. Se `attribute::Watermark` è impostato in un catalogo denominato, il server aggiungerà la filigrana a tutte le richieste di immagini che fanno riferimento all’ID del catalogo nell’URL della richiesta. Se `default::Watermark` è impostata (nel catalogo predefinito, [!DNL default.ini]), la filigrana viene applicata a tutte le richieste di immagini, indipendentemente dal fatto che facciano riferimento o meno a un catalogo.

Le filigrane non vengono applicate alle immagini restituite in risposta alle richieste di miniature ( `req=tmb`) e a determinate richieste dei visualizzatori Scene7.

## Ridimensionamento e allineamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando viene specificata una filigrana, il server genererà innanzitutto l&#39;immagine composita (l&#39;immagine *di* destinazione) a cui deve essere applicata la filigrana (prima di applicare le trasformazioni di visualizzazione). Il server genera quindi l’immagine composita per la filigrana come qualsiasi altra immagine (l’immagine *della* filigrana).

A differenza delle immagini standard, `sizeN=` può essere specificato per layer=0 o layer=comp dell’immagine della filigrana. Questo consente di ridimensionare l&#39;immagine della filigrana rispetto all&#39;immagine di destinazione. Se non `sizeN=` viene specificata, l&#39;immagine della filigrana mantiene le dimensioni in pixel quando viene unita all&#39;immagine di destinazione.

I comandi di richiesta (come `fmt=`) e di visualizzazione (come `wid=`) vengono ignorati nei record delle filigrane, ad eccezione di `align=`. `align=` può essere utilizzata per posizionare l&#39;immagine della filigrana rispetto all&#39;immagine della filigrana relativa all&#39;immagine di destinazione. Questo consente di posizionare la filigrana rispetto a un angolo o a un bordo dell’immagine di destinazione.

Dopo il ridimensionamento e l&#39;allineamento, il server sovrapporrà l&#39;immagine della filigrana all&#39;immagine di destinazione utilizzando i valori `blendMode=` e `opac=` specificati per `layer=0` o `layer=comp` dell&#39;immagine della filigrana. Infine, i comandi di richiesta e visualizzazione specificati per l&#39;immagine di destinazione vengono applicati per creare l&#39;immagine di risposta.

L&#39;immagine della filigrana non si estenderà mai su uno spazio vuoto aggiunto all&#39;immagine di risposta dai `wid=` comandi e `hei=` .

## Esempio {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una tipica filigrana può essere costituita da una semplice immagine RGBA contenente un logo o un avviso di copyright. Create un record nel catalogo immagini (o nel catalogo predefinito) con `catalog::Id` impostato su `watermark` e specificate il file immagine della filigrana in `catalog::Path`. Vogliamo allungare la filigrana in modo da adattarla all&#39;immagine della vista (senza distorcere la filigrana) lasciando un margine aggiuntivo, e ridurre l&#39;opacità al 20% della filigrana originale, quindi impostiamo `catalog::Modifier` su `sizeN=0.9,0.9&opac=20`. Per attivare la filigrana, impostare `attribute::Watermark` l&#39;ID della voce del catalogo filigrane &quot;filigrane&quot; in questo esempio. Potremmo voler sperimentare diverse `blendMode=` scelte per ottenere diversi effetti di filigrana.

## Consultate anche {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attributo::Filigrana](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)

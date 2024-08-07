---
title: config
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# config{#config}

Parametro comune a tutti i visualizzatori.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span> </span> </p> </td> 
   <td colname="col2"> <p>Catalogo/ID per la configurazione del visualizzatore. </p> <p> Specifica una voce del catalogo immagini che contiene le proprietà di configurazione del visualizzatore nel catalogo <span class="codeph">::UserData </span>. Quando questo comando è presente, il visualizzatore invia un comando <span class="codeph"> req=userdata </span> per il configId </span> <span class="codeph"> al server ed estrae le proprietà dalla risposta. Le proprietà vengono utilizzate per inizializzare il visualizzatore. Se la stringa dell'URL specifica le stesse proprietà, sostituiscono i valori del catalogo <span class="codeph">::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tutti i comandi del visualizzatore che è possibile specificare in `catalog::UserData` prevedono `asset`, `serverUrl`, `contentUrl`, `searchServerUrl` e `config`.

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Facoltativo.

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

Nessuno.

## Esempio 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Un catalogo immagini denominato 2020 contiene la voce `preset-oct`. Il campo `catalog::UserData` di questa voce di catalogo include i dati seguenti:

```
style=customStyle.css
```

Carica il visualizzatore con il seguente comando:

```
config=2020/preset-oct
```

Questo esempio equivale al seguente comando specificato esplicitamente nell’URL:

```
style=customStyle.css
```

## Esempio 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

Un catalogo immagini denominato 2019 contiene la voce `spin-oct`. Il campo `catalog::UserData` di questa voce di catalogo include i dati seguenti:

```
zoomStep=3 
maxZoom=200
```

Carica il visualizzatore con il seguente comando:

```
config=2019/spin-oct
```

Questo esempio equivale al seguente comando specificato esplicitamente nell’URL:

```
zoomStep=3&maxZoom=200
```

## Esempio 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

Un predefinito visualizzatore denominato `Shoppable_Banner` include i dati seguenti:

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

Carica il visualizzatore con il seguente comando:

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

Questo esempio equivale ai seguenti comandi specificati esplicitamente nell’URL:

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Esempio 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

Un predefinito visualizzatore denominato `Shoppable_Video_Dark` contiene i dati seguenti:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

Carica il visualizzatore con il seguente comando:

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

Questo esempio equivale ai seguenti comandi specificati esplicitamente nell’URL:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Esempio 5 {#section-19b988551d1d492a9079948e0b04b38f}

Un predefinito visualizzatore denominato `Carousel_Dotted_light` contiene i seguenti dati:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Carica il visualizzatore con il seguente comando:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Questo esempio equivale ai seguenti comandi specificati esplicitamente nell’URL:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

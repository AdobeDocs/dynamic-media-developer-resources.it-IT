---
description: Le impostazioni di questa sezione devono essere considerate solo se è richiesto il rendering SVG.
seo-description: Le impostazioni di questa sezione devono essere considerate solo se è richiesto il rendering SVG.
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SVG{#svg}

Le impostazioni di questa sezione devono essere considerate solo se è richiesto il rendering SVG.

## SV::SvgHeapSize - Dimensione heap SVG {#section-59ab17681daa4be8b5d794713e1a504e}

Dimensione heap Java per il rendering SVG. Il valore predefinito è &quot;200m&quot; (200 Mbyte).

## PS::svgProvider.rootPaths - SVG Data Root Folders {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Posizione dei file di dati sorgente SVG. Può essere uno o più percorsi di file assoluti o relativi a *[!DNL install_folder]*, separati da punto e virgola. In genere, impostate lo stesso valore di `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Dimensione massima file SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Dimensione massima del file sorgente SVG in kBytes. Il server restituisce un errore quando si tenta di eseguire il rendering di un file SVG maggiore di questo limite. Il valore predefinito è 1024 kbyte.

## IS::SvgMAxRenderRongPixels - Limite dimensione immagine di output SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita le dimensioni delle immagini che SVGRender può produrre. Valore intero maggiore di 0 in milioni di pixel. Viene restituito un errore se un&#39;operazione di rendering supera il limite di dimensioni. Il valore predefinito è 4.

## PS::svgProvider.port - Porta di ascolto del server della piattaforma {#section-f7e42a96c2dd4523b46f0557c239e659}

La porta utilizzata per SvgRender per ottenere immagini dal server piattaforma da incorporare nei rendering SVG.

Importante Per il corretto funzionamento del componente SVGRender, questa opzione di configurazione deve essere impostata sullo stesso valore di `TC::PsPort`.

## PS::svgProvider.fontRoot - Cartella dei file di font SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Specifica la posizione in cui SvgRender troverà i file di font necessari per il rendering del testo SVG; in genere uno dei percorsi specificati in `IS::RootPaths`. Il valore predefinito è [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Porta di comunicazione SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura la porta sulla quale comunicano il server immagini e il componente SVGRender.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Per il corretto funzionamento del componente SVGRender, è necessario specificare lo stesso numero di porta per `SVG::SVGRender.port` e `IS::SVGTcpPort`.


---
description: I file di dati sorgente Image Server includono file di immagini e maschere, font e profili ICC.
seo-description: I file di dati sorgente Image Server includono file di immagini e maschere, font e profili ICC.
seo-title: Dati di origine
solution: Experience Manager
title: Dati di origine
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Dati di origine{#source-data}

I file di dati sorgente Image Server includono file di immagini e maschere, font e profili ICC.

Tutti i file di dati di origine devono essere accessibili al server immagini. Image Server offre diverse alternative per specificare la posizione dei file di dati:

` *`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogo::Path|catalogo::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> percorso e nome del file immagine relativo specificati in una richiesta HTTP Image Server</span> </p></td> 
 </tr> 
</table>

Il server combina i segmenti di percorso da destra a sinistra finché non viene definito un percorso di file assoluto.

Tutti i segmenti ` *`rootPath`*` possono essere vuoti, relativi o assoluti.

` *``*` catalogPathis un percorso/nome file assoluto o relativo. ` *``*` requestPathdeve essere un percorso/nome di file relativo.

`Multiple IS::RootPath` i valori possono essere definiti in ImageServerRegistry.xml (o tramite l&#39;interfaccia di amministrazione). Questo consente la distribuzione dei file di dati di origine tra più file system. Il server immagini proverà a utilizzare percorsi alternativi nell’ordine specificato fino a quando il file di dati non viene trovato.

Nuovi file di dati di qualsiasi tipo possono essere aggiunti in qualsiasi momento senza arrestare il server.

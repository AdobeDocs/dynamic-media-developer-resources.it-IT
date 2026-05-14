---
description: I file di dati di origine di Image Server includono file immagine e maschera, font e profili ICC.
solution: Experience Manager
title: Dati Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
TQID: 'https://experienceleague.adobe.com/36EvEOjHZ8ik-gps-vaap5PhFCf5rwV9ecfkKHZcIhk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Dati Source{#source-data}

I file di dati di origine di Image Server includono file immagine e maschera, font e profili ICC.

Tutti i file di dati di origine devono essere accessibili al server immagini. Image Server offre diverse alternative per specificare la posizione dei file di dati:

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> percorso file </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogo::Path|catalogo::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> nome e percorso del file di immagine relativo specificati in una richiesta HTTP di Image Server</span> </p></td> 
 </tr> 
</table>

Il server combina i segmenti di percorso da destra a sinistra fino a quando non viene stabilito un percorso di file assoluto.

Tutti i segmenti `*`rootPath`*` possono essere vuoti, relativi o assoluti.

`*`catalogPath`*` è un nome o un percorso di file assoluto o relativo. `*`requestPath`*` deve essere un nome o un percorso di file relativo.

I valori `Multiple IS::RootPath` possono essere definiti in ImageServerRegistry.xml (o tramite l&#39;interfaccia di amministrazione). Questo consente di distribuire i file di dati di origine su più file system. Il server immagini tenta percorsi alternativi nell&#39;ordine specificato finché non viene trovato il file di dati.

È possibile aggiungere nuovi file di dati di qualsiasi tipo in qualsiasi momento senza arrestare il server.

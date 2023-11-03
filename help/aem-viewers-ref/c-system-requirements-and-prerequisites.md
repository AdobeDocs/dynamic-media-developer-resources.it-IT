---
title: Requisiti di sistema per visualizzatori Dynamic Medie HTML5
description: Requisiti di sistema per visualizzatori Dynamic Medie HTML5.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Requisiti di sistema per visualizzatori Dynamic Medie HTML5{#system-requirements}

Requisiti di sistema per visualizzatori Dynamic Medie HTML5.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Hardware e software per server {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Medie Image Server 6.7.1 o versione successiva.
* I visualizzatori HTML5 richiedono le librerie SDK JavaScript lato server 3.11.5 o successive.
* *Invia un&#39;e-mail a un amico* le funzioni social richiedono s7ondemand 5.0.9 o versione successiva.
* Visualizzatore eCatalog - [Menu a comparsa del pannello Info](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) il supporto richiede info server 2.1.8 o versione successiva.
* I componenti della funzione di ricerca richiedono s7search 2.3.0 o versione successiva.

## Requisiti di sistema dei visualizzatori {#section-cc72b1e209524d038b4d5b92b35e998e}

**Requisiti minimi del browser client per i visualizzatori di componenti:**

* Supportato nelle seguenti versioni del sistema operativo o successive:
   * Microsoft® Windows® 7
   * macOS X 10.12
* Supportato nelle seguenti versioni del browser/piattaforma o successive:
   * Android™ OS 4.x
   * BlackBerry® 10 sui browser nativi. È supportata solo la riproduzione di video.
   * Chrome 82
   * Bordo
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 (solo browser Safari e Chrome)
   * iPhone 3GS
   * Safari 11
* Internet Explorer su dispositivi mobili non è supportato.
* *VisualizzatorePanoramico* è supportato nelle seguenti versioni di browser/piattaforma o successive:
   * Android™ 4.4 (solo dispositivi telefonici)
   * Chrome 82
   * Bordo
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Visualizzatore video360i* e *DimensionalViewer* è supportato nelle seguenti versioni di browser/piattaforma o successive:
   * Android™ 5 (solo dispositivi telefonici)
   * Chrome 82
   * Bordo
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* è supportato nelle seguenti versioni di browser/piattaforma o successive:
   * Android™ 4.x
   * Chrome 82
   * Bordo
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## Fine del supporto per TLS 1.0 e 1.1 {#tls}

<!-- CQDOC-19433 -->

A partire dal 30 settembre 2022, i visualizzatori Dynamic Medie di Adobe hanno terminato il supporto per i seguenti elementi:

* TLS (Transport Layer Security) 1.0 e 1.1
* Le seguenti crittografie deboli in TLS 1.2:
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
   * TLS_RSA_WITH_AES_256_GCM_SHA384
   * TLS_RSA_WITH_AES_256_CBC_SHA256
   * TLS_RSA_WITH_AES_256_CBC_SHA
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_AES_128_GCM_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_256_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_128_CBC_SHA
   * TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA
   * TLS_RSA_WITH_SDES_EDE_CBC_SHA

## Combinazioni di browser Web e sistemi operativi non supportate per i visualizzatori Dynamic Medie {#browser-os-support}

<!-- CQDOC-19433 -->

I visualizzatori Dynamic Medie di Adobe non supportano le seguenti combinazioni di browser web e sistemi operativi:

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Aggiornamento Internet Explorer 11 + Windows Phone 8.1
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9 Mavericks
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android&trade; 2.3.7
* Android&trade; 4.0.4
* Android&trade; 4.1.1
* Android&trade; 4.2.2
* Android&trade; 4.3
* Internet Explorer 7 on Window Vista&reg;
* Internet Explorer 8 on Windows&reg; XP
* Internet Explorer 8-10 on Windows&reg; 7
* Internet Explorer 10 on Windows&reg; Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java&trade; 6u45
* Java&trade; 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->


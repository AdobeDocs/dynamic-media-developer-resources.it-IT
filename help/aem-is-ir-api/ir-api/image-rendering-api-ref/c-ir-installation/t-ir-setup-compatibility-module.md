---
description: È necessario configurare il modulo di compatibilità IR 3.x.
seo-description: È necessario configurare il modulo di compatibilità IR 3.x.
seo-title: Configurazione del modulo di compatibilità IR 3.x
solution: Experience Manager
title: Configurazione del modulo di compatibilità IR 3.x
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Configurazione e configurazione del modulo di compatibilità IR 3.x{#setup-and-configure-ir-x-compatibility-module}

È necessario configurare il modulo di compatibilità IR 3.x.

1. Interruzione `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Passate alla directory delle app Web ImageServer.
1. Copiare il contenuto della directory [!DNL ir] nella directory [!DNL ROOT].
1. Aprite [!DNL ROOT/WEB-INF/web.xml] in un editor di testo.
1. Cerca la riga `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Rimuovete il commento dai tag `<servlet>` e `<servlet-mapping>`.
1. Riavviare `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Esempio Linux**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Quindi, modificate [!DNL web.xml]utilizzando il vostro editor preferito per rimuovere il commento dai tag `<servlet>` e `<servlet-mapping>`.

**Esempio di Windows**

Aprite Esplora risorse e passate a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Selezionate tutti i file e le cartelle e copiateli all&#39;interno di `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Quindi, modificate il file `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, rimuovendo i commenti dai tag `<servlet>` e `<servlet-mapping>`.

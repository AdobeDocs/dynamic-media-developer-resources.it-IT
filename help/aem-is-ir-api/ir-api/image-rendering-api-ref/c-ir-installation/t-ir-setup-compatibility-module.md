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

---


# Configurazione del modulo di compatibilità IR 3.x{#setup-and-configure-ir-x-compatibility-module}

È necessario configurare il modulo di compatibilità IR 3.x.

1. Interruzione `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Passate alla directory delle app Web ImageServer.
1. Copiate il contenuto della [!DNL ir] directory nella [!DNL ROOT] directory.
1. Aprite [!DNL ROOT/WEB-INF/web.xml] in un editor di testo.
1. Ricerca della riga `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Rimuovete il commento dai `<servlet>` tag e `<servlet-mapping>` tag.
1. Restart `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Esempio Linux**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Quindi, [!DNL web.xml]usate il vostro editor preferito per rimuovere il commento dai `<servlet>` tag e `<servlet-mapping>` tag.

**Esempio di Windows**

Aprite Esplora risorse e passate a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Selezionate tutti i file e le cartelle e copiateli all’interno `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Quindi, modificate il file `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, rimuovendo i commenti dai `<servlet>` tag e `<servlet-mapping>` .

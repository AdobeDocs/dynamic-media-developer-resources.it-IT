---
description: È necessario configurare e configurare il modulo di compatibilità IR 3.x.
solution: Experience Manager
title: Configurazione e configurazione del modulo di compatibilità IR 3.x
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# Configurazione e configurazione del modulo di compatibilità IR 3.x{#setup-and-configure-ir-x-compatibility-module}

È necessario configurare e configurare il modulo di compatibilità IR 3.x.

1. Interruzione `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Passa alla directory delle applicazioni Web ImageServer.
1. Copia il contenuto della directory [!DNL ir] nella directory [!DNL ROOT].
1. Apri [!DNL ROOT/WEB-INF/web.xml] in un editor di testo.
1. Cerca la riga `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Rimuovi il commento ai tag `<servlet>` e `<servlet-mapping>` .
1. Riavvia `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Esempio Linux**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Quindi modifica [!DNL web.xml]utilizzando il tuo editor preferito per rimuovere il commento dai tag `<servlet>` e `<servlet-mapping>`.

**Esempio di Windows**

Apri Explorer e vai a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Seleziona tutti i file e le cartelle e copiali all&#39;interno di `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Quindi modifica il file `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, rimuovendo il commento dai tag `<servlet>` e `<servlet-mapping>`.

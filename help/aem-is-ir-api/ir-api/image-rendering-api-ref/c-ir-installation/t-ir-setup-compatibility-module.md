---
title: Configurazione e configurazione del modulo di compatibilità IR 3.x
description: Impostare e configurare il modulo di compatibilità IR 3.x.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurazione e configurazione del modulo di compatibilità IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Interruzione `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Passa alla directory delle applicazioni Web ImageServer.
1. Copia il contenuto del [!DNL ir] nella directory [!DNL `ROOT`] directory.
1. Apri [!DNL `ROOT/WEB-INF/web.xml`] in un editor di testo.
1. Cerca la riga `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Rimuovi il commento da `<servlet>` e `<servlet-mapping>` tag.
1. Riavvia `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Esempio di Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Quindi modifica [!DNL `web.xml`] utilizzo dell&#39;editor preferito per rimuovere il commento `<servlet>` e `<servlet-mapping>` tag.

**Esempio di Windows**

Apri Explorer e vai a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Seleziona tutti i file e le cartelle e copiali all&#39;interno `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Quindi modifica il file `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, rimuovendo i commenti `<servlet>` e `<servlet-mapping>` tag.

---
title: Configurazione del modulo di compatibilità IR 3.x
description: Impostare e configurare il modulo di compatibilità IR 3.x.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# Configurazione del modulo di compatibilità IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Interruzione `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Passare alla directory Web apps di ImageServer.
1. Copia il contenuto del [!DNL ir] directory in [!DNL `ROOT`] directory.
1. Apri [!DNL `ROOT/WEB-INF/web.xml`] in un editor di testo.
1. Cerca la riga `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Rimuovi commento da `<servlet>` e `<servlet-mapping>` tag.
1. Riavvia `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Esempio di Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Quindi modificare [!DNL `web.xml`] utilizzo dell’editor preferito per rimuovere il commento da `<servlet>` e `<servlet-mapping>` tag.

**Esempio di Windows**

Apri Explorer e vai a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Seleziona tutti i file e le cartelle e copiali all’interno `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Quindi modifica il file `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, rimuovendo il commento da `<servlet>` e `<servlet-mapping>` tag.

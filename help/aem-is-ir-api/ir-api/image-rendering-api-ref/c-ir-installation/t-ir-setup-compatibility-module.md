---
title: Configurazione del modulo di compatibilità IR 3.x
description: Impostare e configurare il modulo di compatibilità IR 3.x.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
TQID: 'https://experienceleague.adobe.com/ce7CdClFrrIFb7fhZRKQ7XBpsNm4BTgwVFHPXy3BXhw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 0%

---

# Configurazione del modulo di compatibilità IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Interrompi `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Passare alla directory Web apps di ImageServer.
1. Copiare il contenuto della directory [!DNL ir] nella directory [!DNL `ROOT`].
1. Apri [!DNL `ROOT/WEB-INF/web.xml`] in un editor di testo.
1. Cerca la riga `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Rimuovere il commento dai tag `<servlet>` e `<servlet-mapping>`.
1. Riavvia `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux® esempio**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Quindi modificare [!DNL `web.xml`] utilizzando il tuo editor preferito per rimuovere il commento dai tag `<servlet>` e `<servlet-mapping>`.

**Esempio di Windows**

Apri Explorer e passa a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Selezionare tutti i file e le cartelle e copiarli in `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Quindi modificare il file `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, rimuovendo il commento dai tag `<servlet>` e `<servlet-mapping>`.

---
description: Utilizzare questa procedura per aggiornare Dynamic Media Image Serving su Linux.
seo-description: Utilizzare questa procedura per aggiornare Dynamic Media Image Serving su Linux.
seo-title: Aggiornamento da IS 4.7.4 o successivo
solution: Experience Manager
title: Aggiornamento da IS 4.7.4 o successivo
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Aggiornamento da IS 4.7.4 o successivo{#updating-from-is-or-later}

Utilizzare questa procedura per aggiornare Dynamic Media Image Serving su Linux.

Se stai eseguendo l&#39;aggiornamento da una versione precedente di Image Serving, contatta il supporto per il processo corretto.

La cartella [!DNL webapps] può essere eliminata al momento dell&#39;aggiornamento. Esegui il backup della cartella [!DNL webapps] prima dell&#39;aggiornamento.

1. Accedi all&#39;host del server con privilegi di root.
1. Decomprimi e cancella il file tar di distribuzione Image Serving.
1. Esegui [!DNL ./install-is] per avviare la procedura guidata di installazione che si trova nella cartella [!DNL setup] .

   Il programma di installazione dell&#39;aggiornamento verifica l&#39;integrità e la versione del pacchetto installato. In caso di esito positivo, viene visualizzato il contratto di licenza con l’utente finale (&quot;EULA&quot;).
1. Leggere il contratto di licenza e quindi inserire &quot;**[!UICONTROL y]**&quot; per procedere con l&#39;installazione.

   Il programma di installazione esegue il backup dei vecchi file di configurazione del server nella cartella [!DNL BACKUP/].

   Al termine dell’installazione viene visualizzato il seguente messaggio:

   `Image Server was started successfully`

Durante un aggiornamento, il file [!DNL ImageServing/conf/server.xml] viene aggiornato alle impostazioni più recenti. Se hai modificato o aggiunto dei valori, devi salvare il [!DNL server.xml] esistente e reimplementare le modifiche dopo l&#39;aggiornamento.

Dopo un&#39;installazione di aggiornamento, considera il riscaldamento della cache di risposta HTTP prima di avviare il server. Per ulteriori informazioni, fare riferimento alla descrizione dell&#39;utilità [!DNL playlog] .

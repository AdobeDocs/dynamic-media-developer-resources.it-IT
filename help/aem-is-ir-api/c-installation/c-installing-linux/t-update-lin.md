---
description: Utilizzate questa procedura per aggiornare Scene7 Image Serving su Linux.
seo-description: Utilizzate questa procedura per aggiornare Scene7 Image Serving su Linux.
seo-title: Aggiornamento da IS 4.7.4 o successivo
solution: Experience Manager
title: Aggiornamento da IS 4.7.4 o successivo
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Aggiornamento da IS 4.7.4 o successivo{#updating-from-is-or-later}

Utilizzate questa procedura per aggiornare Scene7 Image Serving su Linux.

Se state effettuando l’aggiornamento da una versione precedente di Image Server, contattate il supporto per il processo corretto.

La [!DNL webapps] cartella potrebbe essere eliminata al momento dell&#39;aggiornamento. Esegui il backup della [!DNL webapps] cartella prima dell&#39;aggiornamento.

1. Effettuate l&#39;accesso all&#39;host del server con i privilegi di root.
1. Decomprimete e decomprimete il file tar di distribuzione Image Server.
1. Eseguire [!DNL ./install-is] per avviare la procedura guidata di installazione che si trova nella [!DNL setup] cartella.

   Il programma di installazione dell&#39;aggiornamento verifica l&#39;integrità e la versione del pacchetto installato. In caso di esito positivo, viene visualizzato il contratto di licenza per l&#39;utente finale (&quot;EULA&quot;).
1. Leggere il contratto di licenza e quindi digitare &quot; **[!UICONTROL y]**&quot; per procedere con l&#39;installazione.

   Il programma di installazione esegue il backup dei vecchi file di configurazione del server nella [!DNL BACKUP/] cartella.

   Quando l&#39;installazione è completa viene visualizzato il seguente messaggio:

   `Image Server was started successfully`
>Durante un aggiornamento, il [!DNL ImageServing/conf/server.xml] file viene aggiornato alle impostazioni più recenti. Se avete modificato o aggiunto dei valori, salvate quelli esistenti [!DNL server.xml] e reimplementate le modifiche dopo l&#39;aggiornamento.
>
>Dopo un&#39;installazione di aggiornamento, prendete in considerazione il riscaldamento della cache delle risposte HTTP prima di rendere attivo il server. Per informazioni dettagliate, fare riferimento alla descrizione dell&#39; [!DNL playlog] utilità.


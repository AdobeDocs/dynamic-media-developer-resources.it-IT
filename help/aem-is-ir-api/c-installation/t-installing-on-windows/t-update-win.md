---
description: Utilizzate questa procedura per aggiornare Scene7 Image Serving.
seo-description: Utilizzate questa procedura per aggiornare Scene7 Image Serving.
seo-title: Aggiornamento da IS 4.7.4 o successivo
solution: Experience Manager
title: Aggiornamento da IS 4.7.4 o successivo
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Aggiornamento da IS 4.7.4 o successivo{#updating-from-is-or-later}

Utilizzate questa procedura per aggiornare Scene7 Image Serving.

Se state effettuando l’aggiornamento da una versione precedente di Image Server, contattate il supporto per il processo corretto.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>La [!DNL webapps] cartella potrebbe essere eliminata al momento dell&#39;aggiornamento. Esegui il backup della [!DNL webapps] cartella prima dell&#39;aggiornamento.

1. Accedete all&#39;host del server con privilegi amministrativi.
1. Estrarre il contenuto del file zip di distribuzione Image Server.
1. Per avviare la procedura guidata di installazione, eseguite setup/setup.exe.
1. Fare clic su **[!UICONTROL Avanti]** per avanzare al contratto di licenza per l&#39;utente finale (EULA), leggere il contratto di licenza e fare clic su **[!UICONTROL Sì]**.

   Nella pagina successiva vengono visualizzate le impostazioni di configurazione precedenti.
1. Fate clic su **[!UICONTROL Avanti]** per avviare l&#39;installazione dell&#39;aggiornamento.

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >Il programma di installazione esegue il backup dei vecchi file di configurazione del server nella [!DNL BACKUP/] cartella.

1. Al termine dell&#39;installazione, fare clic su &quot;Fine&quot; per uscire dalla procedura guidata di installazione.

   In alcuni casi, la procedura guidata di installazione potrebbe richiedere il riavvio del sistema.
>Durante un aggiornamento, il [!DNL ImageServing/conf/server.xml] file viene aggiornato alle impostazioni più recenti. Se avete modificato o aggiunto dei valori, salvate quelli esistenti [!DNL server.xml] e reimplementate le modifiche dopo l&#39;aggiornamento.
>
>Dopo un&#39;installazione di aggiornamento, prendete in considerazione il riscaldamento della cache delle risposte HTTP prima di rendere attivo il server. Per informazioni dettagliate, fare riferimento alla descrizione dell&#39; `playlog` utilità.


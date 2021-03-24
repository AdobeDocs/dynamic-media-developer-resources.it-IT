---
description: Utilizzare questa procedura per aggiornare Dynamic Media Image Server.
solution: Experience Manager
title: Aggiornamento da IS 4.7.4 o successivo
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Aggiornamento da IS 4.7.4 o successivo{#updating-from-is-or-later}

Utilizzare questa procedura per aggiornare Dynamic Media Image Server.

Se stai eseguendo l&#39;aggiornamento da una versione precedente di Image Serving, contatta il supporto per il processo corretto.

>[!NOTE]
>
>La cartella [!DNL webapps] può essere eliminata al momento dell&#39;aggiornamento. Esegui il backup della cartella [!DNL webapps] prima dell&#39;aggiornamento.

1. Accedi all&#39;host del server con privilegi amministrativi.
1. Estrarre il contenuto del file zip di distribuzione Image Serving.
1. Esegui setup/setup.exe per avviare l&#39;installazione guidata.
1. Fare clic su **[!UICONTROL Avanti]** per avanzare al contratto di licenza con l&#39;utente finale (EULA), leggere il contratto di licenza e fare clic su **[!UICONTROL Sì]**.

   Nella pagina successiva vengono visualizzate le impostazioni di configurazione precedenti.
1. Fare clic su **[!UICONTROL Avanti]** per avviare l&#39;installazione dell&#39;aggiornamento.

   >[!NOTE]
   >
   >Il programma di installazione esegue il backup dei vecchi file di configurazione del server nella cartella [!DNL BACKUP/].

1. Al termine dell&#39;installazione, fare clic su &quot;Fine&quot; per uscire dalla procedura guidata di installazione.

   In alcuni casi, la procedura guidata di installazione potrebbe richiedere il riavvio del sistema.

Durante un aggiornamento, il file [!DNL ImageServing/conf/server.xml] viene aggiornato alle impostazioni più recenti. Se hai modificato o aggiunto dei valori, devi salvare il [!DNL server.xml] esistente e reimplementare le modifiche dopo l&#39;aggiornamento.

Dopo un&#39;installazione di aggiornamento, considera il riscaldamento della cache di risposta HTTP prima di avviare il server. Per ulteriori informazioni, fare riferimento alla descrizione dell&#39;utilità `playlog` .

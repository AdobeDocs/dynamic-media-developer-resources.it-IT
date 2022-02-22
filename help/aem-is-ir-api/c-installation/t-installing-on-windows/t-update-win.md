---
title: Aggiornamento da IS 4.7.4 o successivo
description: Utilizzare questa procedura per aggiornare Dynamic Media Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Aggiornamento da IS 4.7.4 o successivo{#updating-from-is-or-later}

Utilizzare questa procedura per aggiornare Dynamic Media Image Server.

Se stai eseguendo l&#39;aggiornamento da una versione precedente di Image Serving, contatta il supporto per il processo corretto.

>[!NOTE]
>
>La [!DNL webapps] È possibile eliminare la cartella in seguito all&#39;aggiornamento. Eseguire il backup [!DNL webapps] prima dell’aggiornamento.

1. Accedi all&#39;host del server con privilegi amministrativi.
1. Estrarre il contenuto del file zip di distribuzione Image Serving.
1. Avvia l&#39;installazione guidata eseguendo `setup/setup.exe`.
1. Seleziona **[!UICONTROL Successivo]** per avanzare al contratto di licenza con l’utente finale (EULA), leggere il contratto di licenza e selezionare **[!UICONTROL Sì]**.

   Nella pagina successiva vengono visualizzate le impostazioni di configurazione precedenti.
1. Fai clic su **[!UICONTROL Successivo]** per avviare l&#39;installazione dell&#39;aggiornamento.

   >[!NOTE]
   >
   >Il programma di installazione esegue il backup dei vecchi file di configurazione del server nel [!DNL BACKUP/] cartella.

1. Al termine dell&#39;installazione, seleziona **[!UICONTROL Fine]** per uscire dalla procedura guidata di installazione.

   A volte la procedura guidata di installazione potrebbe richiedere il riavvio del sistema.

Durante un aggiornamento, il [!DNL ImageServing/conf/server.xml] viene aggiornato alle impostazioni più recenti. Se hai modificato o aggiunto dei valori, devi salvarli [!DNL server.xml] e reimplementare le modifiche dopo l&#39;aggiornamento.

Dopo un&#39;installazione di aggiornamento, considera il riscaldamento della cache di risposta HTTP prima di avviare il server. Fai riferimento alla descrizione del `playlog` utilità per i dettagli.

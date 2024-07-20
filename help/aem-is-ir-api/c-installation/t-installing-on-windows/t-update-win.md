---
title: Aggiornamento da IS 4.7.4 o versione successiva
description: Utilizzare questa procedura per aggiornare Dynamic Medie Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Aggiornamento da IS 4.7.4 o versione successiva{#updating-from-is-or-later}

Utilizzare questa procedura per aggiornare Dynamic Medie Image Server.

Se stai effettuando l’aggiornamento da una versione precedente di Image Server, contatta il supporto per la procedura corretta.

>[!NOTE]
>
>È possibile eliminare la cartella [!DNL webapps] durante l&#39;aggiornamento. Eseguire il backup della cartella [!DNL webapps] prima dell&#39;aggiornamento.

1. Accedi all’host del server con privilegi di amministratore.
1. Estrai il contenuto del file zip di distribuzione di Image Server.
1. Avviare l&#39;installazione guidata eseguendo `setup/setup.exe`.
1. Selezionare **[!UICONTROL Avanti]** per passare al contratto di licenza con l&#39;utente finale, leggere il contratto di licenza e selezionare **[!UICONTROL Sì]**.

   Nella pagina successiva vengono visualizzate le impostazioni di configurazione precedenti.
1. Fai clic su **[!UICONTROL Avanti]** per avviare l&#39;installazione dell&#39;aggiornamento.

   >[!NOTE]
   >
   >Il programma di installazione esegue il backup dei vecchi file di configurazione del server nella cartella [!DNL BACKUP/].

1. Al termine dell&#39;installazione, selezionare **[!UICONTROL Fine]** per uscire dall&#39;installazione guidata.

   A volte la procedura guidata di installazione potrebbe richiedere il riavvio del sistema.

Durante un aggiornamento, il file [!DNL ImageServing/conf/server.xml] viene aggiornato alle impostazioni più recenti. Se sono stati modificati o aggiunti valori, è necessario salvare [!DNL server.xml] esistente e reimplementare le modifiche dopo l&#39;aggiornamento.

Dopo un’installazione di aggiornamento, considera di riscaldare la cache di risposta HTTP prima di attivare il server. Per ulteriori informazioni, vedere la descrizione dell&#39;utilità `playlog`.

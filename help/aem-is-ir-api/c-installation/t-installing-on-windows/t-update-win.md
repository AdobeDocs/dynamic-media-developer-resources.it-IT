---
title: Aggiornamento da IS 4.7.4 o versione successiva
description: Segui questa procedura per aggiornare Dynamic Media Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
TQID: 'https://experienceleague.adobe.com/ibeLWHpA-Lk2wiXkSgGL02uMEYH4t8l0xjjXuN9ooiE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 0%

---

# Aggiornamento da IS 4.7.4 o versione successiva{#updating-from-is-or-later}

Segui questa procedura per aggiornare Dynamic Media Image Server.

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

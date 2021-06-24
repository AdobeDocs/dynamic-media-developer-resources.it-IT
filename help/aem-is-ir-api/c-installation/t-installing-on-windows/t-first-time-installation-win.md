---
description: Utilizzare questi passaggi per installare Image Server per la prima volta su Windows.
solution: Experience Manager
title: Installazione per la prima volta
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Installazione per la prima volta{#installing-for-the-first-time}

Utilizzare questi passaggi per installare Image Server per la prima volta su Windows.

1. Accedi all&#39;host del server con privilegi amministrativi.
1. Se hai già ricevuto una licenza, copiala sul tuo server, quindi esegui l&#39;installazione della licenza facendo doppio clic sul file.

   Se non si dispone ancora di una licenza, è possibile procedere con l&#39;installazione e installare la licenza in un secondo momento.
1. Estrarre il contenuto del file zip di distribuzione Image Serving.
1. Esegui [!DNL setup]/ [!DNL setup.exe] per avviare l&#39;installazione guidata.
1. Fare clic su &quot;Successivo&quot; per passare al contratto di licenza con l&#39;utente finale (EULA), leggere il contratto di licenza e fare clic su **[!UICONTROL Sì]**.

   La finestra di dialogo [!DNL Authentication] viene visualizzata come segue.
1. Se una licenza è già installata e le informazioni sulla licenza vengono visualizzate nella finestra di dialogo [!DNL Authentication], fare clic su **[!UICONTROL Avanti]** per continuare.

   Se non disponi di una licenza, fai clic su **[!UICONTROL Richiedi licenza]**. Nella finestra di dialogo successiva viene visualizzato uno degli indirizzi MAC della scheda di interfaccia di rete del computer. Invia un&#39;e-mail a questo indirizzo MAC, al nome dell&#39;azienda e al prodotto che stai installando come indicato dal prompt.

   **Importante:** la licenza si basa sull&#39;indirizzo MAC di una delle schede di interfaccia di rete installate su questo host. Se disattivi, rimuovi o sostituisci questa scheda, la licenza non verrà più riconosciuta valida. Assicurati di ottenere una licenza per la configurazione hardware che utilizzerai per IS.

   È possibile continuare a installare IS senza una licenza valida e installare la licenza in un secondo momento. Per continuare, fare clic su **[!UICONTROL Indietro]** per tornare alla finestra di dialogo [!DNL Authentication], quindi fare clic su **[!UICONTROL Avanti]**.
1. Procedi alla pagina &quot;Impostazioni amministratore server della piattaforma&quot;. Immetti i nuovi valori desiderati oppure accetta i valori predefiniti.

   Puoi configurare i seguenti elementi:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Porta di connessione HTTP del server della piattaforma </p> </td> 
   <td> <p>Porta di ascolto HTTP principale per Image Server e Image Rendering </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Porta di ascolto amministratore </p> </td> 
   <td> <p>Porta di ascolto amministratore </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Dimensioni della cache del server della piattaforma in MB </p> </td> 
   <td> <p>Dimensione iniziale della cache di risposta principale </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Percorso cache del server della piattaforma </p> </td> 
   <td> <p>Cartella cache PS </p> </td> 
  </tr> 
 </tbody> 
</table>

I numeri di porta specificati devono essere univoci e non devono essere utilizzati da altre applicazioni o servizi.

La schermata successiva offre l’opportunità di rivedere le impostazioni selezionate.
1. Fare clic su **[!UICONTROL Indietro]** per apportare modifiche oppure fare clic su **[!UICONTROL Avanti]** per avviare l&#39;installazione.
1. Fare clic su **[!UICONTROL Fine]** per uscire dalla procedura guidata di installazione.

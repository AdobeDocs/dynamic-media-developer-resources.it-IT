---
description: Per installare Image Server per la prima volta in Windows, effettuate le seguenti operazioni.
seo-description: Per installare Image Server per la prima volta in Windows, effettuate le seguenti operazioni.
seo-title: Prima installazione
solution: Experience Manager
title: Prima installazione
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# Prima installazione{#installing-for-the-first-time}

Per installare Image Server per la prima volta in Windows, effettuate le seguenti operazioni.

1. Accedete all&#39;host del server con privilegi amministrativi.
1. Se avete già ricevuto una licenza, copiatela sul server, quindi eseguite l&#39;installazione della licenza facendo doppio clic sul file.

   Se non disponete ancora di una licenza, potete procedere con l&#39;installazione e installare la licenza in un secondo momento.
1. Estrarre il contenuto del file zip di distribuzione Image Server.
1. Eseguire [!DNL setup]/ [!DNL setup.exe] per avviare l&#39;installazione guidata.
1. Fare clic su &quot;Avanti&quot; per avanzare al contratto di licenza con l&#39;utente finale (EULA), leggere il contratto di licenza e fare clic su **[!UICONTROL Sì]**.

   Nella finestra di dialogo [!DNL Authentication] viene visualizzata la casella successiva.
1. Se una licenza è già installata e le informazioni sulla licenza vengono visualizzate nella finestra di dialogo [!DNL Authentication], fare clic su **[!UICONTROL Next]** per continuare.

   Se non si dispone di una licenza, fare clic su **[!UICONTROL Richiedi licenza]**. Nella finestra di dialogo successiva viene visualizzato uno degli indirizzi MAC della scheda di interfaccia di rete del computer. Inviate questo indirizzo MAC, il nome della società e il prodotto che state installando come indicato dal prompt.

   **Importante:** la licenza si basa sull&#39;indirizzo MAC di una delle schede di interfaccia di rete installate sull&#39;host. Se si disabilita, rimuove o sostituisce questa scheda, la licenza non verrà più riconosciuta come valida. Assicuratevi di ottenere una licenza per la configurazione hardware che utilizzerete per IS.

   È possibile continuare a installare IS senza una licenza valida e installare la licenza in un secondo momento. Per continuare, fare clic su **[!UICONTROL Indietro]** per tornare alla finestra di dialogo [!DNL Authentication], quindi fare clic su **[!UICONTROL Avanti]**.
1. Passate alla pagina &quot;Impostazioni amministratore server piattaforma&quot;. Immettete nuovi valori in base alle esigenze o accettate i valori predefiniti.

   Puoi configurare i seguenti elementi:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Porta connessione HTTP server piattaforma </p> </td> 
   <td> <p>Porta di ascolto HTTP principale per Image Server e Image Rendering </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Porta di ascolto amministratore </p> </td> 
   <td> <p>Porta di ascolto amministratore </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Dimensione cache server piattaforma in MB </p> </td> 
   <td> <p>Dimensione iniziale della cache di risposta principale </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Percorso cache server piattaforma </p> </td> 
   <td> <p>Cartella cache PS </p> </td> 
  </tr> 
 </tbody> 
</table>

I numeri di porta specificati devono essere univoci e non devono essere utilizzati da altre applicazioni o servizi.

Nella schermata successiva è possibile esaminare le impostazioni selezionate.
1. Fare clic su **[!UICONTROL Indietro]** per apportare modifiche oppure fare clic su **[!UICONTROL Avanti]** per avviare l&#39;installazione.
1. Fare clic su **[!UICONTROL Fine]** per uscire dalla procedura guidata di installazione.

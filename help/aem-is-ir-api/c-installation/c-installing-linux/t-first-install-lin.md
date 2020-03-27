---
description: Questa procedura mostra come installare Image Serving per la prima volta su Linux.
seo-description: Questa procedura mostra come installare Image Serving per la prima volta su Linux.
seo-title: Prima installazione
solution: Experience Manager
title: Prima installazione
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prima installazione{#installing-for-the-first-time}

Questa procedura mostra come installare Image Serving per la prima volta su Linux.

1. Effettuate l&#39;accesso all&#39;host del server con le autorizzazioni radice.
1. Create la cartella [!DNL /usr/local/scene7/licenses].

   Se è disponibile il file della licenza Image Server e/o Image Rendering (con suffisso [!DNL .sc8] file), copiatelo in questa cartella. In caso contrario, continuate con l&#39;installazione e installate il codice di licenza in un secondo momento.
1. Decomprimete e decomprimete il file tar di distribuzione Image Server.
1. 
   4. Eseguite [!DNL ./install-is], che si trova nella [!DNL Setup] cartella, per avviare la procedura guidata di installazione.
   Se non viene trovata alcuna chiave di licenza, vengono visualizzate istruzioni che descrivono come ottenere un file di licenza. A questo punto, oppure procedere con l’installazione di Image Server e installare il codice di licenza in un secondo momento.
1. Quando viene visualizzato il contratto di licenza per l&#39;utente finale (EULA), leggete il contratto di licenza e immettete `y` per proseguire.

   Il programma di installazione visualizza i prompt elencati nella tabella seguente.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta di ascolto principale [8080]:</span> </p> </td> 
   <td colname="col2"> <p>Porta di ascolto HTTP principale per Image Server e Image Rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta di ascolto amministratore [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Porta di ascolto amministratore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Dimensione massima cache HTTP (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Dimensione iniziale della cache di risposta principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Cartella principale cache [/usr/local/scene7/Image Server/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Cartella cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID proprietario server immagini [root]:</span> </p> </td> 
   <td colname="col2"> <p>L’account utente in cui installare i server Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID gruppo server immagini [root]:</span> </p> </td> 
   <td colname="col2"> <p>L’account del gruppo in cui installare i server Image Server. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Premere **[!UICONTROL Invio]** per accettare il valore predefinito o specificare un valore diverso.

   Verificate che tutti i numeri di porta specificati siano univoci e che non vengano utilizzati in caso contrario su questo host.

   **Importante: **Se è specificato un account diverso da root, è necessario assicurarsi che le autorizzazioni di accesso per tutti i file e le cartelle che il server immagini deve leggere e/o scrivere siano impostate correttamente quando queste cartelle vengono riconfigurate nei file di configurazione.
>Image Server è ora installato in [!DNL /usr/local/Scene7/ImageServing]. Alcuni contenuti di rendering delle immagini sono installati in [!DNL /usr/local/Scene7/ImageRendering].
>
>Al termine dell’installazione, la procedura guidata di installazione tenta di avviare Image Server. Se non viene trovata alcuna chiave di licenza valida, Image Server non può avviarsi. Se è presente una licenza valida e Image Server non è ancora in fase di avvio, consultare i file di registro.
>[!NOTE]
Se la licenza è installata dopo l’installazione di Image Server, il server immagini deve essere avviato manualmente prima di utilizzarlo.
>
>
>


---
title: Installazione per la prima volta
description: Questa procedura mostra come installare Image Serving per la prima volta su Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Installazione per la prima volta{#installing-for-the-first-time}

Questa procedura mostra come installare Image Serving per la prima volta su Linux®.

1. Accedi all&#39;host del server con le autorizzazioni root.
1. Crea la cartella [!DNL /usr/local/scene7/licenses].

   Se il file della chiave di licenza Image Server e/o Image Rendering (con [!DNL .sc8] suffisso file) disponibile, copiarlo in questa cartella. In caso contrario, procedere con l&#39;installazione e installare la chiave di licenza in un secondo momento.
1. Decomprimi e cancella il file tar di distribuzione Image Serving.
1. In [!DNL Setup] cartella, avviare l&#39;installazione guidata eseguendo [!DNL ./install-is].

   Se non viene trovata alcuna chiave di licenza, vengono visualizzate istruzioni che descrivono come ottenere un file di licenza. A questo punto, procedi con l&#39;installazione di Image Serving e installa la chiave di licenza in un secondo momento.
1. Quando viene visualizzato il contratto di licenza con l’utente finale (EULA), leggere il contratto di licenza e quindi immettere `y` per procedere.

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
   <td colname="col1"> <p><span class="codeph"> Dimensione massima della cache HTTP (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Dimensione iniziale della cache di risposta principale. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Cartella principale cache [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Cartella cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID proprietario server immagini [root]:</span> </p> </td>
   <td colname="col2"> <p>L'account utente in cui deve essere installato il server Image Server. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID gruppo server immagini [root]:</span> </p> </td>
   <td colname="col2"> <p>L'account del gruppo in cui deve essere installato il server Image Server. </p> </td>
  </tr>
 </tbody>
</table>

1. Press **[!UICONTROL Invio]** per accettare il valore predefinito o specificare un valore diverso.

   Assicurati che tutti i numeri di porta specificati siano univoci e non vengano utilizzati altrimenti su questo host.

   >[!IMPORTANT]
   >
   >Se viene specificato un account diverso da root, è necessario assicurarsi che le autorizzazioni di accesso per tutti i file e le cartelle che Image Server deve leggere e scrivere siano impostate correttamente quando queste cartelle vengono riconfigurate nei file di configurazione.
   >
   >Image Server è ora installato in [!DNL /usr/local/Scene7/ImageServing]. Alcuni contenuti di Image Rendering sono installati in [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Verso la fine dell&#39;installazione, la procedura guidata di installazione tenta di avviare Image Server. Se non viene trovata alcuna chiave di licenza valida, Image Server non può avviarsi. Se è presente una licenza valida e Image Server non è ancora in fase di avvio, consultare i file di registro.

>[!NOTE]
>
>Se la licenza viene installata dopo l&#39;installazione di Image Server, è necessario avviare manualmente Image Server prima dell&#39;utilizzo.

---
description: Contiene le impostazioni di Platform Server.
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---


# PlatformServer.conf{#platformserver-conf}

Contiene le impostazioni di Platform Server.

Questo file è un file di proprietà JAVA. Si deve fare attenzione a seguire le convenzioni appropriate; in caso contrario, l&#39;avvio del server Platform potrebbe non riuscire. Utilizzare una barra rovesciata doppia &#39;\\&#39; o una singola barra rovesciata &#39;/&#39; invece di una barra rovesciata &#39;\&#39; nei percorsi dei file di Windows. La barra rovesciata viene utilizzata come carattere di escape in questo tipo di file.

Le modifiche a questo file hanno effetto dopo il salvataggio del file.

Solo le impostazioni elencate di seguito possono essere modificate in [!DNL PlatformServer.conf]. Se una particolare impostazione è assente, può essere aggiunta in qualsiasi punto del file. Può essere presente una sola istanza di ciascuna impostazione.

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Impostazioni generali di Platform Server </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000  </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824  </span> </p> <p> <span class="codeph"> isConnection.port=27345  </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequsts=true  </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000  </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configurazione del cluster di cache </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50  </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000  </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Errore di configurazione del reindirizzamento </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000  </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configurazione SVG </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./immagini </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024  </span> </p> <p> <span class="codeph"> svgProvider.port=8080  </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./immagini </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Risposte al set di file multimediali </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false  </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10  </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20  </span> </p> </td> 
 </tr> 
</table>


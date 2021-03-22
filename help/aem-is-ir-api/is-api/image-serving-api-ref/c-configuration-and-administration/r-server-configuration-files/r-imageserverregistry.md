---
description: Contiene le impostazioni di configurazione del server immagini.
seo-description: Contiene le impostazioni di configurazione del server immagini.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Contiene le impostazioni di configurazione del server immagini.

Quando si modifica questo file XML, è necessario prestare attenzione a mantenere una sintassi XML valida, altrimenti il server immagini potrebbe non avviarsi.

Per rendere effettive le modifiche, riavviare il server immagini dopo aver modificato il file. Sono supportati per la modifica solo i valori degli elementi elencati di seguito. Modifica qualsiasi altro contenuto di questo file solo se richiesto dal supporto tecnico Dynamic Media.

>[!NOTE]
>
>Non modificare la struttura di `<imageserverregistry>`, compreso l’ordine degli elementi. Presta attenzione quando modifichi questo file, altrimenti il server immagini potrebbe non avviarsi.

I seguenti elementi illustrano quali elementi possono essere modificati. Sono presenti altri elementi che non devono essere modificati. L&#39;ordine degli elementi qui sotto non riflette l&#39;ordine in cui devono essere presenti nel file.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Note {#section-7217f011f69f41e7af4f3983d7776d6f}

Possono essere presenti più elementi `<RootPath>` (uno per ogni cartella del file di dati di origine). Image Server cerca i percorsi principali nell&#39;ordine specificato per trovare un particolare file di origine.

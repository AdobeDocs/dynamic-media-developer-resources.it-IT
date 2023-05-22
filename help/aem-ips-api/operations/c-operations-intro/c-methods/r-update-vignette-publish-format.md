---
description: Aggiorna le impostazioni del formato di pubblicazione vignettatura.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 5%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

Aggiorna le impostazioni del formato di pubblicazione vignettatura.

## Tipi di utenti autorizzati {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Input (updateVignettePublishFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| vignetteFormatHandle | `xsd:string` | Sì | Handle di formato di pubblicazione. |
| nome | `xsd:string` | No | Nome formato di pubblicazione. |
| targetWidth | `xsd:int` | Sì | Specifica la larghezza di destinazione della visualizzazione vignettatura risultante, in pixel. Utilizzare zero in modo che la vignettatura di output abbia le stesse dimensioni della vignettatura principale. |
| targetHeight | `xsd:int` | Sì | Specifica l&#39;altezza di destinazione in pixel della visualizzazione vignettatura risultante. Utilizzare zero in modo che la vignettatura di output abbia le stesse dimensioni della vignettatura principale. |
| createPyramid | `xsd:boolean` | Sì | Crea una vignettatura piramidale ottimizzata per lo zoom sul server Image Rendering. Partendo dalla dimensione massima, impostata dai campi Dimensione vignettatura di destinazione, vengono create visualizzazioni con più dimensioni in un singolo file di output vignettatura. Ogni dimensione di visualizzazione successiva viene dimezzata fino a raggiungere valori di larghezza e altezza compresi tra 128x128 pixel. |
| thumbWidth | `xsd:int` | Sì | Specifica la larghezza in pixel di ciascuna miniatura risultante. Questa impostazione è facoltativa. Lascia zero per non creare alcun file di miniatura. |
| saveAsVersion | `xsd:int` | Sì | Specifica il formato di file per le vignettature pubblicate. Se si utilizza una nuova versione di Image Authoring e una precedente versione di Image Rendering Server, è necessario specificare una versione di vignettatura che il server ImageRendering possa leggere. Se specificate una versione successiva, il server Image Rendering non sarà in grado di leggere le vignettature pubblicate. Impostate questo valore su zero per pubblicare le vignettature all&#39;ultima versione. |
| sizeSuffixSeparator | `xsd:string` | Sì | Specifica il carattere che separa il nome della vignettatura e il suffisso che ne indica la larghezza. |
| nitidezza | `xsd:int` | No | Applica la nitidezza all&#39;immagine della visualizzazione principale per ogni dimensione di vignettatura pubblicata. La nitidezza può compensare la sfocatura quando le vignettature vengono ridimensionate. |
| usmImporto | `xsd:double` | Sì | Il mascheramento digitale è un modo flessibile e potente per aumentare la nitidezza, soprattutto nelle immagini digitalizzate. Questa opzione consente di controllare la grandezza di ciascuna sovrascrittura (quanto più scuri e chiari diventano i bordi del bordo). |
| usmRadius | `xsd:double` | Sì | Influisce sulla dimensione degli spigoli da aumentare o sulla larghezza dei bordi, quindi un raggio più piccolo migliora i dettagli di scala più piccola. Valori di raggio più alti possono causare aloni sui bordi. I dettagli fini richiedono un raggio più piccolo, in quanto vengono persi piccoli dettagli della stessa dimensione o più piccoli del raggio. |
| usmThreshold | `xsd:int` | Sì | Controlla la variazione minima della luminosità da rendere più nitida o la distanza tra i valori tonali adiacenti prima che il filtro funzioni. Questa impostazione consente di rendere più nitidi i bordi pronunciati lasciando invariati quelli più sottili. L’intervallo di soglia consentito è compreso tra 0 e 255. |

**Output (updateVignettePublishFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Sì | Gestisci il formato di pubblicazione vignettatura aggiornato. |

## Esempio {#section-fcba4bf2b7264786a676e315a35dbe43}

In questo esempio di codice viene aggiornato un formato di pubblicazione vignettatura e viene ripristinato il formato aggiornato dell&#39;handle.

**Request Contents (Richiesta contenuto)**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Risposta**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```

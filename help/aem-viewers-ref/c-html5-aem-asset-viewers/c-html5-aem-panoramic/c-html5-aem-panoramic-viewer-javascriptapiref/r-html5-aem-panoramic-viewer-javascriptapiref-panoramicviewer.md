---
title: Visualizzatore panoramico
description: Costrutore, crea una nuova istanza HTML5 Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 13d15bd9483d939de8391d5cfe814c48fed30f22
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---

# Visualizzatore panoramico{#panoramicviewer}

`PanoramicViewer([config])`
Crea una nuova istanza di visualizzatore panoramico di HTML5.

## Parametro {#section-fa807db629ce43bab286b1e1dc96c492}

La configurazione {Object} dell&#39;oggetto di configurazione JSON opzionale consente di passare tutte le impostazioni del visualizzatore al costruttore ed evitare di chiamare i singoli metodi del setter. Contiene le seguenti proprietà:
* containerId - {String} ID del contenitore DOM (in genere un DIV) in cui verrà inserito il visualizzatore. Non è necessario che l&#39;elemento contenitore sia creato dal momento in cui viene chiamato questo metodo, tuttavia il contenitore deve esistere quando viene eseguito init(). Obbligatorio
* params - Oggetto JSON {Object} con parametri di configurazione del visualizzatore in cui il nome della proprietà è un’opzione di configurazione specifica per il visualizzatore o un modificatore SDK e il valore di tale proprietà è un valore di impostazioni corrispondente. Obbligatorio
* gestori - oggetto JSON {Object} con callback di eventi del visualizzatore, dove il nome della proprietà è il nome dell&#39;evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript per il callback appropriato. Per ulteriori informazioni sugli eventi del visualizzatore, consulta la sezione Callback evento . Facoltativo


## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
	"initComplete":function() {
		console.log("init complete");
}
}
});
```

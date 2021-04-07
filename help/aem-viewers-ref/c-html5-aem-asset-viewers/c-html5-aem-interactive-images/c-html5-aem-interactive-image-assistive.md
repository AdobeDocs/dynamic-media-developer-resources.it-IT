---
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
title: Supporto tecnologico per assistenza
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Immagini interattive,Accessibilità
role: Sviluppatore, Business Practices
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Supporto della tecnologia di assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha l’attributo ruolo `region` e `aria-label` impostato sul nome del visualizzatore. Puoi controllare l’etichetta con il simbolo di localizzazione `Container.LABEL` .

La vista principale ha il ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente di visualizzazione principale corrispondente. I suggerimenti per la navigazione degli utenti tramite tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT` . Se una risorsa ha un’etichetta definita nel campo UserData , l’attributo `aria-label` viene impostato con il valore di tale etichetta.

Le aree calde, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label` , con il valore dell&#39;etichetta di area sensibile o mappa immagine. Quando l&#39;utente mette a fuoco punti o mappe immagine, i suggerimenti per la navigazione degli utenti tramite tastiera vengono forniti utilizzando `aria-describedby`, con il testo per il suggerimento di utilizzo proveniente dal simbolo di localizzazione `USAGE_HINT`.

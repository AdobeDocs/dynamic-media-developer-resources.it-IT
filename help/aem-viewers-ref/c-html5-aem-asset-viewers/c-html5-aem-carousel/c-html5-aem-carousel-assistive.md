---
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
title: Supporto tecnologico per assistenza
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello,Accessibilità
role: Developer,Business Practitioner
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: f464a7adcb8035a5bdebf1a6c9b647ba04535431
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Supporto tecnologico per assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha l’attributo ruolo `region` e `aria-label` impostato sul nome del visualizzatore. Puoi controllare l’etichetta con il simbolo di localizzazione `Container.LABEL` .

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label` . Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disabilitato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

I pulsanti che consentono di spostarsi tra le diapositive carosello presentano etichette che vengono aggiornate in fase di esecuzione a seconda della diapositiva attualmente selezionata. Il modello per l’etichetta di questo pulsante è impostato con il simbolo di localizzazione `CAROUSELVIEWER_TOOLTIP_GOTO` .

La vista principale ha il ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente di visualizzazione principale corrispondente. I suggerimenti per la navigazione degli utenti tramite tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT` . Se una risorsa ha un’etichetta definita nel campo UserData , l’attributo `aria-label` viene impostato con il valore di tale etichetta.

Le aree calde, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label` , con il valore dell&#39;etichetta di area sensibile o mappa immagine. Quando l&#39;utente mette a fuoco punti o mappe immagine, i suggerimenti per la navigazione degli utenti tramite tastiera vengono forniti utilizzando `aria-describedby`, con il testo per il suggerimento di utilizzo proveniente dal simbolo di localizzazione `USAGE_HINT`.

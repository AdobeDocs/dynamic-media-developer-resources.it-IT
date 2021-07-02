---
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
title: Supporto tecnologico per assistenza
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi,Accessibilità
role: Developer,Business Practitioner
exl-id: 6cf7f739-cbfb-4fac-8632-904a0d40ad05
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Supporto tecnologico per assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha l’attributo ruolo `region` e `aria-label` impostato sul nome del visualizzatore. Puoi controllare l’etichetta con il simbolo di localizzazione `Container.LABEL` .

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label` . Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disabilitato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

La vista principale ha il ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente di visualizzazione principale corrispondente. I suggerimenti per la navigazione degli utenti tramite tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT` . Se una risorsa ha un’etichetta definita nel campo UserData , l’attributo `aria-label` viene impostato con il valore di tale etichetta.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con l’attributo `aria-label` impostato sul valore del simbolo di localizzazione `LABEL` di quel componente. I singoli campioni hanno il ruolo `option` con gli attributi `aria-setsize` e `aria-posinset` per descrivere la posizione del campione nel set. Se è selezionato un campione, l’attributo `aria-selected` viene impostato su `true`.

I componenti cursore hanno il ruolo `slider` con attributi `aria-valuenow`, `aria-valuemin` e `aria-valuemax` per descrivere la posizione corrente del cursore.

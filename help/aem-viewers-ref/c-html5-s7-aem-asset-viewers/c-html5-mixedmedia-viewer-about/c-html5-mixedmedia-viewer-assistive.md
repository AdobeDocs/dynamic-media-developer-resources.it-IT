---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets,Accessibility
role: Developer,User
exl-id: 6cf7f739-cbfb-4fac-8632-904a0d40ad05
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di primo livello ha il ruolo `region` e `aria-label` attributo impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con `Container.LABEL` simbolo di localizzazione.

I pulsanti hanno il ruolo `button` e set di testo descrittivo con `aria-label` attributo. Il valore di `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, `aria-disabled` viene impostato di conseguenza.

La visualizzazione principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito da `ROLE_DESCRIPTION` simbolo di localizzazione del componente della vista principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera sono forniti tramite `aria-describedby`, il testo per l’hint di utilizzo proviene da `USAGE_HINT` simbolo di localizzazione. Se per una risorsa è stata definita un’etichetta nel campo UserData, il `aria-label` viene impostato con il valore di tale etichetta.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con `aria-label` attributo impostato sul valore del `LABEL` simbolo di localizzazione del componente. I singoli campioni hanno il ruolo `option` con `aria-setsize` e `aria-posinset` attributi per descrivere la posizione del campione nel set. Se viene selezionato un campione, questo ottiene `aria-selected` attributo impostato su `true`.

I componenti cursore hanno il ruolo `slider` con attributi `aria-valuenow`, `aria-valuemin`, e `aria-valuemax` per descrivere la posizione corrente del cursore.

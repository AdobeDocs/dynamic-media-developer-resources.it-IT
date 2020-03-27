---
description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-title: Supporto per tecnologie di assistenza
solution: Experience Manager
title: Supporto per tecnologie di assistenza
topic: Dynamic media
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per tecnologie di assistenza{#assistive-technology-support}

Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l&#39;integrazione con tecnologie di supporto come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha ruolo `region` e `aria-label` attributo impostati sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di `Container.LABEL` localizzazione.

La visione principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di `ROLE_DESCRIPTION` localizzazione del componente di visualizzazione principale corrispondente. I suggerimenti di navigazione per gli utenti della tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo viene dal simbolo di `USAGE_HINT` localizzazione. Se una risorsa ha un&#39;etichetta definita nel campo UserData, l&#39; `aria-label` attributo è impostato con il valore di tale etichetta.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con `aria-label` l’attributo impostato sul valore del simbolo di `LABEL` localizzazione del componente. I singoli campioni hanno il ruolo `option` con `aria-setsize` e `aria-posinset` gli attributi per descrivere la posizione del campione nel set. Se viene selezionato un campione, l’ `aria-selected` attributo viene impostato su `true`.

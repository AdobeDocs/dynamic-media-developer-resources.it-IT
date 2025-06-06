---
description: Imposta la password di un utente specifico o di quello predefinito su un valore specifico, a seconda che sia stato specificato un handle utente.
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e8d95b55-0a97-4887-b711-7be99833c389
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 2%

---

# setPassword{#setpassword}

Imposta la password di un utente specifico o di quello predefinito su un valore specifico, a seconda che sia stato specificato un handle utente.

La data di scadenza della password è facoltativa. Se omessa, la password non scade mai.

## Tipi di utenti autorizzati {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*Solo* il tipo di utente `IpsAdmin` è autorizzato a eseguire chiamate setPassword contro altri utenti.

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## Parametri {#section-0531294341f7483d89dacaa393dd659a}

**Input (setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obbligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> UserHandle </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:stringa </span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Handle utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> password </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:stringa </span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Password. </p> <p>I seguenti requisiti vengono applicati alla password scelta: </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">Le password distinguono tra maiuscole e minuscole. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">La password deve avere una lunghezza minima di otto caratteri. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">La password deve contenere uno o più caratteri delle seguenti classi di caratteri: 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">Caratteri inglesi minuscoli. <span class="codeph"> a b c d e </span> e così via </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">Caratteri inglesi maiuscoli. <span class="codeph"> A B C D E </span> e così via. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">Numeri. Ad esempio, <span class="codeph"> 1 2 3 4 5 </span> e così via. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">Caratteri simbolo speciali. Ad esempio, è possibile utilizzare uno dei seguenti elementi: <span class="codeph"> &grave; ~ ! @ # $ % ^ * ( ) _ + - = { } | [ ] &amp; \ : " ; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordScade </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Determina la data di scadenza della password. <p>Nota: specifica il fuso orario con la richiesta per questo campo. Fusi orari adeguati all’ora centrale. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (setPasswordReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-23a6fbabdb3c4c3180076057e47ae567}

In questo esempio di codice viene creata una password utente. La password non scade mai perché `passwordExpires` è stato omesso.

**Richiesta**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**Risposta**

Nessuno.

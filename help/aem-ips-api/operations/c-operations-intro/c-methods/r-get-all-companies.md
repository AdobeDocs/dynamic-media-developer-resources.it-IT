---
description: Restituisce un array di tutte le aziende.
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 17%

---

# getAllCompanies{#getallcompanies}

Restituisce un array di tutte le aziende.

Sintassi

## Tipi di utenti autorizzati {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Parametri {#section-efd74992e6904ebabe7383b577af4fdb}

**Input (getAllCompaniesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`includeExpired`*` | `xsd:boolean` | Sì | Imposta su true per restituire le società scadute e non scadute. |

**Output (getAllCompaniesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyArray`*` | `types:CompanyArray` | Sì | La gamma di aziende. |

## Esempi {#section-3eecf4e6900b41fb92a0e3214791c6b9}

Questo esempio di codice restituisce tutte le società in IPS in un array. La risposta di esempio viene troncata per brevità.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**Risposta**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```

[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entità: AgriProductType  
=======================  
[Licenza aperta](https://github.com/smart-data-models//dataModel.Agrifood/blob/master/AgriProductType/LICENSE.md)  
[documento generato automaticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
Descrizione globale: **Questa entità contiene una descrizione armonizzata di un tipo generico di prodotto agricolo. Questa entità è associata principalmente al verticale agricolo e alle relative applicazioni IoT. L'AgriProductType include una struttura gerarchica che consente di raggruppare i tipi di prodotto in modo flessibile **.  
versione: 0.0.1  

## Elenco delle proprietà  

- `agroVocConcept`: Riferimento al termine agrovoc associato a questa voce  - `alternateName`: Un nome alternativo per questa voce  - `category`: Categoria del prodotto. Enum:'fertilizzante, nutrizione delle colture, protezione delle colture, varietà di colture, prodotto del raccolto'.  - `dataProvider`: Una sequenza di caratteri che identifica il fornitore dell'entità di dati armonizzata.  - `dateCreated`: Timestamp di creazione dell'entità. Di solito viene assegnato dalla piattaforma di archiviazione.  - `dateModified`: Timestamp dell'ultima modifica dell'entità. Di solito viene assegnato dalla piattaforma di archiviazione.  - `description`: Descrizione dell'articolo  - `hasAgriProductTypeChildren`: Riferimento ai tipi di prodotto figli, cioè immediatamente sotto questa entità nella gerarchia.  - `hasAgriProductTypeParent`: Riferimento al tipo di prodotto padre, cioè immediatamente sopra l'entità nella gerarchia.  - `id`: Identificatore univoco dell'entità  - `name`: Il nome di questo elemento.  - `owner`: Un elenco contenente una sequenza di caratteri codificata JSON che fa riferimento agli ID univoci dei proprietari.  - `relatedSource`: Elenco di ID che l'entità corrente può avere in applicazioni esterne.  - `root`: Indicatore logico che questo prodotto è la radice di una gerarchia di AgriProductType. Il valore logico true indica che si tratta della radice.  - `seeAlso`: elenco di uri che puntano a risorse aggiuntive sull'elemento  - `source`: Una sequenza di caratteri che indica la fonte originale dei dati dell'entità come URL. Si consiglia di utilizzare il nome di dominio completamente qualificato del provider di origine o l'URL dell'oggetto di origine.  - `type`: Tipo di entità NGSI: Deve essere AgriProductType    
Proprietà richieste  
- `id`  - `name`  - `root`  - `type`    
Questa entità è associata principalmente al settore agricolo verticale e alle relative applicazioni IoT. AgriProductType include una struttura gerarchica che consente di raggruppare i tipi di prodotto in modo flessibile.  
## Modello di dati descrizione delle proprietà  
Ordinati in ordine alfabetico (clicca per i dettagli)  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
AgriProductType:    
  description: 'This entity contains a harmonised description of a generic agricultural product type. This entity is primarily associated with the agricultural vertical and related IoT applications. The AgriProductType includes a hierarchical structure that allows product types to be grouped in a flexible way.'    
  properties:    
    agroVocConcept:    
      description: 'Reference to the agrovoc term associated with this item'    
      format: uri    
      type: string    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Relationship    
    alternateName:    
      description: 'An alternative name for this item'    
      type: string    
      x-ngsi:    
        type: Property    
    category:    
      description: 'Category of the product. Enum:''fertiliser, cropNutrition, cropProtection, cropVariety, harvestCommodity''.'    
      items:    
        enum:    
          - fertiliser    
          - cropNutrition    
          - cropProtection    
          - cropVariety    
          - harvestCommodity    
        type: string    
      type: array    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Property    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: string    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    description:    
      description: 'A description of this item'    
      type: string    
      x-ngsi:    
        type: Property    
    hasAgriProductTypeChildren:    
      description: 'Reference to child product types i.e. immediately below this entity in the hierarchy'    
      items:    
        - anyOf: &agriproducttype_-_properties_-_id_-_anyof    
            - description: 'Property. Identifier format of any NGSI entity'    
              maxLength: 256    
              minLength: 1    
              pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
              type: string    
            - description: 'Property. Identifier format of any NGSI entity'    
              format: uri    
              type: string    
          description: 'Property. Unique identifier of the entity'    
      type: array    
      x-ngsi:    
        type: Relationship    
    hasAgriProductTypeParent:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Reference to the parent product type i.e. immediately above the entity in the hierarchy.'    
      x-ngsi:    
        type: Relationship    
    id:    
      anyOf: *agriproducttype_-_properties_-_id_-_anyof    
      description: 'Unique identifier of the entity'    
      x-ngsi:    
        type: Property    
    name:    
      description: 'The name of this item.'    
      type: string    
      x-ngsi:    
        type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *agriproducttype_-_properties_-_id_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: array    
      x-ngsi:    
        type: Property    
    relatedSource:    
      description: 'List of IDs the current entity may have in external applications'    
      items:    
        - type: object    
          values:    
            application:    
              anyOf: *agriproducttype_-_properties_-_id_-_anyof    
              description: 'Property. Unique identifier of the entity'    
            applicationEntityId:    
              type: string    
      type: array    
      x-ngsi:    
        type: Property    
    root:    
      description: 'A logical indicator that this product is the root of an AgriProductType hierarchy. Logical true indicates it is the root.'    
      type: boolean    
      x-ngsi:    
        type: Property    
    seeAlso:    
      description: 'list of uri pointing to additional resources about the item'    
      oneOf:    
        - items:    
            format: uri    
            type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      x-ngsi:    
        type: Property    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: 'NGSI Entity Type: It has to be AgriProductType'    
      enum:    
        - AgriProductType    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - name    
    - root    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2021 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.Agrifood/blob/master/AgriProductType/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.Agrifood/AgriProductType/schema.json    
  x-model-tags: ""    
  x-version: 0.0.1    
```  
</details>    
## Esempi di payload  
#### Valori chiave di AgriProductType NGSI-v2 Esempio  
Ecco un esempio di AgriProductType in formato JSON-LD come valori-chiave. Questo è compatibile con NGSI-v2 quando si usa `options=keyValues` e restituisce i dati di contesto di una singola entità.  
```json  
{  
  "id": "urn:ngsi-ld:AgriProductType:398aa5f4-6a81-4dea-9f85-e9869441a257",  
  "type": "AgriProductType",  
  "dateCreated": "2017-01-01T01:20:00Z",  
  "dateModified": "2017-05-04T12:30:00Z",  
  "name": "Soft Fruits",  
  "description": "Soft edible fruits",  
  "relatedSource": [  
    {  
      "application": "urn:ngsi-ld:AgriApp:72d9fb43-53f8-4ec8-a33c-fa931360259a",  
      "applicationEntityId": "app:product1"  
    }  
  ],  
  "agroVocConcept": "http://aims.fao.org/aos/agrovoc/c_3128",  
  "category": ["cropVariety"],  
  "root": true,  
  "hasAgriProductTypeParent": "urn:ngsi-ld:AgriProductType:b99c940d-7156-4280-9a2b-4a9e533cd20e",  
  "hasAgriProductTypeChildren": [  
    "urn:ngsi-ld:AgriProductType:836258d0-448b-11e8-84ec-ef61d9425fe8",  
    "urn:ngsi-ld:AgriProductType:83d607f8-448b-11e8-9fe3-0fd5140ae8db",  
    "urn:ngsi-ld:AgriProductType:90cbac88-448b-11e8-acb0-a78dab9d0555"  
  ]  
}  
```  
#### AgriProductType NGSI-v2 normalizzato Esempio  
Ecco un esempio di AgriProductType in formato JSON-LD normalizzato. Questo è compatibile con NGSI-v2 quando non si utilizzano opzioni e restituisce i dati di contesto di una singola entità.  
```json  
{  
  "id": "urn:ngsi-ld:AgriProductType:398aa5f4-6a81-4dea-9f85-e9869441a257",  
  "type": "AgriProductType",  
  "dateCreated": {  
    "type": "DateTime",  
    "value": "2017-01-01T01:20:00Z"  
  },  
  "dateModified": {  
    "type": "DateTime",  
    "value": "2017-05-04T12:30:00Z"  
  },  
  "name": {  
    "value": "Soft Fruits"  
  },  
  "description": {  
    "value": "Soft edible fruits"  
  },  
  "relatedSource": {  
    "value": [  
      {  
        "application": "urn:ngsi-ld:AgriApp:72d9fb43-53f8-4ec8-a33c-fa931360259a",  
        "applicationEntityId": "app:product1"  
      }  
    ]  
  },  
  "agroVocConcept": {  
    "type": "URL",  
    "value": "http://aims.fao.org/aos/agrovoc/c_3128"  
  },  
  "category": {  
    "value": ["cropVariety"]  
  },  
  "root": {  
    "value": true  
  },  
  "hasAgriProductTypeParent": {  
    "type": "Relationship",  
    "value": "urn:ngsi-ld:AgriProductType:b99c940d-7156-4280-9a2b-4a9e533cd20e"  
  },  
  "hasAgriProductTypeChildren": {  
    "type": "Relationship",  
    "value": [  
      "urn:ngsi-ld:AgriProductType:836258d0-448b-11e8-84ec-ef61d9425fe8",  
      "urn:ngsi-ld:AgriProductType:83d607f8-448b-11e8-9fe3-0fd5140ae8db",  
      "urn:ngsi-ld:AgriProductType:90cbac88-448b-11e8-acb0-a78dab9d0555"  
    ]  
  }  
}  
```  
#### AgriProductType Valori chiave NGSI-LD Esempio  
Ecco un esempio di AgriProductType in formato JSON-LD come valori-chiave. Questo è compatibile con NGSI-LD quando si usa `options=keyValues` e restituisce i dati di contesto di una singola entità.  
```json  
{  
    "id": "urn:ngsi-ld:AgriProductType:398aa5f4-6a81-4dea-9f85-e9869441a257",  
    "type": "AgriProductType",  
    "agroVocConcept": "http://aims.fao.org/aos/agrovoc/c_3128",  
    "category": [  
        "cropVariety"  
    ],  
    "createdAt": "2017-01-01T01:20:00Z",  
    "description": "Soft edible fruits",  
    "hasAgriProductTypeChildren": [  
        "urn:ngsi-ld:AgriProductType:836258d0-448b-11e8-84ec-ef61d9425fe8",  
        "urn:ngsi-ld:AgriProductType:83d607f8-448b-11e8-9fe3-0fd5140ae8db",  
        "urn:ngsi-ld:AgriProductType:90cbac88-448b-11e8-acb0-a78dab9d0555"  
    ],  
    "hasAgriProductTypeParent": "urn:ngsi-ld:AgriProductType:b99c940d-7156-4280-9a2b-4a9e533cd20e",  
    "modifiedAt": "2017-05-04T12:30:00Z",  
    "name": "Soft Fruits",  
    "relatedSource": [  
        {  
            "application": "urn:ngsi-ld:AgriApp:72d9fb43-53f8-4ec8-a33c-fa931360259a",  
            "applicationEntityId": "app:product1"  
        }  
    ],  
    "root": true,  
    "@context": [  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld",  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.Agrifood/master/context.jsonld"  
    ]  
}  
```  
#### AgriProductType NGSI-LD normalizzato Esempio  
Ecco un esempio di AgriProductType in formato JSON-LD normalizzato. Questo è compatibile con NGSI-LD quando non si utilizzano opzioni e restituisce i dati di contesto di una singola entità.  
```json  
{  
    "id": "urn:ngsi-ld:AgriProductType:398aa5f4-6a81-4dea-9f85-e9869441a257",  
    "type": "AgriProductType",  
    "agroVocConcept": {  
        "type": "Property",  
        "value": "http://aims.fao.org/aos/agrovoc/c_3128"  
    },  
    "category": {  
        "type": "Property",  
        "value": [  
            "cropVariety"  
        ]  
    },  
    "createdAt": "2017-01-01T01:20:00Z",  
    "description": {  
        "type": "Property",  
        "value": "Soft edible fruits"  
    },  
    "hasAgriProductTypeChildren": {  
        "type": "Relationship",  
        "object": [  
            "urn:ngsi-ld:AgriProductType:836258d0-448b-11e8-84ec-ef61d9425fe8",  
            "urn:ngsi-ld:AgriProductType:83d607f8-448b-11e8-9fe3-0fd5140ae8db",  
            "urn:ngsi-ld:AgriProductType:90cbac88-448b-11e8-acb0-a78dab9d0555"  
        ]  
    },  
    "hasAgriProductTypeParent": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:AgriProductType:b99c940d-7156-4280-9a2b-4a9e533cd20e"  
    },  
    "modifiedAt": "2017-05-04T12:30:00Z",  
    "name": {  
        "type": "Property",  
        "value": "Soft Fruits"  
    },  
    "relatedSource": {  
        "type": "Property",  
        "value": [  
            {  
                "application": "urn:ngsi-ld:AgriApp:72d9fb43-53f8-4ec8-a33c-fa931360259a",  
                "applicationEntityId": "app:product1"  
            }  
        ]  
    },  
    "root": {  
        "type": "Property",  
        "value": true  
    },  
    "@context": [  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"  
    ]  
}  
```  
Vedere [FAQ 10](https://smartdatamodels.org/index.php/faqs/) per ottenere una risposta su come gestire le unità di grandezza.  

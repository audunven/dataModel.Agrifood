[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entità: AgriCrop  
================  
[Licenza aperta](https://github.com/smart-data-models//dataModel.Agrifood/blob/master/AgriCrop/LICENSE.md)  
[documento generato automaticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
Descrizione globale: **Questa entità contiene una descrizione armonizzata di una coltura generica. Questa entità è principalmente associata alla verticale agricola e alle relative applicazioni IoT.**  
versione: 0.0.1  

## Elenco delle proprietà  

- `agroVocConcept`: Il collegamento con il concetto definito nel vocabolario AgroVoc  - `alternateName`: Un nome alternativo per questa voce  - `dataProvider`: Una sequenza di caratteri che identifica il fornitore dell'entità di dati armonizzata.  - `dateCreated`: Timestamp di creazione dell'entità. Di solito viene assegnato dalla piattaforma di archiviazione.  - `dateModified`: Timestamp dell'ultima modifica dell'entità. Di solito viene assegnato dalla piattaforma di archiviazione.  - `description`: Descrizione dell'articolo  - `harvestingInterval`: Un elenco delle date degli intervalli di raccolta raccomandati per questa coltura. Specificato utilizzando gli intervalli di date ripetute ISO8601: <br/><br/>**intervallo, descrizione**<br/><br/>dove **intervallo** è sotto forma di **data iniziale/data finale**<br/><br/>--MM-GG/--MM-GG<br/><br/>Significa ripetere ogni anno da questa data iniziale a questa data finale.  - `hasAgriFertiliser`: Riferimento ai tipi di fertilizzanti consigliati per la coltivazione di questa coltura.  - `hasAgriPest`: Riferimento ai parassiti noti per attaccare questa coltura  - `hasAgriSoil`: Riferimento ai tipi di terreno consigliati per la coltivazione di questa coltura.  - `id`: Identificatore univoco dell'entità  - `name`: Il nome di questo elemento.  - `owner`: Un elenco contenente una sequenza di caratteri codificata JSON che fa riferimento agli ID univoci dei proprietari.  - `plantingFrom`: Un elenco delle date di intervallo di semina raccomandate per questa coltura. Specificato utilizzando gli intervalli di date ripetute ISO8601: <br/><br/>**intervallo, descrizione**<br/><br/>dove **intervallo** è sotto forma di **data iniziale/data finale**<br/><br/>--MM-GG/--MM-GG<br/><br/>Significa ripetere ogni anno da questa data iniziale a questa data finale.  - `relatedSource`: Elenco di ID che l'entità corrente può avere in applicazioni esterne.  - `seeAlso`: elenco di uri che puntano a risorse aggiuntive sull'elemento  - `source`: Una sequenza di caratteri che indica la fonte originale dei dati dell'entità come URL. Si consiglia di utilizzare il nome di dominio completamente qualificato del provider di origine o l'URL dell'oggetto di origine.  - `type`: Tipo di entità NGSI. deve essere AgriCrop.  - `wateringFrequency`: Una descrizione del programma di irrigazione consigliato. Una scelta da un elenco enumerativo. Una delle seguenti opzioni: **giornaliero, settimanale, bisettimanale, mensile, su richiesta, altro**. Enum:'giornaliero, settimanale, bisettimanale, mensile, su richiesta, altro'.    
Proprietà richieste  
- `id`  - `name`  - `type`    
Questa entità è principalmente associata al settore agricolo verticale e alle relative applicazioni IoT.  
## Modello di dati descrizione delle proprietà  
Ordinati in ordine alfabetico (clicca per i dettagli)  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
AgriCrop:    
  description: 'This entity contains a harmonised description of a generic crop. This entity is primarily associated with the agricultural vertical and related IoT applications.'    
  properties:    
    agroVocConcept:    
      description: 'The link with the defined concept into the AgroVoc vocabulary'    
      format: uri    
      type: string    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Property    
    alternateName:    
      description: 'An alternative name for this item'    
      type: string    
      x-ngsi:    
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
    harvestingInterval:    
      description: 'A list of the recommended harvesting interval date(s) for this crop. Specified using ISO8601 repeating date intervals: <br/><br/>**interval, description**<br/><br/>Where **interval** is in the form of **start date/end date**<br/><br/>--MM-DD/--MM-DD<br/><br/>Meaning repeat each year from this start date to this end date.'    
      items:    
        - type: object    
          values:    
            dateRange:    
              pattern: ^-[0-1][0-9]-[0-3][0-9]/-[0-1][0-9]-[0-3][0-9]$    
              type: string    
            description:    
              type: string    
      maxItems: 2    
      minItems: 2    
      type: array    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Property    
    hasAgriFertiliser:    
      description: 'Reference to the recommended types of fertiliser suitable for growing this crop.'    
      items:    
        - anyOf:    
            - description: 'Property. Identifier format of any NGSI entity'    
              maxLength: 256    
              minLength: 1    
              pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
              type: string    
            - description: 'Property. Identifier format of any NGSI entity'    
              format: uri    
              type: string    
      type: array    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Relationship    
    hasAgriPest:    
      description: 'Reference to the pests known to attack this crop'    
      items:    
        anyOf:    
          - description: 'Property. Identifier format of any NGSI entity'    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
          - description: 'Property. Identifier format of any NGSI entity'    
            format: uri    
            type: string    
      type: array    
      x-ngsi:    
        model: https://schema.org/URL    
        type: Relationship    
    hasAgriSoil:    
      description: 'Reference to the recommended types of soil suitable for growing this crop.'    
      items:    
        anyOf:    
          - description: 'Property. Identifier format of any NGSI entity'    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
          - description: 'Property. Identifier format of any NGSI entity'    
            format: uri    
            type: string    
      type: array    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Relationship    
    id:    
      anyOf: &agricrop_-_properties_-_owner_-_items_-_anyof    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
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
        anyOf: *agricrop_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: array    
      x-ngsi:    
        type: Property    
    plantingFrom:    
      description: 'A list of the recommended planting interval date(s) for this crop. Specified using ISO8601 repeating date intervals: <br/><br/>**interval, description**<br/><br/>Where **interval** is in the form of **start date/end date**<br/><br/>--MM-DD/--MM-DD<br/><br/>Meaning repeat each year from this start date to this end date.'    
      items:    
        - type: object    
          values:    
            dateRange:    
              pattern: ^-[0-1][0-9]-[0-3][0-9]/-[0-1][0-9]-[0-3][0-9]$    
              type: string    
            description:    
              type: string    
      maxItems: 2    
      minItems: 2    
      type: array    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Property    
    relatedSource:    
      description: 'List of IDs the current entity may have in external applications'    
      items:    
        - type: object    
          values:    
            application:    
              anyOf: *agricrop_-_properties_-_owner_-_items_-_anyof    
              description: 'Property. Unique identifier of the entity'    
            applicationEntityId:    
              type: string    
      type: array    
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
      description: 'NGSI Entity Type. it has to be AgriCrop'    
      enum:    
        - AgriCrop    
      type: string    
      x-ngsi:    
        type: Property    
    wateringFrequency:    
      description: 'A description of the recommended watering schedule. A choice from an enumerated list. One of: **daily, weekly, biweekly, monthly, onDemand, other**. Enum:''daily, weekly, biweekly, monthly, onDemand,    other'''    
      enum:    
        - daily    
        - weekly    
        - biweekly    
        - monthly    
        - onDemand    
        - other    
      type: string    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Property    
        units: ""    
  required:    
    - id    
    - type    
    - name    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2021 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.Agrifood/blob/master/AgriCrop/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.Agrifood/AgriCrop/schema.json    
  x-model-tags: ""    
  x-version: 0.0.1    
```  
</details>    
## Esempi di payload  
#### Valori-chiave di AgriCrop NGSI-v2 Esempio  
Ecco un esempio di AgriCrop in formato JSON-LD come valori-chiave. Questo è compatibile con NGSI-v2 quando si usa `options=keyValues` e restituisce i dati di contesto di una singola entità.  
```json  
{  
  "id": "urn:ngsi-ld:AgriCrop:df72dc57-1eb9-42a3-88a9-8647ecc954b4",  
  "type": "AgriCrop",  
  "dateCreated": "2017-01-01T01:20:00Z",  
  "dateModified": "2017-05-04T12:30:00Z",  
  "name": "Wheat",  
  "alternateName": "Triticum aestivum",  
  "agroVocConcept": "http://aims.fao.org/aos/agrovoc/c_7951",  
  "seeAlso": [  
    "https://example.org/concept/wheat",  
    "https://datamodel.org/example/wheat"  
  ],  
  "description": "Spring wheat",  
  "relatedSource": [  
    {  
      "application": "urn:ngsi-ld:AgriApp:72d9fb43-53f8-4ec8-a33c-fa931360259a",  
      "applicationEntityId": "app:weat"  
    }  
  ],  
  "hasAgriSoil": [  
    "urn:ngsi-ld:AgriSoil:00411b56-bd1b-4551-96e0-a6e7fde9c840",  
    "urn:ngsi-ld:AgriSoil:e8a8389a-edf5-4345-8d2c-b98ac1ce8e2a"  
  ],  
  "hasAgriFertiliser": [  
    "urn:ngsi-ld:AgriFertiliser:1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",  
    "urn:ngsi-ld:AgriFertiliser:380973c8-4d3b-4723-a899-0c0c5cc63e7e"  
  ],  
  "hasAgriPest": [  
    "urn:ngsi-ld:AgriPest:1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",  
    "urn:ngsi-ld:AgriPest:380973c8-4d3b-4723-a899-0c0c5cc63e7e"  
  ],  
  "plantingFrom": [  
    {  
      "dateRange": "-09-28/-10-12",  
      "description": "Best Season"  
    },  
    {  
      "dateRange": "-10-11/-10-18",  
      "description": "Season OK"  
    }  
  ],  
  "harvestingInterval": [  
    {  
      "dateRange": "-03-21/-04-01",  
      "description": "Best Season"  
    },  
    {  
      "dateRange": "-04-02/-04-15",  
      "description": "Season OK"  
    }  
  ],  
  "wateringFrequency": "daily"  
}  
```  
#### AgriCrop NGSI-v2 normalizzato Esempio  
Ecco un esempio di AgriCrop in formato JSON-LD normalizzato. Questo è compatibile con NGSI-v2 quando non si utilizzano le opzioni e restituisce i dati di contesto di una singola entità.  
```json  
{  
  "id": "urn:ngsi-ld:AgriCrop:df72dc57-1eb9-42a3-88a9-8647ecc954b4",  
  "type": "AgriCrop",  
  "dateCreated": {  
    "type": "DateTime",  
    "value": "2017-01-01T01:20:00Z"  
  },  
  "dateModified": {  
    "type": "DateTime",  
    "value": "2017-05-04T12:30:00Z"  
  },  
  "name": {  
    "value": "Wheat"  
  },  
  "alternateName": {  
    "value": "Triticum aestivum"  
  },  
  "agroVocConcept": {  
    "type": "URL",  
    "value": "http://aims.fao.org/aos/agrovoc/c_7951"  
  },  
  "seeAlso": {  
    "value": [  
      "https://example.org/concept/wheat",  
      "https://datamodel.org/example/wheat"  
    ]  
  },  
  "description": {  
    "value": "Spring wheat"  
  },  
  "relatedSource": {  
    "value": [  
      {  
        "application": "urn:ngsi-ld:AgriApp:72d9fb43-53f8-4ec8-a33c-fa931360259a",  
        "applicationEntityId": "app:weat"  
      }  
    ]  
  },  
  "hasAgriSoil": {  
    "type": "Relationship",  
    "value": [  
      "urn:ngsi-ld:AgriSoil:00411b56-bd1b-4551-96e0-a6e7fde9c840",  
      "urn:ngsi-ld:AgriSoil:e8a8389a-edf5-4345-8d2c-b98ac1ce8e2a"  
    ]  
  },  
  "hasAgriFertiliser": {  
    "type": "Relationship",  
    "value": [  
      "urn:ngsi-ld:AgriFertiliser:1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",  
      "urn:ngsi-ld:AgriFertiliser:380973c8-4d3b-4723-a899-0c0c5cc63e7e"  
    ]  
  },  
  "hasAgriPest": {  
    "type": "Relationship",  
    "value": [  
      "urn:ngsi-ld:AgriPest:1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",  
      "urn:ngsi-ld:AgriPest:380973c8-4d3b-4723-a899-0c0c5cc63e7e"  
    ]  
  },  
  "plantingFrom": {  
    "value": [  
      {  
        "dateRange": "-09-28/-10-12",  
        "description": "Best Season"  
      },  
      {  
        "dateRange": "-10-11/-10-18",  
        "description": "Season OK"  
      }  
    ]  
  },  
  "harvestingInterval": {  
    "value": [  
      {  
        "dateRange": "-03-21/-04-01",  
        "description": "Best Season"  
      },  
      {  
        "dateRange": "-04-02/-04-15",  
        "description": "Season OK"  
      }  
    ]  
  },  
  "wateringFrequency": {  
    "value": "daily"  
  }  
}  
```  
#### Valori chiave NGSI-LD di AgriCrop Esempio  
Ecco un esempio di AgriCrop in formato JSON-LD come valori-chiave. Questo è compatibile con NGSI-LD quando si usa `options=keyValues` e restituisce i dati di contesto di una singola entità.  
```json  
{  
    "id": "urn:ngsi-ld:AgriCrop:df72dc57-1eb9-42a3-88a9-8647ecc954b4",  
    "type": "AgriCrop",  
    "agroVocConcept": {  
        "type": "Property",  
        "value": "http://aims.fao.org/aos/agrovoc/c_7951"  
    },  
    "alternateName": {  
        "type": "Property",  
        "value": "Triticum aestivum"  
    },  
    "createdAt": "2017-01-01T01:20:00Z",  
    "description": {  
        "type": "Property",  
        "value": "Spring wheat"  
    },  
    "harvestingInterval": {  
        "type": "Property",  
        "value": [  
            {  
                "dateRange": "-03-21/-04-01",  
                "description": "Best Season"  
            },  
            {  
                "dateRange": "-04-02/-04-15",  
                "description": "Season OK"  
            }  
        ]  
    },  
    "hasAgriFertiliser": {  
        "type": "Relationship",  
        "object": [  
            "urn:ngsi-ld:AgriFertiliser:1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",  
            "urn:ngsi-ld:AgriFertiliser:380973c8-4d3b-4723-a899-0c0c5cc63e7e"  
        ]  
    },  
    "hasAgriPest": {  
        "type": "Relationship",  
        "object": [  
            "urn:ngsi-ld:AgriPest:1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",  
            "urn:ngsi-ld:AgriPest:380973c8-4d3b-4723-a899-0c0c5cc63e7e"  
        ]  
    },  
    "hasAgriSoil": {  
        "type": "Relationship",  
        "object": [  
            "urn:ngsi-ld:AgriSoil:00411b56-bd1b-4551-96e0-a6e7fde9c840",  
            "urn:ngsi-ld:AgriSoil:e8a8389a-edf5-4345-8d2c-b98ac1ce8e2a"  
        ]  
    },  
    "modifiedAt": "2017-05-04T12:30:00Z",  
    "name": {  
        "type": "Property",  
        "value": "Wheat"  
    },  
    "plantingFrom": {  
        "type": "Property",  
        "value": [  
            {  
                "dateRange": "-09-28/-10-12",  
                "description": "Best Season"  
            },  
            {  
                "dateRange": "-10-11/-10-18",  
                "description": "Season OK"  
            }  
        ]  
    },  
    "relatedSource": {  
        "type": "Property",  
        "value": [  
            {  
                "application": "urn:ngsi-ld:AgriApp:72d9fb43-53f8-4ec8-a33c-fa931360259a",  
                "applicationEntityId": "app:weat"  
            }  
        ]  
    },  
    "seeAlso": {  
        "type": "Property",  
        "value": [  
            "https://example.org/concept/wheat",  
            "https://datamodel.org/example/wheat"  
        ]  
    },  
    "wateringFrequency": {  
        "type": "Property",  
        "value": "daily"  
    },  
    "@context": [  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld",  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.Agrifood/master/context.jsonld"  
    ]  
}  
```  
#### AgriCrop NGSI-LD normalizzato Esempio  
Ecco un esempio di AgriCrop in formato JSON-LD normalizzato. Questo è compatibile con NGSI-LD quando non si utilizzano opzioni e restituisce i dati di contesto di una singola entità.  
```json  
{  
    "id": "urn:ngsi-ld:AgriCrop:df72dc57-1eb9-42a3-88a9-8647ecc954b4",  
    "type": "AgriCrop",  
    "agroVocConcept": "http://aims.fao.org/aos/agrovoc/c_7951",  
    "alternateName": "Triticum aestivum",  
    "createdAt": "2017-01-01T01:20:00Z",  
    "description": "Spring wheat",  
    "harvestingInterval": [  
        {  
            "dateRange": "-03-21/-04-01",  
            "description": "Best Season"  
        },  
        {  
            "dateRange": "-04-02/-04-15",  
            "description": "Season OK"  
        }  
    ],  
    "hasAgriFertiliser": [  
        "urn:ngsi-ld:AgriFertiliser:1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",  
        "urn:ngsi-ld:AgriFertiliser:380973c8-4d3b-4723-a899-0c0c5cc63e7e"  
    ],  
    "hasAgriPest": [  
        "urn:ngsi-ld:AgriPest:1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",  
        "urn:ngsi-ld:AgriPest:380973c8-4d3b-4723-a899-0c0c5cc63e7e"  
    ],  
    "hasAgriSoil": [  
        "urn:ngsi-ld:AgriSoil:00411b56-bd1b-4551-96e0-a6e7fde9c840",  
        "urn:ngsi-ld:AgriSoil:e8a8389a-edf5-4345-8d2c-b98ac1ce8e2a"  
    ],  
    "modifiedAt": "2017-05-04T12:30:00Z",  
    "name": "Wheat",  
    "plantingFrom": [  
        {  
            "dateRange": "-09-28/-10-12",  
            "description": "Best Season"  
        },  
        {  
            "dateRange": "-10-11/-10-18",  
            "description": "Season OK"  
        }  
    ],  
    "relatedSource": [  
        {  
            "application": "urn:ngsi-ld:AgriApp:72d9fb43-53f8-4ec8-a33c-fa931360259a",  
            "applicationEntityId": "app:weat"  
        }  
    ],  
    "seeAlso": [  
        "https://example.org/concept/wheat",  
        "https://datamodel.org/example/wheat"  
    ],  
    "wateringFrequency": "daily",  
    "@context": [  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"  
    ]  
}  
```  
Vedere [FAQ 10](https://smartdatamodels.org/index.php/faqs/) per ottenere una risposta su come gestire le unità di grandezza.  

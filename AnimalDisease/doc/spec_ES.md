[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entidad: AnimalDiseño  
=====================  
[Licencia abierta](https://github.com/smart-data-models//dataModel.Agrifood/blob/master/AnimalDisease/LICENSE.md)  
[documento generado automáticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
Descripción global: **Objeto que modela una enfermedad animal para una explotación ganadera.**  
versión: 0.0.1  

## Lista de propiedades  

- `address`: La dirección postal  - `alternateName`: Un nombre alternativo para este artículo  - `animals`: Animales o lista de animales diagnosticados con la enfermedad. Modelo https://github.com/smart-data-models/dataModel.Agrifood/blob/master/Animal/schema.json  - `areaServed`: La zona geográfica en la que se presta un servicio o se ofrece un artículo  - `dataProvider`: Una secuencia de caracteres que identifica al proveedor de la entidad de datos armonizada.  - `date`: Fecha del diagnóstico de la enfermedad por un veterinario.  - `dateCreated`: Marca de tiempo de creación de la entidad. Suele ser asignada por la plataforma de almacenamiento.  - `dateModified`: Marca de tiempo de la última modificación de la entidad. Normalmente será asignada por la plataforma de almacenamiento.  - `description`: Una descripción de este artículo  - `diagnosticTest`: Prueba de diagnóstico realizada en los animales para la determinación de la enfermedad por un veterinario.  - `disease`: Enfermedad del animal. Indica la enfermedad que tiene el animal diagnosticada por un veterinario. Fuente española de enfermedades https://www.mapa.gob.es/es/ganaderia/temas/sanidad-animal-higiene-ganadera/sanidad-animal/enfermedades/  - `id`: Identificador único de la entidad  - `location`: Referencia Geojson al elemento. Puede ser Point, LineString, Polygon, MultiPoint, MultiLineString o MultiPolygon  - `name`: El nombre de este artículo.  - `owner`: Una lista que contiene una secuencia de caracteres codificada en JSON que hace referencia a los identificadores únicos de los propietarios  - `seeAlso`: lista de uri que apuntan a recursos adicionales sobre el artículo  - `source`: Una secuencia de caracteres que indica la fuente original de los datos de la entidad en forma de URL. Se recomienda que sea el nombre de dominio completo del proveedor de origen o la URL del objeto de origen.  - `type`: Tipo de entidad NGSI. Tiene que ser AnimalDisease  - `veterinarian`: Veterinario de diagnóstico. Relación con el veterinario prescriptor  - `veterinarianTreatment`: Tratamiento médico diagnosticado por el veterinario para tratar la enfermedad. https://github.com/smart-data-models/dataModel.Agrifood/blob/master/VeterinarianTreatment/schema.json    
Propiedades requeridas  
- `disease`  - `id`  - `type`  ## Descripción del modelo de datos de las propiedades  
Ordenados alfabéticamente (haga clic para ver los detalles)  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
AnimalDisease:    
  description: 'Object modelling an animal disease for a livestock farm.'    
  properties:    
    address:    
      description: 'The mailing address'    
      properties:    
        addressCountry:    
          description: 'Property. The country. For example, Spain. Model:''https://schema.org/addressCountry'''    
          type: string    
        addressLocality:    
          description: 'Property. The locality in which the street address is, and which is in the region. Model:''https://schema.org/addressLocality'''    
          type: string    
        addressRegion:    
          description: 'Property. The region in which the locality is, and which is in the country. Model:''https://schema.org/addressRegion'''    
          type: string    
        postOfficeBoxNumber:    
          description: 'Property. The post office box number for PO box addresses. For example, 03578. Model:''https://schema.org/postOfficeBoxNumber'''    
          type: string    
        postalCode:    
          description: 'Property. The postal code. For example, 24004. Model:''https://schema.org/https://schema.org/postalCode'''    
          type: string    
        streetAddress:    
          description: 'Property. The street address. Model:''https://schema.org/streetAddress'''    
          type: string    
      type: object    
      x-ngsi:    
        model: https://schema.org/address    
        type: Property    
    alternateName:    
      description: 'An alternative name for this item'    
      type: string    
      x-ngsi:    
        type: Property    
    animals:    
      description: 'Animals or list of animals diagnosed with the disease. Model https://github.com/smart-data-models/dataModel.Agrifood/blob/master/Animal/schema.json'    
      items:    
        format: uri    
        type: string    
      type: array    
      x-ngsi:    
        type: Relationship    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided'    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: string    
      x-ngsi:    
        type: Property    
    date:    
      description: 'Date of diagnosis of the disease by a veterinarian.'    
      format: date-time    
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
    diagnosticTest:    
      description: 'Diagnostic test performed in the animals for the determination of the disease by a veterinarian.'    
      type: string    
      x-ngsi:    
        type: Property    
    disease:    
      description: 'Animal disease. Indicates the disease the animal has as diagnosed by a veterinarian. Spanish source of diseases https://www.mapa.gob.es/es/ganaderia/temas/sanidad-animal-higiene-ganadera/sanidad-animal/enfermedades/'    
      type: string    
      x-ngsi:    
        type: Property    
    id:    
      anyOf: &animaldisease_-_properties_-_owner_-_items_-_anyof    
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
    location:    
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
      oneOf:    
        - description: 'Geoproperty. Geojson reference to the item. Point'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                type: number    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - Point    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Point'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. LineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - LineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON LineString'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. Polygon'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 4    
                type: array    
              type: array    
            type:    
              enum:    
                - Polygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Polygon'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiPoint'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPoint    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPoint'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiLineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiLineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiLineString'    
          type: object    
        - description: 'Geoproperty. Geojson reference to the item. MultiLineString'    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    items:    
                      type: number    
                    minItems: 2    
                    type: array    
                  minItems: 4    
                  type: array    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPolygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPolygon'    
          type: object    
      x-ngsi:    
        type: Geoproperty    
    name:    
      description: 'The name of this item.'    
      type: string    
      x-ngsi:    
        type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *animaldisease_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
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
      description: 'NGSI entity type. It has to be AnimalDisease'    
      enum:    
        - AnimalDisease    
      type: string    
      x-ngsi:    
        type: Property    
    veterinarian:    
      description: 'Diagnostic veterinarian. Relationship to the prescribing veterinarian'    
      format: uri    
      type: string    
      x-ngsi:    
        type: Relationship    
    veterinarianTreatment:    
      description: 'Medical treatment diagnosed by the veterinarian to treat the disease. https://github.com/smart-data-models/dataModel.Agrifood/blob/master/VeterinarianTreatment/schema.json'    
      format: uri    
      type: string    
      x-ngsi:    
        type: Relationship    
  required:    
    - id    
    - type    
    - disease    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2021 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.Agrifood/blob/master/AnimalDisease/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.Agrifood/AnimalDisease/schema.json    
  x-model-tags: I4Trust    
  x-version: 0.0.1    
```  
</details>    
## Ejemplo de carga útil  
#### AnimalDisease NGSI-v2 key-values Ejemplo  
Aquí hay un ejemplo de un AnimalDisease en formato JSON-LD como valores-clave. Esto es compatible con NGSI-v2 cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
```json  
{  
  "id": "urn:ngsi-ld:AnimalDisease:ca3f1295-500c-4aa3-b745-d143097d5c01",  
  "type": "AnimalDisease",  
  "disease": "Lameness",  
  "diagnosticTest": "Visual inspection",  
  "date": "2022-01-01T01:20:00Z",  
  "animals": [  
    "urn:ngsi-ld:Animal:ca3f1295-500c-4aa3-b745-d143097d5c01",  
    "urn:ngsi-ld:Animal:bb3f1295-500c-4aa3-b745-d143097d4321"  
  ],  
  "veterinarianTreatment": "urn:ngsi-ld:VeterinarianTreatment:ca3f1295-500c-4aa3-b745-d143097d5c65",  
  "veterinarian": "urn:ngsi-ld:Veterinarian:ca3f1295-500c-4aa3-b745-d143097d5d11"  
}  
```  
#### AnimalDisease NGSI-v2 normalizado Ejemplo  
Este es un ejemplo de AnimalDisease en formato JSON-LD normalizado. Esto es compatible con NGSI-v2 cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
```json  
{  
  "id": "urn:ngsi-ld:AnimalDisease:ca3f1295-500c-4aa3-b745-d143097d5c01",  
  "type": "AnimalDisease",  
  "disease": {  
    "type": "Text",  
    "value": "Lameness"  
  },  
  "diagnosticTest": {  
    "type": "Text",  
    "value": "Visual inspection"  
  },  
  "date": {  
    "type": "Date-Time",  
    "value": "2022-01-01T01:20:00Z"  
  },  
  "animals": {  
    "type": "array",  
    "value": [  
      "urn:ngsi-ld:Animal:ca3f1295-500c-4aa3-b745-d143097d5c01",  
      "urn:ngsi-ld:Animal:bb3f1295-500c-4aa3-b745-d143097d4321"  
    ]  
  },  
  "veterinarianTreatment": {  
    "type": "Relationship",  
    "value": "urn:ngsi-ld:VeterinarianTreatment:ca3f1295-500c-4aa3-b745-d143097d5c65"  
  },  
  "veterinarian": {  
    "type": "Relationship",  
    "value": "urn:ngsi-ld:Veterinarian:ca3f1295-500c-4aa3-b745-d143097d5d11"  
  }  
}  
```  
#### AnimalDisease NGSI-LD key-values Ejemplo  
Aquí hay un ejemplo de un AnimalDisease en formato JSON-LD como valores-clave. Esto es compatible con NGSI-LD cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
```json  
{  
  "id": "urn:ngsi-ld:AnimalDisease:ca3f1295-500c-4aa3-b745-d143097d5c01",  
  "type": "AnimalDisease",  
  "disease": "Lameness",  
  "diagnosticTest": "Visual inspection",  
  "date": "2022-01-01T01:20:00Z",  
  "animals": [  
    "urn:ngsi-ld:Animal:ca3f1295-500c-4aa3-b745-d143097d5c01",  
    "urn:ngsi-ld:Animal:bb3f1295-500c-4aa3-b745-d143097d4321"  
  ],  
  "veterinarianTreatment": "urn:ngsi-ld:VeterinarianTreatment:ca3f1295-500c-4aa3-b745-d143097d5c65",  
  "veterinarian": "urn:ngsi-ld:Veterinarian:ca3f1295-500c-4aa3-b745-d143097d5d11",  
  "@context": [  
    "https://smart-data-models.github.io/dataModel.Agrifood/context.jsonld"  
  ]  
}  
```  
#### AnimalDisease NGSI-LD normalizado Ejemplo  
Este es un ejemplo de AnimalDisease en formato JSON-LD normalizado. Esto es compatible con NGSI-LD cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
```json  
{  
  "id": "urn:ngsi-ld:AnimalDisease:ca3f1295-500c-4aa3-b745-d143097d5c01",  
  "type": "AnimalDisease",  
  "disease": {  
    "type": "Property",  
    "value": "Lameness"  
  },  
  "diagnosticTest": {  
    "type": "Property",  
    "value": "Visual inspection"  
  },  
  "date": {  
    "type": "Property",  
    "value": {  
      "@type": "Date-Time",  
      "@value": "2022-01-01T01:20:00Z"  
    }  
  },  
  "animals": {  
    "type": "Property",  
    "value": [  
      "urn:ngsi-ld:Animal:ca3f1295-500c-4aa3-b745-d143097d5c01",  
      "urn:ngsi-ld:Animal:bb3f1295-500c-4aa3-b745-d143097d4321"  
    ]  
  },  
  "veterinarianTreatment": {  
    "type": "Relationship",  
    "object": "urn:ngsi-ld:VeterinarianTreatment:ca3f1295-500c-4aa3-b745-d143097d5c65"  
  },  
  "veterinarian": {  
    "type": "Relationship",  
    "object": "urn:ngsi-ld:Veterinarian:ca3f1295-500c-4aa3-b745-d143097d5d11"  
  },  
  "@context": [  
    "https://smart-data-models.github.io/dataModel.Agrifood/context.jsonld"  
  ]  
}  
```  
Consulte [FAQ 10](https://smartdatamodels.org/index.php/faqs/) para obtener una respuesta sobre cómo tratar las unidades de magnitud  

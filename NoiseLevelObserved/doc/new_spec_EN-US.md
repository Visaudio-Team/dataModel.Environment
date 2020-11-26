Entity: NoiseLevelObserved  
==========================







<details><summary><strong>full yaml details</strong></summary>    

NoiseLevelObserved:    
  description: 'An observation of those acoustic parameters that estimate noise pressure levels at a certain place and time. '    
  properties:    
    address:    
      description: 'The mailing address.'    
      properties:    
        addressCountry:    
          type: string    
        addressLocality:    
          type: string    
        addressRegion:    
          type: string    
        areaServed:    
          type: string    
        postOfficeBoxNumber:    
          type: string    
        postalCode:    
          type: string    
        streetAddress:    
          type: string    
      type: Property    
    alternateName:    
      description: 'An alternative name for this item'    
      type: Property    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided.'    
      type: Property    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    dateObserved:    
      type: string    
    dateObservedFrom:    
      format: date-time    
      type: string    
    dateObservedTo:    
      format: date-time    
      type: string    
    description:    
      description: 'A description of this item'    
      type: Property    
    id:    
      anyOf: &noiselevelobserved_-_properties_-_owner_-_items_-_anyof    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
    location:    
      $id: https://geojson.org/schema/Geometry.json    
      $schema: "http://json-schema.org/draft-07/schema#"    
      oneOf:    
        - properties:    
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
        - properties:    
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
        - properties:    
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
        - properties:    
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
        - properties:    
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
        - properties:    
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
      title: 'GeoJSON Geometry'    
    name:    
      description: 'The name of this item.'    
      type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *noiselevelobserved_-_properties_-_owner_-_items_-_anyof    
      type: Property    
    refDevice:    
      anyOf: *noiselevelobserved_-_properties_-_owner_-_items_-_anyof    
    refPointOfInterest:    
      anyOf: *noiselevelobserved_-_properties_-_owner_-_items_-_anyof    
    refWeatherObserved:    
      anyOf: *noiselevelobserved_-_properties_-_owner_-_items_-_anyof    
    seeAlso:    
      oneOf:    
        - items:    
            - format: uri    
              type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
    sonometerClass:    
      enum:    
        - 0    
        - 1    
        - 2    
      type: string    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: Property    
    type:    
      description: 'NGSI Entity type'    
      enum:    
        - NoiseLevelObserved    
      type: string    
  required:    
    - id    
    - type    
    - dateObservedFrom    
    - dateObservedTo    
    - location    
  type: object    
```  
</details>    




  "id": "Vitoria-NoiseLevelObserved-2016-12-28T11:00:00_2016-12-28T12:00:00",  
  "type": "NoiseLevelObserved",  
  "LAS": 91.6,  
  "LAeq": 67.8,  
  "LAeq_d": 65.4,  
  "LAmax": 94.5,  
  "dateObservedFrom": "2016-12-28T11:00:00.00Z",  
  "dateObservedTo": "2016-12-28T12:00:00.00Z",  
  "location": {  
    "type": "Point",  
    "coordinates": [-2.698, 42.8491]  
  }  
}  
```  




  "dateObservedFrom": {  
    "type": "DateTime",  
    "value": "2016-12-28T11:00:00.00Z"  
  },  
  "LAmax": {  
    "value": 94.5  
  },  
  "LAeq": {  
    "value": 67.8  
  },  
  "dateObservedTo": {  
    "type": "DateTime",  
    "value": "2016-12-28T12:00:00.00Z"  
  },  
  "LAeq_d": {  
    "value": 65.4  
  },  
  "location": {  
    "type": "geo:json",  
    "value": {  
      "type": "Point",  
      "coordinates": [-2.698, 42.8491]  
    }  
  },  
  "type": "NoiseLevelObserved",  
  "id": "Vitoria-NoiseLevelObserved-2016-12-28T11:00:00_2016-12-28T12:00:00",  
  "LAS": {  
    "value": 91.6  
  }  
}  
```  




              "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"],  
 "LAS": 91.6,  
 "LAeq": 67.8,  
 "LAeq_d": 65.4,  
 "LAmax": 94.5,  
 "dateObservedFrom": {"@type": "DateTime", "@value": "2016-12-28T11:00:00.00Z"},  
 "dateObservedTo": {"@type": "DateTime", "@value": "2016-12-28T12:00:00.00Z"},  
 "id": "urn:ngsi-ld:NoiseLevelObserved:Vitoria-NoiseLevelObserved-2016-12-28T11:00:00_2016-12-28T12:00:00",  
 "location": {"coordinates": [-2.698, 42.8491], "type": "Point"},  
 "type": "NoiseLevelObserved"}  
```  




    "id": "urn:ngsi-ld:NoiseLevelObserved:Vitoria-NoiseLevelObserved-2016-12-28T11:00:00_2016-12-28T12:00:00",  
    "type": "NoiseLevelObserved",  
    "dateObservedFrom": {  
        "type": "Property",  
        "value": {  
            "@type": "DateTime",  
            "@value": "2016-12-28T11:00:00.00Z"  
        }  
    },  
    "LAmax": {  
        "type": "Property",  
        "value": 94.5  
    },  
    "LAeq": {  
        "type": "Property",  
        "value": 67.8  
    },  
    "dateObservedTo": {  
        "type": "Property",  
        "value": {  
            "@type": "DateTime",  
            "@value": "2016-12-28T12:00:00.00Z"  
        }  
    },  
    "LAeq_d": {  
        "type": "Property",  
        "value": 65.4  
    },  
    "location": {  
        "type": "GeoProperty",  
        "value": {  
            "type": "Point",  
            "coordinates": [  
                -2.698,  
                42.8491  
            ]  
        }  
    },  
    "LAS": {  
        "type": "Property",  
        "value": 91.6  
    },  
    "@context": [  
        "https://schema.lab.fiware.org/ld/context",  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"  
    ]  
}  
```  
FORMAT: 1A
HOST: http://api.datasnap.io/v1.0

# Datasnap.io
Eventa API is the service to store all the events happenidng in your application.

# Events (AKA Indegestor)
Events related resources of the **Events API**

## Events Collection [/organization/${organization}/events/?api_key=${api_key}]


+ Parameters
    + api_key (required, string, `E9NZuB6A91e2J03PKA2g7wx0629czel8`) ... String `api-key` for the Datasnap account/organization (optional if you use Authorization header)
    + organization (required, number, ) ... Number `organization`    
     
### Create a Event [POST]


+ Request (application/json)
    
    + Headers

            Authorization: E9NZuB6A91e2J03PKA2g7wx0629czel8
      
    + Body
    
            {
                "event_type": "beacon_sighting" 
            
            }
        
    + Schema
    
            {
                "type": "object",
                "required": false,
                "properties": {
                    "event_type": {
                        "type": ["string", "null"],
                        "required": true
                    },
                    "id": {
                        "type": "number",
                        "required": false
                    }
                }
            }
    

    
+ Response 200 (application/json)

        { "created": true}
        
        
        
### Create a Event [GET]

This is used to perform pixel based tracking where its easier to embed into email and html <img /> tags and
harder to perform a mopre programmatic POST request. 


+ Request (application/json)


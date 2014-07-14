FORMAT: 1A
HOST: http://api.datasnap.io/v1.0

# Datasnap.io
Eventa API is the service to store all the events happenidng in your application.

# Events (AKA Indegestor)
Events related resources of the **Events API**

## Events Collection [/organization/${organization}/events/?api_key=${api_key}]

### Create a Event [POST]

+ Request (application/json)
    
    
            
    + Body
    
            {
                "event_type": "Buy cheese and bread for breakfast." 
            
            }
        
    + Schema
    
            {
                "type": "object",
                "required": false,
                "properties": {
                    "title": {
                        "type": ["string", "null"],
                        "required": false
                    },
                    "id": {
                        "type": "number",
                        "required": true
                    }
                }
            }
        
        
    + Parameters
        + api_key (required, string, `E9NZuB6A91e2J03PKA2g7wx0629czel8`) ... 
        
                String `api-key` for the Datasnap account/organization
    
        + event_type (required, string, `user_opt_in_location`) ... 
String `event_type` ... 
Other examples could>
user_opt_in_location
user_opt_in_push_notifications
user_opt_in_vendor
beacon_arrive
beacon_sigting
beacon_departed
interaction_tap
interaction_view
interaction_swipe
interaction_shake
    
+ Response 200 (application/json)

        { "created": true}

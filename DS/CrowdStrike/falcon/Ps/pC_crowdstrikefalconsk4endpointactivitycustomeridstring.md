#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-endpoint-activity-customeridstring
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"eid":""", """"CustomerIdString":""", """destinationServiceName =CrowdStrike""", """"EventType":"Event_ExternalApiEvent"""" ]
  Fields = [
     """suser=(system|({user}[^\s]+))"""
    """"EventType":"({event_name}[^"]+)""",
# eid is removed
    """"SHA256HashData":"({hash_sha256}[^"]+)""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
# cid is removed
    
    ]



}
```
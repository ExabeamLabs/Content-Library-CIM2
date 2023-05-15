#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-endpoint-activity-customeridstring
  ParserVersion = "v1.0.0"
  Conditions = [ """"eid":""", """"CustomerIdString":""", """"destinationServiceName":"CrowdStrike"""", """"EventType":"Event_ExternalApiEvent"""" ]

json-crowdstrike-endpoint-activity = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """suser=(system|({user}[^\s]+))"""
    """"EventType":"({event_name}[^"]+)""",
# eid is removed
    """"SHA256HashData":"({hash_sha256}[^"]+)""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
# cid is removed
    
}
```
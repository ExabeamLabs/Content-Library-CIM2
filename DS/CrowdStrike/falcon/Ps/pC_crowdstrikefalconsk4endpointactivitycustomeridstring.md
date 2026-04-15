#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-endpoint-activity-customeridstring
  ParserVersion = "v1.0.0"
  Conditions = [ """"eid":""", """"CustomerIdString":""", """destinationServiceName =CrowdStrike""", """"EventType":"Event_ExternalApiEvent"""" ]

json-crowdstrike-endpoint-activity = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"EventType":"({event_name}[^"]+)""",
# eid is removed
    """"SHA256HashData":"({hash_sha256}[^"]+)""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
# cid is removed
    """"cid":"({cid}[^"]+)"""",
    """"IssuerDN":"({object_dn}[^"]+)""""
    """"UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    json-crowdstrike-endpoint-activity = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"EventType":"({event_name}[^"]+)""",
# eid is removed
    """"SHA256HashData":"({hash_sha256}[^"]+)""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
# cid is removed
    """"cid":"({cid}[^"]+)"""",
    """"IssuerDN":"({object_dn}[^"]+)""""
    """"UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    ]
}
}
```
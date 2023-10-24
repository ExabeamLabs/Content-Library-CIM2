#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-identityprotection"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  Conditions = [ """"eventType":"IdentityProtectionEvent"""", """"Severity":""", """"FalconHostLink":""" ]
  TimeFormat = "epoch"
  Fields = [
    """"eventCreationTime":({time}\d{13}),""",
    """"IncidentType":"({alert_name}[^"]+)"""",
    """"eventType":"({alert_type}[^"]+)"""",
    """"Severity":({alert_severity}\d{1,5}),""",
    """"EndpointName":"({host}[^"]+)"""",
    """"UserName":"(({full_name}({first_name}[^\s"\\\/]+)\s({last_name}[^"\\\/]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((({domain}[^\\\s]+)\\)?({user}[\w\.\-]{1,40}\$?)))"""",
    """"Category":"({category}[^"]+)"""",
    """"FalconHostLink":"({falcon_host_link}[^"]+)""""    
  ]
  ParserVersion = "v1.0.0"


}
```
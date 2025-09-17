#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-identityprotection"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ExtractionType = json
  Conditions = [ """"eventType"""", """"IdentityProtectionEvent"""", """"Severity":""", """"FalconHostLink":""" ]
  TimeFormat = ["epoch", "epoch_sec"]
  Fields = [
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_json_path=$.metadata.eventType,exa_field_name=alert_type""",
    """exa_json_path=$.event.IncidentType,exa_field_name=alert_name""",
    """exa_json_path=$.event.Severity,exa_field_name=alert_severity""",
    """exa_json_path=$.event.SeverityName,exa_field_name=alert_severity""",
    """exa_json_path=$.event.EndpointName,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.event.UserName,exa_regex=(({full_name}({first_name}[^\s"\\\/]+)\s({last_name}[^"\\\/]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))("|$)""",
    """exa_regex="UserName":"(({full_name}({first_name}[^\s"\\\/]+)\s({last_name}[^"\\\/]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """exa_json_path=$.event.Category,exa_field_name=category""",
    """exa_json_path=$.event.FalconHostLink,exa_field_name=falcon_host_link"""    
    """"eventCreationTime":\s*({time}\d{10,13}),""",
    """"IncidentType":\s*"({alert_name}[^"]+)"""",
    """"eventType":\s*"({alert_type}[^"]+)"""",
    """"Severity":\s*({alert_severity}\d{1,5}),""",
    """"SeverityName":\s*({alert_severity}[^"]+),""",
    """"EndpointName":\s*"({host}[\w\-.]+)"""",
    """"UserName":\s*"(({full_name}({first_name}[^\s"\\\/]+)\s({last_name}[^"\\\/]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """"Category":\s*"({category}[^"]+)"""",
    """"FalconHostLink":\s*"({falcon_host_link}[^"]+)""""    
  ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = google-workspace-json-rule-trigger-success-ruletrigger
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"applicationName":"rules"""", """"rule_trigger"""",  """"rule_type"""", """"kind":"""", """"events":""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"profileId":"({user_id}\d+)""",
    """"resource_owner_email"[^}]+?"value":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """suser=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+[\w=]+""",
    """"actor"\s*:\s*\{[^=]*?"email"\s*:\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"data_source"[^}]+?"value":"({rule_source}[^"]+)"""",
    """"resource_id"[^}]+?"value":"({resource_id}[^"]+)"""",
    """"rule_name"[^}]+?"value":"({rule}[^"]+)"""",
    """"rule_type"[^}]+?"value":"({rule_type}[^"]+)"""",
    """"severity"[^}]+?"value":"({rule_severity}[^"]+)"""",
    """"resource_type"[^}]+?"value":"({resource_type}[^"]+)"""",
    """"rule_resource_name"[^\}]+?"value":"({resource_path}[^"]+)"""",
    """"resource_title"[^\}]+?"value":"({resource_name}[^"]+)"""",
    """"scan_type"[^\}]+?"value":"({scan_type}[^"]+)"""",
    """"multiValue":\[({recipients}[^\]]+)\][^\}]+?"resource_recipients"""",
    """"kind":"({operation}[^"]+)"""",
    """flexString1=({action}.+?)\s\w+="""
  ]
  DupFields = [ "rule_source->app" ]


}
```
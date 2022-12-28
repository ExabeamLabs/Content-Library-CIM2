#### Parser Content
```Java
{
Name = cybereason-cr-json-alert-trigger-success-affectedusers
  Vendor = Cybereason
  Product = Cybereason
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """"hasSuspicions": true""", """"hasMalops": true""", """"affectedMachines"""", """"affectedUsers"""" ]
  Fields = [
    """"creationTime":\s+"({time}\d{13})"""",
    """"detectionType":\s*"({alert_type}[^"]+)""",
    """"affectedMachines":\s*\{[^\}]+?"elementType":\s*"Machine"[^\}]+?"name":\s*"({dest_host}[^"]+)"""",
    """"affectedUsers":\s*\{[^\}]+"elementType":\s*"User"[^\}]+"name":\s*"((nt service|nt instans|({domain}[^\\"]+))\\+)?(network service|system|({user}[^"]+))"""",
    """'message':\s*'({additional_info}[^']+?)\s*'""",
    """"elementDisplayName":\s*\{[^\}]+"values":\s*\["+({additional_info}[^"]+)"""",
    """"malopActivityTypes":\s*"({threat_category}[^"]+)"""",
    """"severity":\s*"({alert_severity}[^"]+)""""
  ]
  DupFields = ["alert_type->alert_name"]


}
```
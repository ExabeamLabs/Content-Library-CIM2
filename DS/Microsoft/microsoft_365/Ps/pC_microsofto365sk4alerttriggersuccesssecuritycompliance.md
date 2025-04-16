#### Parser Content
```Java
{
Name = microsoft-o365-sk4-alert-trigger-success-securitycompliance
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""Operation":"""
""""AlertEntityGenerated""""
""""Workload":"""
"""SecurityComplianceCenter""""
""""Category":"""
""""EntityType":"""
]
Fields = [
""""CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
""""Operation":\s*"({operation}[^"]*)""""
"""requestClientApplication=({app}[^=]+)\s+(\w+=|$)"""
""""AlertEntityId":\s*"({malware_url}[^"]+)".+?Category":\s*"ThreatManagement".+?MaliciousUrl"""
""""ResultStatus":\s*"({result}[^"]+)""""
""""Category":\s*"({category}[^"]+)""""
""""AlertType":\s*"({alert_type}[^"]+)""""
""""Severity":\s*"({alert_severity}[^"]+)""""
""""Name":\s*"({alert_name}[^"]+?)(\\u200b)?""""
""""trc\\":\s*\\"({email_address}[^"\s@]+@[^"\s@\\]+)\\""""
""""AlertId":\s*"({alert_id}[^"]+)"""",
""""Source":\s*"({alert_source}[^"]+)""""
""""Category":\s*"({category}[^"]+)""""
]
ParserVersion = "v1.0.0"
DupFields = [ "alert_name->alert_subject" ]


}
```
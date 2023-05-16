#### Parser Content
```Java
{
Name = microsoft-o365-sk4-alert-trigger-success-securitycompliance
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""Operation":"AlertEntityGenerated""""
""""UserKey":"SecurityComplianceAlerts""""
"""MaliciousUrlClick"""
]
Fields = [
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
""""Operation":"({operation}[^"]*)""""
"""requestClientApplication=({app}[^=]+)\s+(\w+=|$)"""
""""AlertEntityId":"({malware_url}[^"]+)""""
""""ResultStatus":"({result}[^"]+)""""
""""Category":"({category}[^"]+)""""
""""AlertType":"({alert_type}[^"]+)""""
""""Severity":"({alert_severity}[^"]+)""""
""""Name":"({alert_name}[^"]+)""""
""""trc\\":\\"({email_address}[^"\s@]+@[^"\s@\\]+)\\""""
""""AlertId":"({alert_id}[^"]+)"""",
""""Source":"({alert_source}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```
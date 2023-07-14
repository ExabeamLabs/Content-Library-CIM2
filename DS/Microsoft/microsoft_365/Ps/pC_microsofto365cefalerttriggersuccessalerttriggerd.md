#### Parser Content
```Java
{
Name = microsoft-o365-cef-alert-trigger-success-alerttriggerd
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """AlertTriggered""", """"AlertType":""", """AlertId""", """destinationServiceName =Office 365"""]
  Fields = [
   """"(ts|CreationTime)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
   """\\?"f3u\\?":\\?"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\\?"""",
   """"ad\\?":\\?"({additional_info}[^"]+?)\\?"""",
   """"(Name|an)":"({alert_name}[^"]+)""",
   """"AlertId":"({alert_id}[^"]+)""""
   """"(sev|Severity)":"({alert_severity}[^"]+)""",
   """"AlertType":"({alert_type}[^"]+)"""",
   """requestClientApplication=({process_path}.*?)\s\w+=""",
   """"Source":"({alert_source}[^"]+)"""
  ]
  DupFields = ["process_path->process_name", "alert_name->alert_subject"]
  ParserVersion = "v1.0.0"


}
```
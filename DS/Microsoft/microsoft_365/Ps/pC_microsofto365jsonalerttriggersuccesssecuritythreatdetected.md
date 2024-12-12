#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-securitythreatdetected
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"event-name":"security-threat-detected""""
  """Severity":""""
  """"src-application-name":"Office 365""""
  """Operation"""
]
Fields = [
  """CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """Operation"*:\s*"+({operation}[^"]+)""""
  """"ObjectId":"({email_address}[^<@]+@[^",]+)",""""
  """"f3u\\?":\\?"({email_address}[^@]+@[^",]+?)\\?""""
  """"result":"({result}[^"]+)"""
  """"Category":"({category}[^"]+)"""
  """"Severity":"({alert_severity}[^"]+)"""
  """"Source":"({additional_info}[^"]+)"""
  """"Status":"({incident_status}[^"]+)"""
  """"category":"({alert_type}[^"]+)"""
  """"action":"({alert_name}[^"]+)"""
  """"src-account-name":"({account}[^"]+)"""
  """Workload":"({app}[^"]+)"""
  """"id":({alert_id}\d+)"""
]
ParserVersion = "v1.0.0"


}
```
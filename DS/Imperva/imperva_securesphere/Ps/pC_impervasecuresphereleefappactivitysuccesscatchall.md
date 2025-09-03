#### Parser Content
```Java
{
Name = imperva-securesphere-leef-app-activity-success-catchall
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """|Event Type="""
  """LEEF:"""
  """|SecureSphere|"""
]
Fields = [
  """(\s|\|)devTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """(\s|\|)Severity=({alert_severity}[^\|]+)"""
  """usrName =(({domain}[^\\|]+)(\\))?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Message=({additional_info}[^"|]+)\|"""
  """SecureSphere\|[^|]+?\|({operation}[^\|]+)\|"""
]
DupFields = [
  "operation->event_name"
]
ParserVersion = "v1.0.0"


}
```
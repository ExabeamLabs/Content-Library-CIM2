#### Parser Content
```Java
{
Name = "appsense-am-leef-alert-trigger-success-appsenseapplicationmanager"
Vendor = "AppSense"
Product = "AppSense Application Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """ LEEF """
  """AppSense Application Manager"""
  """message="""
  """application="""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[^\s]+)\s\S+\sLEEF"""
  """cat=({alert_type}[^=]+?)\s*\w+="""
  """resource=({dest_host}[^=]+?)\s*\w+="""
  """application=({app}[^=]+?)\s*\w+="""
  """message=({alert_name}[^\"]+?)\s*$"""
  """usrName =(N\/A|(({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+="""
  """LEEF\s({event_code}\d+)"""
  """sev=({alert_severity}\d+)"""
]
DupFields = [
  "dest_host->host"
]
ParserVersion = "v1.0.0"


}
```
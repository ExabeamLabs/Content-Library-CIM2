#### Parser Content
```Java
{
Name = firemon-f-json-app-activity-success-bulkupdate
 Vendor = FireMon
 Product = FireMon
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
 Conditions = [ """Event Name:""", """User Tag Bulk Update""", """ [FireMon] """ ]
 Fields = [
   """\d{1,2}:\d{1,2}:\d{1,2} ({host}[\w\-\.]+)"""
   """Date:\s*({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,6})"""
   """Event Name:\s*({event_name}[^:]+) User:\s*({user}[\w\.\-]{1,40}\$?)\s\w+:"""
   """({app}FireMon)"""
 ]
 DupFields = [ "event_name->operation" ]
 ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = firemon-f-str-app-notification-success-changesdetected
 Vendor = FireMon
 Product = FireMon
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
 Conditions = [ """Changes Detected in Revision""", """ [FireMon] """ ]
 Fields = [
   """\d{1,2}:\d{1,2}:\d{1,2} ({host}[\w\-\.]+)"""
   """({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,6})"""
   """({additional_info}\d*\s*Changes Detected in Revision)"""
 ]
 ParserVersion = "v1.0.0"


}
```
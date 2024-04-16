#### Parser Content
```Java
{
Name = firemon-f-str-app-notification-success-controlsfailed
 Vendor = FireMon
 Product = FireMon
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
 Conditions = [ """Controls Failed""", """ [FireMon] """ ]
 Fields = [
   """\d{1,2}:\d{1,2}:\d{1,2} ({host}[\w\-\.]+)"""
   """({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,6})"""
   """({additional_info}\d*\s*Controls Failed[^"]+?)\s\-\s\d\d\d\d"""
 ]
 ParserVersion = "v1.0.0"


}
```
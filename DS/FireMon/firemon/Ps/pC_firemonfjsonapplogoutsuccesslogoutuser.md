#### Parser Content
```Java
{
Name = firemon-f-json-app-logout-success-logoutuser
 Vendor = FireMon
 Product = FireMon
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
 Conditions = [ """Logout User: """, """"username":"""", """ [FireMon] """ ]
 Fields = [
   """\d{1,2}:\d{1,2}:\d{1,2} ({host}[\w\-\.]+)"""
   """Date:\s*({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,6})"""
   """Event Name:\s*({event_name}[^:]+) User:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+:"""
   """({operation}Logout)"""
   """"username":"\s*(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))""""
   """"username":"\s*(({domain}[^"\\]+)\\+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
 ]
 ParserVersion = "v1.0.0"


}
```
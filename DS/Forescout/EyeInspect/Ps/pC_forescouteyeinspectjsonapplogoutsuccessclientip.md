#### Parser Content
```Java
{
Name = forescout-eyeinspect-json-app-logout-success-clientip
  Vendor = Forescout
  Product = EyeInspect 
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"action":"Logout"""", """"resource":"Operating system Command Center"""", """"clientIP":""", """"user":"""", """"otherInfo":"""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """"user":"({user}[^",]+)"""",
    """"clientIP":"({src_ip}[A-Fa-f:\d.]+)"""",
    """"otherInfo":"({additional_info}[^",]+)"""",
    """"action":"({event_name}[^",]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```
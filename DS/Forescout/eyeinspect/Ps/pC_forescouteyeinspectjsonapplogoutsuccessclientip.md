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
    """"user":"({user}[\w\.\-]{1,40}\$?)"""",
    """"clientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"otherInfo":"({additional_info}[^",]+)"""",
    """"action":"({event_name}[^",]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```
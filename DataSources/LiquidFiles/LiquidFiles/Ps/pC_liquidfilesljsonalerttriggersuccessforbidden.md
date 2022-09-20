#### Parser Content
```Java
{
Name = liquidfiles-l-json-alert-trigger-success-forbidden
  Vendor = LiquidFiles
  Product = LiquidFiles
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """liquidfiles[""", """"message":"Blacklisted client with IP:""" ,""""status":"forbidden"""" ]
  Fields = [
      """"hostname":"({host}[^"]+)"""",
      """"ip":"({src_ip}[A-Fa-f\d:.]+)"""",
      """"message":"({event_name}[^:"]+)""",
      """({app}liquidfiles)""",
    ]


}
```
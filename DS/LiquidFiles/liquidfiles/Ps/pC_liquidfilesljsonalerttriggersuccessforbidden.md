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
      """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"message":"({event_name}[^:"]+)""",
      """({app}liquidfiles)""",
    ]


}
```
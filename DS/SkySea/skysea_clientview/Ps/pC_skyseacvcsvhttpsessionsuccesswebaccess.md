#### Parser Content
```Java
{
Name = skysea-cv-csv-http-session-success-webaccess
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [""",Webアクセス,""", """,,Webアクセス,"""]
  Fields = [
    """({host}[^,]+),(({src_ip}[A-Fa-f:\d.]+)|({src_host}[\w\-.]+)),[^,]*,({user}[^,]*),[^,]*,[^,]*,[^,]*,[^,]*,Webアクセス""",
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """,Webアクセス,[^,]*,[^,]*,(|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)?(:({dest_port}\d+))?({uri_path}\/[^,]*)?))""",
    """({action}Webアクセス)""",
  ]
  DupFields = ["action->method"]


}
```
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
    """({host}[^,]+),(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+)),[^,]*,({user}[^,]*),[^,]*,[^,]*,[^,]*,[^,]*,Webアクセス""",
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """,Webアクセス,[^,]*,[^,]*,(|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)?(:({dest_port}\d+))?({uri_path}\/[^,]*)?))""",
    """({action}Webアクセス)""",
  ]
  DupFields = ["action->method"]


}
```
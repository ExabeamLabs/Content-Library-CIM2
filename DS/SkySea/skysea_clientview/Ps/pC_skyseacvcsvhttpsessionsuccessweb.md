#### Parser Content
```Java
{
Name = "skysea-cv-csv-http-session-success-web"
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [""",Webアクセス,""", """,Web書き込み,"""]
  Fields = [
    """({host}[^,]+),(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+)),[^,]*,({user}[\w\.\-]{1,40}\$?),[^,]*,[^,]*,[^,]*,[^,]*,Webアクセス""",
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """,Webアクセス,[^,]*,[^,]*,({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)?(:({dest_port}\d+))?({uri_path}\/[^,]*)?)""",
    """Web書き込み,([^,]*,){23}({uri_query}[^,]*),""",
    """({action}Web書き込み)""",
  ]
  DupFields = ["action->method"]
  ParserVersion = "v1.0.0"


}
```
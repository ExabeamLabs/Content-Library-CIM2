#### Parser Content
```Java
{
Name = hp-arubacpm-kv-endpoint-authentication-fail-authfailed
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Authentication failed""", """method=""", """server=""", """authmgr""" ]
  Fields = [
      """({time}\d{4}-\d{2}-\d{2}T\d\d:\d\d:\d\d)\+""",
      """\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\+\d{2}:\d{2}\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\s+({host}[^\s]+)\s+authmgr\[""",
      """(authmgr|stm)\[({event_code}\d+)\]""",
      """Authentication result=({event_name}Authentication failed)""",
      """method=({auth_type}[^\,\s]+)""",
      """server=({auth_server}[\w\d]+)""",
      """user=({src_mac}[a-fA-F\d:]+)""",
   ]


}
```
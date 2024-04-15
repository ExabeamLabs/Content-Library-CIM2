#### Parser Content
```Java
{
Name = "f5-apm-json-endpoint-login-0149"
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Login":""", """"failure_reason":"""", """"auth_method":"""", """"session_id":"""", """0149""", """:5:""" ]
  Fields = [
    """>\w+ \d\d \d\d:\d\d:\d\d ({host}[\w.\-]+)""",
    """"result":"({action}[^"]+)""",
    """"user":"({user}[^"]+)""",
    """"src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"failure_reason":"({failure_reason}[^"]+)""",
    """"auth_method":"({auth_method}[^"]+)""",
    """"dst_host":"({dest_host}[^"]+)""",
    """({event_name}Login)""",
  ]
  ParserVersion = "v1.0.0"


}
```
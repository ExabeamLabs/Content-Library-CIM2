#### Parser Content
```Java
{
Name = f5-apm-str-vpn-login-success-clientip
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """:Common:""", """ client IP """, """/Common/""" ]
  Fields = [
    """:Common:({session_id}[^:]+)""",
    """\s(?i)Client IP\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """Listener \/Common\/({dest_host}({host}[\w\-\.]+))_({dest_port}\d{1,5})\s"""
  ]
  ParserVersion = "v1.0.0"


}
```
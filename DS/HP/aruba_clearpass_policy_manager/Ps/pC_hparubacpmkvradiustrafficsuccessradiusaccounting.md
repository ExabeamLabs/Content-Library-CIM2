#### Parser Content
```Java
{
Name = hp-arubacpm-kv-radius-traffic-success-radiusaccounting
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
  Conditions = [ """ Radius Accounting """, """RADIUS.Acct-Timestamp=""" ]
  Fields = [
    """RADIUS\.Acct-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\.\d+)?[\+\-]\d+)""",
    """\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({host}[\w\-.]+)""",
    """RADIUS\.Acct-Username=(?:({user_type}host)/)?(({domain}[^\\\s,]+)\\+)?(anonymous|({user}[\w\.\-]{1,40}\$?))""",
    """RADIUS\.Acct-Username=({email_address}[^\\\s,@]+@[^\\\s,@]+)""",
    """RADIUS\.Acct-Service-Name =({network}[^,]+)""",
    """RADIUS\.Acct-NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """RADIUS\.Acct-Framed-IP-Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  DupFields = [ "host->auth_server" ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = hp-arubaclearpass-kv-radius-traffic-success-radiusaccounting
  Vendor = HP
  Product = Aruba ClearPass Access Control and Policy Management
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
  Conditions = [ """ Radius Accounting """, """RADIUS.Acct-Timestamp=""" ]
  Fields = [
    """RADIUS\.Acct-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\.\d+)?[\+\-]\d+)""",
    """\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({host}[\w\-.]+)""",
    """RADIUS\.Acct-Username=(?:({user_type}host)/)?(({domain}[^\\\s,]+)\\+)?(anonymous|({user}[^\\\s,@]+))""",
    """RADIUS\.Acct-Username=({email_address}[^\\\s,@]+@[^\\\s,@]+)""",
    """RADIUS\.Acct-Service-Name =({network}[^,]+)""",
    """RADIUS\.Acct-NAS-IP-Address=({dest_ip}[A-Fa-f:\d.]+)""",
    """RADIUS\.Acct-Framed-IP-Address=({src_ip}[A-Fa-f:\d.]+)""",
  ]
  DupFields = [ "host->auth_server" ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = hp-arubacpm-kv-radius-traffic-success-radiusacc
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
  Conditions = [
    """ Radius Acco """
	"""RADIUS.Acct-Timestamp=""" ]
  Fields = [
    """RADIUS\.Acct-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\.\d+)?[\+\-]\d+)""",
    """\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({host}[\w\-.]+)""",
    """RADIUS\.Acct-Username=(?:({user_type}host)/)(({src_domain}[^\\\s,]+)\\+)?(anonymous|({src_host}[^\\\s,@]+))""",
    """RADIUS\.Acct-Username=(?!(host)/)(({domain}[^\\\s,]+)\\+)?(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """RADIUS\.Acct-Username=({email_address}[^\\\s,@]+@[^\\\s,@]+)""",
    """RADIUS\.Acct-Service-Name =({network}[^,]+)""",
    """RADIUS\.Acct-NAS-IP-Address=({dest_ip}[A-Fa-f:\d.]+)""",
    """RADIUS\.Acct-Framed-IP-Address=({src_ip}[A-Fa-f:\d.]+)""",
    """\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({auth_server}[\w\-.]+)""",
  ]


}
```
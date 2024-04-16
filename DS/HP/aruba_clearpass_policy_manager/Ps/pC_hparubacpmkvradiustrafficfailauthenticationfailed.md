#### Parser Content
```Java
{
Name = hp-arubacpm-kv-radius-traffic-fail-authenticationfailed
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [
    """ Authentication failed"""
	"""Common.NAS-IP-Address="""
	"""Common.Request-Timestamp=""" ]
  Fields = [
    """Common\.Request-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\.\d+)?[\+\-]\d+)""",
    """\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({host}[\w\-.]+)""",
    """Common\.Service=({network}[^,]+)""",
    """Common\.Host-MAC-Address=({src_mac}\w+)""",
    """Common\.NAS-IP-Address=({dest_ip}[A-Fa-f:\d.]+)""",
    """Common\.Username=(?:({user_type}host)/)(({src_domain}[^\\\s,]+)\\+)?(anonymous|({src_host}[^\\\s,@]+))""",
    """Common\.Username=(?!(host)/)(({domain}[^\\\s,]+)\\+)?(anonymous|({user}[\w\.\-]{1,40}\$?))""",
    """RADIUS\.Auth-Method=({auth_method}[^=]+?),[\w.-]+=""",
    """Common\.Alerts=({failure_reason}[^=]+?),[\w.-]+=""",
    """Common\.Error-Code=({event_code}[^=]+?),[\w.-]+="""
   ]
   DupFields = [ "host->auth_server" ]


}
```
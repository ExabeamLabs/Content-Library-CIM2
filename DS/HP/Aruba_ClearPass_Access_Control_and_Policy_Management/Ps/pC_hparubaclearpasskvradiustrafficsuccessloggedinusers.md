#### Parser Content
```Java
{
Name = hp-arubaclearpass-kv-radius-traffic-success-loggedinusers
  Conditions = [ """ Logged in users """, """Common.Request-Timestamp=""" ]
  ParserVersion = "v1.0.0"

q-aruba-nac-logon = {
  Vendor = HP
  Product = Aruba ClearPass Access Control and Policy Management
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Fields = [
    """Common\.Request-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\.\d+)?[\+\-]\d+)""",
    """\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({host}[\w\-.]+)""",
    """Common\.Username=(?:({user_type}host)/)?(({domain}[^\\\s,]+)\\+)?(anonymous|({user}[^\\\s,@]+))""",
    """Common\.Username=({email_address}[^\\\s,@]+@[^\\\s,@]+)""",
    """Common\.Service=({network}[^,]+)""",
    """Common\.Host-MAC-Address=({src_mac}\w+)""",
    """Common\.NAS-IP-Address=({dest_ip}[A-Fa-f:\d.]+)"""
  ]
  DupFields = [ "host->auth_server" 
}
```
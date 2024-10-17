#### Parser Content
```Java
{
Name = hp-arubacpm-kv-radius-traffic-fail-authfailed
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """ Failed Auth """, """Common.NAS-IP-Address=""" ]
  Fields = ${HPEParsersTemplates.q-aruba-nac-logon.Fields} [
    """Common\.Request-Timestamp=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d-\d+)"""
]

q-aruba-nac-logon = {
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Fields = [
    """Common\.Request-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\.\d+)?[\+\-]\d+)""",
    """\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({host}[\w\-.]+)""",
    """Common\.Username=(?:({user_type}host)/)?(({domain}[^\\\s,]+)\\+)?(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """Common\.Username=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """Common\.Service=({network}[^,]+)""",
    """Common\.Host-MAC-Address=({src_mac}\w+)""",
    """Common\.NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  ]
  DupFields = [ "host->auth_server" 
}
```
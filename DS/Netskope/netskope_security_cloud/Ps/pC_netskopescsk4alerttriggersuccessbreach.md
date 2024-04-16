#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-breach
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type":"Compromised Credential"""", """destinationServiceName =Netskope""", """"type":"breach"""", """"alert":"yes""" ]
 Fields = [
    """"timestamp":({time}\d{10})""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """"_id":"({alert_id}[^"]+)""",
    """"category":"(n\/a|({threat_category}[^"]+))""",
    """"alert_type"+:"+({alert_name}[^"]+)""",
    """"hostname":"({src_host}[^"]+)""",
    """security-threat-detected\|({alert_severity}\d+)""",
    """"alert_name":"({additional_info}[^"]+)""",
    """"type":"({alert_type}[^"]+)"""
    """msg=.*?\[({alert_source}[^\]]+)\]:"""
  ]


}
```
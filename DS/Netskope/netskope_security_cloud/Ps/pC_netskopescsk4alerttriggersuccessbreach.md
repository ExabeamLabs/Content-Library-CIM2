#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-breach
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type":""", """"Compromised Credential"""", """destinationServiceName =Netskope""", """"type":""", """"breach"""", """"alert":""", """"yes"""" ]
 Fields = [
    """"timestamp":\s*({time}\d{10})""",
    """"user":\s*"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"_id":\s*"({alert_id}[^"]+)""",
    """"category":\s*"(n\/a|({threat_category}[^"]+))""",
    """"alert_type"+:\s*"+({alert_name}[^"]+)""",
    """"hostname":\s*"({src_host}[^"]+)""",
    """security-threat-detected\|({alert_severity}\d+)""",
    """"alert_name":\s*"({additional_info}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)"""
    """msg=.*?\[({alert_source}[^\]]+)\]:"""
  ]


}
```
#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-compromised
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"alert_type":""", """"Compromised Credential"""", """"alert":""", """"yes"""", """"src-application-name":""", """"Netskope"""", """"type":""", """"breach"""", """"event-name":""", """"security-threat-detected"""" ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"user":\s*"(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"_id":\s*"({alert_id}[^"]+)""",
    """"category":\s*"(n\/a|({threat_category}[^"]+))""",
    """"alert_type":\s*"({alert_name}[^"]+)"""",
    """"severity":\s*"*({alert_severity}\d{1,2})""",
    """"alert_name":\s*"({additional_info}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"breach_description":\s*"({additional_info}[^"]+)"""",
    """"target-users":\[\{"user-email":\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  ]


}
```
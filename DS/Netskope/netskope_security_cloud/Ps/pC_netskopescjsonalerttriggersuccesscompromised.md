#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-compromised
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"alert_type":"Compromised Credential"""", """"alert":"yes"""", """"src-application-name":"Netskope"""", """"type":"breach"""", """"event-name":"security-threat-detected"""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"_id":"({alert_id}[^"]+)""",
    """"category":"(n\/a|({threat_category}[^"]+))""",
    """"alert_type":"({alert_name}[^"]+)"""",
    """"severity":({alert_severity}\d{1,2})""",
    """"alert_name":"({additional_info}[^"]+)""",
    """"type":"({alert_type}[^"]+)""",
    """"breach_description":"({additional_info}[^"]+)"""",
    """"target-users":\[\{"user-email":"({dest_email_address}[^"@]+@[^"\.]+\.[^"]+)""""
  ]


}
```
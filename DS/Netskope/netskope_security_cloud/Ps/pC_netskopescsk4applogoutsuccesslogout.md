#### Parser Content
```Java
{
Name = netskope-sc-sk4-app-logout-success-logout
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"audit_log_event":""", """"Logout Successful"""", """"type":""", """"event-name":""", """"logout"""", """"src-application-name":""", """"Netskope"""" ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"data_values":\s*\["({additional_info}[^"]+)""",
    """"user":\s*"(unknown|({email_address}[^@"]+@[^\."]+\.[^"]+))""",
    """"audit_log_event":\s*"({operation}[^"]+)""",
    """"({event_name}logout)""""
  ]


}
```
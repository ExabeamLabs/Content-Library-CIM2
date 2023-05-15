#### Parser Content
```Java
{
Name = netskope-sc-sk4-app-notification-success-auditevent
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"event-name":"audit-event"""", """"audit_log_event":"""", """"src-application-name":"Netskope"""", """"data_values":""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"user":"(unknown|({email_address}[^@"]+@[^\."]+\.[^"]+))""",
    """"audit_log_event":"({operation}[^"]+)""",
    """"({app}Netskope)""""
  ]


}
```
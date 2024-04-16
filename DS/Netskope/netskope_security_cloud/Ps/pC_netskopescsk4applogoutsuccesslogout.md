#### Parser Content
```Java
{
Name = netskope-sc-sk4-app-logout-success-logout
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"audit_log_event":"Logout Successful"""" , """"type":"""", """"event-name":"logout"""", """"src-application-name":"Netskope"""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"data_values":\["({additional_info}[^"]+)""",
    """"user":"(unknown|({email_address}[^@"]+@[^\."]+\.[^"]+))""",
    """"audit_log_event":"({operation}[^"]+)""",
    """"({event_name}logout)""""
  ]


}
```
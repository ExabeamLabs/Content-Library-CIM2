#### Parser Content
```Java
{
Name = netskope-sc-json-app-activity-success-propertyupdated
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"event-name":"resource-property-updated"""", """"audit_log_event":""", """"triggered-by":""", """"src-application-name":"Netskope"""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"user":"(unknown|({email_address}[^@"]+@[^\."]+\.[^"]+))""",
    """"audit_log_event":"({event_name}[^"]+)""",
    """"({operation}resource-property-updated)"""",
    """"({app}Netskope)"""",
    """"identifier":\{({additional_info}[^\}]+?"name":"({object}[^"]+)")\}"""
  ]


}
```
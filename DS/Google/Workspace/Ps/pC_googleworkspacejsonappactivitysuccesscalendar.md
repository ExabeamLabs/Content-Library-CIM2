#### Parser Content
```Java
{
Name = google-workspace-json-app-activity-success-calendar
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Workspace
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"applicationName":""", """"calendar"""", """"uniqueQualifier":""",  """"event_change"""" ]
  Fields = [
    """"time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"ipAddress"\s*:\s*"({src_ip}[\da-fA-F\.:]+)""",
    """"profileId"\s*:\s*"({user_id}\d+)""",
    """"actor"\s*:\s*\{.*?"email"\s*:\s*"({email_address}({user}[^@"]+)@[^"]+)"""",
    """"type"\s*:\s*"event_change",\s*"name"\s*:\s*"({operation}[^"]+)"""",
    """"type"\s*:\s*"event_change".*?"name"\s*:\s*"event_id",\s*"value"\s*:\s*"({additional_info}[^"]+)"""",
    """"type"\s*:\s*"event_change".*?"name"\s*:\s*"event_title",\s*"value"\s*:\s*"({object}[^"]+)"""",
  ]


}
```
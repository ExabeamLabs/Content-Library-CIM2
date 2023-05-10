#### Parser Content
```Java
{
Name = pan-tesm-csv-app-notification-success-validationfailed
  Vendor = Palo Alto Networks
  Product = Traps Endpoint Security Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """,Traps""", """,Machine License Validation Failed,""" ]
  Fields = [
    """\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}Machine License Validation Failed),({src_host}[^,]+),(|({user}[^\s,]+)),({host}[^,]+)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```
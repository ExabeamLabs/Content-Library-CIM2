#### Parser Content
```Java
{
Name = pan-tesm-csv-app-notification-success-heartbeat
  Product = Traps Endpoint Security Manager
  ParserVersion = "v1.0.0"
  Conditions = [ """,Traps""", """,Heartbeat,""" ]
  Fields = ${DLPaloAltoParsersTemplates.pan-system-events.Fields} [
    """,Heartbeat,([^,]*,){7}({src_ip}[A-Fa-f:\d.]+)""",
  ]

pan-system-events = {
  Vendor = Palo Alto Networks
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({host}[^,]+),(|({user}[^\s,]+)),""",
  ]
  DupFields = [ "host->dest_host" 
}
```
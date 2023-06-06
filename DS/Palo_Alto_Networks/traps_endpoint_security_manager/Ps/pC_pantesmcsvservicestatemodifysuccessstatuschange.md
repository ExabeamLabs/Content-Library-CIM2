#### Parser Content
```Java
{
Name = pan-tesm-csv-service-state-modify-success-statuschange
  Product = Traps Endpoint Security Manager
  ParserVersion = "v1.0.0"
  Conditions = [ """,Traps""", """,Traps Service Status Change,""" ]
  Fields = ${DLPaloAltoParsersTemplates.pan-system-events.Fields} [
    """,Traps Service Status Change,([^,]*,){2}({result}[^,]+)""",
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
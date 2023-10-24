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
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({host}[^,]+),(|({user}[\w\.\-]{1,40}\$?)),""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    ]
    DupFields = [ "host->dest_host" 
}
```
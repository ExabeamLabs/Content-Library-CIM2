#### Parser Content
```Java
{
Name = pan-tesm-csv-app-notification-success-heartbeat
  Product = Traps Endpoint Security Manager
  ParserVersion = "v1.0.0"
  Conditions = [ """,Traps""", """,Heartbeat,""" ]
  Fields = ${DLPaloAltoParsersTemplates.pan-system-events.Fields} [
    """,Heartbeat,([^,]*,){7}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]

pan-system-events = {
    Vendor = Palo Alto Networks
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({host}[^,]+),(|({user}[^\s,]+)),""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    ]
    DupFields = [ "host->dest_host" 
}
```
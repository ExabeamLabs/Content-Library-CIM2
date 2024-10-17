#### Parser Content
```Java
{
Name = pan-tesm-csv-endpoint-stop-success-shutdown
  Product = Traps Endpoint Security Manager
  ParserVersion = "v1.0.0"
  Conditions = [ """,Traps""", """,System Shutdown,""" ]

pan-system-events = {
    Vendor = Palo Alto Networks
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd yyyy HH:mm:ss"]
    Fields = [
      """\d\d:\d\d ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}[^,]+),({host}[^,]+),(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    ]
    DupFields = [ "host->dest_host" 
}
```
#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-packet
  ParserVersion = v1.0.0 
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [
""",THREAT,packet,""",
""",client""",
""",,"""
  ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,""",
    """,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),({src_ip}[A-Fa-f:\d.]+),({dest_ip}[A-Fa-f:\d.]+),""",
    """,\d+\/\d+\/\d+\s+\d+:\d+:\d+,\d+,\d+,({src_port}\d+),({dest_port}\d+),\d*,\d*,\w*,({protocol}[^\s,]+),({action}[^,]+),[^,]*,({additional_info}[^,]+),[^,]*,({severity}[^,]*),({direction}[^,]*),"""
  ]


}
```
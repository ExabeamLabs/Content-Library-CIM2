#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-packet
  ParserVersion = v1.0.0 
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
""",THREAT,packet,""",
""",client""",
""",,"""
  ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,""",
    """,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),""",
    """,\d+\/\d+\/\d+\s+\d+:\d+:\d+,\d+,\d+,({src_port}\d+),({dest_port}\d+),\d*,\d*,\w*,({protocol}[^\s,]+),({result}[^,]+),[^,]*,({additional_info}[^,]+),[^,]*,({severity}[^,]*),({direction}[^,]*),""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]


}
```
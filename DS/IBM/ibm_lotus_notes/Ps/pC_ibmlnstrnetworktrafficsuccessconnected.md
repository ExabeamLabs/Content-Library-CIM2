#### Parser Content
```Java
{
Name = ibm-ln-str-network-traffic-success-connected
  ParserVersion = v1.0.0
  Vendor = IBM
  Product = IBM Lotus Notes
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = ["""  SMTP Server: """, """ connected""", ]
  Fields = [
    """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))""",
    """SMTP Server:\s*({dest_host}.+?) \(({dest_ip}[a-fA-F\d.:]+)\)""",
  ]


}
```
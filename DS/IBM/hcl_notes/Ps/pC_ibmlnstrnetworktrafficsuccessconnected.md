#### Parser Content
```Java
{
Name = ibm-ln-str-network-traffic-success-connected
  ParserVersion = v1.0.0
  Vendor = IBM
  Product = HCL Notes
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = ["""  SMTP Server: """, """ connected""", ]
  Fields = [
    """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))""",
    """SMTP Server:\s*({dest_host}.+?) \(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\)""",
  ]


}
```
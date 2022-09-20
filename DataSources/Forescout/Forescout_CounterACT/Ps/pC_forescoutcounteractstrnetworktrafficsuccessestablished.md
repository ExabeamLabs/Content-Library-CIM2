#### Parser Content
```Java
{
Name = forescout-counteract-str-network-traffic-success-established
  Vendor = Forescout
  Product = Forescout CounterACT
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""Connection has been established:""" 
]
  Fields = [
    """(\w+\s+\d+ \d+:\d+:\d+)\s+({host}\S+)\s""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """from\[({src_ip}[a-fA-F\d.:]+)\](\s+to\[({dest_ip}[a-fA-F\d.:]+)\])?""",
    """({event_name}Connection has been established)"""
  ]


}
```
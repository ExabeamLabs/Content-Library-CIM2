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
    """from\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+to\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]""",
    """({event_name}Connection has been established)"""
  ]


}
```
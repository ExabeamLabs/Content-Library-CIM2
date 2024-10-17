#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-thresholdviolation
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """%SFF8472-3-THRESHOLD_VIOLATION""" ]
  Fields = [ 
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s+""",
    """({event_code}%\w+\-[^:]+)""", 
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$""" 
  ]


}
```
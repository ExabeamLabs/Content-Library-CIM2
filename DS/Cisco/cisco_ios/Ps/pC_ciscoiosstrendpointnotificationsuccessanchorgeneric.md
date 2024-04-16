#### Parser Content
```Java
{
Name = cisco-ios-str-endpoint-notification-success-anchorgeneric
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """: %MM_LOG-6-ANCHOR_GENERIC_INFO: """, """: mobilityd: """, """: Anchor: """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s\d+:""",
    """client mac:\s({src_mac}[^\s$]+)\s*$""",
    """%MM_LOG-6-ANCHOR_GENERIC_INFO:\s*({additional_info}[^"$]+?)\s*$"""
  ]


}
```
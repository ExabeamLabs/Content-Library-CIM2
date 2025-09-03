#### Parser Content
```Java
{
Name = cisco-ios-str-endpoint-notification-success-exclusionlist
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """: %CLIENT_EXCLUSION_SERVER-5-ADD_TO_EXCLUSIONLIST_REASON_DYNAMIC: """, """ was added to exclusion list """, """ reason:""", """: wncmgrd: """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s\d+:""",
    """:\sClient MAC:\s({src_mac}[^\s]+)\s\w+""",
    """%CLIENT_EXCLUSION_SERVER-5-ADD_TO_EXCLUSIONLIST_REASON_DYNAMIC:\s*({additional_info}[^"$]+?)\s*$"""
  ]


}
```
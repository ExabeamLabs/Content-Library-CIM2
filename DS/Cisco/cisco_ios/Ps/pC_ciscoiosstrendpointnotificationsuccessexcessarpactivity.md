#### Parser Content
```Java
{
Name = cisco-ios-str-endpoint-notification-success-excessarpactivity
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """: %SISF-4-EXCESS_ARP_ACTIVITY: """, """: wncd: """, """: Excessive ARP activity detected for the client """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s\d+:""",
    """: Excessive ARP activity detected for the client\s({src_mac}[^\s]+?)\.?\s\w+""",
    """%SISF-4-EXCESS_ARP_ACTIVITY:\s*({additional_info}[^"$]+?)\s*$"""
  ]


}
```
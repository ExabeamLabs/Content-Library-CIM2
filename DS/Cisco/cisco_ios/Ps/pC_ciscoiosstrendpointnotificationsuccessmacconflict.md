#### Parser Content
```Java
{
Name = cisco-ios-str-endpoint-notification-success-macconflict
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """: %IOSXE-4-PLATFORM:""", """ %SWPORT-4-MAC_CONFLICT: """, """: Dynamic mac """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s\d+:""",
    """:\sDynamic mac\s({src_mac}[^\s]+)\sfrom""",
    """\sfrom\s({src_interface}[^\s]+)\s""",
    """%IOSXE-4-PLATFORM:\s*({additional_info}[^"$]+?)\s*$"""
  ]


}
```
#### Parser Content
```Java
{
Name = citrix-appfw-str-app-notification-message
  ParserVersion = v1.0.0
  Vendor = Citrix Netscaler VPN
  Product = Citrix AppFW
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [ """ : default""", """ Message """, """-PPE"""]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)""",
    """Message.*?"\s*({additional_info}[^"]+)""",
    """Message.*?"\s*({additional_info}[^"]+)\s+""",
    ]


}
```
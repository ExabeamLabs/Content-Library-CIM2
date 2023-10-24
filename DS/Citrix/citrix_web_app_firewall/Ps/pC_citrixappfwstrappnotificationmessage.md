#### Parser Content
```Java
{
Name = citrix-appfw-str-app-notification-message
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Web App Firewall
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ : default""", """ Message """, """-PPE"""]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)(\s+GMT)?\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)""",
    """Message.*?"\s*({additional_info}[^\|]+?)[\s"]*(\||$)"""
    ]


}
```
#### Parser Content
```Java
{
Name = citrix-cgateway-str-app-notification-sslvpn
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [ """ SSLVPN Message """ ]
  Fields = [
    """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_name}SSLVPN Message)\s""",
    """\sSSLVPN Message(\s+\S+){3}\s+\\*"+\s*({additional_info}[^"]+?)\s*\\*"+""",
  ]


}
```
#### Parser Content
```Java
{
Name = cisco-fp-str-app-notification-success-fmc
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ PRIN-CISCO-FMC-1: """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\sPRIN-CISCO-FMC-1:\s*({host}[\w\-\.]+):[^\@]+\@([\w\s]+|({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))),([^,]+),\s*({additional_info}[^"]+)"""
  ]


}
```
#### Parser Content
```Java
{
Name = vmware-vmsdwan-str-app-notification-catchall
  Vendor = VMware
  Product = VMware VeloCloud SD-WAN
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """ velocloud.sdwan: """ ]
  Fields = [
    """({time}\w\w\w\s*\d+\s+\d\d:\d\d:\d\d)\s+({host}[\w\-\.]+)\s*({log_source}[^:]+):\s+({event_name}[^:]+):\s*({additional_info}[^\$]+?)\s*($)"""
    ]


}
```
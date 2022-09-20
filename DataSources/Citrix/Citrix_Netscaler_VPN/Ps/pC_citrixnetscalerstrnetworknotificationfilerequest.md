#### Parser Content
```Java
{
Name = citrix-netscaler-str-network-notification-filerequest
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Netscaler VPN
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ TRANSFORM FILE_REQUEST """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}.+?)\s+($|")""",
    """Client\s*({src_ip}[A-Fa-f:\d.]+)""",
  ]
  DupFields = ["host->src_host"]


}
```
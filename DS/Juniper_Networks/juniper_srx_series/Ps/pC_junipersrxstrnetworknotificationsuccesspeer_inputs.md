#### Parser Content
```Java
{
Name = juniper-srx-str-network-notification-success-peer_inputs
  ParserVersion = "v1.0.0"
  Conditions = [ """ peer_inputs:""", """ kernel:""" ]

juniper-network-notification-events = {
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "MMM dd HH:mm:ss"
  Fields = [
    """({time}\w{3}\s\d+\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\skernel:""",
    """\skernel:\s({additional_info}[^$]+)\s*$"""
  
}
```
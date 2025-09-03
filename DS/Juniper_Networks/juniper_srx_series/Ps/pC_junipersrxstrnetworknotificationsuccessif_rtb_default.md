#### Parser Content
```Java
{
Name = juniper-srx-str-network-notification-success-if_rtb_default
  ParserVersion = "v1.0.0"
  Conditions = [ """ if_rtb_default_ifl_bitmap_set()""", """ kernel:""" ]

juniper-network-notification-events = {
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "MMM dd HH:mm:ss"
  Fields = [
    """({time}\w{3}\s\d+\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\skernel:""",
    """\skernel:\s({additional_info}[^$]+)\s*$"""
  
}
```
#### Parser Content
```Java
{
Name = infoblox-nios-str-configuration-modify-success-zrqtransaction
  Vendor = Infoblox
  Product = Infoblox NIOS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ named[""", """ZRQ applying transaction""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """\d\d:\d\d:\d\d ({host}[\w\-\.]+)""",
    """zone ({dns_query}[^:\/]+)\/({record_type}[^:\/]+)""",
    """({event_name}ZRQ applying transaction)"""
    """named\[\S+?:\s+({additional_info}[^"$]+)\."""
  ]


}
```
#### Parser Content
```Java
{
Name = f5-bigip-str-vpn-logout-success-01490521
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""01490521:5:"""  
]
  Fields = [
    """\d\d:\d\d\s+({host}[^\s]+)\s([^\s]+\s)?[^\s]+\[\d+\]""",
    """01490521:5:.*?({session_id}[^:\s]+): Session statistics""",
    """bytes out:\s*({bytes_out}\d+)""",
    """bytes in:\s*({bytes_in}\d+)"""
  ]


}
```
#### Parser Content
```Java
{
Name = cisco-fp-str-ssl-start-725001
  Vendor = Cisco
  Product = Cisco Firepower  
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
  """-725001"""
  """%FTD-""" 
  ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Starting SSL handshake)""",
    """({src_interface}[^\s]+):(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+))\/({src_port}\d+)"""
    """to\s*(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+))\/({dest_port}\d+)"""
    """for\s+({protocol}\S+)\s+session"""
  ]


}
```
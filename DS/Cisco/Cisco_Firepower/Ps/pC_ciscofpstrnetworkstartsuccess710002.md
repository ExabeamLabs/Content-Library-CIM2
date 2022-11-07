#### Parser Content
```Java
{
Name = cisco-fp-str-network-start-success-710002
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-710002""", """%FTD-""" ]
  Fields = [
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s*:\s*%FTD""",
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """({protocol}[^\s:]+?)\s+({event_name}access permitted .+?)\s+$""",
    """ from\s+({src_ip}[A-Fa-f:\d.]+)\/({src_port}\d+)""",
    """ to Inside:\s*({dest_ip}[A-Fa-f:\d.]+)""",
    """ from (({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+) to ({dest_interface}\S+?)\s*:\s*(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)"""
  ]


}
```
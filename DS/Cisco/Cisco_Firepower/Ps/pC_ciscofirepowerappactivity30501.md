#### Parser Content
```Java
{
Name = cisco-firepower-app-activity-30501
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""FTD""", """30501"""]
  Fields = [
    """eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """(\w{3} \d\d \d\d:\d\d:\d\d)\s+({host}[\w\.-]+)\s*%FTD""",
    """({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)\s*({host}[\w\-.]+)?""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """\d{6}:\s*({event_name}[^;]+?);\s*Connection for udp src outside:({src_ip}[A-Fa-f:\d.]+)\/({src_port}\d+).+?dst outside:({dest_ip}[A-Fa-f:\d.]+)\/({dest_port}\d+)"""
    """\d{6}:\s*({event_name}.+?({protocol}\w+)\s*translation)\sfrom"""
    """from\s*({src_interface}[^:]+):(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)(\([^\s)]+\))?\s*to\s*({dest_interface}[^:]+):(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```
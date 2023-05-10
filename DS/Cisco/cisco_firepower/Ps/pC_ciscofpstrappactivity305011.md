#### Parser Content
```Java
{
Name = cisco-fp-str-app-activity-305011
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-305011:""", """ Built dynamic TCP translation """ ]
  Fields = [
    """%FTD-\d+-({event_code}305011)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s\S+\s+:\s+%FTD-\d+-305011:""",
    """({time}\w{3} (\d\d| \d) \d\d\d\d (\d\d| \d):\d\d:\d\d)""",
    """({host}[\w+\.-]+)\s+(\S*:\s*)?%FTD-\d+-\d+:""",
    """\s*({event_name}Built dynamic TCP translation)""",
    """(?i)(LAN|inside):({src_ip}(\d{1,3}\.){3}\d{1,3})\/({src_port}\d+)""",
    """(?i)(INET|Bank):({src_translated_ip}(\d{1,3}\.){3}\d{1,3})\/({src_translated_port}\d+)""",
    """:({src_ip}(\d{1,3}\.){3}\d{1,3})\/({src_port}\d+) to (outside|Outside):({dest_ip}(\d{1,3}\.){3}\d{1,3})\/({dest_port}\d+)"""
    """from OUTSIDE:({src_ip}(\d{1,3}\.){3}\d{1,3})\/({src_port}\d+).*?to OUTSIDE:({dest_ip}(\d{1,3}\.){3}\d{1,3})\/({dest_port}\d+)"""
  ]


}
```
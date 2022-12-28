#### Parser Content
```Java
{
Name = cisco-fp-str-app-activity-success-609002
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%FTD-""", """-609002""", """: Teardown """ ]
  Fields = [
    """({host}[\w\-.]+)\s*:\s*%FTD-""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Teardown .+?)\s+$""",
    """(Teardown|Built) local-host ([^\s]+|INSIDE|Outside|outside):(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))($|\s)"""
  ]


}
```
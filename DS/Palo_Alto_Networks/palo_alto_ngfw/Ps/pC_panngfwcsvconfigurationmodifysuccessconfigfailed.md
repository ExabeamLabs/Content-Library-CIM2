#### Parser Content
```Java
{
Name = "pan-ngfw-csv-configuration-modify-success-configfailed"
  Vendor = "Palo Alto Networks"
  Product = "Palo Alto NGFW"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """,CONFIG,""",
    """Failed"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s(?:-|({host}[^:\s]+))\s\d+,\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d,"""
    """CONFIG,.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
    """,({asset_id}\d+),CONFIG,"""
    """({event_category}CONFIG)"""
    """,CONFIG.+?\s\d\d:\d\d:\d\d,(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+)),"""
    """CONFIG,([^,]*,){5}({operation}[^,]+),"""
    """CONFIG,.+?\d\d:\d\d:\d\d([^,]*,){4}({user}[\w\.\-]{1,40}\$?),"""
    """CONFIG,([^,]*,){8}({result}[^,]+),"""
    """CONFIG,([^,]*,){9}\s*({object}[^,]+),"""
    """CONFIG,([^,]*,){17}({host}[^\s,]+)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = "v1.0.0"


}
```
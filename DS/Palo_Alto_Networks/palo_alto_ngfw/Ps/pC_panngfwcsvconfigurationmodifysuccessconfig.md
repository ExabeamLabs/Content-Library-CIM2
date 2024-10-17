#### Parser Content
```Java
{
Name = "pan-ngfw-csv-configuration-modify-success-config"
  Vendor = "Palo Alto Networks"
  Product = "Palo Alto NGFW"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
  Conditions = [
    """,CONFIG,""",
    """Submitted"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s(?:-|({host}[^:\s]+))\s\d+,\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d,"""
    """CONFIG,.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
    """,({serial_num}({asset_id}\d+)),CONFIG,"""
    """({event_category}CONFIG)"""
    """,CONFIG.+?\s\d\d:\d\d:\d\d,(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+)),"""
    """CONFIG,([^,]*,){5}({operation}[^,]+),"""
    """CONFIG,.+?\d\d:\d\d:\d\d([^,]*,){4}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
    """CONFIG,([^,]*,){8}({result}[^,]+),"""
    """CONFIG,([^,]*,){9}\s*({object}[^,]+),"""
    """CONFIG,([^,]*,){17}({host}[^\s,]+)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    """({serial_num}\d+),CONFIG,"""
    """CONFIG,([^,]*,){17}({device_name}[^\s,]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```
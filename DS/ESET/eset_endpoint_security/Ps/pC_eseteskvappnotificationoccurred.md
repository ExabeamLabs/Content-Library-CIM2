#### Parser Content
```Java
{
Name = eset-es-kv-app-notification-occurred
  Vendor = ESET
  Product = ESET Endpoint Security
  TimeFormat = "MM/dd/yy, HH:mm:ss a"
  Conditions = [ """An Event Log notification has occurred with the following parameters:""", """Category:""", """ComputerName =""", """Notification=""" ]
  Fields = [
    """\d+\.\d+Z\s+({host}[^\s]+)\s""",
    """(ComputerName|Source)=({src_host}[^\|\s]+)""",
    """Target=({dest_host}[^|]+)""",
    """HardwareDetection=({device_facility}[^|]+)\|""",
    """Notification=({additional_info}[^|]+?)\s*$""",
    """Time=({time}\d{1,2}\/\d{1,2}\/\d{2,4}, \d{1,2}:\d{1,2}:\d{1,2} (am|AM|pm|PM))""",
    """Category:\s*({alert_name}[^:]+?)\s+Monitored static group:"""
  ]
  ParserVersion = "v1.0.0"


}
```